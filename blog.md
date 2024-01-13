---
layout: page
title: "Blog"
permalink: /blog/
---
<style>
        nav {
            position: fixed;
            width: 400px;
            height: 400px;
            background-color: #f0f0f0;
            padding: 20px;
            box-sizing: border-box;
            overflow-y: auto; /* Add scroll bar if content overflows */
        }

        nav ul {
            list-style: none;
            padding: 0;
            margin: 0;
        }

        nav ul li {
            margin-bottom: 10px;
        }

        section {
            margin-left: 420px; /* Adjusted for the fixed navigation width */
        }
		
        p {
            text-align: justify;
        }
</style>
### Contents

<nav>
    <ul>
        <li><a href="#section1">Analyzing the Missteps: A Post-Mortem of Darkness Profound</a></li>
        <li><a href="#section2">Beyond Difficulty: Examining the Design of the Vice City's Demolition Man</a></li>
        <li><a href="#section3">An in Depth Look of The Troop's Accuracy Mechanics</a></li>
		<li><a href="#section4">Lessons from Game Jams  </a></li>
    </ul>
</nav>

<section id="section1">
    <h2>Analyzing the Missteps: A Post-Mortem of Darkness Profound</h2>
</section>

Participating in game jams is a thrilling yet challenging experience, demanding a unique blend of creativity, skill, and time management. The Scream Jam 2023, with 494 total submissions, marked a significant attempt for many game developers.  In this jam venture, I’ve submitted my game **[Darkness Profound](https://htramu.github.io/2023/10/28/darknesProfound/)**, which received numerous 3-point ratings out of 5 that Gauss would be proud if he’d saw this rating distribution graphic:
  
![Picture 1](/assets/DP_gaussProud.png)
  
So, where did I go wrong? Why so many 3-point ratings instead of 5? In this post-mortem essay, I will delve into the reasons behind the mediocrity of my game, "Darkness Profound," focusing on critical aspects that contributed to its shortcomings.
The first mistake, and the one to rule them all, was the scope of the game. The design in my mind was too ambitious, at least for a solo participant.
Based on the enveloping darkness theme, I devised two design pillars: Health and Sanity. Player had to utilize these resources carefully in order to succeed. I visualized it with this graphic:

![Picture 2](/assets/DP_designPillars.png)


Sanity decreases when the player turns the flashlight off and goes into stealth mode. Sanity would decrease permanently, with no way to replenish it. When it reaches zero, it results in a game over. The main design point here is to create tension between resources – should the player opt for stealth and risk losing sanity, or should they engage in combat, risking limited ammo and health?
However, it became apparent that due to the limitations of Construct 3's free version and the constrained time available for game development, I could not implement the sanity system.  With the wrong scope chosen, game lost one of its main design pillars leading to incomplete gameplay.  This also made the stealth mechanics almost useless which will be the following subject. 

Stealth system:
Another bite more than I can chew is the stealth system. Designing and implementing meaningful stealth mechanics is hard already, even to a team of experienced designers (which for one I am not). With limited time and resources of the jam environment it become even harder. With the sanity system gone, it become meaningless to spend time on to craft a detailed stealth system, so I left the simple stealth mechanics that I’ve already implemented. It is just a LoS reduction for the zombies, when player turns of the flashlight, zombie LoS is down to a quarter of its original value of 400 px. Which is almost pointless and makes gameplay dull; turn of the flashlight, walk through all the level from start to finish with no harm. What is also dull is the level design – third subject I will go through.

Level design:
Darkness Profound’s level design features big empty spaces. This empty spaces was meant to be used by player in order to avoid the zombie menace while stealthing.


---------------------------
---------------------------

<section id="section2">
    <h2>Beyond Difficulty: Examining the Design of the Vice City's Demolition Man</h2>
</section>

The infamous Demolition Man mission in Grand Theft Auto: Vice City has caused many players to quit the game due to its notorious difficulty. But is the challenge the only issue, or are there game design mistakes by the developers? Let’s find out. 

***(Warning! Grand Theft Auto: Vice City spoilers beyond this point.)***

This mission is the second given by Avery Carrington. It requires the player to control a remote-controlled helicopter, delivering four demolition charges to specific locations within a construction site in 7 minutes. Alongside the time limit, hazards include melee weapon-wielding enemies and pistol users. The gameplay area is confined by walls, stairs, and safety nets, leaving little room for maneuvering. Objectives are placed vertically on a four-story construction site, forcing the player to make several back-and-forth journeys to the starting point to pick up bombs, as the helicopter can only carry one at a time. With multiple hazards, a time limit, and blockers, this mission is intentionally designed to be challenging. There is no game design mistake here; it is simply a very difficult mission.

So, the design issues are not related to the mission itself. Let’s address them:

Firstly, there is an issue related to PC players. It is evident that this mission is designed to be played with a gamepad, as the developers prioritized console versions and their control schemes. Without rumble pads and with the awkward keyboard control scheme of the PC version, this mission became even more challenging. Also, it should be remembered that, when Vice City was released in 2002, gamepads were not a common accesory in PC gaming.

Secondly, there is a concern about the timing of the mission's appearance. Depending on your playstyle, this mission can be encountered very early in the game, around the 9th or 10th mission. With the skills required to handle this mission, it should have appeared later in the game, perhaps as the 40th mission or so (Vice City offers a total of 59 missions).

Thirdly, the most significant issue is that this mission is not mandatory to finish the game; it is optional and required only for 100% completion. However, this information is not relayed to the player. There is no indication anywhere, in any form, like a different marker on the map compared to the usual Grand Theft Auto mission style or a message in the briefing. Even worse, after the Cop Land mission, no other markings will be left except the “A” letter of this mission (assuming the player undertook all initial story missions). To make the game progress further, the player should buy assets and complete their respective missions in order for the main story missions to reappear. This information is only mentioned once in the ending cutscene of the Shakedown mission as if it's an optional feature. Avery's phone call after the Shakedown mission hints at it slightly, but no other information or guidance is provided to the player. It is easy to assume that, without passing this mission, the story would not continue. Many people must have given up in frustration, thinking the they are stuck (there was no YouTube back in 2002, even Google was a toddler). This is a significant design mistake; the game should have clearly advertised the direction to the player.

---------------------------
---------------------------

<section id="section3">
    <h2>An in Depth Look of The Troop's Accuracy Mechanics</h2>
</section>

Many turn-based combat is like this: Player rushes forward units in order to eliminate the range penalty, and takes a shot at point blank range. (And misses with 95% percent accuracy :) – I am looking at you XCOM: **[XCOM in a nutshell](https://youtu.be/zAThQV-vj08)**). This won’t be a problem depending the setting of the game, but how about the realistic titles of the World War II? Where in real life no stabilizers exist, tanks have to stop in order to take an accurate shot.  Turning its turret and aiming with WWII era optics, setting up the shot would reduce the accuracy. Wouldn’t be firing after moving hinders infantry, where he has to control his breathing in order to shoot accurately. Enter the solution of The Troop.

First mechanic is the steadiness mechanic. In developers’ words; “It represents a unit's ability to take action competently at a given moment in the midst of battle.” Steadiness value effects “attack accuracy” and “final actions” of the units, but only accuracy will be addressed. Steadiness is reduced by unit movement, tank turret rotation and/or target acquisition and the suppression value of the unit. When a unit moves (rotation also counts as moving), depending the type of the unit, steadiness gets decreased by certain point; for vehicles 20% per tile and infantry 10%. This value is subtracted from a base accuracy value of 100%. 



---------------------------
---------------------------


<section id="section4">
    <h2>Lessons from Game Jams  </h2>
</section>  
1. If a single polygon moves, playtesting should begin. This is an exaggeration, of course, but it underscores the importance of early playtesting. In my first jam, GDFG TEAM JAM #3, we couldn’t discover that our coyote timer was broken until our game, 'run.u.run,' was published. In both of my jams, I became so accustomed to the controls and mechanics that I failed to notice the floaty jumping in 'run.u.run.' Even worse, I wasn’t aware that I had not implemented diagonal movement in 'Darkness Profound' (my Scream Jam 2023 submission where I go solo) until the last minute! There was almost zero playtesting in both jams.    
2. No one reads instructions, so a tutorial is a must. Write even the nicest, simplest, easiest-to-understand, and brief instructions; no one reads them (slight exaggeration). Some argue that tutorials are unnecessary, but I believe they must be implemented. They should be in-game, designed to be an organic part of the game, for example, a dedicated level with a story hook.    
3. Jams are microcosms of the game development industry, such as:
    - Time constraints are a constant challenge in game jams, mirroring the broader game development process.
    - Success hinges on assembling the right team. In my first Jam, our team struggled to allocate enough time, resulting in failure. With my last-minute efforts, I barely published the game. Conversely, opting to go solo in my second jam, I realized it was a significant mistake given the game's scope—it truly required a team effort.
    - Advertising plays a pivotal role. In my second jam, I dedicated time to extensive promotion to ensure my game garnered a high number of ratings. But games that are better than mine, that did not pay attention to announce themselves, went unnoticed and got lower rating numbers.