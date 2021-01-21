# Pathing and Navigation Strategy

- [Pathing and Navigation Strategy](#pathing-and-navigation-strategy)
- [Introduction to pathing and navigation](#introduction-to-pathing-and-navigation)
  - [How to use our 24 bits of flag width to communicate with between the robots and enlightenment centers](#how-to-use-our-24-bits-of-flag-width-to-communicate-with-between-the-robots-and-enlightenment-centers)
    - [packing bits](#packing-bits)
    - [coordinates above 10,000](#coordinates-above-10000)
    - [Coordinates using modululos 128](#coordinates-using-modululos-128)
    - [128 by 128 square](#128-by-128-square)
- [The Game, explained](#the-game-explained)
  - [Background](#background)
  - [Environment](#environment)
  - [Overview: Map](#overview-map)
  - [Overview: Influence](#overview-influence)
  - [Overview: Votes](#overview-votes)
  - [The characters: Robots](#the-characters-robots)
  - [Note: radius squared](#note-radius-squared)
  - [Movement](#movement)
  - [Sensing, detecting and vision](#sensing-detecting-and-vision)
    - [EC Enlightenment Centers](#ec-enlightenment-centers)
    - [Politicians](#politicians)
    - [Slanderers](#slanderers)
    - [Muckrakers](#muckrakers)
  - [1500 Rounds, you take turns, can have multiple robots making changes each round](#1500-rounds-you-take-turns-can-have-multiple-robots-making-changes-each-round)
  - [How scoring is counted to determine the winner](#how-scoring-is-counted-to-determine-the-winner)
  - [Rushing](#rushing)
  - [Buffs](#buffs)
  - [Cooldown Periods](#cooldown-periods)
  - [Communications between the Robots](#communications-between-the-robots)
- [Inportant useful functions available to us](#inportant-useful-functions-available-to-us)
- [Various Stratigies Reviewed and Defined](#various-stratigies-reviewed-and-defined)
  - [Basic Bug Strategy](#basic-bug-strategy)
  - [Bug 1](#bug-1)
  - [Bug 2](#bug-2)
- [Using enlightenment centers to coordinate locations and using flags to communicate](#using-enlightenment-centers-to-coordinate-locations-and-using-flags-to-communicate)
  - [More pathing and navigation](#more-pathing-and-navigation)
    - [Breadth-first-search](#breadth-first-search)
    - [MapLocation Java code](#maplocation-java-code)
    - [An example of an how to break up an expensive operation so it will continue over multiple rounds](#an-example-of-an-how-to-break-up-an-expensive-operation-so-it-will-continue-over-multiple-rounds)

# Introduction to pathing and navigation  
 
From lecture #2
[Twitch video](https://www.twitch.tv/videos/866439939)

## How to use our 24 bits of flag width to communicate with between the robots and enlightenment centers  
- Our actual coordinates, our grid, is 64 x 64  
- Map coordinates are from 10,000 to 30,000 - they are offset from zero
- Number of rounds: 3000  
- 32,768 = 2 to the 15th power  
- Which would require 30 bits  
- We only have 24 bits each turn  
- So we can send the X coordinate on the odd rounds  
- Send the Y coordinate on the even rounds  
- We will have 9 other bits to pack extra info each round  
- 24 bits each round, 15 for the X or Y coordinate  
- 9 remaining for extra info  
- We do know our grid is at most 64 in any one direction  
- It may be a rectangle, but the longest side is at most 64
- So we can do the modulus of the given coordinate, 20,000 etc, divide by 64  
- The actual cordinate we will use is the modulus, represented by a percent symbol  
- 20,000 % 64 results in some number between 0 and 63  
- For both X and Y   

<br />  
<img width="600px" src="https://github.com/coding-to-music/battlecode2021/blob/main/Assets/grid-modulus-64-max-size.png?raw=true" align="center" alt="grid-modulus-64-max-size" />
</b>
[Twitch video time 49:18](https://www.twitch.tv/videos/866439939)

- 
### packing bits   
<br />  
<img width="600px" src="https://github.com/coding-to-music/battlecode2021/blob/main/Assets/packing-bits.png?raw=true" align="center" alt="packing-bits" />
</b>

### coordinates above 10,000
<br />  
<img width="600px" src="https://github.com/coding-to-music/battlecode2021/blob/main/Assets/coordinates-above-10000.png?raw=true" align="center" alt="coordinates-above-10000" />
</b>

### Coordinates using modululos 128  
<br />  
<img width="600px" src="https://github.com/coding-to-music/battlecode2021/blob/main/Assets/coordinates-using-128.png?raw=true" align="center" alt="coordinates-using-128" />
</b>

### 128 by 128 square
<br />  
<img width="600px" src="https://github.com/coding-to-music/battlecode2021/blob/main/Assets/128-by-128-square.png?raw=true" align="center" alt="128-by-128-square" />
</b>

# The Game, explained  
## Background  
In the aftermath of the robots' [deadly escape to Mars](https://s3.amazonaws.com/battlecode-2018/specs/battlecode-specs-2018.html) and their survival of the treacherous landscape of [rising Martian ocean levels](https://github.com/battlecode/battlecode20/blob/master/specs/specs.md), the remnants of Martian civilization have gathered yet again to assert their dominance on the planet. Amidst the chaos, the robots grew to form two opposing factions: the Research Engineering Division (Red) and the Branched Logistics Union of Electronicists (Blue). Battlecode: Campaign is set in a tumultuous election in the struggle for longstanding peace.

At the center of the battle for precious votes are impassioned speeches imbued with heartfelt conviction, in the pursuit of a growing army of robotic politicians. However, renowned robot historians have discovered that success often comes with slander and sabotage, and both parties realise that reality is no different on Mars.

The history, and indeed the future, of Mars is being written now. You are to lead your party to victory, but you must beware, for the campaign is especially thick with calumny, and your opponents are working against you. Your objective is to overcome your political obstacles and win the election—at all costs.  

## Environment  
In Battlecode: Campaign, you will write code to control your team of robots, and lead your party to victory.

In each Campaign battle, your robots will face an opponent party of robots on the game map. The game is turn-based, taking place over 1500 rounds: in every round, each robot takes one turn, in order of creation. Each robot receives limited computation time per turn, as described in the Bytecode Limits section.  

## Overview: Map  
The world of Mars is a discrete 2-dimensional rectangular grid, of size ranging between 32×32 and 64×64. The bottom-left corner of the map will have integer coordinates generated uniformly at random between 10,000 and 30,000; in other words, all map coordinates will be offset by this amount. Coordinates increase East (right) and North (up).  

(Map Diagram goes here)

Figure 1: Example map coordinates for a 8×8 map. Each unit occupies one grid cell.
The map defines the Martian terrain: each map square has a certain passability, which is a real number between 0.1 and 1.0, inclusive. Squares with lower passability values are covered in Martian swamp and slow down robot actions; this is described in more detail in the Robots section.

The map also defines the locations of the starting units. At the beginning of a match, each team will own between 1 and 3 Enlightenment Centers. These buildings serve as the foundation of your army, and are where your new politicians will be educated. There may also be up to 6 neutral Enlightenment Centers scattered on the map, which your team may wish to acquire.

In order to prevent maps from favoring one player over another, it is guaranteed that Mars is always symmetric by either a rotation or reflection.  

## Overview: Influence  
The core resource is influence. Wielding influence enables you to amass a larger and more powerful army of robots. Influence is not a global resource: your team's influence is distributed among your Enlightenment Centers, and is generated passively both by the Enlightenment Centers and by specific robot types.

Each robot has a hard limit of 108 influence: any influence in excessive of this will be permanently lost.

## Overview: Votes  
The objective of Battlecode: Campaign is to win the most votes. Each round, one citizen's vote is up for auction. Each Enlightenment Center may bid a non-negative amount of influence to win that vote, and Enlightenment Center which enters the highest bid will win that vote for its team.

The victory conditions and tiebreakers are described in more detail in the Victory section.  
  
## The characters: Robots  
Each robot runs an independent copy of your code. It acts given only its own nearby surroundings through actions, such as movement and special abilities. Robots are assigned unique random IDs no smaller than 10,000.

Each action (movement or active ability) incurs a cooldown penalty, which varies for different robot types; robots can only perform actions when their cooldown is less than 1. Performing an action adds a corresponding cooldown penalty to the robot's total cooldown, given by
base cooldown valuepassability of current map square
Each round, all robots' cooldowns will decrease by 1, regardless of whether they choose to take an action.  

Overview
Units are robots which can move; these will be your team's primary means of combat. Different types of units have different special abilities, and success in the election will depend on how your team uses these abilities to your advantage.

You are able to create units by transferring part of your influence to the new unit. The influence you spend is an integer parameter C, which you may choose for each new unit you create. Newly built politicians and muckrakers will have a cooldown of 10 rounds.

The conviction of a unit describes how loyal it is to your party; by transferring more influence, you will obtain units that have greater conviction and are therefore more loyal.

Buildings are immobile robots; the only type of available building is Enlightenment Centers.


|  |  Enlightenment Center  |  Politician  |  Slanderer  |  Muckraker  |  
|  Class  |  Building  |  Unit  |  Unit  |  Unit  |  
Influence  |  Cannot be created	C (variable)	C (variable)	C (variable)  |  
Minimum influence  |  N/A  |  1  |  	1  |  	1  |  
Initial conviction1  |  = current influence  |  	⌈1.0C⌉  |  	⌈1.0C⌉  |  	⌈0.7C⌉  |  
Initial cooldown  |  0  |  	10  |  	0  |  	10  |  
Base action cooldown  |  2.0  |  	1.0  |  	2.0  |  	1.5  |  
Action radius squared  |  2  |  	9  |  	0  |  	12  |  
Sensor radius squared  |  40  |  	25  |  	20  |  	30  |  
Detection radius squared  |  40  |  	25  |  	20  |  	40  |  
True sense  |  Yes  |  	No  |  	No  |  	Yes  |  
Ability2  |  Bid  |  	Empower  |  	Embezzle, Camouflage  |  	Expose  |  
Bytecode limit  |  20,000  |  15,000  |  7,500  |  15,000  |  
1 The ⌈⋅⌉ denotes the ceiling function, which you may read more about here. 2 an advanced mechanic; see below   

## Note: radius squared
To preserve integer arithmetic, all distances are measured in distance-squared units. For example, a location 3 squares east and 4 squares north is a distance of 32+42=25 squared-units away, and all locations within a distance of 25 squared-units form a circle of radius 5. If you wish, you may obtain the true Euclidean distance by taking the square-root of this value.  

## Movement  
Units may choose to move to unoccupied adjacent tiles. This is legal when all of the following constraints are met.

The unit's cooldown is low enough to perform an action.
The destination tile is adjacent to the current location (the 8 tiles around the unit's current location).
The destination tile is not occupied by another robot.
Moving will then increase the robot's action cooldown.

## Sensing, detecting and vision  
Each map square has a passability value, and each robot has a number of characteristics including its robot type, influence, and current conviction.

All robots may sense the passability of nearby map squares and any robots located on them. Each robot has a specific sensor radius, and is able to sense map properties and robots within that range. However, there is the exception that politicians and slanderers do not have true sense: this means they are unable to distinguish between other politicians and slanderers. To them, all slanderers will appear to be politicians.

Additionally, robots can detect the presence of robots near them, without sensing any properties about those robots other than their location. Muckrakers have a larger detection radius than sensor radius, and so are able to detect robots further away than they can sense.  

### EC Enlightenment Centers
### Politicians  
### Slanderers  
### Muckrakers  
## 1500 Rounds, you take turns, can have multiple robots making changes each round  
## How scoring is counted to determine the winner    
## Rushing  
## Buffs  
## Cooldown Periods  
## Communications between the Robots  
# Inportant useful functions available to us


# Various Stratigies Reviewed and Defined  

## Basic Bug Strategy  
<br />  
<img width="600px" src="https://github.com/coding-to-music/battlecode2021/blob/main/Assets/basicBug.png?raw=true" align="center" alt="basicBug" />
</b>

## Bug 1  


## Bug 2  

# Using enlightenment centers to coordinate locations and using flags to communicate  

<br />  
<img width="600px" src="https://github.com/coding-to-music/battlecode2021/blob/main/Assets/using-24-bits-to-communicate-between-robots-and-centers.png?raw=true" align="center" alt="using-24-bits-to-communicate-between-robots-and-centers" />
</b>

[Twitch video time 44:04](https://www.twitch.tv/videos/866439939)

## More pathing and navigation  

### Breadth-first-search  
<br />  
<img width="600px" src="https://github.com/coding-to-music/battlecode2021/blob/main/Assets/breadth-first-search.png?raw=true" align="center" alt="breadth-first-search" />
</b>

### MapLocation Java code  
<br />  
<img width="600px" src="https://github.com/coding-to-music/battlecode2021/blob/main/Assets/Battlecode-MapLocation.png?raw=true" align="center" alt="Battlecode-MapLocation" />
</b>

### An example of an how to break up an expensive operation so it will continue over multiple rounds  
<br />  
<img width="600px" src="https://github.com/coding-to-music/battlecode2021/blob/main/Assets/Battlecode expensive loop.png?raw=true" align="center" alt="Battlecode expensive loop" />
</b>

