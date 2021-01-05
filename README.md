# battlecode2021

BattleCode 2020 - Overview  
  
  
  
https://2020.battlecode.org/getting-started  
  
   
This is the Battlecode 2020 contest website, which will be your main hub for all Battlecode-related things for the duration of the contest. For a general overview of what Battlecode is, visit our landing page.  
This year's game is a thrilling survival adventure involving 🍲, ▀⛓, 🐮, 🤖, and more. You will write bots in Java.  
Battlecode 2020 is released! Read the game specifications. Check out this example replay for a demo of the game!  
Account and Team Creation  
To participate in Battlecode, you need an account and a team. Each team can consist of 1 to 4 people.  
Create an account on this website, and then go to the team section to either create or join a team.  

## Installation  
If you experience problems with the instructions below, check common issues, and if that doesn't help, ask on the Discord.  
STEP 1: INSTALL JAVA  
You'll need a Java Development Kit (JDK) version 8. Unfortunately, higher versions will not work. Download it here. You may need to create an Oracle account.  
I downloaded   
jdk-8u271-linux-aarch64  
   
## Installation Instructions for Java JDK  
https://docs.datastax.com/en/jdk-install/doc/jdk-install/installOpenJdkDeb.html  
   
http://openjdk.java.net/install/  
   
   
If you're unsure how to install the JDK, you can find instructions for all operating systems here (pay attention to PATH and CLASSPATH).  
   
   
Linux  
Click the appropriate link:  
"JDK Installation for Linux Platforms"  
"JRE Installation for Linux Platforms"  
"Server JRE 8 Installation for Linux Platforms"  
"Manual Installation and Registration of Java Plugin for Linux"  
To run Java applets in a browser, you must install the JRE plugin manually. This does not apply to the server JRE.  
JRE for Linux system requirements and gives installation instructions for several JRE-Linux combinations.  
This page contains these topics:  
"System Requirements"  
"JRE 8 Installation Instructions"  
"General Installation Notes"  
See "JDK 8 and JRE 8 Installation Start Here" for general information about installing JDK 8 and JRE 8.  
Linux - To find out if the path is properly set  
To find out if the path is properly set:  
In a terminal windows, enter:  
% java -version  
connorstom@penguin:~$ java -version  
openjdk version "1.8.0_232"  
OpenJDK Runtime Environment (build 1.8.0_232-8u232-b09-1~deb9u1-b09)  
OpenJDK 64-Bit Server VM (build 25.232-b09, mixed mode)  
   
   
  
This will print the version of the java tool, if it can find it. If the version is old or you get the error java: Command not found, then the path is not properly set.  
Determine which java executable is the first one found in your PATH  
In a terminal window, enter:  
% which java  
Set the PATH permanently  
To set the path permanently, set the path in your startup file.  
Note: Instructions for two most popular Shells on Linux and Solaris are listed. If you are using other shells, see the Path Setting Tutorial.  
Bash Shell  
Edit the startup file (~/.bashrc)  
Modify PATH variable  
PATH=/usr/local/jdk1.8.0/bin:$PATH  
export PATH  
Save and close the file  
Load the startup file  
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
 
 
STEP 2: DOWNLOAD BATTLECODE
Next, you should download the Battlecode 2020 scaffold. To get up and running quickly, you can click "Clone or download" and then "Download ZIP," and move on to the next step.
We recommend, however, that you instead use Git to organize your code. If you haven't used Git before, read this guide (or wait for our lecture covering it). On the scaffold page, click "Use this template." Importantly, on the next page, make your new repo private (you don't want other teams to steal your code!). You can then clone your newly created repo and invite your team members to collaborate on it.
Error - Terminal won’t load from within Intellij and Gradle won’t build
git clone https://github.com/battlecode/battlecode20-scaffold.git
Message when trying to open Terminal within Intellij
Platform SDK does not point to valid JDK
STEP 3: LOCAL SETUP
We recommend using an IDE like IntelliJ IDEA or Eclipse to work on Battlecode, but you can also use your favorite text editor combined with a terminal. Battlecode 2020 uses Gradle to run tasks like run, debug and jarForUpload (but don't worry about that — you don't need to install it).
View instructions for:
IntelliJ IDEAEclipseTerminal
Install IntelliJ IDEA Community Edition from here.
In the Welcome to IntelliJ IDEA window that pops up when you start IntelliJ, select Import Project
In the Select File or Dictionary to Import window, select the build.gradle file in the scaffold folder.
Hit OK.
We need to set the jdk properly; open the settings with File > Settings (IntelliJ IDEA > Preferences on Mac) or ctrl+alt+s. Navigate to Build, Execution, Deployment > Build Tools > Gradle and change Gradle JVM to 1.8
Time for a first build! On the right side of the screen, click the small button that says gradle and has a picture of an elephant. Navigate to battlecode20-scaffold > Tasks > battlecode and double click on build. This will install the client and engine for you.
If you haven't seen any errors, you should be good to go.
There should now be a folder called client in your scaffold folder; if you go in there, and double click the Battlecode Client application, you should be able to run and watch matches. (Please don't move that application, it will be sad.) If you're on Linux, navigate to the client folder and run ./battlecode-visualizer to launch the client.
Run a Match
Player code is in the src directory of the scaffold: each package inside src corresponds to one distinct player. We have provided examplefuncsplayer, and you can create your own player by either modifying it or copying and renaming it.
You should have a client application in the client folder. Launch it, and go to the Runner section. There, you can specify which players to run against each other, and on which map, and you can view the match as it is running.
You can also run a match without the client, by invoking the Gradle task run. For example, gradle run -PteamA=examplefuncsplayer -PteamB=examplefuncsplayer -Pmaps=FourLakeLand runs examplefuncsplayer against itself on the FourLakeLand map. This produces a replay file in the matches directory of the scaffold, which you can upload to the client to view.
Upload Your Bot and Scrimmage
Create a zip file containing only your robot code (only 1 package), and uploaded it to the submissions page.
Your bot will automatically be ran against other players to determine your ranking. You can also request scrimmages with other teams, and see the replays.
Setup your computer

Installation of the 64-bit JDK on Linux Platforms
This procedure installs the Java Development Kit (JDK) for 64-bit Linux, using an archive binary file (.tar.gz).
These instructions use the following file:
jdk-8uversion-linux-x64.tar.gz

Download the file.
Before the file can be downloaded, you must accept the license agreement. The archive binary can be installed by anyone (not only root users), in any location that you can write to. However, only the root user can install the JDK into the system location.
Change directory to the location where you would like the JDK to be installed, then move the .tar.gz archive binary to the current directory.
Unpack the tarball and install the JDK.
% tar zxvf jdk-8uversion-linux-x64.tar.gz

The Java Development Kit files are installed in a directory called jdk1.8.0_version in the current directory.
Delete the .tar.gz file if you want to save disk space.
 
Idea Installation Instructions
Unpack the idea idea-2019.3.1.tar.gz file to an empty directory using the following command: 
tar -xzf idea-2019.3.1.tar.gz
Note: A new instance MUST NOT be extracted over an existing one. The target folder must be empty.


Run idea.sh from the bin subdirectory.
