# Player

Every player has the following properties in the game:<br>
- Level
- Maximum Health
- Melee Damage
- Projectile Damage
- Critical Chance
- Critical Multiplier
- Movement Speed
- Defense
- Evasion
- Barter
- Luck
<br>
The descriptions (ex: perks) usually refers to these properties as "stats" [melee damage stat]<br>
These stats can be found right side on your screen (on scoreboard) some of them are hidden<br>
<br>
All of the stats has a starting value and sometimes a max value what they can reach<br>

## Level

Doesn't have any effect on it's own but your overall level, starts at 1

## Max Health

Controls your maximum health, maximum health limited at 500

## Melee Damage / Projectile Damage

Additional damage when you use a corresponding weapon<br>
Worth to mention they can reach negative values in that case<br>
it simply substracted from the weapon's damage if that too falls below 0<br>
then you fail to deal any damage to an entity

## Critical Chance

The chance (%) being rolled when you are shooting with a bow or deal damage with a melee weapon<br>
If it makes the damage critical then it multiplies your damage by [Critical Multiplier]<br>
Max value is 90%

## Critical Multiplier

Multiplies the damage by the value when your damage is a critical<br>
Keep in mind it starts at 1.0x so even if you manage to deal critical chance (even with perks)<br>
with 1.0x multiplier you will deal the same damage as a regular attack<br>
Max value is 6x

## Movement Speed

How fast your character moves, starting value is 0.1 (vanilla minecraft)<br>
Max value is 0.25

## Defense

Defense reduces the received damage by the given percentage<br>
Keep in mind some monsters have ignore defense stat so it will reduce your defense<br>
Max value is 95%

## Evasion

Evasion is when your health falls below or equals to 0 then evasion's chance is rolled<br>
If it is a success then you only receive the damage's half so you won't die and a resurrection effect will be played<br>
Max value is 80%

## Barter

Barter allows you to see more slots in the merchants, it doesn't give you any bonus or discount<br>
The merchant's content is all the same for everybody except with lower barter one can't see a lot of slots<br>
Max value is 1150

## Luck

Luck adds additional chance to open more items in a chest, however it has a very low effect on them<br>
It is better with rolling more perks in the same altars. Altars can have up to 2 additional persk to them.<br>
Additionally it affects if you are able to choose more perks from the additional perks.<br>
With a high luck you can find altars with 3 perks and all the 3 choosable<br>
Max value is 200

<hr>
Keep in mind the max value of these stats are not what you can upgrade to rather<br>
is a safe gate to prevent game breaking values ever reached<br>