---
layout: page
title: "Blog"
permalink: /blog/
---
<style>

        p {
            text-align: justify;
        }
		
		 #goToTopBtn {
            display: none;
            position: fixed;
            bottom: 20px;
            right: 20px;
            background-color: #007BFF;
            color: #fff;
            border: none;
            border-radius: 5px;
            padding: 10px 15px;
            cursor: pointer;
        }

        #goToTopBtn:hover {
            background-color: #0056b3;
        }

        body:hover #goToTopBtn {
            display: block;
        }
		
</style>

### Contents

<nav>
    <ul>
		<li><a href="#section1">Rock, Paper, Scissors and… Flamethrower!?</a></li>
        <li><a href="#section2">Analyzing the Missteps: A Post-Mortem of Darkness Profound</a></li>
		<li><a href="#section3">Game Design Breakdown of World of Goo</a></li>
        <li><a href="#section4">Beyond Difficulty: Examining the GTA:Vice City's Demolition Man</a></li>
        <li><a href="#section5">A Look to The Troop's Accuracy Mechanics</a></li>
		<li><a href="#section6">Player's Frustration, Designer's Insight</a></li>
		<li><a href="#section7">Notes from Game Jams</a></li>
    </ul>
</nav>

---------------------------

<section id="section1">
    <h2>Rock, Paper, Scissors and… Flamethrower!?</h2>
</section>
Rock, Paper, Scissors (abbreviated as RPS from now on) is a centuries-old game with good reasons: it's easy to learn, easy to play, and fun. RPS is perfectly balanced; no weapon has a particular advantage over the others. It is used for decision-making occasionally and serves as a base for balance adjustments in video games (especialy in strategy games like Age of Empires, Starcraft etc.). A flow channel graph and visualized balance diagram for RPS can be found below:

![Picture 1](/assets/blog_RPS1.png)


Now is the time to add the fourth weapon: The flamethrower! (What!? It is my favorite weapon of choice in any game. And my favorite chapter in the Warhammer 40K universe is Salamanders. And no, I am not a pyromaniac. And again, no, this is not a blowtorch right next to me. No, I don’t need any professional help either!!)

In our first scenario, let’s assume that every weapon defeats two other weapons. Starting from the original win conditions with every weapon and working our way to the bottom, I have inserted new conditions into the table below:

![Picture 2](/assets/blog_RPS2.png)

According to the table,the three original weapons get 2 wins against the other weapons. Newly added weapon, the flamethrower gets "0" wins. This condition "breaks" the game. No one will select the flamethrower, because it is almost a guaranteed defeat - at best a draw. The game simply returned to its original in a flawed form. 

For the second scenario, we will assume that every weapon must win **one time** at least. Working our way from top to the bottom, with original win conditions pritorized, I have created a table with new conditions, which can be seen below:

![Picture 3](/assets/blog_RPS3.png)

Now at least our poor(!) flamethrower can have a win. But this have consequences; paper is down to 1 win, while rock and scissors have 2 wins. Any logical player would choose either rock or scissors, with the higher win rates, which puts rock a slightly advantageous position, as it beats the scissors. This version is also broken and unbalanced, this is unplayable too.

Time to move on to the third scenario: Every weapon wins **only** one time. This makes it 1 win, 2 draws and 1 defeat for each weapon according to the table below:

![Picture 4](/assets/blog_RPS4.png)

With this new rule, every weapon has equal chance to win and lose, but with an inconvenience: the draws doubled in number! Game is balanced and playable in this state but becomes less fun as most of the time it will end in a draw with a whooping 50% chance! 

![Picture 5](/assets/blog_RPS5.png)

