======================================
vbotka.freebsd_ports 2.6 Release Notes
======================================

.. contents:: Topics


2.6.1
=====

Release Summary
---------------
Ansible 2.17 update

Major Changes
-------------
* Update README.
* Update config and fix lint.
* Add tasks dirs.yml
* Change option update to auto in the command "portsnap auto"

Minor Changes
-------------
* Add var ports_role_version
* Update debug


2.6.0
=====

Release Summary
---------------
Ansible 2.16 update

Major Changes
-------------
* Supported FreeBSD 13.3 and 14.0
* Add tasts/sanity.yml, add variable ports_sanity (default=true).
* Add variable ports_config (default false).

Minor Changes
-------------
* Update ansible lint config.
* Update README.
* Fix Ansible lint.

Bugfixes
--------

Breaking Changes / Porting Guide
--------------------------------
* By default, portsnap will not be configured (ports_config=false).
