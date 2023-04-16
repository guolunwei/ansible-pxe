Refer to https://www.tecmint.com/install-pxe-network-boot-server-in-centos-7/

## Prerequisite
- PXE server: CentOS 7
- PXE client: CentOS-7-x86_64-DVD-2009.iso

## Configure the Network
Configure the PXE boot server with a fixed IP address 10.0.0.10 on the NIC which will provide PXE services.

## Setup PXE boot server with ansible

```
ansible-playbook kickstart.yml
```

To test FTP Installation Source network path:

```
ftp://10.0.0.10/pub
```

To debug PXE server for eventual misconfigurations or other information and diagnostics in live mode:

```
sudo tail  -f /var/log/messages
```
