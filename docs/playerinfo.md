# _PlayerInfo()

## Description
`_PlayerInfo()` is used, as it's name suggests, for getting player's information.

## Syntax
### `_PlayerInfo()`  
**Arguments:**  
- `playerid` - ID of the player. Type: `number`  
- `request` - Requested variable. Type: `string`  
**Returns:**
- `state` - State of `request` for specified player. Type: depends on `request`

## Requests
Here's a list of every known `request` parameter:  
- `connected`: returns if connected, type: `boolean`  
- `health`: returns player's health, type: `number`  
- `armor`: returns player's armor, type: `number`
- `alive`: returns `true` if player is alive, type: `boolean`
- `kills`: player's kills, type: `number`

## Examples
### Healthy spam
```
function loop()
	for playerid = 1, _MaxPlayers() do
		if _PlayerInfo(playerid, "connected") == true then
			_PrintMessageAll(HUD_PRINTCONSOLE, _PlayerInfo(playerid, "name") .. "'s Health is " .. tostring(_PlayerInfo(playerid, "health")) .. "%!")
		end
	end
end

AddTimer(1, 0, loop)
```
