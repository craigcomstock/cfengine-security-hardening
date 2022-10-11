FTP servers are useful for large file sharing but provide an attack surface.
There exist many online services for sharing files that are likely more safe if not more free.
Removing FTP server packages makes it less likely that a server is accidentally enabled.

This module makes sure that common FTP server packages are not installed
on hosts and thus also not running. Currently only centos, redhat and debian-based
distributions such as ubuntu are supported.

## Example

    # sudo apt install vsftpd
    # cf-agent -KI
        info: Successfully removed package 'vsftpd'

## Adding exceptions

If FTP server packages are really needed on some specific hosts, they can be
marked as such by defining the `hardening_ftp_server_allowed` class in either
augments or CMDB.
