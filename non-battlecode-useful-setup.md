
- [Outline of this document](#outline-of-this-document)
  - [Setup your computer, we will cover each item](#setup-your-computer-we-will-cover-each-item)
    - [- nvm - node version manager](#--nvm---node-version-manager)
    - [- npm - node package manager](#--npm---node-package-manager)
    - [- yarn - facebook's version of node](#--yarn---facebooks-version-of-node)
  - [How to Install Node.js and npm on Ubuntu](#how-to-install-nodejs-and-npm-on-ubuntu)
  - [Check os version in Linux](#check-os-version-in-linux)
  - [/etc/os-release file](#etcos-release-file)
  - [lsb_release command](#lsb_release-command)
  - [hostnamectl command](#hostnamectl-command)
  - [uname command](#uname-command)
    - [**Installation instructions - node**](#installation-instructions---node)
    - [**Installation instructions - yarn**](#installation-instructions---yarn)
  - [**Installing Node.js and npm using NVM**](#installing-nodejs-and-npm-using-nvm)
    - [**1. Installing NVM (Node Version Manager) script**](#1-installing-nvm-node-version-manager-script)
    - [**2. Installing Node.js and npm**](#2-installing-nodejs-and-npm)
- [Install Yarn](#install-yarn)
    - [Debian / Ubuntu](#debian--ubuntu)
    - [**Install build-essential Package**](#install-build-essential-package)
    - [**Create C program, compile and run it**](#create-c-program-compile-and-run-it)

# Outline of this document  
## Setup your computer, we will cover each item    
### - nvm - node version manager  
### - npm - node package manager  
### - yarn - facebook's version of node  


## How to Install Node.js and npm on Ubuntu

[https://linuxize.com/post/how-to-install-node-js-on-ubuntu-18.04/](https://linuxize.com/post/how-to-install-node-js-on-ubuntu-18.04/)


## Check os version in Linux

The procedure to find os name and version on Linux:



1. Open the terminal application (bash shell)
2. For remote server login using the ssh: **<code>ssh user@server-name</code></strong>
3. Type any one of the following command to find os name and version in Linux: \
<strong><code>cat /etc/os-release \
lsb_release -a \
hostnamectl</code></strong>
4. Type the following command to find Linux kernel version: \
<strong><code>uname -r</code></strong>

Let us see all examples in detailed.


## /etc/os-release file

Type the following [cat command](https://www.cyberciti.biz/faq/linux-unix-appleosx-bsd-cat-command-examples/):


```
    $ cat /etc/os-release
```


Sample outputs:


```
NAME="Ubuntu"
VERSION="17.10 (Artful Aardvark)"
ID=ubuntu
ID_LIKE=debian
PRETTY_NAME="Ubuntu 17.10"
VERSION_ID="17.10"
HOME_URL="https://www.ubuntu.com/"
SUPPORT_URL="https://help.ubuntu.com/"
BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"
VERSION_CODENAME=artful
UBUNTU_CODENAME=artful
```


## lsb_release command

The lsb_release command gives LSB (Linux Standard Base) and distribution-specific information on the CLI. The syntax is:


```
    $ lsb_release -a
```

Sample outputs:


```
LSB Version:        :core-4.1-amd64:core-4.1-noarch
Distributor ID:        CentOS
Description:        CentOS Linux release 7.4.1708 (Core) 
Release:        7.4.1708
Codename:        Core
```

## hostnamectl command

Use hostnamectl command to query and change the system hostname and related settings. Just type the following command to check OS name and Linux kernel version:


```
    $ hostnamectl
```


Sample outputs:


```
  Static hostname: nixcraft-www-42
         Icon name: computer-vm
           Chassis: vm
        Machine ID: beb217fbb4324b7d9959f78c279e6599
           Boot ID: 10f00cc5ca614b518a84d1793d0134bc
    Virtualization: qemu
  Operating System: Ubuntu 16.04.3 LTS
            Kernel: Linux 4.10.0-42-generic
      Architecture: x86-64
```



## uname command

Just print Linux kernel version, run:


```
    $ uname -r
```


Sample outputs:



<p id="gdcalert2" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image2.jpg). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert3">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image2.jpg "image_tooltip")


Another option is to type the following command:

```
    $ cat /proc/version
```

Sample outputs:


```
Linux version 3.10.0-693.11.6.el7.x86_64 (mockbuild@x86-041.build.eng.bos.redhat.com) (gcc version 4.8.5 20150623 (Red Hat 4.8.5-16) (GCC) ) #1 SMP Thu Dec 28 14:23:39 EST 2017
```

### **Installation instructions - node**

[https://github.com/nodesource/distributions/blob/master/README.md#debinstall](https://github.com/nodesource/distributions/blob/master/README.md#debinstall)

Node.js v15.x:


```
# Using Ubuntu (Digitalocean)
curl -sL https://deb.nodesource.com/setup_15.x | sudo -E bash -
sudo apt-get install -y nodejs

# Using Debian, as root  (Chromebook)
curl -sL https://deb.nodesource.com/setup_15.x | sudo bash -
sudo apt-get install -y nodejs
```

### **Installation instructions - yarn**


```
curl -sL https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
     echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
     sudo apt-get update && sudo apt-get install yarn
```


connorstom@penguin:~$ node --version

v15.3.0

connorstom@penguin:~$ yarn --version

1.22.5


## **Installing Node.js and npm using NVM**

NVM (Node Version Manager) is a bash script used to manage multiple active Node.js versions. With NVM you can install and uninstall any specific Node.js version you want to use or test.

To install Node.js and npm using NVM on your Ubuntu system, perform the following steps:


### **1. Installing NVM (Node Version Manager) script**

To download and install the `nvm` script run:

Also check latest info from: [https://github.com/nvm-sh/nvm](https://github.com/nvm-sh/nvm)


```
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.35.3/install.sh | bash
```

The command above will clone the NVM repository from Github to the `~/.nvm` directory:

The script clones the nvm repository to ~/.nvm, and attempts to add the source lines from the snippet below to the correct profile file (~/.bash_profile, ~/.zshrc, ~/.profile, or ~/.bashrc).


```
=> Close and reopen your terminal to start using nvm or run the following to use it now:

export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  # This loads nvm bash_completion
```


As the output above says, you should either close and reopen the terminal or run the commands to [add the path](https://linuxize.com/post/how-to-add-directory-to-path-in-linux/) to `nvm` script to the current shell session. You can do whatever is easier for you.

Once the script is in your `PATH`, verify that `nvm` was properly installed by typing:


```
nvm --version
0.34.0
```

### **2. Installing Node.js and npm**

Now that the `nvm` is installed you can install the latest available version of Node.js, by typing:


```
nvm install node
```


The output should look something like this:


```
Downloading and installing node v12.8.1...
Downloading https://nodejs.org/dist/v12.8.1/node-v12.8.1-linux-x64.tar.xz...
######################################################################### 100.0%
Computing checksum with sha256sum
Checksums matched!
Now using node v12.8.1 (npm v6.10.2)
Creating default alias: default -> node (-> v12.8.1)
```

Once the installation is completed, verify it by printing the Node.js version:

```
node --version
v12.8.1
```

Let’s install two more versions, the latest LTS version and version 8.10.0

```
nvm install --lts
nvm install 8.10.0
nvm install 10.20.0
```

To list installed Node.js versions type:


```
nvm ls
```

The output should look something like this:


```
->      v8.10.0
       v10.16.3
        v12.8.1
default -> node (-> v12.8.1)
node -> stable (-> v12.8.1) (default)
stable -> 12.8 (-> v12.8.1) (default)
iojs -> N/A (default)
unstable -> N/A (default)
lts/* -> lts/dubnium (-> v10.16.3)
lts/argon -> v4.9.1 (-> N/A)
lts/boron -> v6.17.1 (-> N/A)
lts/carbon -> v8.16.1 (-> N/A)
lts/dubnium -> v10.16.3
```


The entry with an arrow on the right (-> v8.10.0) is the Node.js version used in the current shell session and the default version is set to v12.8.1. Default version is the version that will be active when opening new shells.

You can change the currently active version with:


```
nvm use 10.16.3
Now using node v10.16.3 (npm v6.9.0)
```


If you want to change the default Node.js version use the following command:


```
nvm alias default 10.16.3
```

# Install Yarn

Before you start using Yarn, you'll first need to install it on your system. There are a growing number of different ways to install Yarn:


Operating system:


Debian / Ubuntu 


Version:


         Stable (1.22.5)         Release Candidate (1.22.0)         Nightly (1.23.0-20200928.1349)       


### Debian / Ubuntu

On Debian or Ubuntu Linux, you can install Yarn via our Debian package repository. You will first need to configure the repository:


```
curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
sudo apt update && sudo apt install yarn
sudo apt update && sudo apt install apt-utils
```

### **Install build-essential Package**

[https://www.osetc.com/en/how-to-install-build-essential-on-ubuntu-16-04-18-04-linux.html](https://www.osetc.com/en/how-to-install-build-essential-on-ubuntu-16-04-18-04-linux.html)


---

The build-essential package is already available on the default Ubuntu repository. so you just need to install it with the apt install command. Before installing build-essential package, you need to update the Ubuntu repo index with the following command:


```
$ sudo apt update
```


Then type the following command to install build-essential package:

```
$ sudo apt install build-essential
```


Outputs:


```
devops@devops-osetc:~$ sudo apt install build-essential
Reading package lists... Done
Building dependency tree
Reading state information... Done
The following packages were automatically installed and are no longer required:
libllvm6.0 x11proto-dri2-dev x11proto-gl-dev
Use 'sudo apt autoremove' to remove them.
The following NEW packages will be installed:
build-essential
0 upgraded, 1 newly installed, 0 to remove and 0 not upgraded.
Need to get 4,758 B of archives.
After this operation, 20.5 kB of additional disk space will be used.
Get:1 http://mirrors.aliyun.com/ubuntu bionic/main amd64 build-essential amd64 12.4ubuntu1 [4,758 B]
Fetched 4,758 B in 1s (3,325 B/s)
Selecting previously unselected package build-essential.
(Reading database ... 231616 files and directories currently installed.)
Preparing to unpack .../build-essential_12.4ubuntu1_amd64.deb ...
Unpacking build-essential (12.4ubuntu1) ...
Setting up build-essential (12.4ubuntu1) ...
```

**Check GCC Version**

After the installation process is completed, you can confirm your installation by checking for GCC version with the following command:


```
$ gcc --version
```


Outputs:


```
devops@devops-osetc:~$ gcc --version
gcc (Ubuntu 7.3.0-27ubuntu1~18.04) 7.3.0
Copyright (C) 2017 Free Software Foundation, Inc.
This is free software; see the source for copying conditions. There is NO
warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
```

### **Create C program, compile and run it**

Let’s write a simple C program as below:


```
#include <stdio.h>

int main()
{
    printf("Hell, World!\n ");
}
```

Save this program as test.c file in your Ubuntu system, and try to execute the following command to compile and execute it:

```
$ gcc -o test test.c
$ ./test
```

Outputs:


```
devops@devops-osetc:~$ gcc -o test test.c
devops@devops-osetc:~$ ./test
Hell, World!
```

---

You should know that how to install build-essential on your Ubuntu 14.04 or 16.04 or 18.04 Linux from this guide. And if you want to learn more about the build-essential, you can go the below [official web site](https://packages.ubuntu.com/xenial/build-essential) to checking the getting started guide directly.
