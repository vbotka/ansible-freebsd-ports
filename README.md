# freebsd_ports

[![quality](https://img.shields.io/ansible/quality/27910)](https://galaxy.ansible.com/vbotka/freebsd_ports)[![Build Status](https://app.travis-ci.com/vbotka/ansible-freebsd-ports.svg?branch=master)](https://app.travis-ci.com/vbotka/ansible-freebsd-ports)[![GitHub tag](https://img.shields.io/github/v/tag/vbotka/ansible-freebsd-ports)](https://github.com/vbotka/ansible-freebsd-ports/tags)

[Ansible role.](https://galaxy.ansible.com/vbotka/freebsd_ports/) FreeBSD. Install and update ports.

Feel free to [share your feedback and report issues](https://github.com/vbotka/ansible-freebsd-ports/issues).

[Contributions are welcome](https://github.com/firstcontributions/first-contributions).


## Requirements

### Collections

- community.general


## Role Variables

See the defaults end examples in vars.


## Workflow

1) Change shell on the remote host to /bin/sh if necessary

```bash
shell> ansible host -e 'ansible_shell_type=csh ansible_shell_executable=/bin/csh' -a 'sudo pw usermod user -s /bin/sh'
```

2) Install the role and collection

```bash
shell> ansible-galaxy role install vbotka.freebsd_ports
```
Install the collection if necessary

```bash
shell> ansible-galaxy collections install community.general
```

3) Fit variables, for example, in vars/main.yml

```bash
shell> editor vbotka.freebsd_ports/vars/main.yml
```

Set "freebsd_install_method=ports"

See vars/main.yml.sample
See vbotka.freebsd_postinstall/defaults/main/pkgdict_*.yml

4) Create playbook

```bash
shell> cat freebsd-ports.yml

- hosts: srv.example.com
  roles:
    - vbotka.freebsd_ports
```

5) Manage the ports

Check syntax

```bash
shell> ansible-playbook freebsd-ports.yml --syntax-check
```

Display variables

```bash
shell> ansible-playbook freebsd-ports.yml -e ports_debug=true -t ports_debug
```

Dry-run the playbook and display changes

```bash
shell> ansible-playbook freebsd-ports.yml --check --diff
```

Optionally, update ports

```bash
shell> ansible-playbook freebsd-ports.yml -t ports_update -e ports_update=true
```

Dry-run the installation of the ports

```bash
shell> ansible-playbook freebsd-ports.yml -e ports_dryrun=true
```

If all seems to be right manage the packages

```bash
shell> ansible-playbook freebsd-ports.yml
```


## Ansible lint

Use the configuration file *.ansible-lint.local* when running *ansible-lint*. Some rules might be disabled and some warnings might be ignored. See the notes in the configuration file.

```bash
shell> ansible-lint -c .ansible-lint.local
```


## References

- [FreeBSD handbook: Using the Ports Collection](https://docs.freebsd.org/en/books/handbook/ports/#ports-using)
- [FreeBSD handbook: Building Packages with Poudriere](https://docs.freebsd.org/en/books/handbook/ports/#ports-poudriere)
- [poudriere](https://github.com/freebsd/poudriere/wiki)


## License

[![license](https://img.shields.io/badge/license-BSD-red.svg)](https://www.freebsd.org/doc/en/articles/bsdl-gpl/article.html)


## Author Information

[Vladimir Botka](https://botka.info)
