---
title: Rundown
parent: Game Data
has_children: false
---

# Rundown
This is the setup for a Rundown, this allows you to customize the look of the Rundown as well as expedition related data.

Some sections of the game data blocks will be skimmed over in this guide as they aren't useful to modders.

### ReqToReachTierB-E
This sets how many badges you need to get to a tier, see [Guidelines - Rundown Setup]() for more info.
> `N/A`

### TierA-E
This contains an array of each level in a tier
> `List`

### name
This is the internal name of the rundown, not visible in game.
> `String`

### internalEnabled
See {{site.internal_enabled_link}}
> `Boolean`

---

# StorytellingData

### Title
The title of the rundown, this is displayed on the "Connect to Rundown" screen.
> {{ site.rich_string_link }}

### TextLog
This doesn't seem to display anywhere currenrtly.
> `String`

---

# Visuals
This section contains everything related to the visual look of the rundown.

### ColorBackground
Unused.
> `N/A`

### TierA-EVisuals
This affects the color and scale of each tier

```json
{
    "Color": {
        "a": 1.0,
        "r": 0.4509804,
        "g": 0.7490196,
        "b": 0.858823538
    },
    "Scale": 0.2
}
```
---

# Rundown In Tier
This contains the data that forms an expedition icon on the rundown.

### Enabled
Dictates if this expedition appears on the rundown.
> `Boolean`

### Accessibility
Defines how this expedition's icon appears on the rundown.
> `Enum  0: Normal, 1: AlwayBlock, 2: AlwaysAllow, 3: BlockedAndScrambled`

### LevelLayoutData
The {{site.persistent_id}} of the [Level Layout](https://gtfo-modding.github.io/wiki/docs/gamedata/levellayout.html#level-layout)
> {{ site.persistent_id_link }}

---

# Descriptive
This contains all the text elements of an expedition.

### Prefix
This is a text string that displays before the auto-prefixed number on an expedition.
> {{ site.rich_string_link }}

### PublicName
This is the name of the expedition.
> {{ site.rich_string_link }}

### ExpeditionDepth
The depth of the expedition.
> `Integer`

### EstimatedDuration
Dev info.
> `String`

### ExpeditionDescription
The description of the expedition.
> {{ site.rich_string_link }}

### RoleplayedWardenIntel
The description of the expedition.
> {{ site.rich_string_link }}

### DevInfo
What it says on the tin. Not visible in game.
> `String`

---

# Seeds
Contains data related to seeding the level generator.

### BuildSeed
The seed used to generate the rooms of the level
> `Integer`

### FunctionMarkerOffset
Effects the layout inside rooms?
> `Integer`

### StandardMarkerOffset
Does *something*.
> `Integer`

### LightJobSeedOffset
Effects the placement of lights.
> `Integer`

---

# Expedition
This contains general data related to the expedition that isn't related to the level layout.

### ComplexResourceData
The {{site.persistent_id}} of this level’s [Complex Resource Set]().
> {{site.persistent_id_link}}

### LightSettings
The {{site.persistent_id}} of this level’s [Light Settings]().
> {{site.persistent_id_link}}

### FogSettings
The {{site.persistent_id}} of this level’s [Fog Settings]().
> {{site.persistent_id_link}}

### EnemyPopulation
The {{site.persistent_id}} of this level’s [Enemy Population]().
> {{site.persistent_id_link}}

### ExpeditionBalance
The {{site.persistent_id}} of this level’s [Expedition Balance]().
> {{site.persistent_id_link}}

### ScoutWaveSettings
The {{site.persistent_id}} of this level’s [Scout Wave Settings]().
> {{site.persistent_id_link}}

### ScoutWavePopulation
The {{site.persistent_id}} of this level’s [Scout Wave Population]().
> {{site.persistent_id_link}}

---

# Main Layer Data
This contains setup for general level information

### ZoneAliasStart
The number zones start with, for instance setting this to 100 would have the zones go 100, 101, etc
> `Integer`

### ZonesWithBulkheadEntrance
> `List`

### BulkheadDoorControllerPlacements
> `List`

### BulkheadKeyPlacements
> `List`

---

# ObjectiveData
Contains setup for this level's warden objective.
See also {{site.guides_wardenobj}}.

### DataBlockId
The {{site.persistent_id}} of this levels [Warden Objective]()
> {{site.persistent_id_link}}

### WinCondition
Where the exit scan spawns.
> `Enum; 0: Spawn, 1: Custom exit`

### ZonePlacementDatas
See {{site.placement_data_link}}.
> `List`

---

# Layers
Settings for layered difficulty, secondary and tertiary layouts are the same.

### SecondaryLayerEnabled
If this level has a secondary layer
> `Boolean`

### SecondaryLayout
The {{site.persistent_id}} of the [Level Layout](https://gtfo-modding.github.io/wiki/docs/gamedata/levellayout.html#level-layout)
> {{ site.persistent_id_link }}

## BuildSecondaryFrom

#### Layer
The layer from which the secondary layer is built.
> `Enum; 0-MainLayer 1-SecondaryLayer 2-ThirdLayer`

#### Zone
The zone index from which to build from.
> `Enum; 0-20`