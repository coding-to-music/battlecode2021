# Pathing and Navigation Strategy

- [Pathing and Navigation Strategy](#pathing-and-navigation-strategy)
- [Introduction to pathing and navigation](#introduction-to-pathing-and-navigation)
  - [How to use our 24 bits of flag width to communicate with between the robots and enlightenment centers](#how-to-use-our-24-bits-of-flag-width-to-communicate-with-between-the-robots-and-enlightenment-centers)
    - [packing bits](#packing-bits)
    - [coordinates above 10,000](#coordinates-above-10000)
    - [Coordinates using modululos 128](#coordinates-using-modululos-128)
    - [128 by 128 square](#128-by-128-square)
- [Bug 1](#bug-1)
  - [Basic Bug Strategy](#basic-bug-strategy)
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

# Bug 1  

## Basic Bug Strategy  
<br />  
<img width="600px" src="https://github.com/coding-to-music/battlecode2021/blob/main/Assets/basicBug.png?raw=true" align="center" alt="basicBug" />
</b>

# Bug 2  

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

