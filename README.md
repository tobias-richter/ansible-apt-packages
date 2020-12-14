# tobias_richter.apt_packages

[![Build Status](https://github.com/tobias-richter/ansible-apt-packages/workflows/CI/badge.svg)](https://github.com/tobias-richter/ansible-apt-packages/actions)

This role installs apt packages on debian based systems.

## Requirements

This role requires Ansible 2.7 or higher.

## Role Variables

See [defaults/main.yml](defaults/main.yml) for the documented role variables.

It is recommended to configure `apt_packages_default` via
`group_vars/all/apt_packages.yml` and then configure
`apt_packages_custom` vie `host_vars` or via more specific `group_vars`.

## Example Playbook

This playbook installs some packages via apt.

    - hosts: apt_packages
	  roles:
	    - role: tobias_richter.apt_packages
	      apt_packages_default:
          - nano
          - htop
          - bmon