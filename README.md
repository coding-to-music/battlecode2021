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
- [Setup your computer, we will cover each item](#setup-your-computer-we-will-cover-each-item)
  - [- Enable Linux on your Chromebook](#--enable-linux-on-your-chromebook)
  - [- details about your computer and operating system](#--details-about-your-computer-and-operating-system)
    - [Chromebook is Debian](#chromebook-is-debian)
    - [Digitalocean is Ubuntu](#digitalocean-is-ubuntu)
  - [- handy aliases and abbreviations into .bashrc and .bash_aliases](#--handy-aliases-and-abbreviations-into-bashrc-and-bash_aliases)
  - [Installing Git so you can work with GitHub](#installing-git-so-you-can-work-with-github)
  - [Configuring GitHub git config user.name user.email](#configuring-github-git-config-username-useremail)
  - [- create .ssh directory and generate SSH public and private keys](#--create-ssh-directory-and-generate-ssh-public-and-private-keys)
    - [Create a directory for the public keys](#create-a-directory-for-the-public-keys)
    - [Create SSH Key for Github](#create-ssh-key-for-github)
  - [- GitHub - set your ssh keys](#--github---set-your-ssh-keys)
    - [Get your vscode token from github account settings](#get-your-vscode-token-from-github-account-settings)
    - [Let vscode know about the GitHub token at the bottom left of vscode click and paste github token](#let-vscode-know-about-the-github-token-at-the-bottom-left-of-vscode-click-and-paste-github-token)
    - [VS Code install for Debian and Ubuntu based distributions](#vs-code-install-for-debian-and-ubuntu-based-distributions)
  - [**Installing Visual Studio Code on Ubuntu**](#installing-visual-studio-code-on-ubuntu)
  - [Starting Visual Studio Code](#starting-visual-studio-code)
    - [Connect with vscode in the cloud so your settings persist over devices and sessions](#connect-with-vscode-in-the-cloud-so-your-settings-persist-over-devices-and-sessions)
    - [setup a password you will be prompted for each time you start vscode](#setup-a-password-you-will-be-prompted-for-each-time-you-start-vscode)
    - [If you previously have a cloud account you can merge your data](#if-you-previously-have-a-cloud-account-you-can-merge-your-data)
  - [**Updating Visual Studio Code**](#updating-visual-studio-code)
- [- End general setup of your computer](#--end-general-setup-of-your-computer)
- [- Begin MIT Content](#--begin-mit-content)
    - [- Java version 8](#--java-version-8)
- [Install Java Release 8](#install-java-release-8)
  - [Installation Instructions for Java JDK](#installation-instructions-for-java-jdk)
  - [Download the correct Java Version 8](#download-the-correct-java-version-8)
    - [- Set environment variables `PATH` and `CLASSPATH` `JAVA_HOME` etc](#--set-environment-variables-path-and-classpath-java_home-etc)
- [- Begin Battlecode](#--begin-battlecode)
    - [- Clone the Battlecode Scaffold, where you can run your robot](#--clone-the-battlecode-scaffold-where-you-can-run-your-robot)
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
- [- Setup editor such as vscode, IntelliJ, Eclipse etc (empty)](#--setup-editor-such-as-vscode-intellij-eclipse-etc-empty)
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


# Setup your computer, we will cover each item     
## - Enable Linux on your Chromebook     

In your Chromebook settings, enable the Linux (Beta)

## - details about your computer and operating system    
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

## - handy aliases and abbreviations into .bashrc and .bash_aliases   

There are some useful aliases in .bash_alias of this repo:
https://github.com/coding-to-music/bash_aliases_docker_alias_cheat_sheet

In this file here [.bash_aliases](https://raw.githubusercontent.com/coding-to-music/bash_aliases_docker_alias_cheat_sheet/master/.bash_aliases)


Edit the file .bash_aliases and put the contents from GitHub
```
source ~/.bashrc

// in the future, you will just need to type 'sc' and it will source your .bashrc which calls .bash_aliases
```

## Installing Git so you can work with GitHub

Download and install Git
```
$ sudo apt-get install git
// Now git should be installed. To check use
$ git --version
git version 2.19.1
```

## Configuring GitHub git config user.name user.email 

Once the installation has successfully completed, the next thing to do is to set up the configuration details of the GitHub user. To do this use the following two commands by replacing "user_name" with your GitHub username and replacing "email_id" with your email-id you used to create your GitHub account.
```
git config --global user.name coding-to-music
git config --global user.email connors.tom@gmail.com
```

The following image shows an example of my configuration with my "user_name" being "akshaypai" and my "email_id" being "abc123@gmail.com"

## - create .ssh directory and generate SSH public and private keys  

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

## - GitHub - set your ssh keys   

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


### Let vscode know about the GitHub token at the bottom left of vscode click and paste github token  

<br />  
<img width="600px" src="https://github.com/coding-to-music/battlecode2021/blob/main/Assets/bottom-left-of-vscode-click-and-paste-github-token.png?raw=true" align="center" alt="bottom-left-of-vscode-click-and-paste-github-token.png" />
</b>
<br />  
  
### VS Code install for Debian and Ubuntu based distributions

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


## Starting Visual Studio Code

Now that VS Code is installed on your Ubuntu system you can launch it either from the command line by typing `code` or by clicking on the VS Code icon (`Activities -> Visual Studio Code`).

When you start VS Code for the first time, a window like the following should appear:

<img width="800px" src="https://github.com/coding-to-music/battlecode2021/blob/main/Assets/vscode-default-home-screen.jpg?raw=true" align="center" alt="vscode-default-home-screen.jpg" />
</b>

### Connect with vscode in the cloud so your settings persist over devices and sessions

vscode->settings->Sync Data

### setup a password you will be prompted for each time you start vscode  
<img width="800px" src="https://github.com/coding-to-music/battlecode2021/blob/main/Assets/choose-password-for-vscode-sync-data.png?raw=true" align="center" alt="choose-password-for-vscode-sync-data.png" />
</b>



### If you previously have a cloud account you can merge your data    
<br />  
<img width="800px" src="https://github.com/coding-to-music/battlecode2021/blob/main/Assets/merge-or-replace-cloud-sync-data.png?raw=true" align="center" alt="merge-or-replace-cloud-sync-data.png" />
</b>
<br />  
  

You can now start installing extensions and configuring VS Code according to your preferences.


## **Updating Visual Studio Code**


When a new version is released you can update the Visual Studio Code package through your desktop standard Software Update tool or by running the following commands in your terminal:

```bash
sudo apt update
sudo apt upgrade
```

# - End general setup of your computer
# - Begin MIT Content
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
# - Begin Battlecode 
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
  

# - Setup editor such as vscode, IntelliJ, Eclipse etc (empty)    
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
  
