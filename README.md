Role Name
=========
[![license][2i]][2p]
[![twitter][3i]][3p]

A umurmur role using docker.

Description
-----------

The role provisions a umurmur docker container for you to use with [abaez.domain][4]. The combination of using ansible for the provision, allows for extremely easy domain association and setup of a murmur server.

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Requirements
------------

For the role to function, you do need to have docker install. With it, you can optionally add domain role to have domain association for the role.

* [abaez.docker][5]
* (optional) [abaez.domain][4]

Usage
-----

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

``` yaml
- hosts: servers
    roles:
        - [abaez.docker][5]
        - [abaez.domain][4]
        - umurmur
```

Author Information
------------------

[Alejandro Baez][1]

[1]: https://keybase.io/baez
[2i]: https://img.shields.io/badge/license-BSD_2-green.svg
[2p]: ./LICENSE
[3i]: https://img.shields.io/badge/twitter-a_baez-blue.svg
[3p]: https://twitter.com/a_baez
[4]: https://galaxy.ansible.com/abaez/domain
[5]: https://galaxy.ansible.com/abaez/docker
