nodejs
========

Installs node and npm on RHEL 6/CentOS 6/Ubuntu 12.04 via standard packaging mechanisms - 
Chris Lea's PPA on Debian and the EPEL repository on RHEL/CentOS.

Can also configure a set of global packages.

Adheres to semantic versioning (http://semver.org/) - you are advised to install / depend
on a major version number.

Credits: I initially developed this in isolation, but later took some inspiration from 
https://github.com/bcen/ansible-nodejs and bennojoy/openldap_server.

Requirements
------------

None.

Role Variables
--------------

  nodejs_global_packages: [ ]  # Packages to install globally

Examples
--------

  - hosts: all
    roles:
    - role: mjmaisey.nodejs
      nodejs_global_packages:
        - underscore
        - async
        - grunt

Dependencies
------------

- Uses goozbach.EPEL on RHEL/CentOS to install the EPEL repo
- Uses cederberg.bootstrap-debian to install essential Ubuntu packages

License
-------

Apache v2
