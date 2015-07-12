# Ansible generator

This Ansible project provides two playbooks to create Ansible
infrastructure for roles or projects with TDD infrastructure
integrated.

* role.yml: create a role
* project.yml create a  (project.yml)


## role.yml

### Playbook variables

This playbook requires two variables from the user which must be set
using the ansible-playbook argument ``-e`` (``--extra-vars``). These are

* ``role_name``: Name of the role without prefix (string, default: ``<empty>``, **mandatory**)
* ``role_path``: Base path of the role fed to *--init-path* from *ansible-galaxy init* (string, default: ``<empty>``, **mandatory**)
* ``role_prefix``: Directory name prefix for the role (string, choices ['ansible', 'galaxy', 'silpion'], default: ``ansible``)
* ``vagrant_box_name``: Name of the box to use for Vagrant integration testing (string, default: ``ubuntu/trusty64``)

### ansible-playbook

    ansible-playbook -i inventory \
      -e role_name=heka \
      -e role_path=$HOME/work/git/ansible-roles \
      role.yml

## project.yml

Not implemented yet.


<!-- vim: set nofen ts=4 sw=4 et: -->
