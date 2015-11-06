# 0.9.2


* Disable host key checking for role in ansible.cfg

Alvaro Aleman (1):
# 0.9.1


* Fix releasescript to correctly order generated changelog

Alvaro Aleman (1):
# 0.9.0

Alvaro Aleman (1):

* Add infra as allowed prefix

Mark Kusch (6):

* Add role\_version variable to default vars/main.yml
* Fix missing bracket in jinja method call
* Always run ansible with --diff in Vagrant
* Always run ansible with --diff in docker
* Add --check to ansible.raw\_arguments if configured in environment
* Allow to deconfigure git

# 0.8.0

Mark Kusch (1):

* Use source from list for copying static files (thx to Marc Rohlfs)

# 0.7.0

Alvaro Aleman (9):

* Releasescript: Make all errors fatal
* Releasescript: Typos
* Added usage check and message, added exit return codes
* Releasescript: Fixed formatting in generated CHANGELOG.md output, added diff displaying
* Releasescript: Added check if a tag named $RELEASE_VERSION already exists
* Releasescript: Various fixups, improved error handling
* Releasescript: added execution bit
* Releasecript: fixed up parameterization
* Releasecript: fixed version detection

# 0.6.0

Alvaro Aleman (2):

* added vim \.*\.swp files to .gitignore for both this repo and created roles
* TDD Vagrant: Added checkmode option, prefixed the various environment settings with $role\_name

# 0.5.0

Alvaro Aleman (5):

* added update functionality
* update functionality: removed tests/playbook.yml, typo fixed
* added ruby friendly role\_name\_nodash and replaced role\_name with it where needed

# 0.4.0

Alvaro Aleman (7):

* Added options to set verbosity and skip\_tags to vagrantfile
* Vagrantfile: Replacing dashes to avoid ruby substitution errors
* vagrant box name parameterized using env vars
* vagrant provider parameterized using env vars
* vagrantfile: added config for libvirt provider
* rake suite vagrant: Added parameter to prevent the vagrant box from getting destroyed after each run
* Vagrant tdd: Added defaults for box and provider to keep behaviour consistent

Marc Rohlfs (1):

* First (quick and dirty) attempt of shell script to create releases.

Mark Kusch (3):

* Add minimal documentation for contributing
* Ansible shall not write .retry files
* Do not add .retry files

# 0.3.1

Marc Rohlfs (2):

* Add Gemfile.lock file to gitignore patterns for the generated roles and projects.
* Define gitignore patterns for the gnerator project itself.

Mark Kusch (3):

* Do not install test playbooks with sudo: yes
* Fix YAML indentation to two whitespace indents
* Add synopsis to documentation

# 0.3.0

Mark Kusch (5):

* Add Gemfile.lock to the repositories
* Install a travis configuration in a role
* Update spec_helper for Rspec/Specinfra 2.N

# 0.2.1

Mark Kusch (1):

* Better collaborative .gitignore

# 0.1.2

* Add --hostname option to docker run command

# 0.1.1

* Install .gitignore

# 0.1.0

* First functioning state


<!-- vim: set nofen ts=4 sw=4 et: -->
