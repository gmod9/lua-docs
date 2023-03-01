# Traces
## Description
Traces are invisible lines that can be used for stuff like checking if there's empty space in front of the player.

## Syntax
### `_TraceLine()`
**Arguments:**  
- `vector_start` - Start of line. Type: `vector`  
- `vector_direction` - Rotates the line. Type: `vector`  
- `length` - Length of the line. Type: `number`  
- `ignore` - EntID that will not be detected. Type: `number`  
**Returns:**  
Nothing  

### `PlayerLookTrace()`
**Arguments:**  
- `playerid` - PlayerID of player. Type: `number`  
- `length` - Length of the line. Type: `number`  
**Returns:**  
Nothing  

### `_TraceHit()`
**Arguments:**  
Nothing  
**Returns:**  
- `hit_something` - Is `true` if trace hit something. Type: `bool`  

### `_TraceHitWorld()`
**Arguments:**  
Nothing  
**Returns:**  
- `hit_world` - Is `true` if trace hit world geometry. Type: `bool`  

### `_TraceHitNonWorld()`
**Arguments:**  
Nothing  
**Returns:**  
- `hit_entity` - Is `true` if trace hit entity. Type: `bool`  

### `_TraceDidHitWater()`
**Arguments:**  
Nothing  
**Returns:**  
- `hit_water` - Is `true` if trace hit water. Type: `bool`  

### `_TraceDidHitHitbox()`
**Arguments:**  
Nothing  
**Returns:**  
- `hit_hitbox` - Is `true` if trace hit hitbox. Type: `bool`  


### `_TraceDidHitSky()`
**Arguments:**  
Nothing  
**Returns:**  
- `hit_sky` - Is `true` if trace hit skybox. Type: `bool`  

### `_TraceGetEnt()`
**Arguments:**  
Nothing
**Returns:**  
- `entid` - EntID of entity that was hit by trace. Returns `0` if no entity was found. Type: `number`  

### `_TraceGetTexture()`
**Arguments:**  
Nothing  
**Returns:**  
- `texture` - Texture of surface that was hit by trace. Returns `**studio**` if no geometry was hit. Type: `string`  

### `_TraceGetSurfaceNormal()`
**Arguments:**  
Nothing  
**Returns:**  
- `texture` - This is probably a normal map of the texture. Type: probably `string`  

### `_TraceFraction()`
**Arguments:**  
Nothing  
**Returns:**
- `percentage` - Percentage of trace length that something was detected at. Type: `number`  

### `_TraceEndPos()`
**Arguments:**  
Nothing  
**Returns:**
- `vector` - Vector with the end position of trace. Type: `vector`  

### `_TraceAttack()`
**Arguments:**  
- `victim` - EntID of target. Type: `number`  
- `inflictor` - EntID of damage inflictor. Type: `number`  
- `attacker` - EntID of attacker. Type: `number`  
- `amount` - Amount of damage. Type: `number`  
**Returns:**  
Nothing  

### `_TraceAttack()`
**Arguments:**  
- `victim` - EntID of target. Type: `number`  
- `inflictor` - EntID of damage inflictor. Type: `number`  
- `attacker` - EntID of attacker. Type: `number`  
- `amount` - Amount of damage. Type: `number`  
**Returns:**  
Nothing  

## Examples
### Laser sight
```
-- Thanks to Nafrayu for helping me understand this
function laser_sight()
	for id = 1, _MaxPlayers() do
		PlayerLookTrace(id, 2048)
		if _TraceHit() == true and _TraceHitNonWorld() == true then
			_TraceAttack(_TraceGetEnt(), id, id, 10)
		end
	end
end

AddTimer(0, 0, laser_sight)
```

### Bunny Hopping
```
```