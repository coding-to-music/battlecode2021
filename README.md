# BattleCode 2021 - Overview  
<img width="800px" src="https://github.com/coding-to-music/battlecode2021/blob/main/Assets/2021_Battlecode.png?raw=true" align="center" alt="Battlecode 2021 Image" />
</b>
-  
</b>
- [BattleCode 2021 - Overview](#battlecode-2021---overview)
  - [Introduction](#introduction)
  - [Why this document is needed](#why-this-document-is-needed)
  - [Account and Team Creation](#account-and-team-creation)
  - [Links and resources for this year's Battlecode](#links-and-resources-for-this-years-battlecode)
- [Outline of this document](#outline-of-this-document)
  - [Setup your computer, we will cover each item](#setup-your-computer-we-will-cover-each-item)
    - [- Enable Linux on your Chromebook](#--enable-linux-on-your-chromebook)
    - [- Setup editor such as vscode, IntelliJ, Eclipse etc](#--setup-editor-such-as-vscode-intellij-eclipse-etc)
    - [- Detailed instructions for vscode installation](#--detailed-instructions-for-vscode-installation)
      - [- vscode keyring so your settings persist when you log out](#--vscode-keyring-so-your-settings-persist-when-you-log-out)
      - [- vscode extensions such as this Table of Contents](#--vscode-extensions-such-as-this-table-of-contents)
      - [- vscode extensions for Markup, Go CSS JavaScript Java etc](#--vscode-extensions-for-markup-go-css-javascript-java-etc)
    - [- handy aliases and abbreviations into .bashrc and .bash_aliases](#--handy-aliases-and-abbreviations-into-bashrc-and-bash_aliases)
    - [- create .ssh directory and generate SSH public and private keys](#--create-ssh-directory-and-generate-ssh-public-and-private-keys)
    - [- git](#--git)
    - [- vscode](#--vscode)
    - [- use your ssh keys](#--use-your-ssh-keys)
      - [- netflify - uses ssh keys](#--netflify---uses-ssh-keys)
      - [- digitalocean - uses ssh keys](#--digitalocean---uses-ssh-keys)
      - [- github - uses ssh keys](#--github---uses-ssh-keys)
    - [- nvm - node version manager](#--nvm---node-version-manager)
    - [- npm - node package manager](#--npm---node-package-manager)
    - [- yarn - facebook's version of node](#--yarn---facebooks-version-of-node)
    - [- End general setup of your computer](#--end-general-setup-of-your-computer)
  - [- Begin MIT Content](#--begin-mit-content)
    - [- Java version 8](#--java-version-8)
    - [- Set environment variables `PATH` and `CLASSPATH` `JAVA_HOME` etc](#--set-environment-variables-path-and-classpath-java_home-etc)
  - [- Begin Battlecode](#--begin-battlecode)
    - [- Clone the Battlecode Scaffold, where you can run your robot](#--clone-the-battlecode-scaffold-where-you-can-run-your-robot)
    - [- Run the sample robot](#--run-the-sample-robot)
    - [- Create and modify your own robot](#--create-and-modify-your-own-robot)
    - [- Run your robot](#--run-your-robot)
- [now the content begins](#now-the-content-begins)
- [Setup your computer, we will cover each item](#setup-your-computer-we-will-cover-each-item-1)
  - [- Enable Linux on your Chromebook](#--enable-linux-on-your-chromebook-1)
  - [- details about your computer and operating system](#--details-about-your-computer-and-operating-system)
  - [- Setup editor such as vscode, IntelliJ, Eclipse etc](#--setup-editor-such-as-vscode-intellij-eclipse-etc-1)
  - [- Detailed instructions for vscode installation](#--detailed-instructions-for-vscode-installation-1)
    - [- vscode keyring so your settings persist when you log out](#--vscode-keyring-so-your-settings-persist-when-you-log-out-1)
    - [- vscode extensions such as this Table of Contents](#--vscode-extensions-such-as-this-table-of-contents-1)
    - [- vscode extensions for Markup, Go CSS JavaScript Java etc](#--vscode-extensions-for-markup-go-css-javascript-java-etc-1)
  - [- handy aliases and abbreviations into .bashrc and .bash_aliases](#--handy-aliases-and-abbreviations-into-bashrc-and-bash_aliases-1)
  - [- git](#--git-1)
  - [- create .ssh directory and generate SSH public and private keys](#--create-ssh-directory-and-generate-ssh-public-and-private-keys-1)
  - [- use your ssh keys](#--use-your-ssh-keys-1)
    - [- netflify - uses ssh keys](#--netflify---uses-ssh-keys-1)
    - [- digitalocean - uses ssh keys](#--digitalocean---uses-ssh-keys-1)
    - [- github - uses ssh keys](#--github---uses-ssh-keys-1)
  - [- nvm - node version manager](#--nvm---node-version-manager-1)
  - [- npm - node package manager](#--npm---node-package-manager-1)
  - [- yarn - facebook's version of node](#--yarn---facebooks-version-of-node-1)
  - [**0 Installing Git for Linux**](#0-installing-git-for-linux)
  - [**1 Installing Git for Linux**](#1-installing-git-for-linux)
  - [**2 Configuring GitHub**](#2-configuring-github)
  - [Chromebook is Debian](#chromebook-is-debian)
  - [Digitalocean is Ubuntu](#digitalocean-is-ubuntu)
    - [Install Git on the server](#install-git-on-the-server)
  - [SSH Keys](#ssh-keys)
    - [Create a directory for the public keys](#create-a-directory-for-the-public-keys)
    - [Create SSH Key for Github](#create-ssh-key-for-github)
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
    - [**Visual Studio Code on Linux**](#visual-studio-code-on-linux)
    - [**VS Code install for Debian and Ubuntu based distributions**](#vs-code-install-for-debian-and-ubuntu-based-distributions)
  - [**Installing Visual Studio Code on Ubuntu**](#installing-visual-studio-code-on-ubuntu)
  - [**Starting Visual Studio Code**](#starting-visual-studio-code)
  - [**Updating Visual Studio Code**](#updating-visual-studio-code)
    - [- Set environment variables `PATH` and `CLASSPATH` `JAVA_HOME` etc](#--set-environment-variables-path-and-classpath-java_home-etc-1)
  - [- Begin Battlecode](#--begin-battlecode-1)
    - [- Clone the Battlecode Scaffold, where you can run your robot](#--clone-the-battlecode-scaffold-where-you-can-run-your-robot-1)
  - [Changes to .bashrc for your environment variables, PATH and JAVA_HOME](#changes-to-bashrc-for-your-environment-variables-path-and-java_home)
    - [This update-alternatives is something that may be useful but you probably do not need it](#this-update-alternatives-is-something-that-may-be-useful-but-you-probably-do-not-need-it)
  - [Validating Java works correctly](#validating-java-works-correctly)
    - [To verify the installation, get the Java version](#to-verify-the-installation-get-the-java-version)
    - ['Which' Java as a validation test](#which-java-as-a-validation-test)
  - [Cleaning up](#cleaning-up)
- [FROM HERE ON is from Last Year and needs to be edited/corrected](#from-here-on-is-from-last-year-and-needs-to-be-editedcorrected)
- [Install the Scaffold](#install-the-scaffold)
  - [STEP 2: DOWNLOAD the competition scaffold for BATTLECODE](#step-2-download-the-competition-scaffold-for-battlecode)
    - [Error - Terminal won’t load from within Intellij and Gradle won’t build](#error---terminal-wont-load-from-within-intellij-and-gradle-wont-build)
- [STEP 3: Build the game - LOCAL SETUP](#step-3-build-the-game---local-setup)
- [Use VSCode](#use-vscode)
- [Install IntelliJ](#install-intellij)
    - [View instructions for:](#view-instructions-for)
  - [Idea Installation Instructions](#idea-installation-instructions)
- [Install the sample player bot](#install-the-sample-player-bot)
- [Have the sample bot play itself](#have-the-sample-bot-play-itself)
- [Modify the bot and make it your own](#modify-the-bot-and-make-it-your-own)
- [RUNNING GAME FROM THE TERMINAL](#running-game-from-the-terminal)
- [Run a Match](#run-a-match)
- [Upload the bot to compete against others](#upload-the-bot-to-compete-against-others)
- [Upload Your Bot and Scrimmage](#upload-your-bot-and-scrimmage)
  
## Introduction  
This is the Battlecode 2021 contest website, which will be your main hub for all Battlecode-related things for the duration of the contest. For a general overview of what Battlecode is, visit our landing page.  
This year's game is a thrilling survival adventure involving 🍲, ▀⛓, 🐮, 🤖, and more. You will write bots in Java.  
## Why this document is needed  
## Account and Team Creation  
To participate in Battlecode, you need an account and a team. Each team can consist of 1 to 4 people.  
Create an account at [battlecode.org](https://2021.battlecode.org/getting-started), and then go to the [team](https://2021.battlecode.org/team) section to either create or join a team.  
## Links and resources for this year's Battlecode  
[battlecode.org - getting started](https://2020.battlecode.org/getting-started)  
[Discord](https://discord.com/channels/386965718572466197/386965718572466199)  
[Battlecode Github](https://github.com/battlecode/battlecode21)  
[Scaffold Repository](https://github.com/battlecode/battlecode21-scaffold)    
[Robot properties](https://2021.battlecode.org/javadoc/index.html)  
[Game Specifications for this year](https://2021.battlecode.org/specs/specs.md.html#)  
Some tweets about battlecode are on [Twitter](https://twitter.com/search?q=thomasconnors%20battlecode)  
A great postmortum from 2020 [Team Battlegaode](http://web.mit.edu/agrebe/www/battlecode/20/index.html)    
# Outline of this document  
## Setup your computer, we will cover each item    
### - Enable Linux on your Chromebook  
### - Setup editor such as vscode, IntelliJ, Eclipse etc  
### - Detailed instructions for vscode installation  
#### - vscode keyring so your settings persist when you log out    
#### - vscode extensions such as this Table of Contents  
#### - vscode extensions for Markup, Go CSS JavaScript Java etc  
### - handy aliases and abbreviations into .bashrc and .bash_aliases  
### - create .ssh directory and generate SSH public and private keys  
### - git  
### - vscode  
### - use your ssh keys  
#### - netflify - uses ssh keys  
#### - digitalocean - uses ssh keys  
#### - github - uses ssh keys  
### - nvm - node version manager  
### - npm - node package manager  
### - yarn - facebook's version of node  
### - End general setup of your computer  
## - Begin MIT Content  
### - Java version 8  
### - Set environment variables `PATH` and `CLASSPATH` `JAVA_HOME` etc  
## - Begin Battlecode   
### - Clone the Battlecode Scaffold, where you can run your robot  
### - Run the sample robot  
### - Create and modify your own robot  
### - Run your robot    
  



# now the content begins      
# Setup your computer, we will cover each item    
## - Enable Linux on your Chromebook    
## - details about your computer and operating system    
## - Setup editor such as vscode, IntelliJ, Eclipse etc    
## - Detailed instructions for vscode installation  
### - vscode keyring so your settings persist when you log out    
### - vscode extensions such as this Table of Contents  
### - vscode extensions for Markup, Go CSS JavaScript Java etc  
## - handy aliases and abbreviations into .bashrc and .bash_aliases  
## - git  
## - create .ssh directory and generate SSH public and private keys  
## - use your ssh keys  
### - netflify - uses ssh keys  
### - digitalocean - uses ssh keys  
### - github - uses ssh keys  
## - nvm - node version manager  
## - npm - node package manager  
## - yarn - facebook's version of node  
## **0 Installing Git for Linux**  

Edit the file .bash_aliases and put the contents from GitHub


```
source ~/.bashrc
```


The above command is for Ubuntu and works on all Recent Ubuntu versions, tested from Ubuntu 


## **1 Installing Git for Linux**

Download and install Git for Linux:


```
sudo apt-get install git
```


The above command is for Ubuntu and works on all Recent Ubuntu versions, tested from Ubuntu 16.04 to Ubuntu 18.04 LTS (Bionic Beaver) and it's likely to work the same way on future versions.


## **2 Configuring GitHub**

Once the installation has successfully completed, the next thing to do is to set up the configuration details of the GitHub user. To do this use the following two commands by replacing "user_name" with your GitHub username and replacing "email_id" with your email-id you used to create your GitHub account.


```
git config --global user.name coding-to-music
git config --global user.email connors.tom@gmail.com
```


The following image shows an example of my configuration with my "user_name" being "akshaypai" and my "email_id" being "abc123@gmail.com"


## Chromebook is Debian


```
connorstom@penguin:~$ cat /etc/os-release
PRETTY_NAME="Debian GNU/Linux 10 (buster)"
NAME="Debian GNU/Linux"
VERSION_ID="10"
VERSION="10 (buster)"
VERSION_CODENAME=buster
ID=debian
HOME_URL="https://www.debian.org/"
SUPPORT_URL="https://www.debian.org/support"
BUG_REPORT_URL="https://bugs.debian.org/"
```



## Digitalocean is Ubuntu


### Install Git on the server

 sudo apt-get install git

Now git should be installed. To check use

 git --version

git version 2.19.1


## SSH Keys


### Create a directory for the public keys

In root

Mkdir .ssh

Chmod 700 .ssh

Cd .ssh

Create SSH public and private keys

Store them here

Chmod 600 private_key


### Create SSH Key for Github

Now you need to create your SSH key for Github

ssh-keygen -t rsa -C “connors.tom@gmail.com”

It will get saved to 

home/tom/.ssh/id_rsa                // this is the private key, very long paragraph

home/tom/.ssh/id_rsa.pub         // this is the public key,         short paragraph

Copy that key in that file. I would suggest using Win SCP to download the file similar to FTP

ssh-rsa 
7 lines long private key short paragraph this is what you will paste into GitHub and Digitalocean
e1f0vfsMPOANChLOUWbSJTtf4s4P2x6CAYCOQYcd “connors.tom@gmail.com”
-----BEGIN RSA PRIVATE KEY-----
really big long private key
-----END RSA PRIVATE KEY-----

Once you copy the key, sign into Github and goto “Settings->SSH and GPG Keys” and add and name the new key 



<p id="gdcalert1" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image1.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert2">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image1.png "image_tooltip")



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


### **Visual Studio Code on Linux**


### **VS Code install for Debian and Ubuntu based distributions**

[https://code.visualstudio.com/docs/setup/linux](https://code.visualstudio.com/docs/setup/linux)

The easiest way to install Visual Studio Code for Debian/Ubuntu based distributions is to download and install the [.deb package (64-bit)](https://go.microsoft.com/fwlink/?LinkID=760868), either through the graphical software center if it's available, or through the command line with:


```
sudo apt install ./<file>.deb

download the file from the website to downloads and move it to linux file system then run:

https://code.visualstudio.com/docs/setup/linux
https://github.com/nodesource/distributions/blob/master/README.md#debinstall

# If you're on an older Linux distribution, you will need to run this instead:
# sudo dpkg -i <file>.deb
# sudo apt-get install -f # Install dependencies
connorstom@penguin:~$ code --version
1.51.1
e5a624b788d92b8d34d1392e4c4d9789406efe8f
x64
```


Installing the .deb package will automatically install the apt repository and signing key to enable auto-updating using the system's package manager. Note that 32-bit and .tar.gz binaries are also available on the [VS Code download page](https://code.visualstudio.com/Download).

The repository and key can also be installed manually with the following script:


```
curl https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > packages.microsoft.gpg
sudo install -o root -g root -m 644 packages.microsoft.gpg /usr/share/keyrings/
sudo sh -c 'echo "deb [arch=amd64 signed-by=/usr/share/keyrings/packages.microsoft.gpg] https://packages.microsoft.com/repos/vscode stable main" > /etc/apt/sources.list.d/vscode.list'
```


Then update the package cache and install the package using:


```
sudo apt-get install apt-transport-https
sudo apt-get update
sudo apt-get install code # or code-insiders

sudo apt install gnome-keyring
```



## **Installing Visual Studio Code on Ubuntu**

[https://linuxize.com/post/how-to-install-visual-studio-code-on-ubuntu-18-04/](https://linuxize.com/post/how-to-install-visual-studio-code-on-ubuntu-18-04/)

To install Visual Studio Code on your Ubuntu system, follow these steps:



1. First, update the packages index and install the dependencies by typing:
2. `sudo apt update`
3. `sudo apt install software-properties-common apt-transport-https wget`
4. Next, import the Microsoft GPG key using the following [wget command](https://linuxize.com/post/wget-command-examples/):
5. `wget -q https://packages.microsoft.com/keys/microsoft.asc -O- | sudo apt-key add -`
6. And enable the Visual Studio Code repository by typing:
7. `sudo add-apt-repository "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main"`
8. Once the [apt repository is enabled](https://linuxize.com/post/how-to-add-apt-repository-in-ubuntu/), install the latest version of Visual Studio Code with:
9. `sudo apt update`
10. `sudo apt install code`

That’s it. Visual Studio Code has been installed on your Ubuntu desktop and you can start using it.


## **Starting Visual Studio Code**

Now that VS Code is installed on your Ubuntu system you can launch it either from the command line by typing `code` or by clicking on the VS Code icon (`Activities -> Visual Studio Code`).

When you start VS Code for the first time, a window like the following should appear:
<p id="gdcalert3" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image3.jpg). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert4">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>
![alt_text](images/image3.jpg "image_tooltip")
You can now start installing extensions and configuring VS Code according to your preferences.
## **Updating Visual Studio Code**
When a new version is released you can update the Visual Studio Code package through your desktop standard Software Update tool or by running the following commands in your terminal:
```
sudo apt update
sudo apt upgrade
## - End general setup of your computer
## - Begin MIT Content
### - Java version 8
# Install Java Release 8  
## Installation Instructions for Java JDK  
If you're unsure how to install the JDK, you can find instructions for all operating systems here (pay attention to PATH and CLASSPATH).  
   
https://docs.datastax.com/en/jdk-install/doc/jdk-install/installOpenJdkDeb.html  
   
http://openjdk.java.net/install/  
   
I am using a chromebook, which is Debian flavor of Linux   
There are two related packages  
- JRE - Java Runtime Environment
- JDK - Java Development Kit
  
## Download the correct Java Version 8  
Before the file can be downloaded, you must accept the license agreement. The archive binary can be installed by anyone (not only root users), in any location that you can write to. However, only the root user can install the JDK into the system location.
// Change directory to the location where you would like the JDK to be installed, then move the .tar.gz archive binary to the current directory.  
That leads to this page [here, you are looking for Java SE 8](https://www.oracle.com/java/technologies/javase/javase-jdk8-downloads.html)
```java
// Previously I had Java - let's see if it works
// Oops, I ran into a problem and got this error 
connorstom@penguin:$ java -version
bash: /usr/local/jdk1.8.0_271/bin/java: No such file or directory
// yet I appeared to have java installed
connorstom@penguin:$ find /usr -name java
/usr/bin/java
/usr/lib/jvm/jdk1.8.0_271/bin/java
/usr/lib/jvm/jdk1.8.0_271/jre/bin/java
/usr/local/jdk1.8.0_271/bin/java
/usr/local/jdk1.8.0_271/jre/bin/java
/usr/share/bash-completion/completions/java
/usr/share/code/resources/app/extensions/java
```
From this video [How To Install Oracle Java 8 JDK on Linux - Ubuntu 20.04 / 18.04 / 16.04 LTS / Debian](https://youtu.be/kiaWng4wR-k)
```java
// ok lets try this one
- Linux x64 Compressed Archive	 
- 136.51 MB	 
- jdk-8u271-linux-x64.tar.gz  
// I downloaded this and left it in my root home directory, it is just a temporary file we will delete it later
jdk-8u271-linux-x64.tar.gz
// you may not need to make this next directory, you may already have it
mkdir /usr/lib/jvm
cd /usr/lib/jvm
// untar the file that is located in your home dir
sudo tar -xzvf ~/jdk-8u271-linux-x64.tar.gz 
```
The Java Development Kit files are installed in a directory called `jdk1.8.0_version` in the current directory.  
```java
// this directory was just created
/usr/lib/jvm/jdk1.8.0_271
```
### - Set environment variables `PATH` and `CLASSPATH` `JAVA_HOME` etc
## - Begin Battlecode 
### - Clone the Battlecode Scaffold, where you can run your robot
## Changes to .bashrc for your environment variables, PATH and JAVA_HOME  
Paste thise into your Path in your .bashrc 
```java
export JAVA_HOME="/usr/lib/jvm/jdk1.8.0_271/bin"
export PATH=$PATH:/usr/lib/jvm/jdk1.8.0_271/bin:/usr/lib/jvm/jdk1.8.0_271/jre/bin
```
### This update-alternatives is something that may be useful but you probably do not need it
```java
// probably not needed
sudo update-alternatives --install "/usr/bin/java" "java" "/usr/lib/jvm/jdk1.8.0_271/bin/java" 0
sudo update-alternatives --install "/usr/bin/javac" "javac" "/usr/lib/jvm/jdk1.8.0_271/bin/javac" 0
sudo update-alternatives --set java /usr/lib/jvm/jdk1.8.0_271/bin/java
sudo update-alternatives --set javac /usr/lib/jvm/jdk1.8.0_271/bin/javac
// you can test this but it did not work for me
update-alternatives --list java
update-alternatives --list javac
```
## Validating Java works correctly
### To verify the installation, get the Java version
```java
connorstom@penguin:~$ env | grep JAVA
JAVA_HOME=/usr/lib/jvm/jdk1.8.0_271/bin
// test to find the java version
connorstom@penguin:~$ java -version
java version "1.8.0_271"
Java(TM) SE Runtime Environment (build 1.8.0_271-b09)
Java HotSpot(TM) 64-Bit Server VM (build 25.271-b09, mixed mode)
```
### 'Which' Java as a validation test   
This will print the version of the java tool, if it can find it. 
If the version is old or you get the error `java: Command not found`, then the path is not properly set.  
Determine which java executable is the first one found in your PATH  
```java
connorstom@penguin:~$ which java
/usr/bin/java
```
## Cleaning up 
Delete the .tar.gz file if you want to save disk space.  
      
This may also be useful but I have not tested it yet
```java
% . /.profile  
// Verify that the path is set by repeating the java command  
% java -version  
```   
```java
// Modify build.gradle to view the Java version  
task version {  
    group 'battlecode'  
    doLast{  
        println("\nJDK version: ${System.properties['java.home']}")  
        println("\nVersion: " + versions.battlecode + "\n")  
    }  
}  
```
# FROM HERE ON is from Last Year and needs to be edited/corrected   
# Install the Scaffold   
## STEP 2: DOWNLOAD the competition scaffold for BATTLECODE  
Next, you should download the Battlecode 2021 scaffold. To get up and running quickly, you can click "Clone or download" and then "Download ZIP," and move on to the next step.  
We recommend, however, that you instead use Git to organize your code. If you haven't used Git before, read this guide (or wait for our lecture covering it). On the scaffold page, click "Use this template." Importantly, on the next page, make your new repo private (you don't want other teams to steal your code!). You can then clone your newly created repo and invite your team members to collaborate on it.  
```java
git clone https://github.com/battlecode/battlecode21-scaffold.git
```
    
### Error - Terminal won’t load from within Intellij and Gradle won’t build  
Message when trying to open Terminal within Intellij  
Platform SDK does not point to valid JDK  
  
# STEP 3: Build the game - LOCAL SETUP  
Open a terminal in the scaffold you just downloaded. Run the commands `./gradlew update` and `./gradlew build`  
We recommend using an IDE like IntelliJ IDEA or Eclipse to work on Battlecode, but you can also use your favorite text editor combined with a terminal. Battlecode 2020 uses Gradle to run tasks like run, debug and jarForUpload (but don't worry about that — you don't need to install it).  
  
# Use VSCode  
# Install IntelliJ
### View instructions for:  
- IntelliJ IDEAEclipseTerminal  
- Install IntelliJ IDEA Community Edition from here.  
In the Welcome to IntelliJ IDEA window that pops up when you start IntelliJ, select Import Project  
In the Select File or Dictionary to Import window, select the build.gradle file in the scaffold folder.  
- Hit OK.  
We need to set the jdk properly; 
- open the settings with File > Settings (IntelliJ IDEA > Preferences on Mac) or ctrl+alt+s. 
- Navigate to Build, Execution, Deployment > Build Tools > Gradle and 
- change Gradle JVM to 1.8  
Time for a first build! 
- On the right side of the screen, click the small button that says gradle and has a picture of an elephant. 
- Navigate to battlecode20-scaffold > Tasks > battlecode and double click on build. 
- This will install the client and engine for you.  
If you haven't seen any errors, you should be good to go.  
There should now be a folder called client in your scaffold folder; if you go in there, and double click the Battlecode Client application, you should be able to run and watch matches. (Please don't move that application, it will be sad.) If you're on Linux, navigate to the client folder and run ./battlecode-visualizer to launch the client.  
  
  
## Idea Installation Instructions  
Unpack the idea idea-2019.3.1.tar.gz file to an empty directory using the following command:   
  
```java
tar -xzf idea-2019.3.1.tar.gz  
```
  
Note: A new instance MUST NOT be extracted over an existing one. The target folder must be empty.  
```java
Run idea.sh from the bin subdirectory.  
```
# Install the sample player bot  
  
# Have the sample bot play itself  
  
# Modify the bot and make it your own  
Place each version of your robot in a new subfolder in the `src` folder. Make sure every version has a `RobotPlayer.java`    
# RUNNING GAME FROM THE TERMINAL  
Open a terminal in the scaffold. Run the commands `./gradlew run -Pmaps=[map] -PteamA=[Team A] -PteamB=[Team B]`  
# Run a Match  
Player code is in the src directory of the scaffold: each package inside src corresponds to one distinct player. We have provided examplefuncsplayer, and you can create your own player by either modifying it or copying and renaming it.  
You should have a client application in the client folder. Launch it, and go to the Runner section. There, you can specify which players to run against each other, and on which map, and you can view the match as it is running.  
You can also run a match without the client, by invoking the Gradle task run. For example, gradle run -PteamA=examplefuncsplayer -PteamB=examplefuncsplayer -Pmaps=FourLakeLand runs examplefuncsplayer against itself on the FourLakeLand map. This produces a replay file in the matches directory of the scaffold, which you can upload to the client to view.  

# Upload the bot to compete against others  
# Upload Your Bot and Scrimmage  
Create a zip file containing only your robot code (only 1 package), and uploaded it to the submissions page.  
Your bot will automatically be ran against other players to determine your ranking. You can also request scrimmages with other teams, and see the replays.  
  
