# Pathing and Navigation Strategy

- [Pathing and Navigation Strategy](#pathing-and-navigation-strategy)
- [Introduction to pathing and navigation](#introduction-to-pathing-and-navigation)
- [Bug 1](#bug-1)
- [Bug 2](#bug-2)
- [Using enlightenment centers to coordinate locations and using flags to communicate](#using-enlightenment-centers-to-coordinate-locations-and-using-flags-to-communicate)
  - [How to use our 24 bits of flag width to communicate with between the robots and enlightenment centers](#how-to-use-our-24-bits-of-flag-width-to-communicate-with-between-the-robots-and-enlightenment-centers)

# Introduction to pathing and navigation  
 
From lecture #2
[Twitch video](https://www.twitch.tv/videos/866439939)

# Bug 1  
# Bug 2  

# Using enlightenment centers to coordinate locations and using flags to communicate  

<br />  
<img width="600px" src="https://github.com/coding-to-music/battlecode2021/blob/main/Assets/using-24-bits-to-communicate-between-robots-and-centers.png?raw=true" align="center" alt="using-24-bits-to-communicate-between-robots-and-centers" />
</b>

[Twitch video time 44:04](https://www.twitch.tv/videos/866439939)

## How to use our 24 bits of flag width to communicate with between the robots and enlightenment centers  
- Number of rounds: 3000  
- 32,768 = 2 to the 15th power  
- Which would require 30 bits  
- We only have 24 bits each turn  
- So we can send the X coordinate on the odd rounds  
- Send the Y coordinate on the even rounds  
- We will have 9 other bits to pack extra info each round  
- 24 bits each round, 15 for the X or Y coordinate  
- 9 remaining for extra info  



