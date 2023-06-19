# Events
## Description
In short, events are functions that get called when a certan thing happens, like when a player is joining or they get killed.

## Syntax
### `HookEvent()`  
**Arguments:**  
- `name` - Event type. Type: `string`  
- `func` - Function that will be executed on event. Type: `function`  
**Returns:**  
- `id` - ID of the hook used for unhooking. Type: `number`  

### `UnHookEvent()`  
**Arguments:**  
- `id` - ID of the hook. Type: `number`  
**Returns:**  
Nothing  

## Events
### `eventPlayerActive(name, userid, steamid)`
### `eventPlayerConnect(name, address, steamid)`
### `eventPlayerDisconnect(name, userid, address, steamid, reason)`
### `eventPlayerChangeTeam(name, userid, new_team, old_team)`
### `eventPlayerKilled(userid, attacker, weapon)`
### `eventPlayerNameChange(userid, newname, oldname)`
### `eventPlayerHurt(userid, newhealth, attacker)` - When `newhealth` is `1`, the player will die unless you update their health using `_PlayerSetHealth()`
### `PickDefaultSpawnTeam(userid)` - Return `false` to choose a random valid team
### `eventPlayerSpawn(userid)`
### `eventPlayerSpawnProp(userid, propname)` - Return `true` to allow
### `eventPlayerDuplicateProp(userid, propid)` - Return `true` to allow
### `eventPlayerSpawnRagdoll(userid, propname)` - Return `true` to allow
### `eventPlayerDuplicateRagdoll(userid, propid)` - Return `true` to allow
### `eventPlayerPropSpawned(userid, propid)`
### `eventPlayerRagdollSpawned(userid, propid)`
### `eventPlayerSay(userid, strText, bTeam)` - Player will 'say' returned text if it's not empty
### `eventPropBreak(breakerid, propid)`
### `eventNPCKilled(killerid, killed, inflictor)`
### `canPlayerHaveItem(playerid, item)` - Return `true` if the player can pickup item
### `eventPlayerUseEntity(playerid, entity)` - Return `true` to disable default actions
### `eventPlayerInitialSpawn(playerid)`
### `eventKeyPressed(playerid, in_key)`
### `eventKeyReleased(playerid, in_key)`
### `OnBalloonExplode(balloon, killer)`
### `onPhysTakeDamage(entid, inflictor, attacker)`
### `onTakeDamage(entid, inflictor, attacker, damage)`
### `onPlayerRemove(playerid, entity)` - Return `true` if player can delete specified entity
### `onGravGunPunt(playerid, entity)` - Return `true` to allow
### `onGravGunPickup(playerid, entity)` - Return `true` to allow
### `onGravGunLaunch(playerid, entity)` - Return `true` to allow
### `onGravGunDrop(playerid, entity)` - Return `true` to allow
### `onPhysPickup(playerid, entity) - Return `true` to allow
### `onPhysFreeze(playerid, entity) - Return `true` to allow
### `onPhysDrop(player, entity)` - Return `true` to allow
### `GetPlayerDamageScale(hitgroup)` - Is set to `1` by default
### `onShowHelp(userid)` - By default bound to F1
### `onShowTeam(userid)` - By default bound to F2
### `onShowSpare1(userid)` - By default bound to F3
### `onShowSpare2(userid)` - By default bound to F4

## Examples
### Chat commands
```
-- This will unhook previous hook if executing another time
if chat_commands then
	UnHookEvent(chat_commands.hook)
end

chat_commands = {
	prefix = "!",
	commands = {
		help = function(playerid, args)
			_PrintMessage(playerid, HUD_PRINTTALK, "Available Chat Commands")
			for command, _ in pairs(chat_commands.commands) do
				_PrintMessage(playerid, HUD_PRINTTALK, chat_commands.prefix .. command)
			end
		end,
		argtest = function(playerid, args)
			_PrintMessage(playerid, HUD_PRINTTALK, "Here are your arguments:")
			for index, arg in pairs(args) do
				_PrintMessage(playerid, HUD_PRINTTALK, "[" .. index .. "] " .. arg)
			end
		end,
		kill = function(playerid, args)
			_PlayerKill(playerid)
		end,
		yeet = function(playerid, args)
			_EntSetVelocity(playerid, vector3(0, 0, 999999999))
		end
	}
}

chat_commands.hook = HookEvent("eventPlayerSay", function(playerid, message, _)
	-- For some reason, `message` also contains player's name, so we remove it. Also, space **MUST** be always present, check next comment for more details
	message = string.gsub(message, _PlayerInfo(playerid, "name") .. ": ", "") .. " "
	if string.sub(message, 1, 1) == chat_commands.prefix then
		local key = string.sub(message, 2, string.find(message, " ") - 1)
		if chat_commands.commands[key] then
			message = string.sub(message, string.find(message, " "), string.len(message))
			local args = {}
			for arg in string.gfind(message, "(%w+)") do
				table.insert(args, arg)
			end
			chat_commands.commands[key](playerid, args)
		end
	end
end)
```
