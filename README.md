# Ansible generator

This Ansible project provides two playbooks to create Ansible
infrastructure for roles or projects with TDD infrastructure
integrated. It can also be used to add or update the TDD infrastucture
for an existing role.

* role.yml: create a role boilerplate
* project.yml: create a project boilerplate


## role.yml

### Playbook variables

This playbook requires two variables from the user which must be set
using the ansible-playbook argument ``-e`` (``--extra-vars``). These are

* ``role_name``: Name of the role without prefix (string, default: ``<empty>``, **mandatory**)
* ``role_path``: Base path of the role fed to *--init-path* from *ansible-galaxy init* (string, default: ``<empty>``, **mandatory**)
* ``role_prefix``: Directory name prefix for the role (string, choices ['ansible', 'silpion', 'infra', 'pronto'], default: ``ansible``)
* ``role_manage_with_git``: Whether to manage the created role with Git (boolean, default: ``true``)
* ``force``: Whether to force override files (boolean, default: ``false``)

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
* ``project_manage_with_git``: Whether to manage the created project with Git (boolean, default: ``true``)
* ``force``: Whether to force override files (boolean, default: ``false``)

### ansible-playbook

    ansible-playbook \
      -e project_name=testproject \
      -e project_path=$HOME/work/git/projects \
      project.yml


<!-- vim: set nofen ts=4 sw=4 et: -->
