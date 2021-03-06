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
  - [Excellent seven minute video by Max Mann of how to get everything installed](#excellent-seven-minute-video-by-max-mann-of-how-to-get-everything-installed)
- [Setup your computer, we will cover each item](#setup-your-computer-we-will-cover-each-item)
  - [Enable Linux on your Chromebook](#enable-linux-on-your-chromebook)
  - [Details about your computer and operating system](#details-about-your-computer-and-operating-system)
    - [Chromebook is Debian](#chromebook-is-debian)
    - [Digitalocean is Ubuntu](#digitalocean-is-ubuntu)
  - [Handy aliases and abbreviations into .bashrc and .bash_aliases](#handy-aliases-and-abbreviations-into-bashrc-and-bash_aliases)
  - [Installing Git so you can work with GitHub](#installing-git-so-you-can-work-with-github)
    - [Configuring GitHub git config user.name user.email](#configuring-github-git-config-username-useremail)
  - [VS Code install for Debian and Ubuntu based distributions](#vs-code-install-for-debian-and-ubuntu-based-distributions)
    - [Installing Visual Studio Code on Ubuntu](#installing-visual-studio-code-on-ubuntu)
    - [Starting Visual Studio Code](#starting-visual-studio-code)
    - [Connect with vscode in the cloud so your settings persist over devices and sessions](#connect-with-vscode-in-the-cloud-so-your-settings-persist-over-devices-and-sessions)
    - [Setup a password for cloud sync - you will be prompted each time you start vscode](#setup-a-password-for-cloud-sync---you-will-be-prompted-each-time-you-start-vscode)
    - [If you previously have a cloud account you can merge your data](#if-you-previously-have-a-cloud-account-you-can-merge-your-data)
    - [Updating Visual Studio Code - every month need to do this](#updating-visual-studio-code---every-month-need-to-do-this)
  - [Create .ssh directory and generate SSH public and private keys](#create-ssh-directory-and-generate-ssh-public-and-private-keys)
    - [Create a directory for the public keys](#create-a-directory-for-the-public-keys)
    - [Create SSH Key for Github](#create-ssh-key-for-github)
  - [GitHub - set your ssh key and get your GitHub token for vscode](#github---set-your-ssh-key-and-get-your-github-token-for-vscode)
    - [Get your vscode token from github account settings](#get-your-vscode-token-from-github-account-settings)
    - [Let vscode know about the GitHub token at the bottom left of vscode click bottom-left and paste github token into the command prompt area in the top menu toolbar](#let-vscode-know-about-the-github-token-at-the-bottom-left-of-vscode-click-bottom-left-and-paste-github-token-into-the-command-prompt-area-in-the-top-menu-toolbar)
- [- End general setup of your computer](#--end-general-setup-of-your-computer)
- [- Begin MIT Content](#--begin-mit-content)
- [Install Java Release 8](#install-java-release-8)
  - [Installation Instructions for Java JDK using OpenJava - we won't use this but it is another option](#installation-instructions-for-java-jdk-using-openjava---we-wont-use-this-but-it-is-another-option)
  - [We will use Oracle's version of Java - Download the correct Java Version 8](#we-will-use-oracles-version-of-java---download-the-correct-java-version-8)
  - [Also install the latest version Java 15 so that vscode is happy for it's extensions](#also-install-the-latest-version-java-15-so-that-vscode-is-happy-for-its-extensions)
  - [Changes to .bashrc for your environment variables, PATH and JAVA_HOME](#changes-to-bashrc-for-your-environment-variables-path-and-java_home)
    - [- Set environment variables `PATH` and `JAVA_HOME`](#--set-environment-variables-path-and-java_home)
  - [Validating Java works correctly](#validating-java-works-correctly)
    - [To verify the installation, get the Java version](#to-verify-the-installation-get-the-java-version)
    - ['Which' Java as a validation test](#which-java-as-a-validation-test)
  - [Cleaning up](#cleaning-up)
- [- Begin Battlecode](#--begin-battlecode)
  - [- Clone the Battlecode Scaffold, where you can run your robot](#--clone-the-battlecode-scaffold-where-you-can-run-your-robot)
  - [Download (clone) the Battlecode competition scaffold for BATTLECODE](#download-clone-the-battlecode-competition-scaffold-for-battlecode)
  - [Create our own PRIVATE empty repo on GitHub](#create-our-own-private-empty-repo-on-github)
- [- Setup editor such as vscode, IntelliJ, Eclipse etc](#--setup-editor-such-as-vscode-intellij-eclipse-etc)
  - [Download IntelliJ IDEA](#download-intellij-idea)
  - [Idea Installation Instructions](#idea-installation-instructions)
  - [Changes to .bashrc for your PATH variable](#changes-to-bashrc-for-your-path-variable)
- [Install IntelliJ - I usually use vscode, turn it off to preserve memory](#install-intellij---i-usually-use-vscode-turn-it-off-to-preserve-memory)
    - [IntelliJ - Error Message: "Please fix JAVA_HOME variable"](#intellij---error-message-please-fix-java_home-variable)
    - [IntelliJ-IDEA Setting the JAVA Variable](#intellij-idea-setting-the-java-variable)
    - [When IntelliJ IDEA first starts it may take 12 minutes for the full build on a Chromebook](#when-intellij-idea-first-starts-it-may-take-12-minutes-for-the-full-build-on-a-chromebook)
    - [IntelliJ-IDEA Spash Screen](#intellij-idea-spash-screen)
    - [IntelliJ-IDEA Home Screen](#intellij-idea-home-screen)
  - [Time for a first build!](#time-for-a-first-build)
    - [IntelliJ Gradle Icon - right-hand side](#intellij-gradle-icon---right-hand-side)
    - [Run the gradle from the command line and view the output in the visualizer](#run-the-gradle-from-the-command-line-and-view-the-output-in-the-visualizer)
  - [Now execute the runner and run the default example robot](#now-execute-the-runner-and-run-the-default-example-robot)
- [Using the terminal - Build the game - `./gradlew update`](#using-the-terminal---build-the-game---gradlew-update)
    - [Build the gradle](#build-the-gradle)
    - [each robot you build lives in it's own src directory](#each-robot-you-build-lives-in-its-own-src-directory)
    - [Using the Client UI](#using-the-client-ui)
    - [Using the command line `gradle run`](#using-the-command-line-gradle-run)
- [Modify the bot and make it your own](#modify-the-bot-and-make-it-your-own)
- [RUNNING GAME FROM THE TERMINAL](#running-game-from-the-terminal)
    - [gradle.properties file is what will be run](#gradleproperties-file-is-what-will-be-run)
- [If you're experiencing memory problems with the client, please try:](#if-youre-experiencing-memory-problems-with-the-client-please-try)
- [Upload the bot to compete against others](#upload-the-bot-to-compete-against-others)
  - [Upload Your Bot and Scrimmage](#upload-your-bot-and-scrimmage)

## Introduction  
This is my scrapbook for the Battlecode 2021 contest, I will attempt to keep it up-to-date for all Battlecode-related things for the duration of the contest. For a general overview of what Battlecode is, visit the [Battlecode landing page](https://2020.battlecode.org).  
This year's game is a thrilling survival adventure involving 🍲, ▀⛓, 🐮, 🤖, and more. You will write bots in Java.  

<br />  
<img width="600px" src="https://github.com/coding-to-music/battlecode2021/blob/main/Assets/Battlecode-inspirational-quotes.png?raw=true" align="center" alt="Battlecode-inspirational-quotes" />
</b>

## Why this document is needed  
In software it is common to write good documentation. This is so that other members of the team can be equally up-to-date with how things work. This is normal documentation for any well-run organization.  
You really don't want to have some production problem and not have written down important details. Everything should be documented that you will need to be successful. Team members who do not document leave behind a technical debt of unfinished work that snowballs up and eventually really disrupts the stability and effectiveness of the organization.  

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

It is assumed you will be developing on a linux environment, this document provides instructions for Chromebook and also there are some references to Digitalocean, that way you can use the cloud for your development environment, giving access to greater stability and unlimted resources. By developing in Digitalocean you can create specific environments and install and remove software without worrying about it messing up your Chromebook or main computer. Generally I have to wipe and rebuild my chromebook linux environment several times per year, all the various changes end up hurting the stablility of the chromebook, so better to use Digitalocean in the cloud as your messy sandbox.

## Excellent seven minute video by Max Mann of how to get everything installed
His main [YouTube page](https://www.youtube.com/user/fghulds)
His [videos](https://www.youtube.com/user/fghulds/videos)
In this [video, his notes for Installation instructions:](https://www.youtube.com/watch?v=G-SxsYLlk44&ab_channel=MaxMann)

Visit oracle.com/java/technologies/javase/javase-jdk8-downloads.html
- Accept cookies
- Select the Windows x64 package, jdk-8u271-windows-x64.exe
- Create an account with Oracle if you don't have one already
-  It can take a half hour to receive the email address confirmation link :(
- Use your Oracle account to download the JDK package.

Download https://github.com/battlecode/battlecode21-scaffold.git   
-Edit environment variable JAVA_HOME to point to the jdk  
-Open command prompt  
- cd Downloads\battlecode21-scaffold-master  
- gradlew.bat  
- gradlew.bat update  
- gradlew.bat build   
- gradlew.bat run   -- runs a match using the settings in gradle.properties  
-Double click on client\Battlecode Client.exe  
- Go to Queue tab  
- Click Upload a .bc21 replay file  
- Watch the match  

# Setup your computer, we will cover each item     
## Enable Linux on your Chromebook     

In your Chromebook settings, enable the Linux (Beta)

## Details about your computer and operating system    
### Chromebook is Debian

```java
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

### Digitalocean is Ubuntu  

```java
// this chart would be different on Ubuntu. Here is a Debain example
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

## Handy aliases and abbreviations into .bashrc and .bash_aliases   

There are some useful aliases in .bash_alias of this repo:
https://github.com/coding-to-music/bash_aliases_docker_alias_cheat_sheet

In this file here [.bash_aliases](https://raw.githubusercontent.com/coding-to-music/bash_aliases_docker_alias_cheat_sheet/master/.bash_aliases)


Edit the file .bash_aliases and put the contents from GitHub
```java
source ~/.bashrc

// in the future, you will just need to type 'sc' and it will source your .bashrc which calls .bash_aliases
```
## Installing Git so you can work with GitHub

Download and install Git
```java
$ sudo apt-get install git
// Now git should be installed. To check use
$ git --version
git version 2.19.1
```

### Configuring GitHub git config user.name user.email 

Once the installation has successfully completed, the next thing to do is to set up the configuration details of the GitHub user. To do this use the following two commands by replacing "user_name" with your GitHub username and replacing "email_id" with your email-id you used to create your GitHub account.
```java
git config --global user.name coding-to-music
git config --global user.email connors.tom@gmail.com
```

The following image shows an example of my configuration with my "user_name" being "akshaypai" and my "email_id" being "abc123@gmail.com"


## VS Code install for Debian and Ubuntu based distributions

[https://code.visualstudio.com/docs/setup/linux](https://code.visualstudio.com/docs/setup/linux)

The easiest way to install Visual Studio Code for Debian/Ubuntu based distributions is to download and install the [.deb package (64-bit)](https://go.microsoft.com/fwlink/?LinkID=760868), either through the graphical software center if it's available, or through the command line with:


```java
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


```java
curl https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > packages.microsoft.gpg
sudo install -o root -g root -m 644 packages.microsoft.gpg /usr/share/keyrings/
sudo sh -c 'echo "deb [arch=amd64 signed-by=/usr/share/keyrings/packages.microsoft.gpg] https://packages.microsoft.com/repos/vscode stable main" > /etc/apt/sources.list.d/vscode.list'
```


Then update the package cache and install the package using:


```java
sudo apt-get install apt-transport-https
sudo apt-get update
sudo apt-get install code # or code-insiders

sudo apt install gnome-keyring
```

### Installing Visual Studio Code on Ubuntu

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


### Starting Visual Studio Code

Now that VS Code is installed on your Ubuntu system you can launch it either from the command line by typing `code` or by clicking on the VS Code icon (`Activities -> Visual Studio Code`).

When you start VS Code for the first time, a window like the following should appear:

<img width="800px" src="https://github.com/coding-to-music/battlecode2021/blob/main/Assets/vscode-default-home-screen.jpg?raw=true" align="center" alt="vscode-default-home-screen.jpg" />
</b>

### Connect with vscode in the cloud so your settings persist over devices and sessions

vscode->settings->Sync Data

There is a very good set of detailed instructions about vscode cloud settings sync [HERE](https://code.visualstudio.com/docs/editor/settings-sync)

### Setup a password for cloud sync - you will be prompted each time you start vscode  
<img width="800px" src="https://github.com/coding-to-music/battlecode2021/blob/main/Assets/choose-password-for-vscode-sync-data.png?raw=true" align="center" alt="choose-password-for-vscode-sync-data.png" />
</b>



### If you previously have a cloud account you can merge your data    
<br />  
<img width="800px" src="https://github.com/coding-to-music/battlecode2021/blob/main/Assets/merge-or-replace-cloud-sync-data.png?raw=true" align="center" alt="merge-or-replace-cloud-sync-data.png" />
</b>
<br />  
  

You can now start installing extensions and configuring VS Code according to your preferences.


### Updating Visual Studio Code - every month need to do this


When a new version is released you can update the Visual Studio Code package through your desktop standard Software Update tool or by running the following commands in your terminal:

```java
sudo apt update
sudo apt upgrade
// or just this
sudo apt update
sudo apt upgrade code
```

## Create .ssh directory and generate SSH public and private keys  

### Create a directory for the public keys

```java
// In root
Mkdir .ssh
Chmod 700 .ssh
Cd .ssh
// Create SSH public and private keys  
// Store them here  

Chmod 600 private_key
```

### Create SSH Key for Github

Now you need to create your SSH key for Github

```java  
ssh-keygen -t rsa -C “connors.tom@gmail.com”  

// It will get saved to 
home/tom/.ssh/id_rsa                // this is the private key, very long paragraph
home/tom/.ssh/id_rsa.pub         // this is the public key,         short paragraph
// Copy that key in that file. I would suggest using Win SCP to download the file similar to FTP
```

file: ssh-rsa 
- 7 lines long private key 
- a short paragraph 
- this is what you will paste into GitHub and Digitalocean
  e1f0vfsMPOANChLOUWbSJTtf4s4P2x6CAYCOQYcd “connors.tom@gmail.com”

-----BEGIN RSA PRIVATE KEY-----
really big long private key
-----END RSA PRIVATE KEY-----

## GitHub - set your ssh key and get your GitHub token for vscode   

Once you copy the key, 
- sign into Github and 
- goto “Settings->SSH and GPG Keys” and 
- add and name of the new key   

<img width="800px" src="https://github.com/coding-to-music/battlecode2021/blob/main/Assets/ssh-keys-in-GitHub.png?raw=true" align="center" alt="Battlecode 2021 Image" />
</b>


### Get your vscode token from github account settings 

</b>
<img width="400px" src="https://github.com/coding-to-music/battlecode2021/blob/main/Assets/vscode-github-token.png?raw=true" align="center" alt="vscode-github-token.png" />
</b>


### Let vscode know about the GitHub token at the bottom left of vscode click bottom-left and paste github token into the command prompt area in the top menu toolbar 

<br />  
<img width="600px" src="https://github.com/coding-to-music/battlecode2021/blob/main/Assets/bottom-left-of-vscode-click-and-paste-github-token.png?raw=true" align="center" alt="bottom-left-of-vscode-click-and-paste-github-token.png" />
</b>
<br />  
  
# - End general setup of your computer
# - Begin MIT Content
# Install Java Release 8  
## Installation Instructions for Java JDK using OpenJava - we won't use this but it is another option  
If you're unsure how to install the JDK, you can find instructions for all operating systems here (pay attention to PATH and CLASSPATH).  
   
https://docs.datastax.com/en/jdk-install/doc/jdk-install/installOpenJdkDeb.html  
   
http://openjdk.java.net/install/  
   
I am using a chromebook, which is Debian flavor of Linux   
There are two related packages  
- JRE - Java Runtime Environment
- JDK - Java Development Kit
  
## We will use Oracle's version of Java - Download the correct Java Version 8  
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
// You will need to log into Oracle and agree to the conditions to start the download  
// ok lets try this one
- Linux x64 Compressed Archive	 
- 136.51 MB	 
- jdk-8u271-linux-x64.tar.gz  
// I downloaded this and left it in my root home directory, it is just a temporary file we will delete it later
jdk-8u271-linux-x64.tar.gz
// you may not need to make this next directory, you may already have it
sudo mkdir /usr/lib/jvm
cd /usr/lib/jvm
// untar the file that is located in your home dir
sudo tar -xzvf ~/jdk-8u271-linux-x64.tar.gz 
```
The Java Development Kit files are installed in a directory called `jdk1.8.0_version` in the current directory.  
```java
// this directory was just created
/usr/lib/jvm/jdk1.8.0_271
```

## Also install the latest version Java 15 so that vscode is happy for it's extensions
https://www.oracle.com/java/technologies/javase-downloads.html

<br />  
<img width="600px" src="https://github.com/coding-to-music/battlecode2021/blob/main/Assets/java15-download.png?raw=true" align="center" alt="java15 download" />
</b>

Clicking Download brings us to this page
https://www.oracle.com/java/technologies/javase-jdk15-downloads.html


```java
// You will need to log into Oracle and agree to the conditions to start the download  
// lets try this one
XXXXXXX - Linux x64 Compressed Archive	 
XXXXXXX - 179.33 MB	 
XXXXXXX - jdk-15.0.1_linux-x64_bin.tar.gz  
// I downloaded this and left it in my root home directory, it is just a temporary file we will delete it later
XXXXXXX   jdk-15.0.1_linux-x64_bin.tar.gz

cd /usr/lib/jvm
// untar the file that is located in your home dir
XXXXXXX sudo tar -xzvf ~/jdk-8u271-linux-x64.tar.gz 
```
The Java Development Kit files are installed in a directory called `jdk1.8.0_version` in the current directory.  
```java
// this directory was just created
XXXXXXX  /usr/lib/jvm/jdk1.8.0_271
```


## Changes to .bashrc for your environment variables, PATH and JAVA_HOME  
### - Set environment variables `PATH` and `JAVA_HOME`   
Paste thise into your Path in your .bashrc 
```java
export JAVA_HOME="/usr/lib/jvm/jdk1.8.0_271"
export PATH=$PATH:/usr/lib/jvm/jdk1.8.0_271/bin:/usr/lib/jvm/jdk1.8.0_271/jre/bin

// then at the command line in root:
$ source ~/.bashrc

// then in the future you just need to source .bashrc by using the alias 'sc'
sc
```
## Validating Java works correctly
### To verify the installation, get the Java version
```java
connorstom@penguin:~$ env | grep JAVA
JAVA_HOME=/usr/lib/jvm/jdk1.8.0_271
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
/usr/lib/jvm/jdk1.8.0_271/bin/java  
```
## Cleaning up 
Delete the .tar.gz file if you want to save disk space.  
      
This may also be useful but I have not tested it yet
```java
% . /.profile  
// Verify that the path is set by repeating the java command  
% java -version  
```   
# - Begin Battlecode 

This next snippet is not needed as far as I know  
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
## - Clone the Battlecode Scaffold, where you can run your robot
## Download (clone) the Battlecode competition scaffold for BATTLECODE  
Next, you should download the Battlecode 2021 scaffold. To get up and running quickly, you can click "Clone or download" and then "Download ZIP," and move on to the next step.  
We recommend, however, that you instead use Git to organize your code. If you haven't used Git before, read this [guide](https://guides.github.com/introduction/git-handbook/) (or wait for our lecture covering it). On the [scaffold page](https://github.com/battlecode/battlecode20-scaffold), click `"Use this template."` Importantly, on the next page, make your new repo private (you don't want other teams to steal your code!). You can then clone your newly created repo and invite your team members to collaborate on it.  
```java
connorstom@penguin:~/aprojects$ git clone https://github.com/battlecode/battlecode21-scaffold.git
Cloning into 'battlecode21-scaffold'...
remote: Enumerating objects: 50, done.
remote: Counting objects: 100% (50/50), done.
remote: Compressing objects: 100% (30/30), done.
remote: Total 50 (delta 17), reused 36 (delta 10), pack-reused 0
Unpacking objects: 100% (50/50), done.
```
    
## Create our own PRIVATE empty repo on GitHub  
Private so other people won't look at it during the competition. We can make it public when the competition is over.  
We will name the repo: my-battlecode-2021-scaffold  
```java  
// first we must delete the .git directory that came from the original GitHub battlecode scaffold
connorstom@penguin:~/aprojects/my-battlecode-2021-scaffold$ rm -rf .git  

// follow the instructions provided on GitHub
git init
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:coding-to-music/my-battlecode-2021-scaffold.git
git push -u origin main
// may need to do this  
git push --set-upstream origin master

Enumerating objects: 21, done.
Counting objects: 100% (21/21), done.
Delta compression using up to 2 threads
Compressing objects: 100% (15/15), done.
Writing objects: 100% (21/21), 22.16 KiB | 2.01 MiB/s, done.
Total 21 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), done.
To github.com:coding-to-music/my-battlecode-2021-scaffold.git
 * [new branch]      master -> master
Branch 'master' set up to track remote branch 'master' from 'origin'.
```

# - Setup editor such as vscode, IntelliJ, Eclipse etc     
  
## Download IntelliJ IDEA
The JetBrains website to [downlowd Intellij IDEA is located Here](https://www.jetbrains.com/idea/download/#section=linux)

Choose windows/mac/linux  
then, below that,  
Choose the Community button   

## Idea Installation Instructions  

Note: A new instance MUST NOT be extracted over an existing one. The target folder must be empty.  

```java
// install into a new directory
cd /usr  
// untar the file that is located in your home dir
sudo tar -xzvf ~/ideaIC-2020.3.1.tar.gz 

// to clean up, remove the original tar file
rm ~/ideaIC-2020.3.1.tar.gz
```

The Java Development Kit files are installed in a directory called `idea-IC-203.6682.168` in the current directory.  
```java
// this directory was just created
/usr/idea-IC-203.6682.168
```
## Changes to .bashrc for your PATH variable  
Paste thise into your Path in your .bashrc 
```java
export PATH=$PATH:/usr/idea-IC-203.6682.168/bin
```

Now run IntelliJ!  
```java
Run idea.sh from the bin subdirectory.  
```

# Install IntelliJ - I usually use vscode, turn it off to preserve memory
Battlecode 2020 uses Gradle to run tasks like `run`, `debug` and `jarForUpload` (but don't worry about that — you don't need to install it).

Install IntelliJ IDEA Community Edition from [here](https://www.jetbrains.com/idea/download/).
In the `Welcome to IntelliJ IDEA window` that pops up when you start IntelliJ, select `Import Project`
In the `Select File or Dictionary to Import` window, select the `build.gradle` file in the scaffold folder.
Hit OK.  

We need to set the jdk properly; open the settings with `File > Settings (IntelliJ IDEA > Preferences on Mac`) or `ctrl+alt+s`. Navigate to `Build, Execution, Deployment > Build Tools > Gradle` and change `Gradle JVM` to 1.8  

### IntelliJ - Error Message: "Please fix JAVA_HOME variable"   
<br />  
<img width="600px" src="https://github.com/coding-to-music/battlecode2021/blob/main/Assets/Please-fix-JAVA_HOME-variable.png?raw=true" align="center" alt="Please-fix-JAVA_HOME-variable" />
</b>

### IntelliJ-IDEA Setting the JAVA Variable  
<br />  
<img width="600px" src="https://github.com/coding-to-music/battlecode2021/blob/main/Assets/IntelliJ-IDEA-setting-JAVA-variable.png?raw=true" align="center" alt="IntelliJ-IDEA-setting-JAVA-variable" />
</b>

### When IntelliJ IDEA first starts it may take 12 minutes for the full build on a Chromebook

<br />  
<img width="800px" src="https://github.com/coding-to-music/battlecode2021/blob/main/Assets/IntelliJ_IDEA_Battlecode_Scaffold_full_screen.png?raw=true" align="center" alt="IntelliJ_IDEA_Battlecode_Scaffold_full_screen.png" />
</b>
<br />  

### IntelliJ-IDEA Spash Screen  
<br />  
<img width="600px" src="https://github.com/coding-to-music/battlecode2021/blob/main/Assets/IntelliJ-IDEA-splash-screen.png?raw=true" align="center" alt="IntelliJ-IDEA-splash-screen" />
</b>

### IntelliJ-IDEA Home Screen  
<br />  
<img width="600px" src="https://github.com/coding-to-music/battlecode2021/blob/main/Assets/IntelliJ-IDEA-home-screen.png?raw=true" align="center" alt="IntelliJ-IDEA-home-screen" />
</b>


## Time for a first build!   
On the right side of the screen, click the small button that says gradle and has a picture of an elephant. Navigate to battlecode20-scaffold > Tasks > battlecode and double click on build. This will install the client and engine for you.
If you haven't seen any errors, you should be good to go.

### IntelliJ Gradle Icon - right-hand side   
<br />  
<img width="100px" src="https://github.com/coding-to-music/battlecode2021/blob/main/Assets/IntelliJ-IDEA-Gradle-icon.png?raw=true" align="center" alt="IntelliJ-IDEA-Gradle-icon" />
</b>


There should now be a folder called `client` in your scaffold folder; if you go in there, and double click the `Battlecode Client` application, you should be able to run and watch matches. (Please don't move that application, it will be sad.) If you're on Linux, navigate to the `client` folder and run `./battlecode-visualizer` to launch the client.

### Run the gradle from the command line and view the output in the visualizer  
```java
./gradlew run
./client/battlecode-visualizer
```

<br />  
<img width="800px" src="https://github.com/coding-to-music/battlecode2021/blob/main/Assets/battlecode-visualizer-initial-spash-screen.png?raw=true" align="center" alt="battlecode-visualizer-initial-spash-screen.png" />
</b>
<br />  

## Now execute the runner and run the default example robot
<br />  
<img width="800px" src="https://github.com/coding-to-music/battlecode2021/blob/main/Assets/battlecode-visualizer-runner-execute.png?raw=true" align="center" alt="battlecode-visualizer-runner-execute.png" />
</b>
<br />  

# Using the terminal - Build the game - `./gradlew update`  
Open a terminal in the scaffold you just downloaded. Run the commands `./gradlew update` and `./gradlew build`  

```java
// Now run "./gradle update"
connorstom@penguin:~/aprojects/battlecode21-scaffold$ ./gradlew update

Welcome to Gradle 6.0.1!

Here are the highlights of this release:
 - Substantial improvements in dependency management, including
   - Publishing Gradle Module Metadata in addition to pom.xml
   - Advanced control of transitive versions
   - Support for optional features and dependencies
   - Rules to tweak published metadata
 - Support for Java 13
 - Faster incremental Java and Groovy compilation
 - New Zinc compiler for Scala
 - VS2019 support
 - Support for Gradle Enterprise plugin 3.0

For more details see https://docs.gradle.org/6.0.1/release-notes.html

Starting a Gradle Daemon (subsequent builds will be faster)

> Task :update
Updated to 2021.2.3.0

BUILD SUCCESSFUL in 23s
1 actionable task: 1 executed
```

<br />  
<img width="600px" src="https://github.com/coding-to-music/battlecode2021/blob/main/Assets/gradlew_update_which_java_JAVA_HOME.png?raw=true" align="center" alt="gradlew_update_which_java_JAVA_HOME" />
</b>

### Build the gradle  
```java
connorstom@penguin:~/aprojects/battlecode21-scaffold$ ./gradlew build

> Task :compileScala
Scala Compiler interface compilation took 38.592 secs

> Task :compileTestScala
Scala Compiler interface compilation took 38.471 secs

Deprecated Gradle features were used in this build, making it incompatible with Gradle 7.0.
Use '--warning-mode all' to show the individual deprecation warnings.
See https://docs.gradle.org/6.0.1/userguide/command_line_interface.html#sec:command_line_warnings

BUILD SUCCESSFUL in 3m 16s
8 actionable tasks: 8 executed
```

<br />  
<img width="600px" src="https://github.com/coding-to-music/battlecode2021/blob/main/Assets/gradlew-build.png?raw=true" align="center" alt="gradlew_update_which_java_JAVA_HOME" />
</b>

### each robot you build lives in it's own src directory

Run a Match
Player code is in the `src` directory of the scaffold: each package inside `src` corresponds to one distinct player. We have provided `examplefuncsplayer`, and you can create your own player by either modifying it or copying and renaming it. The only restriction is that each player must have a file named `RobotPlayer.java` which implements a `run(RobotController rc)` method.

### Using the Client UI  
You should have a client application in the `client` folder. Launch it, and go to the `Runner` section. There, you can specify which players to run against each other, and on which map, and you can view the match as it is running.

### Using the command line `gradle run`
You can also run a match without the client, by invoking the Gradle task `run`. For example, `gradle run -PteamA=examplefuncsplayer -PteamB=examplefuncsplayer -Pmaps=FourLakeLand` runs `examplefuncsplayer` against itself on the `FourLakeLand` map. This produces a replay file in the `matches` directory of the scaffold, which you can upload to the client to view.

```java

// run the game as defined in the gradle.properties - but to the console, it is huge
connorstom@penguin:~/aprojects/battlecode21-scaffold$ ./gradlew run 

// this went on forever I needed to kill it with ctrl-C ^C
[A:SLANDERER#11514@68] I am trying to move NORTH; false 9.072361313166404 false
[A:POLITICIAN#10475@68] I'm a POLITICIAN! Location [10007, 23925]
[A:POLITICIAN#10475@68] I am trying to move NORTHEAST; false 1.6308742204463966 false
[B:POLITICIAN#11218@68] I'm a POLITICIAN! Location [10027, 23928]
[B:POLITICIAN#11218@68] I am trying to move SOUTHEAST; false 2.282011952169438 false
[A:MUCKRAKER#13908@68] I'm a MUCKRAKER! Location [10005, 23927]
[A:MUCKRAKER#13908@68] I am trying to move EAST; true 0.0 true
[A:MUCKRAKER#13908@68] I moved!
[B:SLANDERER#10110@68] I'm a SLANDERER! Location [10025, 23927]
[B:SLANDERER#10110@68] I am trying to move NORTHEAST; false 2.5545705508935868 false
[B:SLANDERER#13348@68] I'm a SLANDERER and I just got created!
[B:SLANDERER#13348@68] I'm a SLANDERER! Location [10026, 23927]

// run the game as defined in the gradle.properties - but output it to a junk.txt file - add that to the .gitignore
// Or send the output to >> /dev/null
connorstom@penguin:~/aprojects/battlecode21-scaffold$ ./gradlew run >> /dev/null

// find out how many lines of output are in the console output
connorstom@penguin:~/aprojects/battlecode21-scaffold$ wc -l junk.txt
309508 junk.txt

// there are 310,000 lines in the output of doing a run
// it took about 30 or 60 seconds to run the game itself

```


# Modify the bot and make it your own  
Place each version of your robot in a new subfolder in the `src` folder. Make sure every version has a `RobotPlayer.java`    
# RUNNING GAME FROM THE TERMINAL  
Open a terminal in the scaffold. Run the commands 
```java
// general how-to  
./gradlew run -Pmaps=[map] -PteamA=[Team A] -PteamB=[Team B]

// run this to run your robot  
./gradlew run >> /dev/null

// run this to run your robot  
./gradlew run > junk.txt

// Then view the results of the run  
tail junk.txt

```  

### gradle.properties file is what will be run
```java
// gradle.properties
// modify this file to change project properties
teamA=examplefuncsplayer
teamB=MyFirstRobot
maps=maptestsmall
source=src
gpr.user=battlecodedownloadpackage
profilerEnabled=false
```
# If you're experiencing memory problems with the client, please try:
Client Tips  

Making fewer logs and/or disabling log processsing in the client (toggled with "L").
Making .bc21 files with the engine directly and uploading them to the client's match queue, rather than using the client's runner. With this method, you can just use the web version at 2021.battlecode.org/visualizer.html rather than the desktop application.  

# Upload the bot to compete against others  
## Upload Your Bot and Scrimmage  
Create a zip file containing only your robot code (only 1 package), and uploaded it to the submissions page.  
Your bot will automatically be ran against other players to determine your ranking. You can also request scrimmages with other teams, and see the replays.  

