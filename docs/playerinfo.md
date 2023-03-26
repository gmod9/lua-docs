# _PlayerInfo()

## Description
`_PlayerInfo()` is used, as it's name suggests, for getting player's information.

## Syntax
### `_PlayerInfo()`  
**Arguments:**  
- `playerid` - ID of the player. Type: `number`  
- `request` - Requested variable. Type: `string`  
**Returns:**
- `state` - State of `request` for specified player. Returns `<Not Found>` if a request wasn't implemented. Type: depends on `request`

## Requests
Here's a list of every known `request` parameter:  
- `connected` - `true` if connected. Type: `boolean`  
- `health` - Player's health. Type: `number`  
- `armor` - Player's armor. Type: `number`  
- `alive` - `true` if alive. Type: `boolean`  
- `kills` - Player's kills. Type: `number`  
- `networkid` - Player's SteamID. Type: `string`  
- `deaths` - Player's deaths. Type: `number`  
- `packetloss` - Player's packet loss. Type: `number`  
- `ping` - Player's ping. Type: `number`  
*Thanks to mv#7803 for figuring out more requests*

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
