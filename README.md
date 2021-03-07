Packages
=========

This playbook allows you install extra packages through ansible.

Supported OS list
- Centos

(Support for more will come)


TODO
----

Support for more distro's.

Requirements
------------

There are no requirements for this role.


Role Variables
--------------

The var `packages` is used to install packages. The full usage of this var is used like this:
```
packages:
  - name: "htop"
    state: installed # Default 'installed'
    enablerepo: epel # Default 'ignore'
    disable_gpg_check: no # Default 'ignore'
```


Dependencies
------------

There are no Dependecies for this role

Example Playbook
----------------

    - name: Install packages
      hosts: all
      roles:
        - role: ggiinnoo.packages
          packages:
            - name: "htop"
          tags: [pacakges]

License
-------

BSD

Author Information
------------------

    Creator: Gino Jansen
    Website: www.ginojansen.nl
