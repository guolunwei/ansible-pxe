Refer to https://www.tecmint.com/install-ubuntu-via-pxe-server-using-local-dvd-sources

## Prerequisite
- PXE server: CentOS 7
- PXE client: ubuntu-18.04.6-server-amd64.iso

## Configure the Network
Configure the PXE boot server with a fixed IP address 10.0.0.10 on the NIC which will provide PXE services.

## Setup PXE boot server with ansible

```
ansible-playbook preseed.yml
```

SELinux state temporarily changed from 'enforcing' to 'permissive'. State change will take effect next reboot.
```
reboot
```

To test FTP Installation Source network path:

```
ftp://10.0.0.10/pub
```

To debug PXE server for eventual misconfigurations or other information and diagnostics in live mode:

```
sudo tail  -f /var/log/messages
```
