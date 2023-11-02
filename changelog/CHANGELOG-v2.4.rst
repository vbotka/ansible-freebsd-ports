======================================
vbotka.freebsd_ports 2.4 Release Notes
======================================

.. contents:: Topics


2.4.0
=====

Release Summary
---------------
Split tasks ports_install.yml and ports_delete.yml. Configure
portsnap. Update ports. Add tasks stat.yml.

Major Changes
-------------
- Configure portsnap.
- Optionally, update ports.
- Optionally, create lists of outdated ports ports_outdated.
- Add variables: ports_stat, ports_outdated_enabled (default=false).
- Split tasks to ports_install.yml and ports_delete.yml
- Add tags: ports_install, ports_delete,
  ports_install_*_individually, ports_delete_list_individually

Minor Changes
-------------
- Add support for all parameters of ansible.builtin.cron
- README; Add references.
- Update vars/main.yml.sample; Add example.
- Simplified loop arguments in ports_install.yml
- Simplified set_fact of pkg_* in vars.yml
