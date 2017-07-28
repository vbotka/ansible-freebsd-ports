freebsd-ports
===================

[![Build Status](https://travis-ci.org/vbotka/ansible-freebsd-ports.svg?branch=master)](https://travis-ci.org/vbotka/ansible-freebsd-ports)

[Ansible role](https://galaxy.ansible.com/vbotka/freebsd-ports/). Install and/or update ports at FreeBSD


Requirements
------------

None.


Variables
---------



Workflow
--------

1) Change shell to /bin/sh.

```
ansible host -e 'ansible_shell_type=csh ansible_shell_executable=/bin/csh' -a 'sudo pw usermod user -s /bin/sh'
```

2) Install role.

```
ansible-galaxy install vbotka.freebsd-ports
```

3) Fit variables.

```
~/.ansible/roles/vbotka.freebsd-ports/vars/main.yml
```

4) Create playbook.

```
> cat ~/.ansible/playbooks/freebsd-ports.yml
---
- hosts: example.com
  become: yes
  become_method: sudo
  roles:
    - role: vbotka.freebsd-ports
```

5) Configure the system.

```
ansible-playbook ~/.ansible/playbooks/freebsd-ports.yml
```

License
-------

[![license](https://img.shields.io/badge/license-BSD-red.svg)](https://www.freebsd.org/doc/en/articles/bsdl-gpl/article.html)


Author Information
------------------

[Vladimir Botka](https://botka.link)


References
----------

- [FreeBSD handbook: 4.5. Using the Ports Collection](https://www.freebsd.org/doc/en_US.ISO8859-1/books/handbook/ports-using.html)
