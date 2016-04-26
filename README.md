# Ansible generator

This Ansible project provides two playbooks to create Ansible
infrastructure for roles or projects with TDD infrastructure
integrated. It can also be used to add or update the TDD infrastucture
for an existing role.

* role.yml: create a role
* project.yml create a  (project.yml)


## role.yml

### Playbook variables

This playbook requires two variables from the user which must be set
using the ansible-playbook argument ``-e`` (``--extra-vars``). These are

* ``role_name``: Name of the role without prefix (string, default: ``<empty>``, **mandatory**)
* ``role_path``: Base path of the role fed to *--init-path* from *ansible-galaxy init* (string, default: ``<empty>``, **mandatory**)
* ``role_prefix``: Directory name prefix for the role (string, choices ['ansible', 'galaxy', 'silpion', 'infra'], default: ``ansible``)
* ``update``: Whether to update the TDD functionality for an existing role (boolean, default: ``false``)
* ``git``: Whether to manage the created role with Git (boolean, default: ``true``)

### ansible-playbook

    ansible-playbook -i inventory \
      -e role_name=heka \
      -e role_path=$HOME/work/git/ansible-roles \
      role.yml

## project.yml

### Playbook variables

This playbook requires two variables from the user which must be set
using the ansible-playbook argument ``-e`` (``--extra-vars``). These are

* ``project_name``: Name of the project (string, default: ``<empty>``, **mandatory**)
* ``project_path``: Base path of the project (string, default: ``<empty>``, **mandatory**)

### ansible-playbook

    ansible-playbook \
      -e project_name=testproject \
      -e project_path=$HOME/work/git/projects \
      project.yml



<!-- vim: set nofen ts=4 sw=4 et: -->
