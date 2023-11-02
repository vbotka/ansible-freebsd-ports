======================================
vbotka.freebsd_ports 2.4 Release Notes
======================================

.. contents:: Topics


2.4.0
=====

Release Summary
---------------
Split tasks ports_install.yml and ports_delete.yml. Simplify
vars.yml. Add tasks stat.yml.

Major Changes
-------------
- Split tasks: ports_install.yml and ports_delete.yml
- Simplified loop arguments in packages_*.yml
- Simplified set_fact: pkg_*
- Add support for all parameters of ansible.builtin.cron
- Add tags: ports_install, ports_delete,
  ports_install_*_individually, ports_delete_list_individually
- README; Add references.
- vars/main.yml.sample; Add example.
- Optionally create lists of outdated ports ports_outdated. Add
  variables: ports_stat, ports_outdated_enabled (default=false).

Minor Changes
-------------
- Debug formatting
