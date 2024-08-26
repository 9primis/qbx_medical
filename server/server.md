# **MAIN MODULE**
## Revive
---
"Expecting a source ID number, the export triggers a revival on the specific player."
```lua
exports.qbx_medical:Revive(player)
```
**PARAMETERS**

	 player: `table` | `number`
  
**RETURN STATEMENT**

	 N/A

## Heal
---
"Expecting a source, the export removes all ailments, sets player to full health and fills up hunger/thirst statuses."
```lua
exports.qbx_medical:Heal(player)
```
**PARAMETERS**

	 player: `number`
  
**RETURN STATEMENT**

	 N/A

## HealPartially
---
"Heals a player source partially if injury severity is 2 or lower, or stops bleeding if bleed level is less than 3."
```lua
exports.qbx_medical:healPartially(src)
```
**PARAMETERS**

	 src: `number`
  
**RETURN STATEMENT**

	 N/A

## GetPlayerStatus
---
"With a source ID involved, a table with details of a player's health, injuries, bleed level and current state, and the weapon that caused damage is returned."
```lua
exports.qbx_medical:GetPlayerStatus(src)
```
**PARAMETERS**

	 src: `number`
  
**RETURN STATEMENT**

	 status: `table`
  
		- injuries: `{string}[]`
  
		- bleedLevel: `number`
  
		- bleedState: `string`
  
		- damageCauses: `{ weaponHash: number = true }[]`
**EXAMPLE**
```lua
	{
		injuries = {
			"Arm (Fracture)",
			"Leg (Bruised)"
		},
		bleedLevel = 2,
		bleedState = "Minor Bleeding",
		damageCauses = {
			123456789 = true, -- random weapon hash (placebo numbers)
			123091239 = true, -- random weapon hash (placebo numbers)
		}
	}
```