A five-weapon version has already been explored; in the eighth episode of the second season of Big Bang Theory, Raj and Sheldon attempted to resolve their dispute using the [Rock, Paper, Scissors, Lizard, Spock](https://bigbangtheory.fandom.com/wiki/Rock,_Paper,_Scissors,_Lizard,_Spock){:target="_blank"}. Despite being somewhat more balanced and enjoyable with a reduced number of ties, this version tends to overcomplicate matters, placing it in the upper section of the flow chart diagram:

![Picture 6](/assets/blog_RPS6.png)

Adding the fourth and trying to make it the game balanced, resulted in too many "draws" and made it less fun. Five weapons version, it got more confusing and complex. In the end, the classic game stays the winner because sometimes, simplicity is just more fun! Don't convinced? You can always check the [101-gesture version of Rock-Paper-Scissors](https://www.umop.com/rps101.htm){:target="_blank"}!


---------------------------
---------------------------


<section id="section2">
    <h2>Analyzing the Missteps: A Post-Mortem of Darkness Profound</h2>
</section>

Participating in game jams is a thrilling yet challenging experience, demanding a unique blend of creativity, skill, and time management. The Scream Jam 2023, with 494 total submissions, marked a significant attempt for many game developers.  In this jam venture, I’ve submitted my game **[Darkness Profound](https://htramu.github.io/2023/10/28/darknesProfound/){:target="_blank"}**, which received numerous 3-point ratings out of 5 that Gauss would be proud if he’d saw this rating distribution graphic:  
  
  
![Picture 10](/assets/blog_DP_gaussProud.png)
  
  
So, where did I go wrong? Why so many 3-point ratings instead of 5? In this post-mortem essay, I will delve into the reasons behind the mediocrity of my game, "Darkness Profound," focusing on critical aspects that contributed to its shortcomings.

The first shortcoming, and the one to rule them all, was the scope of the game. The design in my mind was too ambitious, at least for a solo participant.
Based on the enveloping darkness theme, I devised two design pillars: Health and Sanity. Player had to utilize these resources carefully in order to succeed. I visualized it with this graphic:

![Picture 11](/assets/blog_DP_designPillars.png)


Sanity decreases when the player turns the flashlight off and goes into stealth mode. Sanity would decrease permanently, with no way to replenish it. When it reaches zero, it results in a game over. The main design point here is to create tension between resources – should the player opt for stealth and risk losing sanity, or should they engage in combat, risking limited ammo and health?
However, it became apparent that due to the limitations of Construct 3's free version and the constrained time available for game development, I could not implement the sanity system.  With the wrong scope chosen, game lost one of its main design pillars leading to incomplete gameplay. This could be salvaged; after turning the flashlight off, an unnatural being attacks after a certain time. With a chilling sound effect and visual cues this could be the tension creator I was looking for.

Stealth system:
Another bite more than I can chew is the stealth system. Designing and implementing meaningful stealth mechanics is hard already, even to a team of experienced designers (which for one I am not). With limited time and resources of the jam environment it become even harder. With the sanity system gone, it become meaningless to spend time on to craft a detailed stealth system, so I left the simple stealth mechanics that I’ve already implemented. It is just a LoS reduction for the zombies, when player turns of the flashlight, zombie LoS is down to a quarter of its original value of 400 px. This could’ve changed to a battery consuming flashlight system in order to make player turn off the flashlight occasionally and give them the dread of bumping onto an unsuspecting zombie. 

Level design:
Darkness Profound’s level design features big empty spaces. This empty spaces was meant to be used by player in order to avoid the zombie menace while stealthing. With stealth is half-implemented this spaces makes no sense. It also removes whole tension of combat system. I should’ve designed the level with more corridors and closed rooms, less space to maneuver and to avoid zombies, to  create a claustrophobic feeling. Large level design, along with the LoS reduction of the stealth system, makes gameplay dull; turn off the flashlight, walk through all the level from start to finish with almost no harm.


---------------------------
---------------------------

<section id="section3">
    <h2>Game Design Breakdown of World of Goo</h2>
</section>

World of Goo, a critically acclaimed indie puzzle game, is a showcase the power of simplicity and innovation in game design. Developed by 2D Boy, the game's straightforward concept of connecting balls of goo to reach the exit to finish a level, never gets boring thanks to the clever design choices of the developers: the elegant simplicity, the ever-evolving mechanics and player-centric features.

*Simple idea, simple execution*; this is what the World of Goo does best. At its core, World of Goo is based around a very basic idea – connect balls of goo in order to get a requisite number of Goo Balls to reach the exit which is presented on each level as a pipe. This concept serves as the backbone of the game, providing players with an intuitive and easy-to-understand objective. Its brilliance lies in the simplicity of execution; players need only drag and drop goo units to build structures, like bridges and tower, that defy gravity and traverse challenging landscapes. Yet, the limited freedom to pull a goo to a maximum five goo units away, adds a layer of constraint, requiring players to think strategically and plan their moves carefully. This simplicity ensures that the game remains accessible to players of all skill levels and promotes creativity and experimentation.

World of Goo's level design is characterized by expansive maps that offer players enough space to construct their goo-based structures. Gravity, is the main hazard of the game, but also the one of the enablers for the players to overcome the challenges. The game consists several hazardous elements into the levels, ranging from spikes and fire to unpredictable environmental factors.  Levels, after the gravity, feature one or two extra hazards most, never straying far from the simplicity mindset and making things extremely complicated. Each level presents players with multiple solutions, encouraging diverse approaches and fostering a sense of accomplishment through individualized problem-solving. Furthermore, the game introduces hazardless levels, offering a reprieve from the usual challenges and allowing players to focus on building and exploration.

To enhance the player experience, World of Goo features a rewind function facilitated by friendly fireflies. This mechanic allows players to revert to several moves back, providing a safety net for experimentation and mitigating the potential frustration of mistakes. The rewind function not only promotes a sense of agency but also encourages players to push the boundaries of their creativity without fear of irreversible consequences.

For the expert players seeking an additional challenge, World of Goo offers the Obsessive Completion Distinction (OCD) mode. This mode features optional goals, like completing a with minimal moves or collecting a huge number of goo, to push players to optimize their solutions and aim for perfection. The inclusion of OCD mode ensures that the game caters to a wide range of players, from casual enthusiasts to hardcore perfectionists.

In order to keep the gameplay fresh, developers introduce new types of goo frequently throughout the levels. Each of these new types of goo comes with different mechanics, like a sling goo, which player can throw to a certain distance with a sling-like effect or the skull goo, a type of goo that is impervious to spikes.  Yet, the core objective of connecting goo to reach an exit remains constant, providing players with a sense of familiarity. The introduction of new mechanics ensures that the game stays fresh, engaging, and exciting for players over time.

As addressed in the preceding sections of this game design breakdown we came to a conclusion: World of Goo serves as an inspiring example of how a game with a simple idea can evolve into a masterpiece through thoughtful design choices, ultimately leaving a mark on the landscape of indie gaming. 


---------------------------
---------------------------

<section id="section4">
    <h2>Beyond Difficulty: Examining the GTA:Vice City's Demolition Man</h2>
</section>

The infamous Demolition Man mission in Grand Theft Auto: Vice City has caused many players to quit the game due to its notorious difficulty. But is the challenge the only issue, or are there game design mistakes by the developers? Let's find out. 

***(Warning! Grand Theft Auto: Vice City spoilers beyond this point.)***

This mission is the second given by Avery Carrington. It requires the player to control a remote-controlled helicopter, delivering four demolition charges to specific locations within a construction site in 7 minutes. Alongside the time limit, hazards include melee weapon-wielding enemies and pistol wielding enemies. Enemies are appropriately positioned and their count is not unusual; most common route features one melee enemy on ground floor, two on the first floor, one pistol wielder and one melee on second floor and two pistol wielders on the third floor. There are scattered enemies on the floors but they often pose little threat except player decides to tread around the floors. The gameplay area is confined by walls, stairs, window glass, and safety nets, leaving little room for maneuvering. Objectives are placed vertically on a four-story construction site, forcing the player to make several back-and-forth journeys to the starting point to pick up bombs, as the helicopter can only carry one at a time. With multiple hazards, a time limit, and blockers, this mission is intentionally designed to be challenging. There is no apparent design mistake here; it is simply a very difficult mission.

So, there are no design issues related to the mission itself. But what is wrong with it then?

Firstly, there is an issue related to PC players. It is evident that this mission is designed to be played with a gamepad, as the developers prioritized console versions and their control schemes. Without rumble pads and with the awkward keyboard control scheme of the PC version, this mission became even more challenging. Also, it should be remembered that, when Vice City was released in 2002, gamepads were not a common accesory in PC gaming.

Second one is the timing of the mission's appearance. Depending on your playstyle, this mission can be encountered very early in the game, around the 9th or 10th mission. With the skills required to handle this mission, it should have appeared later in the game, perhaps as the 40th mission or so (Vice City offers a total of 59 missions).

The third and the most significant problem is that this mission is not mandatory to finish the story; Demoliton Man is optional and required only for 100% completion. However, this information is not relayed to the player. There is no indication anywhere, in any form, like a different marker on the map compared to the usual Grand Theft Auto mission style or a message in the briefing. Even worse, after the Cop Land mission, no other markings will be left except the “A” letter of this mission (assuming the player undertook all initial story missions). To make the game progress further, the player should buy assets and complete their respective missions in order for the main story missions to reappear. This information is only mentioned once in the ending cutscene of the Shakedown mission as if it's an optional feature. Avery's phone call after the Shakedown mission hints at it slightly, but no other information or guidance is provided to the player. It is easy to assume that, without passing this mission, the story would not continue. Many people must have given up in frustration, thinking the they are stuck (there was no YouTube back in 2002, even Google was a toddler). This is a significant design mistake; the game should have clearly advertised the direction to the player.

---------------------------
---------------------------

<section id="section5">
    <h2>A Look to The Troop's Accuracy Mechanics</h2>
</section>

![Picture 12](/assets/blog_troopPointBlank.png)

Does the scenario in the image above feel familiar? In most of turn-based strategy games, players often rush forward their units to eliminate the range penalty, and takes a shot at point blank range. (And misses with 95% percent accuracy :) – I am looking at you XCOM: **[XCOM in a Nutshell](https://youtu.be/zAThQV-vj08){:target="_blank"}**). This won’t be a problem depending on the game's setting, but for a realistic World War II title, there should be more 'distances' between opposing sides. Moreover, movement of the infantry and any kind of vehicle should cause inaccuracy, as well as rotating a heavy weapon or turning the turret for the tanks. No stabilizers or fire-control systems exists on the WWII era tanks, they have to stop in order to shoot and readjust everything to get an accurate shot. After running or dashing, infantry have to catch their breath to shoot accurately. **[The Troop](https://store.steampowered.com/app/1363740/The_Troop/){:target="_blank"}**, a turn-based, platoon-level tactical World War II title, released in October 2023 and sadly becoming an underdog instantly, addresses these effectively. The game features solid mechanics without the extreme complexity often found in similar games striving for realism. 

The first mechanic is the steadiness mechanic. In developers’ words; “It represents a unit's ability to take action competently at a given moment in the midst of battle.” The steadiness value effects “attack accuracy” and “final actions” of the units. Steadiness is reduced by unit movement, tank turret rotation and/or target acquisition and the suppression value of the unit. If you lose enough steadiness, it is a "final action" and the unit finishes its turn. When a unit moves (rotation also counts as moving), depending on the type of the unit, steadiness gets decreased by a certain point; for vehicles, it's 20% per tile and for infantry, it's 10%. This value is subtracted from a base accuracy value of 100%. 

The second,specific to heavy weapons, is the gunnery mechanic. Gunnery represents the skill and the time to adjust the aiming of the heavy weapon, whether it is a QF 17-pounder anti-tank gun or a  7,5 cm KwK 42 (L/70) on the turret of a Panther. Whenever a heavy weapon turns to aim at a hex, it loses accuracy for each gunnery point spent, with the formula of (spent gunnery points - 1)*5%. Its total count is different among the units and it replenishes at the start of the player's turn.

Let's imagine a scenario where a Panzer IV meets a Sherman Mark III. The Panzer IV moves a tile and aims its gun at the Sherman Mark III. With 1 tile movement, the panzer lost steadiness and now takes a -20% to its accuracy. Its turret was not angled in the same direction of its hull, so it has to spend 3 gunnery points to aim at the enemy tank, resulting in a further 10% _`((3-1)*5%)`_ reduction of accuracy.

Sounds complex? Not at all. All mechanics for shooting are combined into a chance to hit score, which is shown as a percentage below the targeted unit, as seen in the screenshot below.

![Picture 13](/assets/blog_daTroopSShot.jpg)

The same goes for the infantry except for the gunnery mechanic. The screenshot below shows an infantry unit moved 2 tiles away from its starting position which causes a loss in steadiness.

![Picture 14](/assets/blog_daTroopSShot2.jpg)

These two mechanics create a depth of tactical choices. How many tiles should I move before shooting? Should I move at all? If I keep my distance can I penetrate the armor or should I go for a flanking move? But one thing is for sure, instead of mindlessly rushing to melee range, players need to keep their distance, which suits to a realistic WWII title. With "steadiness" and "gunnery", along with other mechanics, the game creates a fun, realistic, but not overly complex turn-based gameplay experience.


---------------------------
---------------------------

<section id="section6">
    <h2>Player's Frustration, Designer's Insight</h2>
</section>  

Achievements in video games are virtual rewards or milestones that players can unlock by completing specific tasks, challenges, or objectives within a game. These achievements serve various purposes and add an extra layer of engagement to the gaming experience. This is the textbook definition of 'achievements.'

As a player, I usually did not see the need for them. They seemed like time wasters, implemented by 'evil' designers to prolong the game as much as possible. As a game designer, I understand their necessity for game development but cannot fathom them as an integral part of a game due to my perspective as a player. Until that fateful day... (eerie music looms).

***(Warning! Warhammer 40,000: Battlesector spoilers beyond this point.)***

Warhammer 40,000: Battlesector is a fine game, both as a turn-based strategy and as a Warhammer 40K video game (as the franchise suffers from bad titles). As a habit, I play video games on the hardest difficulty, and Battlesector was no exception. The 15th mission, called 'The Battle for the Angel’s Fall,' features a bonus objective to save Sisters of Battle from the Tyranids. Each Sisters of Battle squad saved is rewarded with HQ Tokens after the mission ends. This objective is considered very challenging by players on the Steam discussions — even a dev commented that he could only manage to save 4 out of the 7 available on the hardest difficulty.

At mission start, I set myself to save all the Sisters. It was brutal, full of blood, sweat, and tears. In the end, I managed to save them all. It provided immense satisfaction, the rewards were substantial, and... That’s it?? No achievement for completing the hardest secondary objective of the game on the hardest difficulty — which is even recognized by the devs? I was hoping to get one along with only 1% of the players. Now I realize why people are so keen on getting them.

It would’ve given me the recognition — I would be one of the best players to accomplish the hardest of all secondary objectives.
It would’ve given me my bragging rights — How it was so hard, how I created that tactic, made this movement.
It would be the extra reward — The more rewards, the better. Players love them.

My player side and game designer side have now made peace with each other. From a game design perspective, I accept that achievements are necessary; they should be included whenever and wherever they can be. They create recognition, accomplishment, more challenges, a mastery route for the skills gained during playtime, replayability, and so on and so forth.


---------------------------
---------------------------
<section id="section7">
    <h2>Notes from Game Jams  </h2>
</section>  

- If a single polygon moves, playtesting should begin. This is an exaggeration, of course, but it underscores the importance of early playtesting. In my first jam, GDFG TEAM JAM #3, we couldn’t discover that our coyote timer was broken until our game, 'run.u.run,' was published. In both of my jams, I became so accustomed to the controls and mechanics that I failed to notice the floaty jumping in 'run.u.run.' Even worse, I wasn’t aware that I had not implemented diagonal movement in 'Darkness Profound' (my Scream Jam 2023 submission where I go solo) until the last minute! There was almost zero playtesting in both jams.    
- No one reads instructions, so a tutorial is a must. Write even the nicest, simplest, easiest-to-understand, and brief instructions; no one reads them (slight exaggeration). Some argue that tutorials are unnecessary, but I believe they must be implemented. They should be in-game, designed to be an organic part of the game, for example, a dedicated level with a story hook.    
- Time constraints are a constant challenge in game jams, mirroring the broader game development process.
- Success hinges on assembling the right team. In my first Jam, our team struggled to allocate enough time, resulting in failure. With my last-minute efforts, I barely published the game. Conversely, opting to go solo in my second jam, I realized it was a significant mistake given the game's scope—it truly required a team effort.
- Advertising plays a pivotal role. In my second jam, I dedicated time to extensive promotion to ensure my game garnered a high number of ratings. But games that are better than mine, that did not pay attention to announce themselves, went unnoticed and got lower rating numbers.

<a href="#" id="goToTopBtn" title="Go to Top">Go to Top</a>