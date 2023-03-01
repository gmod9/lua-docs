# Defines
## Description
Defines are variables used for giving human-readable names to things like animation IDs and such.

## Variables
### `HUD_PRINTNOTIFY`
**Description:** Works like `HUD_PRINTCONSOLE`, doesn't seem to do anything special.  
**Value**: `1`  
**Type:** `number`  
**For use with**: `_PrintMessage()`, `_PrintMessageAll()`  

### `HUD_PRINTCONSOLE`
**Description:** Prints string in console, like `_Msg()` but for players.  
**Value:** `2`  
**Type:** `number`  
**For use with:** `_PrintMessage()`, `_PrintMessageAll()`  

### `HUD_PRINTTALK`
**Description:** Prints string in chat, like chat message.  
**Value:** `3`  
**Type:** `number`  
**For use with:** `_PrintMessage()`, `_PrintMessageAll()`  

### `HUD_PRINTCENTER`
**Description:** Prints string in the middle of the screen.  
**Value:** `4`  
**Type:** `number`  
**For use with:** `_PrintMessage()`, `_PrintMessageAll()`  


### `DEFAULT_PLAYER_MODEL`
**Description:** Is a model of default player model.  
**Value:** `models/player.mdl`  
**Type:** `string`  
**For use with:** Anything  

### `TEAM_UNASSIGNED`
**Description:** Stores TeamID for the default team used when teamplay is disabled.  
**Value:** `0`  
**Type:** `number`  
**For use with:** `_PlayerChangeTeam()`  

### `TEAM_SPECTATOR`
**Description:** Stores TeamID for the unused spectator team. Joining this team will cause glitches.  
**Value:** `1`  
**Type:** `number`  
**For use with:** `_PlayerChangeTeam()`  

### `TEAM_BLUE`
**Description:** Stores TeamID for the Blue team.  
**Value:** `2`  
**Type:** `number`  
**For use with:** `_PlayerChangeTeam()`  

### `TEAM_YELLOW`
**Description:** Stores TeamID for the Yellow team.  
**Value:** `3`  
**Type:** `number`  
**For use with:** `_PlayerChangeTeam()`  

### `TEAM_GREEN`
**Description:** Stores TeamID for the Green team.  
**Value:** `4`  
**Type:** `number`  
**For use with:** `_PlayerChangeTeam()`  

### `TEAM_UNASSIGNED`
**Description:** Stores TeamID for default team used when teamplay is disabled  
**Value:** `5`  
**Type:** `number`  
**For use with:** `_PlayerChangeTeam()`  
