# 1.2.0

Mark Kusch (9):

* Add role\_version to local facts by default
* Do not manage compiled Python binaries with Git
* Add vendor variables/facts
* Re-add underscore in ANSIBLE\_LIB\_ environment variable names
* Fix bug when removing files
* Fix vagrant bug with galaxy\_roles\_path
* Flatten rake environment (no includes required anymore)
* Repair serverspec infrastructure with Vagrant
* Fix vagrantfile ansible.galaxy\_roles\_path for current Vagrant version 1.8.4

# 1.1.1

Alvaro Aleman (1):

* Disable project cows

# 1.1.0

Alvaro Aleman (2):

* Dont enable public bridging by default
* Use a dedicated dictionary for network configuration in project Vagrantfile

Mark Kusch (23):

* Fix reference to non-existing key in hash for 'ip'
* Fix references to non-existing key in hash for 'ports'
* Fixup comments according to networking configuration updates
* Add user configuration support with vagrant-nugrant plugin
* Remove duplicated line for check mode environment variable
* Major Vagrantfile/ansible-galaxy management enhancements
* Use centos/7 as default VM for building Ansible roles
* Fixup ansible roles\_path
* Add silpion.lib as default dependency when boilerplating roles
* Provide name attribute for role play
* Remove files installed for docker based TDD
* Minor updates to documentation for variable names
* Re-use mechanics from project generation when re-defining role generator
* Allow project generator to configure mode for project\_files
* Rename test playbook according to galaxy-generated travis integration
* Allow to force override files
* Use markdown code block with syntax highlighting in documentation
* Re-integrate role\_name\_tdd variable after merge from next
* Remove docker from rake infrastructure
* Allow vagrant to find the test playbook
* Re-add requirements file gone missing after merge
* Do not negate ssh\_pipelining variable
* Force overrides if ansible-galaxy init is not skipped

# 1.0.0

Anja Siek (24):

* add project generator code
* update Vagrantfile to automated do ansible-galaxy install requirements.yml
* fix typo
* fix coding guidelines issues
* rename file
* remove inventory-path becouse it can not be used with Vagrant environments
* mv templates and files in subdirectories; remove local\_action; update codingstyle in role-playbook
* remove roled-dir; change file=touch to copy empty content becouse touch always triggers changed
* update synced\_folder configuration and documentation
* add some documentation
* fix ip-address 'problem' and update raw\_arguments in Vagrantfile
* fix variable wording error
* fix broken Vagrantfile
* remove multiplaybooks becouse of reusability of variables
* update libvirt variables
* fix README.md error
* use nodash variable
* add default group
* use variable for url
* fix Vagrantfile
* remove all special chars from variable project\_name\_nodash
* add requirements.yml run; fix different resource sizes
* define defaults; fix multi-vm-setup
* add emacs backup files to gitignore

Georg Hopp (17):

* Fix location reference and namig of template files.
* Fix host\_vars naming
* Create empty predefined playbooks.
* Enable pipelining in generated project (conditionally).
* Add bootstrap.yml template
* Fix section ssh\_connection in ansible.cfg template
* We need inventory as pointer to the hosts file.
* Add empty subfolders dev, prod and test under group\_vars.
* Make use of ansible-util which deactivates requiretty now
* file: => src:

* Add playbook.yml which only includes the other playbooks.
* Add basic README's for the predefined stages
* Add machineid role to all playbooks.
* fix project.jml example
* don't try to copy no longer used playbooks (bootstrap.yml, infrastructure.yml)
* Improve group management / enable paralell ansible runs with vagrant.
* fix vm name

Mark Kusch (13):

* Add documentation for the git var in role.yml
* Use YAML highlighting in role documentation for the example playbook
* Use shell syntax highlighting for code blocks in role documentation
* Use digits to refer booleans in ansible.cfg
* Fix deprecation warning for bare variables
* Use Ruby data types in Vagrantfile for projects (and update some comments)
* Use re to strip disallowed characters from role names for internal ansible usage
* Do not enforce role versions for util and machineid when generating a project boilerplate
* Fixup nugrant based user configuration evaluation
* Trivialise nugrant user configuration (draft)
* Fix no such method in nugrant user configuration
* Do not maintain user specific environment configuration with git
* Fix Ruby syntax error when setting host vars


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
