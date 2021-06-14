# freebsd_ports

[![quality](https://img.shields.io/ansible/quality/27910)](https://galaxy.ansible.com/vbotka/freebsd_ports)[![Build Status](https://travis-ci.org/vbotka/ansible-freebsd-ports.svg?branch=master)](https://travis-ci.org/vbotka/ansible-freebsd-ports)

[Ansible role.](https://galaxy.ansible.com/vbotka/freebsd_ports/) FreeBSD. Install and update ports.

Feel free to [share your feedback and report issues](https://github.com/vbotka/ansible-freebsd-ports/issues).

[Contributions are welcome](https://github.com/firstcontributions/first-contributions).


## Requirements

### Collections

- community.general


## Role Variables

See the defaults end examples in vars.


## Workflow

1) Change shell to /bin/sh

```
shell> ansible host -e 'ansible_shell_type=csh ansible_shell_executable=/bin/csh' -a 'sudo pw usermod user -s /bin/sh'
```

2) Install the role and collections

```
shell> ansible-galaxy role install vbotka.freebsd_ports
shell> ansible-galaxy collections install community.general
```

3) Fit variables, e.g. vars/main.yml

```
shell> editor vbotka.freebsd_ports/vars/main.yml
```

Set "freebsd_install_method=ports"

4) Create playbook

```
shell> cat freebsd-ports.yml

- hosts: srv.example.com
  roles:
    - vbotka.freebsd_ports
```

5) Manage the ports

Check syntax

```
shell> ansible-playbook freebsd-ports.yml --syntax-check
```

Display variables

```
shell> ansible-playbook freebsd-ports.yml -e ports_debug=true -t ports_debug
```

Dry-run the playbook and display changes

```
shell> ansible-playbook freebsd-ports.yml --check --diff
```

Dry-run the installation of the ports

```
shell> ansible-playbook freebsd-ports.yml -e ports_dryrun=true
```

Manage the packages if all seems to be right

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
