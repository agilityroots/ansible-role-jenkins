Role Name
=========

agilityroots/ansible-role-jenkins

Requirements
------------

Host System

* A Linux system with Ansible
* Ansible 2.0+ required

Target System:

* Ubuntu 16.04+ (not tested on Ubuntu 14.04)
* CentOS support coming soon.
* Python 2.7+ required for Ansible execution.

Role Variables
--------------

Look at [defaults/main.yml](defaults/main.yml) for the list.

Dependencies
------------

The role depends on `geerlingguy.java` to install OpenJDK 8. Look at [meta/main.yml](meta/main.yml) for the dependencies list.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```
    - hosts: servers
      roles:
         - { role: agilityroots/ansible-role-jenkins, jenkins_http_port: 9095 }
```

License
-------

MIT

Author Information
------------------

* [About Agility Roots](http://www.agilityroots.com)
