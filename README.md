# Ansible TDD generator

This Ansible project creates all necessary files to provide integration
testing infrastructure for Ansible roles.


All static files and templates will override existing files in the
destination role except for the main file containing the RSpec
integration tests (spec/default/\<ROLENAME\>\_spec.rb).


## Variables

This project requires two variables from the user which must be set
using the ansible-playbook argument ``-e`` (``--extra-vars``). These are

* ``role_name``
* ``role_path``

### role_name

This is the name of the role with any documented prefix removed.
Known prefixes are

* *ansible-*
* *galaxy-*
* *silpion-*

If your roles' directory name is *ansible-heka*, the **role_name** is
**heka**.

### role_path

This is the **absolute** path to the roles base directory. If the role
is installed at *~/work/git/ansible-roles/ansible-heka*, the **role_path**
is **$HOME/work/git/ansible-roles/ansible-heka**.


## ansible-playbook

    ansible-playbook -i inventory \
      -e role_name=heka \
      -e role_path=$HOME/work/git/ansible-roles/ansible-heka \
      playbook.yml


<!-- vim: set nofen ts=4 sw=4 et: -->
