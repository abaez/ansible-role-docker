Docker
=========
[![license][2i]][2p]

Install docker with docker-compose for a number of linux variants.

Variables
---------

There are two variables that should be changed if you are using RHEL or SLES.
They are simply the repo url and [version][3] for the enterprise edition of docker.
If you are using any of the other distros, carry along, no need to change.

``` yaml
# default/main.yml
ee:
  url: "string for the url of your repo subscription"
  version: 7 # Optional for RHEL and not required for SLES at all.
```

Usage
-----

All you need to do is make sure you are running the role as a privileged user and append to playbook like so::

``` yaml
- hosts: servers
    roles:
        - abaez.docker
```

Author Information
------------------

[Alejandro Baez][1]

[1]: https://keybase.io/baez
[2i]: https://img.shields.io/badge/license-BSD_2-blue.svg
[2p]: ./LICENSE
[3]: https://docs.docker.com/engine/installation/linux/rhel/#install-using-the-repository
