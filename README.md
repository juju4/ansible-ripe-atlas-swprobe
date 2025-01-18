[![Actions Status - Master](https://github.com/juju4/ansible-ripe-atlas-swprobe/workflows/AnsibleCI/badge.svg)](https://github.com/juju4/ansible-ripe-atlas-swprobe/actions?query=branch%3Amaster)
[![Actions Status - Devel](https://github.com/juju4/ansible-ripe-atlas-swprobe/workflows/AnsibleCI/badge.svg?branch=devel)](https://github.com/juju4/ansible-ripe-atlas-swprobe/actions?query=branch%3Adevel)

# RIPE NCC Atlas Software Probe ansible role

Ansible role to setup [ripe-atlas-software-probe](https://github.com/RIPE-NCC/ripe-atlas-software-probe/) (docs: https://atlas.ripe.net/docs/howtos/software-probes.html)

## Requirements & Dependencies

### Ansible
It was tested on the following versions:
 * 2.17

### Operating systems

Tested on Ubuntu 24.04, 22.04, Centos/Rockylinux 9, Debian 11, 12.

## Example Playbook

Just include this role in your list.
For example

```
- host: myhost
  roles:
    - juju4.ripe_atlas_swprobe
```

you probably want to review variables

## Variables

N/A

## Continuous integration

```
$ pip install molecule docker
$ molecule test
$ MOLECULE_DISTRO=ubuntu:24.04 molecule test --destroy=never
```


## Troubleshooting & Known issues

* Systemd hardening tries to retain functionalities but many options seems to conflict with software probe. If issue, check it first.

## License

BSD 2-clause
