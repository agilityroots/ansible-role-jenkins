Role Name
=========
agilityroots/ansible-role-jenkins

* This role installs Jenkins (bare-metal) via the package manager.
* *The role also installs OpenJDK Java as a dependency*.
* No additional customization is performed (e.g plugins or user creation).

You can use the role:
1. for provisioning a Jenkins CI server
1. as a base role for creating a Jenkins lab - e.g see [agilityroots/jenkins-workshop](http://github.com/agilityroots/jenkins-workshop).

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

Look at [defaults/main.yml](defaults/main.yml) for the list. Any of the variables there can be customized. (See examples below)

Dependencies
------------

The role depends on `geerlingguy.java` to install OpenJDK 8. Look at [meta/main.yml](meta/main.yml) for the dependencies list.

Example Playbook
----------------

Provisions an ansible group `servers` with Jenkins. The Jenkins port is set to 9095.

```
    - hosts: servers
      roles:
         - { role: agilityroots/ansible-role-jenkins, jenkins_http_port: 9095 }
```

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
