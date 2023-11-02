======================================
vbotka.freebsd_ports 2.4 Release Notes
======================================

.. contents:: Topics


2.4.0
=====

Release Summary
---------------
Simplified configuration of repositories. Single unified template
repo.j2 for repositories. Simplified configuration of optional
parameters of *community.general.pkgng*

Major Changes
-------------
- Split tasks: ports_install.yml and ports_delete.yml
- Simplified loop arguments in packages_*.yml
- Simplified set_fact: pkg_*
- Add support for all parameters of ansible.builtin.cron
- Add variables:
  
- Add tags: ports_install, ports_delete,
  ports_install_*_indivindually, ports_delete_list_indivindually

- README; Add references.
- vars/main.yml.sample; Add example.

Minor Changes
-------------
- Debug formatting
