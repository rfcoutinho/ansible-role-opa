![Ansible Lint](https://github.com/rfcoutinho/ansible-role-opa/workflows/Ansible%20Lint/badge.svg)  

Ansible Role OPA
=========

This role installs the [Open Policy Agent](https://www.openpolicyagent.org/) and can also be used to manage your data and policies [configuration](https://www.openpolicyagent.org/docs/latest/configuration/) file

Requirements
------------

If `install_method: "build"` this role will make use of `make` and `golang`

Role Variables
--------------

| variables      | default value  |  type  |  description  |
|----------------|:--------------:|:------:|:--------------|
| config_mode    | false          | bool   | Enable OPA to run with a [configuration file](https://www.openpolicyagent.org/docs/latest/configuration/#example)|
| upload_data    | false          | bool   | Upload you data files within `/templates/data`
| upload_policy  | false          | bool   | Upload you data files within `/templates/policies`
| install_method | download       | string | Preferred installtion method: Set `build` to do it from source


Dependencies
------------

N/A


Example Playbook
----------------

```yaml
---
- hosts: "{{ target_host }}"
  become_method: sudo
  roles:
    - ansible-role-opa
```

License
-------

GPLv3

Author Information
------------------

Rafael Coutinho
