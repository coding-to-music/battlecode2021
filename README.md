# BattleCode 2021 - Overview  

<img width="800px" src="https://github.com/coding-to-music/battlecode2021/blob/main/Assets/2021_Battlecode.png?raw=true" align="center" alt="Battlecode 2021 Image" />
</b>
-  

</b>

- [BattleCode 2021 - Overview](#battlecode-2021---overview)
  - [Introduction](#introduction)
  - [Account and Team Creation](#account-and-team-creation)
  - [Links and resources for this year's Battlecode](#links-and-resources-for-this-years-battlecode)
- [Setup your computer, we will cover each item](#setup-your-computer-we-will-cover-each-item)
  - [- Java version 8](#--java-version-8)
  - [- Set environment variables `PATH` and `CLASSPATH`](#--set-environment-variables-path-and-classpath)
  - [- Setup editor such as vscode, IntelliJ, Eclipse etc](#--setup-editor-such-as-vscode-intellij-eclipse-etc)
  - [- The Battlecode Scaffold, where you can run your robot](#--the-battlecode-scaffold-where-you-can-run-your-robot)
  - [- Run the sample robot](#--run-the-sample-robot)
  - [- Create and modify your own robot](#--create-and-modify-your-own-robot)
  - [- Run your robot](#--run-your-robot)
- [Install Java Release 8](#install-java-release-8)
  - [Installation Instructions for Java JDK](#installation-instructions-for-java-jdk)
  - [Download the correct Java Version 8](#download-the-correct-java-version-8)
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
## - Java version 8
## - Set environment variables `PATH` and `CLASSPATH`
## - Setup editor such as vscode, IntelliJ, Eclipse etc
## - The Battlecode Scaffold, where you can run your robot
## - Run the sample robot
## - Create and modify your own robot
## - Run your robot  
  

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
  
