Filebeat Role
===========

The role installs Filebeat on RHEL-like Linux nodes.

Requirements
------------

Only RHEL-like Linux systems are currently supported.

Role Variables
--------------

| Variable name    | Default | Description                                   |
|------------------|----------|-----------------------------------------------|
| filebeat_version | "7.14.0" | Which version on Filebeat should be installed |

Example Playbook
----------------

    - hosts: all
      roles:
         - filebeat

Notes
-----

Filebeat is installed using RPM into default directories.

To keep idempotency, the playbook leaves Filebeat downloaded binary distribution in the temporary directory `/tmp`. If you don't need it, feel free to remove those files to free some disk space.

License
-------

MIT

Author Information
------------------

Any suggestions for improvements e-mail to [abeletskiy@ppr.ru](mailto:abeletskiy@ppr.ru).
