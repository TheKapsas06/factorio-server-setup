Factorio Server setup
=========

Role used to setup and keep the server as IaC for factorio server.
This playbook does not harden the server.

Requirements
------------

None

Role Variables
--------------

All variables are commented in `defaults/main.yaml`\
`factorioserver_version` variable is the only excpetion and is held in `vars/main.yaml`
With this variables you can control the version of factorio that is being installed.

Dependencies
------------

None.

Example Playbook
----------------

This playbook does not need any variable to use.
```
- hosts: servers
  roles:
    - factorio-server
```
License
-------
GPLv3 Only

Author Information
------------------
Andreas Gabriel Vannas
