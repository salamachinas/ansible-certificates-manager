ansible-certificates-manager
============================

This role manage certificates

[![Ansible Galaxy](https://img.shields.io/ansible/role/xxxxx.svg)](https://galaxy.ansible.com/salamachinas/certificates-manager/)

Requirements
------------

This role requires Ansible 2.0 or higher and platform requirements are listed
in the metadata file.

Install
-------

```sh
ansible-galaxy install salamachinas.certificates-manager
```

Example Playbook
----------------

```yaml
- name: test provision
  hosts: all
  roles:
    - { role: ansible-certificates-manager }
  vars:
    certificates:
      - name: foo.bar.com
        key: YmFzZTY0IGVuY29kZWQgZm9vIGtleSBzdG9yZWQgaW4gdmF1bHQ=
        certificate: YmFzZTY0IGVuY29kZWQgZm9vIGNlcnRpZmljYXRlIHN0b3JlZCBpbiB2YXVsdA==
      - name: bar.foo.com
        key: YmFzZTY0IGVuY29kZWQgYmFyIGtleSBzdG9yZWQgaW4gdmF1bHQ=
        certificate: YmFzZTY0IGVuY29kZWQgYmFyIGNlcnRpZmljYXRlIHN0b3JlZCBpbiB2YXVsdA==
```

Tests
-----

```sh
docker build -t test-ansible-certificates-manager-centos7 -f tests/Dockerfile_centos7 --force-rm .
docker build -t test-ansible-certificates-manager-debian7 -f tests/Dockerfile_debian7 --force-rm .
docker build -t test-ansible-certificates-manager-debian8 -f tests/Dockerfile_debian8 --force-rm .
docker build -t test-ansible-certificates-manager-ubuntu14 -f tests/Dockerfile_ubuntu14 --force-rm .
docker build -t test-ansible-certificates-manager-ubuntu16 -f tests/Dockerfile_ubuntu16 --force-rm .
```
