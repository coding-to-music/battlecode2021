# BattleCode 2021 - Overview  

<img width="800px" src="https://github.com/coding-to-music/battlecode2021/blob/master/assets/2021_battlecode.png?raw=true" align="center" alt="Battlecode 2021 Image" />
</b>



- [BattleCode 2021 - Overview](#battlecode-2021---overview)
- [Introduction](#introduction)
  - [Account and Team Creation](#account-and-team-creation)
  - [Links and resources for this year's Battlecode](#links-and-resources-for-this-years-battlecode)
- [Getting Set Up](#getting-set-up)
  - [Setup your computer, we will cover each item](#setup-your-computer-we-will-cover-each-item)
    - [Java version 8](#java-version-8)
    - [Set environment variables `PATH` and `CLASSPATH`](#set-environment-variables-path-and-classpath)
    - [Setup editor such as vscode, IntelliJ, Eclipse etc](#setup-editor-such-as-vscode-intellij-eclipse-etc)
    - [The Battlecode Scaffold, where you can run your robot](#the-battlecode-scaffold-where-you-can-run-your-robot)
    - [Run the sample robot](#run-the-sample-robot)
    - [Create and modify your own robot](#create-and-modify-your-own-robot)
    - [Run your robot](#run-your-robot)
- [Install Java Release 8](#install-java-release-8)
  - [Installation Instructions for Java JDK](#installation-instructions-for-java-jdk)
  - [Download the correct Java Version 8](#download-the-correct-java-version-8)
  - [Bash Shell](#bash-shell)
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
  

# Introduction  
This is the Battlecode 2021 contest website, which will be your main hub for all Battlecode-related things for the duration of the contest. For a general overview of what Battlecode is, visit our landing page.  
This year's game is a thrilling survival adventure involving 🍲, ▀⛓, 🐮, 🤖, and more. You will write bots in Java.  

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

# Getting Set Up  
## Setup your computer, we will cover each item  
### Java version 8
### Set environment variables `PATH` and `CLASSPATH`
### Setup editor such as vscode, IntelliJ, Eclipse etc
### The Battlecode Scaffold, where you can run your robot
### Run the sample robot
### Create and modify your own robot
### Run your robot  
  

# Install Java Release 8  
## Installation Instructions for Java JDK  

If you're unsure how to install the JDK, you can find instructions for all operating systems here (pay attention to PATH and CLASSPATH).  
   
https://docs.datastax.com/en/jdk-install/doc/jdk-install/installOpenJdkDeb.html  
   
http://openjdk.java.net/install/  
   
I am using a chromebook, which is Debian flavor of Linux   

There are two related packages  
- JRE - Java Runtime Environment
- JDK - Java Development Kit

```java
$ sudo apt-get install openjre-8-jre

$ sudo apt-get install openjdk-8-jdk
```

Installation of the 64-bit JDK on Linux Platforms  
This procedure installs the Java Development Kit (JDK) for 64-bit Linux, using an archive binary file (.tar.gz).  
These instructions use the following file:  
  
```java  
jdk-8u<version>-linux-x64.tar.gz  
```  
  
## Download the correct Java Version 8  
Before the file can be downloaded, you must accept the license agreement. The archive binary can be installed by anyone (not only root users), in any location that you can write to. However, only the root user can install the JDK into the system location.
Change directory to the location where you would like the JDK to be installed, then move the .tar.gz archive binary to the current directory.  

Obtain the file [here - be sure to get Java version 8 of the JDK](https://www.oracle.com/java/technologies/javase-downloads.html)

That leads to this page [here](https://www.oracle.com/java/technologies/javase/javase-jdk8-downloads.html)

Debian on Chromebook would want this file:  
- File Type: Linux ARM 64 Compressed Archive	
- Size: 71.26 MB	
- File Name: jdk-8u271-linux-aarch64.tar.gz

```java
// I downloaded   
jdk-8u271-linux-aarch64  
```


Unpack the tarball and install the JDK.  
```java
% tar zxvf jdk-8u<version>-linux-x64.tar.gz  

// for my specific file:
% tar zxvf jdk-8u271-linux-aarch64.tar.gz    
```
    
The Java Development Kit files are installed in a directory called `jdk1.8.0_version` in the current directory.  
Delete the .tar.gz file if you want to save disk space.  
      
To find out if the environment variables are properly set:  

In a terminal windows, enter:  
```java 
% java -version  
connorstom@penguin:~$ java -version  
openjdk version "1.8.0_232"  
OpenJDK Runtime Environment (build 1.8.0_232-8u232-b09-1~deb9u1-b09)  
OpenJDK 64-Bit Server VM (build 25.232-b09, mixed mode)  
```   
   
This will print the version of the java tool, if it can find it. If the version is old or you get the error java: Command not found, then the path is not properly set.  
Determine which java executable is the first one found in your PATH  
In a terminal window, enter:  
```java
% which java  
```

Set the PATH permanently  
To set the path permanently, set the path in your startup file.  
Note: Instructions for two most popular Shells on Linux and Solaris are listed. If you are using other shells, see the Path Setting Tutorial.  

## Bash Shell  
```java
// Edit the startup file (~/.bashrc)  
// Modify PATH variable  
PATH=/usr/local/jdk1.8.0/bin:$PATH  
export PATH  
// Save and close the file  
// Load the startup file  
```

```java
% . /.profile  
// Verify that the path is set by repeating the java command  
% java -version  
// Modify build.gradle to view the Java version  
task version {  
    group 'battlecode'  
    doLast{  
        println("\nJDK version: ${System.properties['java.home']}")  
        println("\nVersion: " + versions.battlecode + "\n")  
    }  
}  
```   
 
 
# Install the Scaffold  
## STEP 2: DOWNLOAD the competition scaffold for BATTLECODE  
Next, you should download the Battlecode 2020 scaffold. To get up and running quickly, you can click "Clone or download" and then "Download ZIP," and move on to the next step.  
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
  
