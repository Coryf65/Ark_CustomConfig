# Ark_CustomConfig
My custom config file for adding dinos to an ARK server map.

Guide from [diabolicherb](https://steamcommunity.com/app/346110/discussions/0/1812044473320892317/) on Steam

Spawn Locations [Location IDs](https://ark.gamepedia.com/Spawn_Entries)

Dino IDs for [Ragnarock](https://ark.gamepedia.com/Creature_IDs#Creatures_of_Ragnarok)

Dino IDs for [Abberation](https://ark.gamepedia.com/Creature_IDs#Creatures_of_Aberration)

Dino IDs for [Extinction](https://ark.gamepedia.com/Creature_IDs#Creatures_of_Extinction)


## Adding the the config 

## Changing Base Stats

https://ark.gamepedia.com/Server_Configuration#PerLevelStatsMultiplier

example when taming a dino the wild base stats will be at 1.0
``` ini
# Health = 0
PerLevelStatsMultiplier_DinoTamed[0]=1.0
PerLevelStatsMultiplier_DinoTamed_Add[0]=1.0
PerLevelStatsMultiplier_DinoTamed_Affinity[0]=1.0
# Damage = 8
PerLevelStatsMultiplier_DinoTamed[8]=1.0
PerLevelStatsMultiplier_DinoTamed_Add[8]=1.0
PerLevelStatsMultiplier_DinoTamed_Affinity[8]=1.0
```

## Adding in Dinos
This is an example of adding a dino into ARK, adding Ravagers to Monster Island
``` ini
ConfigAddNPCSpawnEntriesContainer=
(NPCSpawnEntriesContainerClassString="DinoSpawnEntriesMonsterIsland",NPCSpawnEntries=((AnEntryName="Ravager1Spawner",EntryWeight=0.14,NPCsToSpawnStrings=("CaveWolf_Character_BP_C"))),NPCSpawnLimits=((NPCClassString="CaveWolf_Character_BP_C",MaxPercentageOfDesiredNumToAllow=0.14)))
```


DinoSpawnEntriesMonsterIsland  = The Spawn Location

Ravager1Spawner                = Entry name and you can change it to whatever you want, its for personal identification uses

EntryWeight=0.14               = This is what controls your spawning, In order to convey that information we type 0.14, to convey 25% we would put 0.25, 50% would be 0.5.

CaveWolf_Character_BP_C        = Dino Id to Spawn in, choose based on Dino ID for the Map
