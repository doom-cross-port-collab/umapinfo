# UMAPINFO Specification Rev 2.? Default Key Values

TODO: explicitly indicate that defaults for outside of the ranges defined by iwads are outside the scope of this spec and no particular defaults should be assumed

## Global defaults
### Author
Empty string: ""

### InterText
`clear`, unless specified otherwise below.

## Map-specific defaults
The default values for most keys depend on both the map and the currently loaded IWAD.
TODO: are level names set in umapinfo treated differently from never setting the name?

### `doom1.wad`

TODO: should partime be in this table since it is cleared when defining a map in umapinfo?

|Map |Levelname|Label|LevelPic|Next|NextSecret|SkyTexture|Music |ParTime|InterBackdrop|NoIntermission|InterMusic|BossAction|
|----|---------|-----|--------|----|----------|----------|------|-------|-------------|--------------|----------|----------|
|E1M1| ?       |E1M1 |WILV00  |E1M2| ?        |SKY1      |D_E1M1|30     |             |false         |          |clear     |
|E1M2| ?       |E1M2 |WILV01  |E1M3| ?        |SKY1      |D_E1M2|75     |             |false         |          |clear     |
|E1M3| ?       |E1M3 |WILV02  |E1M4|E1M9      |SKY1      |D_E1M3|120    |             |false         |          |clear     |
|E1M4| ?       |E1M4 |WILV03  |E1M5| ?        |SKY1      |D_E1M4|90     |             |false         |          |clear     |
|E1M5| ?       |E1M5 |WILV04  |E1M6| ?        |SKY1      |D_E1M5|165    |             |false         |          |clear     |
|E1M6| ?       |E1M6 |WILV05  |E1M7| ?        |SKY1      |D_E1M6|180    |             |false         |          |clear     |
|E1M7| ?       |E1M7 |WILV06  |E1M8| ?        |SKY1      |D_E1M7|180    |             |false         |          |clear     |
|E1M8| ?       |E1M8 |WILV07  |?   | ?        |SKY1      |D_E1M8|30     |FLOOR4_8     |false         |          |(see below)[#e1m8-bossaction] |
|E1M9| ?       |E1M9 |WILV08  |E1M4| ?        |SKY1      |D_E1M9|165    |             |false         |          |clear     |

#### EndGame
describe endgame/endbunny/endpic/endcast

#### E1M8 InterText
```
"Once you beat the big badasses and",
"clean out the moon base you're supposed",
"to win, aren't you? Aren't you? Where's",
"your fat reward and ticket home? What",
"the hell is this? It's not supposed to",
"end this way!,"
"",
"It stinks like rotten meat, but looks",
"like the lost Deimos base.  Looks like",
"you're stuck on The Shores of Hell.",
"The only way out is through.",
"",
"To continue the DOOM experience, play",
"The Shores of Hell and its amazing",
"sequel, Inferno!",
```

#### EnterPic/ExitPic
need to describe how in doom it uses the animated maps when not set in umapinfo

#### E1M8 BossAction
The default BossAction for E1M8 is unrepresentable in UMAPINFO. The three components are specified as follows:
- `thingtype`: In ports that implement the MBF21 specification, this does not default to a specific thing type. Rather, any thing with the E1M8BOSS flag will trigger this bossaction. Otherwise, it is "BaronOfHell".
- `linespecial`: Lower all sectors tagged 666 to the highest touching floor (todo: word this better). This does not necessarily correspond to any actual line special.
- `tag`: 666

### `doom.wad`

Defaults for E1M1-E1M9 are the same as `doom1.wad`, with the following exceptions:
(im pretty sure somethings different for e1m8 but im not sure)

TODO: how do ports treat E4 maps when using non ultimate doom.wad?

|Map |Levelname|Label|LevelPic|Next|NextSecret|SkyTexture|Music |ParTime|InterBackdrop|NoIntermission|InterMusic|BossAction|
|----|---------|-----|--------|----|----------|----------|------|-------|-------------|--------------|----------|----------|
|E2M1| ?       |E2M1 |WILV10  |E2M2| ?        |SKY2      |D_E2M1|90     |             |false         |          |clear     |
|E2M2| ?       |E2M2 |WILV11  |E2M3| ?        |SKY2      |D_E2M2|90     |             |false         |          |clear     |
|E2M3| ?       |E2M3 |WILV12  |E2M4| ?        |SKY2      |D_E2M3|90     |             |false         |          |clear     |
|E2M4| ?       |E2M4 |WILV13  |E2M5|E2M9      |SKY2      |D_E2M4|120    |             |false         |          |clear     |
|E2M5| ?       |E2M5 |WILV14  |E2M6| ?        |SKY2      |D_E2M5|90     |             |false         |          |clear     |
|E2M6| ?       |E2M6 |WILV15  |E2M7| ?        |SKY2      |D_E2M6|360    |             |false         |          |clear     |
|E2M7| ?       |E2M7 |WILV16  |E2M8| ?        |SKY2      |D_E2M7|240    |             |false         |          |clear     |
|E2M8| ?       |E2M8 |WILV17  |?   | ?        |SKY2      |D_E2M8|30     |SFLR6_1      |false         |          |(see below)[#e2m8-bossaction] |
|E2M9| ?       |E2M9 |WILV18  |E2M3| ?        |SKY2      |D_E2M9|90     |             |false         |          |clear     |
|    |         |     |        |    |          |          |      |       |             |              |          |          |
|E3M1| ?       |E3M1 |WILV20  |E3M2| ?        |SKY3      |D_E3M1|90     |             |false         |          |clear     |
|E3M2| ?       |E3M2 |WILV21  |E2M3| ?        |SKY3      |D_E3M2|45     |             |false         |          |clear     |
|E3M3| ?       |E3M3 |WILV22  |E3M4| ?        |SKY3      |D_E3M3|90     |             |false         |          |clear     |
|E3M4| ?       |E3M4 |WILV23  |E3M5| ?        |SKY3      |D_E3M4|150    |             |false         |          |clear     |
|E3M5| ?       |E3M5 |WILV24  |E3M6|E3M9      |SKY3      |D_E3M5|90     |             |false         |          |clear     |
|E3M6| ?       |E3M6 |WILV25  |E3M7| ?        |SKY3      |D_E3M6|90     |             |false         |          |clear     |
|E3M7| ?       |E3M7 |WILV26  |E3M8| ?        |SKY3      |D_E3M7|165    |             |false         |          |clear     |
|E3M8| ?       |E3M8 |WILV27  |?   | ?        |SKY3      |D_E3M8|30     |MFLR8_4      |false         |          |(see below)[#e3m8-bossaction] |
|E3M9| ?       |E3M9 |WILV28  |E3M7| ?        |SKY3      |D_E3M9|135    |             |false         |          |clear     |

#### E2M8 InterText
```
"You've done it! The hideous cyber-",
"demon lord that ruled the lost Deimos",
"moon base has been slain and you",
"are triumphant! But ... where are",
"you? You clamber to the edge of the",
"moon and look down to see the awful",
"truth.",
"",
"Deimos floats above Hell itself!",
"You've never heard of anyone escaping",
"from Hell, but you'll make the bastards",
"sorry they ever heard of you! Quickly,",
"you rappel down to  the surface of",
"Hell.",
"",
"Now, it's on to the final chapter of",
"DOOM! -- Inferno"
```

#### E3M8 InterText
```
"The loathsome spiderdemon that",
"masterminded the invasion of the moon",
"bases and caused so much death has had",
"its ass kicked for all time.",
"",
"A hidden doorway opens and you enter.",
"You've proven too tough for Hell to",
"contain, and now Hell at last plays",
"fair -- for you emerge from the door",
"to see the green fields of Earth!",
"Home at last.",
"",
"You wonder what's been happening on",
"Earth while you were battling evil",
"unleashed. It's good that no Hell-",
"spawn could have come through that",
"door with you ..."
```

#### E2M8 BossAction
The default BossAction for E2M8 is unrepresentable in UMAPINFO. The three components are specified as follows:
- `thingtype`: In ports that implement the MBF21 specification, this does not default to a specific thing type. Rather, any thing with the E2M8BOSS flag will trigger this bossaction. Otherwise, it is "Cyberdemon".
- `linespecial`: exit level (todo: actually properly describe this). This does not necessarily correspond to any actual line special.
- `tag`: tag is unused

#### E3M8 BossAction
The default BossAction for E3M8 is unrepresentable in UMAPINFO. The three components are specified as follows:
- `thingtype`: In ports that implement the MBF21 specification, this does not default to a specific thing type. Rather, any thing with the E3M8BOSS flag will trigger this bossaction. Otherwise, it is "SpiderMastermind".
- `linespecial`: exit level (todo: actually properly describe this). This does not necessarily correspond to any actual line special.
- `tag`: tag is unused

#### E4M6 BossAction
The default BossAction for E4M6 is unrepresentable in UMAPINFO. The three components are specified as follows:
- `thingtype`: In ports that implement the MBF21 specification, this does not default to a specific thing type. Rather, any thing with the E4M6BOSS flag will trigger this bossaction. Otherwise, it is "Cyberdemon".
- `linespecial`: blazing door (todo: actually properly describe this). This does not necessarily correspond to any actual line special.
- `tag`: 666

#### E4M8 BossAction
The default BossAction for E4M8 is unrepresentable in UMAPINFO. The three components are specified as follows:
- `thingtype`: In ports that implement the MBF21 specification, this does not default to a specific thing type. Rather, any thing with the E4M8BOSS flag will trigger this bossaction. Otherwise, it is "SpiderMastermind".
- `linespecial`: Lower all sectors tagged 666 to the highest touching floor (todo: word this better). This does not necessarily correspond to any actual line special.
- `tag`: 666

### `doom2.wad`

|Map  |Levelname|Label|LevelPic|Next |NextSecret|SkyTexture|Music   |ParTime|InterBackdrop|NoIntermission|InterMusic|BossAction|
|-----|---------|-----|--------|-----|----------|----------|--------|-------|-------------|--------------|----------|----------|
|MAP01| ?       |?    |CWILV01 |MAP02| ?        |SKY1      |D_RUNNIN|30     |             |false         |          |clear     |
|MAP02| ?       |?    |CWILV02 |MAP03| ?        |SKY1      |D_STALKS|90     |             |false         |          |clear     |
|MAP03| ?       |?    |CWILV03 |MAP04| ?        |SKY1      |D_COUNTD|120    |             |false         |          |clear     |
|MAP04| ?       |?    |CWILV04 |MAP05| ?        |SKY1      |D_BETWEE|120    |             |false         |          |clear     |
|MAP05| ?       |?    |CWILV05 |MAP06| ?        |SKY1      |D_DOOM  |90     |             |false         |          |clear     |
|MAP06| ?       |?    |CWILV06 |MAP07| ?        |SKY1      |D_THE_DA|150    |SLIME16      |false         |          |clear     |
|MAP07| ?       |?    |CWILV07 |MAP08| ?        |SKY1      |D_SHAWN |120    |             |false         |          |(see below)[#map07-bossaction] |
|MAP08| ?       |?    |CWILV08 |MAP09| ?        |SKY1      |D_DDTBLU|120    |             |false         |          |clear     |
|MAP09| ?       |?    |CWILV09 |MAP10| ?        |SKY1      |D_IN_CIT|270    |             |false         |          |clear     |
|MAP10| ?       |?    |CWILV10 |MAP11| ?        |SKY1      |D_DEAD  |90     |             |false         |          |clear     |
|MAP11| ?       |?    |CWILV11 |MAP12| ?        |SKY1      |D_STLKS2|210    |RROCK14      |false         |          |clear     |
|MAP12| ?       |?    |CWILV12 |MAP13| ?        |SKY2      |D_THEDA2|150    |             |false         |          |clear     |
|MAP13| ?       |?    |CWILV13 |MAP14| ?        |SKY2      |D_DOOM2 |150    |             |false         |          |clear     |
|MAP14| ?       |?    |CWILV14 |MAP15| ?        |SKY2      |D_DDTBL2|150    |             |false         |          |clear     |
|MAP15| ?       |?    |CWILV15 |MAP16|MAP31     |SKY2      |D_RUNNI2|210    |RROCK13      |false         |          |clear     |
|MAP16| ?       |?    |CWILV16 |MAP17| ?        |SKY2      |D_DEAD2 |150    |             |false         |          |clear     |
|MAP17| ?       |?    |CWILV17 |MAP18| ?        |SKY2      |D_STLKS3|420    |             |false         |          |clear     |
|MAP18| ?       |?    |CWILV18 |MAP19| ?        |SKY2      |D_ROMERO|150    |             |false         |          |clear     |
|MAP19| ?       |?    |CWILV19 |MAP20| ?        |SKY2      |D_SHAWN2|210    |             |false         |          |clear     |
|MAP20| ?       |?    |CWILV20 |MAP21| ?        |SKY2      |D_MESSAG|150    |RROCK07      |false         |          |clear     |
|MAP21| ?       |?    |CWILV21 |MAP22| ?        |SKY3      |D_COUNT2|240    |             |false         |          |clear     |
|MAP22| ?       |?    |CWILV22 |MAP23| ?        |SKY3      |D_DDTBL3|150    |             |false         |          |clear     |
|MAP23| ?       |?    |CWILV23 |MAP24| ?        |SKY3      |D_AMPIE |180    |             |false         |          |clear     |
|MAP24| ?       |?    |CWILV24 |MAP25| ?        |SKY3      |D_THEDA3|150    |             |false         |          |clear     |
|MAP25| ?       |?    |CWILV25 |MAP26| ?        |SKY3      |D_ADRIAN|150    |             |false         |          |clear     |
|MAP26| ?       |?    |CWILV26 |MAP27| ?        |SKY3      |D_MESSG2|300    |             |false         |          |clear     |
|MAP27| ?       |?    |CWILV27 |MAP28| ?        |SKY3      |D_ROMER2|330    |             |false         |          |clear     |
|MAP28| ?       |?    |CWILV28 |MAP29| ?        |SKY3      |D_TENSE |420    |             |false         |          |clear     |
|MAP29| ?       |?    |CWILV29 |MAP30| ?        |SKY3      |D_SHAWN3|300    |             |false         |          |clear     |
|MAP30| ?       |?    |CWILV30 |?    | ?        |SKY3      |D_OPENIN|180    |RROCK17      |false         |          |?         |
|MAP31| ?       |?    |CWILV31 |MAP16|MAP31     |SKY3      |D_EVIL  |120    |RROCK19      |false         |          |clear     |
|MAP32| ?       |?    |CWILV32 |MAP16| ?        |SKY3      |D_ULTIMA|30     |             |false         |          |clear     |

#### MAP06 InterText
#### MAP11 InterText
#### MAP20 InterText
#### MAP30 InterText
#### MAP15 InterTextSecret
#### MAP31 InterTextSecret

#### MAP07 BossAction

### `tnt.wad`

Defaults the same as doom2.wad except for map names and intertexts (i think)
list them

### `plutonia.wad`

Defaults the same as doom2.wad except for map names and intertexts (i think)
list them

### `chex.wad`

This gets mentioned in spec.md so i guess it goes here too??
even though i suspect ports vary by whether they need chex.deh for the map names and intertexts

## Episodes
describe behavior of episodes, particularly ep4 here