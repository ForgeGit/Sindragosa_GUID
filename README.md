# 🧀Sindragosa Cheese🧀<br/>GUID 101<br/>

_Vivax (Pagle-US) -_ `Discfordge` _(Discord)_



Sindragosa, queen of the Frostbrood and final boss of the Frostwing Hall at the Icecrown Citadel (ICC), can be “cheesed”. 
Its ability Icy Grip can be avoided, and in this document, I explain in detail how to fully ignore it (making it so _**nobody**_ gets pulled) utilizing the Unique ID of Players (GUID), in the Classic version of World of Warcraft: Wrath of the Lich King (as of February 2024).

## **SUMMARY**
### **Tl;dr**

-	30s into the fight and every 30s after each air phase, Sindragosa casts Icy Grip, which pulls (read: sucks) your raid into the boss hitbox. 

-	Whenever someone stands in the center of Sindragosa hitbox, _**most**_ of the raid will completely ignore the Icy Grip (this is the “cheese”). However, sometimes some people get pulled despite the “cheese”.

-	Who gets pulled or not into Sindragosa while doing the “cheese” is based on the GUID of the character standing inside her hitbox (“the cheeser”). To avoid _**everyone**_ from getting sucked into her hitbox, the person with the lowest/oldest GUID should be the one standing in the middle. Only those with a lower/older GUID relative to the “cheeser” will be sucked into, and those with a higher/newer GUID won’t.



## **Background**

Ignoring Icy Grip has been known since 2010, when the raid and the encounter were first released, as seen in a [YT video explaining how to do the "cheese"](https://www.youtube.com/watch?v=CqIjp4BNY8c&t=37s) and its respective [forum post](https://www.ownedcore.com/forums/world-of-warcraft/world-of-warcraft-exploits/297916-how-avoid-icy-grip-before-blistering-cold-sindragosa.html).

The “cheese” to ignore this mechanic entirely relies on a melee DPS <sup>or anyone? Not confirmed if a ranged DPS can do it, at least I haven’t confirmed this personally. Can someone check this? Thanks</sup> standing on the center of Sindragosa hitbox. This causes Icy Grip to not pull/suck your raid into her hitbox. 

<img src="_img/cheese_visual.jpg" /> <br />

This by itself doesn’t guarantee _**everyone**_ in your raid from ignoring the mechanic, and these “exceptions” are related to the GUID of the characters in your raid.
In short, if the lowest/oldest character in your raid stands under Sindragosa, nobody gets gripped.

## **Illustrated example (for kids)**

The following example is based on the following log:
https://classic.warcraftlogs.com/reports/ftk82FZgKnvW7rYd#fight=36

When not “cheesing” Icy Grip, your entire raid gets pulled into Sindragosa. This leads to lower uptime (and lower DPS) across the entire raid.

![Alt Text](url_to_gif)

In contrast, this is how it looks like when properly cheesing the mechanic. Only a few people get pulled into Sindragosa hitbox.

![Alt Text](url_to_gif)

There is one thing to highlight here: 

There were five (5) players getting pulled/dragged into Sindragosa hitbox. This example has 2 “cheesers” (however, you can do this with one (1) cheeser and it will work just fine).

<img src="_img/zoom_in_example.jpg" /> <br />

The five (5) players still getting gripped into Sindragosa hitbox are getting gripped despite the cheese because their GUIDs (or gameIDs) are lower/older than those of the players doing the “cheese”.

As can be seen in the following table.

<img src="_img/GUID_table.jpg" /> <br />

To the best of my knowledge, you can retrieve the GUIDs of your guild with the following command: 
```
/run g1={GetNumGuildMembers()};g2=tonumber(g1[1]);i=1 repeat local info={GetGuildRosterInfo(i)};if info[17]< UnitGUID("player")then print(info[1])print(info[17])end i=i+1 until i>g2
```
This will print most of the oldest/lowest GUIDs of your guild in your chat window, and you can copy this information out of it using the add-on Prat (Select chat as text -> Ctrl + A -> Ctrl + C)

Alternatively, you can look up the gameID of the characters in your log with the “Mage Analyzer” tool, or directly from [woodchopper website](https://classic.warcraftlogs.com/) API if [you know what you are doing.](https://www.warcraftlogs.com/api/docs)

<img src="_img/Magelyzer.jpg" /> <br />

