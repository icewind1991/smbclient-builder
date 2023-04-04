# smbclient-builder

Mostly static `smbclient` builds for ubuntu 20.04.

Intended to easily install different `smbclient` versions in CI

## Usage

- Download the smbclient binary from https://github.com/icewind1991/smbclient-builder/releases
- Make the download file executable
- Run `apt install libjansson4 libcap2 libbsd0 libreadline8 libicu66`
- Create a bare bones smb config in `/etc/samba/smb.conf`
  ```ini
  [global]
  client min protocol = SMB2
  client max protocol = SMB3
  ```
- Create the `/var/lib/samba/private` folder
- Enjoy your smbclient

## Supported versions

The following versions of `smbclient` are currently build

- 4.18.1
- 4.17.7
- 4.16.10
- 4.15.13
- 4.14.9
- 4.13.12
- 4.11.17
- 4.10.18
- 4.9.18
- 4.8.12
- 4.7.12
- 4.6.16
- 4.5.16
- 4.4.16
- 4.3.13
- 4.2.14
