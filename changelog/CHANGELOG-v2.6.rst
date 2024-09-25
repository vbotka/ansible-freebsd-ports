======================================
vbotka.freebsd_ports 2.6 Release Notes
======================================

.. contents:: Topics
# BEGIN Commits 2.6.3
- Update python 3.11 in .travis.yml
- Start devel 2.6.3
# END Commits 2.6.3
# BEGIN Release notes 2.6.3
2.6.3
=====
Release Summary
---------------
Major Changes
-------------
Minor Changes
-------------
- Update python 3.11 in .travis.yml
- Start devel 2.6.3

Bugfixes
--------
Breaking Changes / Porting Guide
--------------------------------
# END Release notes 2.6.3


2.6.3
=====

Release Summary
---------------
Maintenance update

Major Changes
-------------


2.6.2
=====

Release Summary
---------------
Add supported 14.1


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
