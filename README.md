# freebsd_ports

[![quality](https://img.shields.io/ansible/quality/27910)](https://galaxy.ansible.com/vbotka/freebsd_ports)[![Build Status](https://travis-ci.org/vbotka/ansible-freebsd-ports.svg?branch=master)](https://travis-ci.org/vbotka/ansible-freebsd-ports)

[Ansible role.](https://galaxy.ansible.com/vbotka/freebsd_ports/) FreeBSD. Install and update ports.

Feel free to [share your feedback and report issues](https://github.com/vbotka/ansible-freebsd-ports/issues).

[Contributions are welcome](https://github.com/firstcontributions/first-contributions).


## Requirements

None.


## Role Variables

Review the defaults end examples in vars.


## Workflow

1) Change shell to /bin/sh

```
shell> ansible host -e 'ansible_shell_type=csh ansible_shell_executable=/bin/csh' -a 'sudo pw usermod user -s /bin/sh'
```

2) Install role

```
shell> ansible-galaxy install vbotka.freebsd_ports
```

3) Fit variables

```
shell> editor vbotka.freebsd_ports/vars/main.yml
```

4) Create playbook

```
shell> cat freebsd-ports.yml

- hosts: srv.example.com
  roles:
    - vbotka.freebsd_ports
```

5) Configure the system

```
shell> ansible-playbook freebsd-ports.yml
```


## References

- [FreeBSD handbook: 4.5. Using the Ports Collection](https://www.freebsd.org/doc/en_US.ISO8859-1/books/handbook/ports-using.html)
- [FreeBSD handbook: 4.6. Building Packages with Poudriere](https://www.freebsd.org/doc/handbook/ports-poudriere.html)
- [poudriere](https://github.com/freebsd/poudriere/wiki)


## License

[![license](https://img.shields.io/badge/license-BSD-red.svg)](https://www.freebsd.org/doc/en/articles/bsdl-gpl/article.html)


## Author Information

[Vladimir Botka](https://botka.link)
