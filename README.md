# ansible-role-rssh

[![Build Status](https://travis-ci.org/Lier0/ansible-role-rssh.svg?branch=master)](https://travis-ci.org/Lier0/ansible-role-rssh)

Debian - Restricted shell for scp/sftp

## Requirements

None

## Role Variables

Available variables are listed below, along with default values:

    rssh: True # Required to enable the role, if setted for a specific hosts
    rssh_allowcvs: False
    rssh_allowrdist: False
    rssh_allowrsync: False
    rssh_allowscp: False
    rssh_allowsftp: False
    rssh_logfacility: LOG_USER
    rssh_umask: '022'

Additional variables available, not set by default:

    rssh_chrootpath: /usr/local/chroot
    rssh_users:
      tkimball:
        umask: '022'
        access_bits: '00001'
        path: /usr/local/chroot

## Dependencies

 * none

## Example Playbook

    - hosts: servers
      roles:
        - role: lier0.rssh
          rssh_chrootpath: /usr/local/chroot

## License

GPLv3

## Author Information

This role was initialy created by [Taylor Kimball](http://www.linuxhq.org).
Adapted to Debian by Lier0.
