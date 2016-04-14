Role Name
=========
[![license][2i]][2p]
[![twitter][3i]][3p]

A umurmur role using docker.

Description
-----------

The role provisions a umurmur docker container for you to use with [abaez.domain][4] and is serviced by systemd. The combination of all of these, allows for extremely easy domain association and setup of a murmur server.

Role Variables
--------------

The role has a number of variables, in `vars/main.yml`, that should be changed.

### Required
Must change these variable to get what you need from the role:

``` rust
mm.max: int // max users
mm.password: string // password for the server
user.name: string // name of the user to run the systemd service
dir.srv: path // the server install
dir.tool: path // tool install location
```

### Optional
If you have [abaez.domain][4], then change the **vhosts.murmur** variables:

``` rust
vhosts.murmur.name: url // domain location
vhosts.murmur.port: int // port of the container to expose to domain location
```


Requirements
------------

For the role to function, you do need to have docker install. With it, you can optionally add domain role to have domain association for the role.

* [abaez.docker][5]
* (optional) [abaez.domain][4]

Usage
-----

You need the roles listed in requirements for the role to run. That and you need to adjust variables according to role variables

``` yaml
- hosts: servers
    roles:
        - abaez.docker
        - abaez.domain # optional
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
