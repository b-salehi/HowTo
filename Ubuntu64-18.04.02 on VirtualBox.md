# Install Ubuntu 18.04.02 on Virtual Box

#### Guest Additions

Guest Additions are designed to be installed inside a virtual machine after the guest operating system has been installed

The Oracle VM VirtualBox Guest Additions for all supported guest operating systems are provided as a single CD-ROM image file which is called `VBoxGuestAdditions.iso`.

offer the following features:

- Mouse pointer integration
- Shared folders
- Better video support
- Shared clipboard

prepare system kernel and  install the following packages on your Linux system before starting the installation

```sh
~$ sudo apt install linux-headers-$(uname -r) build-essential  dkms
```
In the **Devices** menu in the virtual machine's menu bar, Oracle VM VirtualBox has a menu item **Insert Guest Additions CD Image**

------


#### Shared Folders

access files of your host system from within the guest system

VirtualBox can only be access by members of  *vboxsf*  group created by the earlier by the autorun.sh script

```shell
$ sudo adduser <username> vboxsf
```
click on Devices, again, from the VirtualBox menu option of the VM window
Devices  → Shared Folders → Shared Folder Settings …

------
### Installing CURL

```shell
$ sudo apt-get update
```

CURL is available in the official package repository of Ubuntu 18.04 Bionic Beaver

```shell
$ sudo apt-get install curl
```

----

### Installation Node.js instructions

**Node.js v10.x**:

```shell
# Using Ubuntu
curl -sL https://deb.nodesource.com/setup_10.x | sudo -E bash -
sudo apt-get install -y nodejs
```

------

### Install Git on Linux

latest stable version

```shell
# apt-get install git
```

this PPA provides the latest stable upstream Git version

```shell
# add-apt-repository ppa:git-core/ppa
# apt update; apt install git
```

