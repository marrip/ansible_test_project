# ansible_test_project

Setting up ansible test env

## Introduction

This is a simple ansible playbook to test things. It can be run just for testing locally or moved to production.

## Dependencies

In order for this playbook to run you need:

- python ≥ 3.8.5
- [ansible](https://docs.ansible.com/) ≥ 2.10.7
- git ≥ 2.24.3

## Required configuration

Setup a configuration file at `~/.ansible.cfg` which can be a copy of
[this](https://raw.githubusercontent.com/ansible/ansible/devel/examples/ansible.cfg).
Set the inventory according to the location of your `hosts` file which can look like
this:

```
[backup]
localhost ansible_connection=local
```

for testing purposes. For production, one should add the FQDNs for the respective hosts
and use `ssh` for connection.

## Usage

The playbook may be run like so:

```
ansible-playbook test.yml
```

Please keep in mind, that for production additional arguments might need to be added.
