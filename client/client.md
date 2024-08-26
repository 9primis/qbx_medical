# **PUBLIC EVENTS**

## qbx_medical:client:heal
---
"Heals players wounds, either all injuries or minor injuries depending on parameter"
```lua
TriggerEvent('qbx_medical:client:heal', type)
```
**PARAMETERS**
	 type?: `'full'` | `string`
  
		 - `'full'`: Heals all wounds
		 - `string`: (Anything other than 'full') Heals only minor wounds
   
**RETURN STATEMENT**
	 N/A
  
# **MAIN MODULE**
## isDead
---
"Check if player is in a 'DEAD' state. Returns true if player is dead, false if otherwise."
```lua
exports.qbx_medical:isDead()
```
**PARAMETERS**
	 N/A
  
**RETURN STATEMENT**
	 state: `true` | `false`

## IsLaststand
---
"Check if player is in a 'LAST_STAND' state. Returns true if player is dead, false if otherwise."
```lua
exports.qbx_medical:IsLaststand()
```
**PARAMETERS**
	 N/A
  
**RETURN STATEMENT**
	 state: `true` | `false`

## GetDeathTime
---
"Acquires current death timer value"
```lua
exports.qbx_medical:GetDeathTime()
```
**PARAMETERS**
	 N/A
  
**RETURN STATEMENT**
	 timer: `number`

## GetLaststandTime
---
"Acquires current last stand timer value"
```lua
exports.qbx_medical:GetLaststandTime()
```
**PARAMETERS**
	 N/A
  
**RETURN STATEMENT**
	 timer: `number`

## IncrementDeathTime
---
"Increment the current death timer by the specified amount, in seconds"
```lua
exports.qbx_medical:IncrementDeathTime(seconds)
```
**PARAMETERS**
	 seconds: `number`
  
**RETURN STATEMENT**
	N/A

## IncrementLaststandTime
---
"Increment the current last stand timer by the specified amount, in seconds"
```lua
exports.qbx_medical:IncrementLaststandTime(seconds)
```
**PARAMETERS**
	 seconds: `number`
  
**RETURN STATEMENT**
	N/A

## GetRespawnHoldTimeDeprecated
---
"Acquire the current respawn hold timer."
```lua
exports.qbx_medical:GetRespawnHoldTimeDeprecated()
```
**PARAMETERS**
	N/A
 
**RETURN STATEMENT**
	timer: `number`

## MakePedLimp
---
"Forces the player to limp"
```lua
exports.qbx_medical:MakePedLimp()
```
**PARAMETERS**
	N/A
 
**RETURN STATEMENT**
	N/A
 
**TODO**
	This export should not check any conditions, but force the ped to limp instead.

## SendBleedAlert
---
"Notify the player of bleeding within their body"
```lua
exports.qbx_medical:SendBleedAlert()
```
**PARAMETERS**
	N/A
 
**RETURN STATEMENT**
	N/A

# **DAMAGE MODULE**

## EnableDamageEffects
---
"Enables all effects related to player damage"
```lua
exports.qbx_medical:EnableDamageEffects()
```
**PARAMETERS**
	 N/A
  
**RETURN STATEMENT**
	 N/A
  
## DisableDamageEffects
---
"Disable all effects related to player damage"
```lua
exports.qbx_medical:DisableDamageEffects()
```
**PARAMETERS**
	 N/A
  
**RETURN STATEMENT**
	 N/A
  
# **DEAD MODULE**

## PlayDeadAnimation
---
"Applies death animation on player, selecting between being on foot, in vehicle, or handcuffed."
```lua
exports.qbx_medical:PlayDeadAnimation(player)
```
**PARAMETERS**
	 N/A
  
**RETURN STATEMENT**
	 N/A

## KillPlayer
---
"Simulate a death state by applying a death animation and disables player's gameplay (Controls, ability to respawn, turns player invincible)"
```lua
exports.qbx_medical:KillPlayer(attacker, weapon)
```
**PARAMETERS**
	 attacker: `number`
  
	 weapon: `number` 
  
**RETURN STATEMENT**
	 N/A

## AllowRespawn
---
"Ensure the ability for a player to respawn after death"
```lua
exports.qbx_medical:AllowRespawn()
```
**PARAMETERS**
	 N/A
  
**RETURN STATEMENT**
	 N/A

## DisableRespawn
---
"Disable the ability for a player to respawn after death"
```lua
exports.qbx_medical:DisableRespawn()
```
**PARAMETERS**
	 N/A
  
**RETURN STATEMENT**
	 N/A

# **LAST STAND MODULE**
## StartLastStand
---
"Applies last stand state to player. Player will be disarmed and critically injured, but not dead, allowing for limited movement. EMS are also notified when this function is called."
```lua
exports.qbx_medical:StartLastStand(player)
```
**PARAMETERS**
	 attacker: `number`
  
	 weapon: `number`
  
**RETURN STATEMENT**
	 N/A
  
**NOTE**
	This function uses "InteractSound", if that should be of any concern.

# **WOUNDING MODULE**

## MakePlayerBlackout
---
"Triggers a blackout effect on player"
```lua
exports.qbx_medical:MakePlayerBlackout()
```
**PARAMETERS**
	 N/A
  
**RETURN STATEMENT**
	 N/A

## MakePlayerFadeOut
---
"Triggers a partial blackout effect on player"
```lua
exports.qbx_medical:makePlayerFadeOut()
```
**PARAMETERS**
	 N/A
  
**RETURN STATEMENT**
	 N/A

## RemoveBleed
---
"Set the player's bleed level to the specified level from 1 to 4. Number can not be negative."
```lua
exports.qbx_medical:removeBleed(level)
```
**PARAMETERS**
	 level: `number`
  
**RETURN STATEMENT**
	 N/A

## EnableBleeding
---
"Enables all systems associated with bleeding"
```lua
exports.qbx_medical:EnableBleeding()
```
**PARAMETERS**
	 N/A
  
**RETURN STATEMENT**
	 N/A
  
## DisableBleeding
---
"Disable all systems associated with bleeding. This also disables damage taken and any ill effects such as blacking out."
```lua
exports.qbx_medical:DisableBleeding()
```
**PARAMETERS**
	 N/A
  
**RETURN STATEMENT**
	 N/A
