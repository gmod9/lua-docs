# Lua Reference

## Player-related
`_PlayerShowScoreboard(playerid)` - Shows the scoreboard on the specified players screen.  
`_PlayerSetSprint(playerid, bool)` - Enable/Disable sprint for player.  
`_PlayerFreeze(playerid, bool)` - Freeze the specified player.  
`_PlayerGetShootPos(playerid)` - Returns the vector of the player's shoot position.  
`_PlayerGetShootAng(playerid)` - Returns the forward vector of the player's shoot angle.  
`_PlayerGetActiveWeapon(playerid)` - Returns the player's active weapon id.  
`_PlayerKill(playerid)` - Kill the specified player.  
`_PlayerGiveAmmo(playerid, amount, ammotype, playsounds)` - Give specified player ammo. `playersounds` is bool.  
`_PlayerRespawn(playerid)` - Force player to respawn.  
`_PlayerSetDrawTeamCircle(playerid, bool)` - Sets whether to draw the team circle or not.  
`_PlayerInfo(playerid, request)` - Returns info about a specific layer. Check _PlayerInfo page for usage.  
`_PlayerChangeTeam(playerid, teamid)` - Changes a player's team.  
`_PlayerSetModel(playerid, model)` - Changes a player's model.  
`_PlayerGetRandomAllowedModel()` - Returns a random allowed player model.
`_PlayerSetHealth(playerid, health)` - Changes a player's health.  
`_PlayerSetArmor(playerid, armor)` - Changes a player's armor.  
`_PlayerSetMaxSpeed(playerid, speed)` - Changes a player's maximum speed.  
`_PlayerAddScore(playerid, score)` - Add to players score (can be minus).  
`_PlayerSetScore(playerid, score)` - Sets to players score.  
`_PlayerAddDeath(playerid, score)` - Add to players deaths score (can be minus).  
`_PlayerGiveItem(playerid, item)` - Give player named item.  
`_PlayerGiveSWEP(playerid, script)` - Give player scripted weapon.  
`_PlayerRemoveAllWeapons(playerid)` - Strip all o a player's weapons.  
`_PlayerRemoveWeapon(playerid, item)` - Strip a specific weapon.  
`_PlayerAllowDecalPaint(playerid)` - Allow the player to spraypaint now rather than waiting the 30 or so seconds.  
`_PlayerSetDrawViewModel(playerid, bool)` - Sets whether to draw the player's view model.  
`_PlayerSelectWeapon(playerid, item)` - Select weapon.  
`_PlayerSetDrawWorldModel(playerid, bool)` - Sets whether to draw the player's world model.  
`_PlayerOption(playerid, callback, timeout)` - Player has an option to select.  
`_PlayerSetVecView(playerid, vector)` - Sets the position of the view vector (0, 0, 64) default.  
`_PlayerIsKeyDown(playerid, key)` - Check whether specified key is pressed.  
`_PlayerSpectatorStart(playerid, mode)` - Stop spectating mode.  
`_PlayerSpectatorTarget(playerid, target)` - Set Spectator target for player.  
`_PlayerSpectatorEnd(playerid)` - Stop spectating mode.  
`_PlayerSetVecDuck(playerid, vector)` - Sets the position of the duck view vector (0, 0, 24) default.  
`_ScreenText(playerid, message, x, y, r, g, b, a, fadeid, fadeout, holdtime, effect, channel)` - Advanced function to print text to the screen. `effect` can be set to 0-2 and `channel` 0-5.  
`_PrintMessage(playerid, type, message)` - Print a message to a specific player.  
`_PrintMessageAll()` - Is like `_PrintMessage()` but for everyone on the server.  
`_PlayerPreferredModel(playerid)` - Returns the player's preferred model. Returns a blank if the model isn't valid.  
`_PlayerSilentKill(playerid, respawn_time, dissolve)` - Silently kill a player.  
`_PlayerDetonateTripmines(playerid)`  
`_PlayerHolsterWeapon(playerid)`  
`_PlayerSetFOV(playerid, fov, time)`  
`_PlayerSetFlashlight(playerid, state)`  
`_PlayerStopZooming(playerid)`  
`_PlayerSetChaseCamDistance(playerid, distance)`  
`_PlayerLockInPlace(playerid, bool)`  
`_PlayerRemoveAllAmmo(playerid)`  
`_PlayerDisableAttack(playerid, bool)`  
`_PlayerShowCrosshair(playerid, bool)`  
`_PlayerEnableSprint(playerid, bool)`  
`_PlayerViewModelSequence(playerid, sequence)` - If successful returns the length of the sequence in seconds.  
`_PlayerGetLimit(playerid, limit)`  
`_PlayerSetAnimation(playerid, sequence)` - Sets a player's animation.  
`_PlayerSetWeaponSequence(player, sequence)` - Sets a players weapon activity.  
`_PlayerIsCrouching(playerid)` - Returns true if a player is crouching.  
`_PlayerUseVehicle(playerid, vehicle)` - Make a player attempt to enter a vehicle.  
`_PlayerGod(playerid, bool)` - Give a player God Mode.  
`_PlayerHasWeapon(playerid, item)` - Returns true if the player has this weapon.  
`_PlayerWeaponTranslateSequence(player, sequence)` - Let the player's weapon decide how we should act out specific sequence.  
`_player.ShowPanel` - Show/Hide a panel by name.  
`_player.SetContextMenu(playerid, name)` - Set the player's context menu.  
`_player.GetFlashlight(player)` - returns true if flashlight is on.  
`_player.SetFlashlight(player, on)` - Set player FL on/off.  
`_player.LastHitGroup(player)` - Get the las place the player was hit.  
`_player.ShouldDropWeapon(player, bool)` - Should player drop weapon on death?  


## Entity-related
`_EntSetMaterial(entid, material_filename)` - Set the material of specified entity.  
`_EntSetGravity(entid, gravity)` - Set the gravity for specified entity.  
`_EntGetType(entid)` - Returns a entity type name.  
`_EntGetByName(name)` - Returns an entity by target name (0 if not found).  
`_EntGetPos(entid)` - Returns a vector representing the position of the entity.  
`_EntEmitSound(entid, filename)` - Make entity emit sound.  
`_EntEmitSoundEx(entid, filename, volume_multiplier, pitch_multiplier)` - Make entity emit sound.  
`_EntSetPos(entid, vector3 pos)` - Sets the position of the entity.  
`_EntGetVelocity(entid)` - Gets the entity velocity. Returned as a vector3.  
`_EntSetVelocity(entid, vector3_velocity)` - Sets the velocity of the entity.  
`_EntGetForwardVector(entid)` - Returns the forward vector.  
`_EntGetRightVector(entid)` - Returns the right vector.  
`_EntGetUpVector(entid)` - Returns the up vector.  
`_EntFire(entid, action, value, delay)` - ent_fire an entity.  
`_EntCreate(entname)` - Creates but doesn't spawn specified entity.  
`_EntSpawn(entindex)` - Spawns specified entity.  
`_EntActivate(entindex)` - Activate an entity.  
`_EntSetKeyValue(entindex, string_keyname, string_keyvalue)` - Sets an entity keyvalue (Must be done before spawning!).  
`_EntSetModel(ent, model_name)` - Sets the model of an entity. PRE-CACHE THE MODEL FIRST.  
`_EntSetOwner(ent, ownerid)` - Sets the owner.  
`_EntGetOwner(ent)` - Gets the entity's owner.  
`_EntRemove(entindex)` - Removes entity..  
`_EntExists(entindex)` - Check if entity exists.  
`_EntPrecacheModel(model_name)` - Pre-caches a model.  
`_EntSetAng(entid, vector3_ang)` - Sets the angle of the entity (using a forward vector).  
`_EntSetAngAngle(entid, vector3_angle)` - Sets the ANGLE of the entity.  
`_EntGetAng(entid)` - Returns the angle as a normalized 'forward' vector.  
`_EntGetAngAngle(entid)` - Returns the angle as a vector3.  
`_EntGetModel(entid)` - Returns the entity's model name.  
`_EntitiesFindByClass(classname)` - Returns a table of entities (or nil if none).  
`_EntitiesFindInSphere(vector_position, radius)` - Returns a table of entities contained in the sphere.  
`_EntitiesFindByName(targetname)` - Returns a table of entities (or nil if none).  
`_EntityGetPhysicsAttacker(entity)` - Returns the last physics attacker.  
`_EntitySetPhyscsAttacker(entity, attacker)` - Sets the physics attacker on a specified object.  
`_EntSetGroundEntity(entity, groundentity)` - Pass entity as -1 to clear the ground entity.  
`_EntGetGroundEntity(entity, groundentity)` - Pass entity as -1 to clear the ground entity.  
`_EntSetMoveType(entity, type)` - Sets the movetype.  
`_EntGetMoveType(entity)` - Gets the movetype.  
`_EntSetMoveCollide(entity, type)` - Sets the movecollide.  
`_EntGetMoveCllide(entity)` - Gets the movecollide.  
`_EntSetSolid(entity, type)` - Sets the solid type.  
`_EntGetSolid(entity)` - Gets the solid type.  
`_EntSetCollisionGroup(entity, group)` - Sets the collision group.  
`_EntGetCollisionGroup(entity)` - Gets the collision group.  
`_EntGetWaterLevel(entity)` - Returns a number representing how under water an entity is. 0 means not underwater. 3 is totally underwater.  
`_EntSetActivity(entid, int_sequence)` - Sets anactivity for an ent. Works for NPC's only.  
`_EntGetDisposition(npc, entity)` - Gets an enemy disposition.  
`_EntSetParent(entid, parent, attachment)` - Sets an entities parent.  
`_EntGetParent(entid)` - Gets an entities parent.  
`_EntGetName(entid)` - Gets an entities name.  
`_EntSetName(entid, name)` - Sets an entities name.  
`_EntSetMaxHealth(entid, health)` - Gets entity max health.  
`_EntGetMaxHealth(entid)` - Sets entity max health.  


## Effects-related
`_EffectInit()` - Resets the effect data  
`_EffectSetOrigin(vector)`  
`_EffectSetAngles(vector)`  
`_EffectSetNormal(vector)`  
`_EffectSetStart(vector)`  
`_EffectSetEnt(entid)`  
`_EffectSetFlags(int)`  
`_EffectSetScale(float)`  
`_EffectSetMagnitude(float)`  
`_EffectSetRadius(float)`  
`_EffectSetAttachIndex(int)`  
`_EffectDispatch(name)`  

## File manipulation
`_file.Exists(filename)` - Returns true if file exists.  
`_file.Read(filename)` - Reads a file into a string.  
`_file.Write(filename, string)` - Writes a string to a file.  
`_file.CreateDir(folder)` - Creates Dir Hierarchy.  
`_file.IsDir(folder)` - Returns true if is Dir.  
`_file.Find(wildcard)` - Finds files, returns table, parameter should be like "maps/-.bsp".  
`_file.Delete(wildcard)` - Deletes specified file.  
`_file.Rename(before, after)` - Renames specified file.  
`_ForceFileConsistency(filename)` - Force the file tobe the same on client and server. Should be called after pre-caching the file.  

## Server-related
`_StartNextLevel(map_name)` - Starts the next level.  
`_GetNextMap()` - Returns next map name.  
`_GetCurrentMap()` - Returns current map name.  
`_GetRule(rule_string)` - Gets a rule.  
`_ServerCommand(command)` - Runs a console command. Don't forget to put `\n` in the end.  
`_GameSetTargetIDRules(int_rule)` - Sets targetID rules.  
`_PluginMsg(userid, title, message, time, r, g, b, a, level)` - Sends a plugin message.  
`_PluginText(userid, title, message, time, r, g, b, a, level)` - Sends plug in text.  
`_GetConVar_Float(name)` - Get a server convar float.  
`_GetConVar_String(name)` - Get a server convar string.  
`_GetConVar_Bool(name)` - Get a server convar bool.  
`_GetClientConVar_String(userid, name)` - Get a client convar string.  
`_CurTime()` - Returns the current time in seconds.  
`_MaxPlayers()` - Returns the max players in the server.  
`_RunString(command)` - Runs a command in the main gameplay script.  
`_GetModPath()` - Gets the path to the gmod folder (on the server). No trailing slash.  
`_IsDedicatedServer()` - Returns whether dedicated server or not.  
`_Msg(message)` - Outputs message to console.  
`_OpenScript(filename)` - Opens a script.  
`_ALERT(message)` - Internal Lua usage. Outputs error message.  



## Trace
`_TraceAttack(victim, inflictor, attacker, amount)` - Attack using the last trace.  
`_TraceSetCollisionGroup(group)` - Sets the collision group for the next trace to use. 
`_TraceSetMask(group)` - Sets the MASK_ to use for the next trace.  
`_TraceLine(vector_start, vector_direction, length, ignore)` - Traces a line. `ignore` is optional.  
`_TraceEndPos()` - Return the end pos from the last trace.  
`_TraceFraction()` - Return the fraction of trace completed.  
`_TraceHitWorld()` - Return the true if the last trace hit the world.  
`_TraceHitNonWorld()` - Return the true if the last trace hit non world.  
`_TraceHit()` - Return the true if the last trace hit something.  
`_TraceGetEnt()` - Return the entity that the last trace hit.  
`_TraceGetSurfaceNormal` - Return the normal of the surface that the trace hit.  
`_TraceDidHitSky()` - Returns true if last hit was the sky.  
`_TraceDidHitHitbox()` - Returns true if last hit was some kind of hitbox.  
`_TraceGetTexture()` - Returns the name of the texture that we hit.  
`_TraceDidHitWater()` - Returns true if we hit water.  
`_MakeDecal(decal)` - Makes a decal using the last trace.  
`PlayerLookTrace(playerid, length)` - Traces a line where player's looking  

## Sounds
`_PlaySound(sound_name)` - Play a sound.  
`_PlaySoundPlayer(playerid, sound_name)` - Play a sound to a specific player.  

## GModText
`_GModText_Start(font_name)` -  Initialize the text.  
`_GModText_SetPos(x, y)` -  Set Position.  
`_GModText_AllowOffscreen(bool)` -  Allow the text to go offscreen.  
`_GModText_SetEntity(entindex)` -  Set entity to hover over.  
`_GModText_SetColor(r, g, b, a)` -  Set Colour.  
`_GModText_SetTime(duration, fadein, fadeout)` -  Set Times.  
`_GModText_SetDelay(delay)` -  Set delay time.  
`_GModText_SetText(text)` -  Set Times.  
`_GModText_SetAdditive(bool)` -  Set Additive mode.  
`_GModText_SetEntityOffset(vector)` -  Set entity offset to draw the text at.  
`_GModText_Send(player, index)` -  If player is 0 it is sent to everyone. Index says which slot this text should fill.  
`_GModText_Hide(player, index, fade_time, delay)` -  Hides specified text.  
`_GModText_HideAll(player)` -  Hides All texts.  
`_GModText_SendAnimate(player, index, length, ease)` -  The same as normal send but will animate from Send to the new values.  

## GModRect
`_GModRect_Start(material)` -  Initialize the rect.  
`_GModRect_SetPos(x, y, width, height)` -  Set Position.  
`_GModRect_SetEntity(entindex)` -  Set entity to hover over.  
`_GModRect_SetColor(r, g, b, a)` -  Set Colour.  
`_GModRect_SetTime(duration, fadein, fadeout)`-  Set Times.  
`_GModRect_SetDelay(delay)` -  Set delay time.  
`_GModRect_SetAdditive(bool)` -  Set Additive mode.  
`_GModRect_SetEntityOffset(vector)` -  Set entity offset to draw the text at.  
`_GModRect_Send(player, index)` -  If player is 0 it is sent to everyone. Index says which slot this text should fill.  
`_GModRect_SendAnimate(player, index, length, ease)` -  If player is 0 it is sent to everyone. Index says which slot this text should fill.  
`_GModRect_Hide(player, index, fade_time, delay)` -  Hides specified rect.  
`_GModRect_HideAll(player)` - Hides All rects.  

## GModQuad
`_GModQuad_Hide(player, index, fade_time, delay)` -  Hides specified world quads.  
`_GModQuad_HideAll(player)` -  Hides All world quads.  
`_GModQuad_Start(material)` -  Initialize the quad.  
`_GModQuad_SetVector(corner, vector)` -  Set a vector of one of the quad's corners. Acceptable `corner` values: 0-3.  
`_GModQuad_SetTimings(delay, fadein, life, fadeout)` -  Set Timings.  
`_GModQuad_SetEntity(entityid)` -  SetEntity to follow.  
`_GModQuad_Send(player, index)` -  Send a quad to player. All players if player is 0.  
`_GModQuad_SenAnimate(player, index, length, ease)` -  Send a quad to player. All players if player is 0.  

## Game Events
`_gameevent.Start(name)` - Starts a (fake) gameevent.  
`_gameevent.SetString(name, value)` - Set Variable.  
`_gameevent.SetInt(name, value)` - Set Variable.  
`_gameevent.Fire()` - Fire event.  

## Spawnmenu
`_spawnmenu.AddItem(playerid, category, name, modelent)`  
`_spawnmenu.RemoveCategory(playerid, category)`  
`_spawnmenu.RemoveAll(playerid)`  
`_spawnmenu.SetCategory(playerid, category)`  

## NPC-related
`_SetDefaultRelationship(class, class, disposition)` -  Sets the default relationship between two life types.  
`_npc.ExitScriptedSequence(ent)`  
`_npc.SetSchedule(end, sched)`  
`_npc.SetLastPosition(ent, vector)`  
`_npc.AddRelationship(ent, ent, disposition, priority)` - `priority` is int  

## Physics-related
`_phys.EnableMotion(entid, boo)` - Enable/Disable motion.  
`_phys.EnableDrag(entid, bool)` - Enable/Disable drag.  
`_phys.EnableGravity(entid, bool)` - Enable/Disable gravity.  
`_phys.EnableCollisions(entid, bool)` - Enable/Disable Collisions.  
`_phys.GetMass(entid)` - Gets mass.  
`_phys.SetMass(entid, mass)` - Sets mass.  
`_phys.Sleep(entid)` - Make object sleep.  
`_phys.Wake(entid)` - Wake a sleeping object.  
`_phys.IsAsleep(entid)` - Check whatever object is rested.  
`_phys.HasPhysics(entid)` - Returns true if entity has a physics object.  
`_phys.ConstraintSetEnts(constraint, entity_1, entity_2)` - Set Entities for constraint.  
`_phys.ApplyForceCenter(entid, force)` - Pushes an object from the center. `force` is vector3.  
`_phys.ApplyForceOffset(entid, force, worldpos)` - Pushes an object from the center. `force` and `worldpos` are vector3.  
`_phys.ApplyTorqueCenter(entid, force)` - Apply torque to the object. `force` is vector3.  


## Team-related
`_TeamAddScore(teamid, score)` - Add score for a team.  
`_TeamSetScore(teamid, score)` - Set score for a team.  
`_TeamNumPlayers(teamid)` - Get the number of players on a team.  
`_TeamCount()` - Returns the number of teams
`_TeamScore(teamid)` - Returns the total team score.  
`_TeamSetName(teamid, name)` - Sets the name of the team.  


## Utilities
`_util.PlayerByName(name)` - Returns playerid of player with name.  
`_util.PlayerByUserId(userid)` - Returns playerid.  
`_util.EntsInBox(min, max)` - Returns entities contained in a box. `min` and `max` are vectors.  
`_util.DropToFloor(ent)` - Drops entity to floor.  
`_util.ScreenShake(pos, amp, frequency, duration, radius)` - Shakes screen.  
`_util.PointAtEntity(ent1, ent2)` - Point one entity towards the other.  


## SWEP-related
All these function are only used when making SWEPs, check SWEP part.  
`_WeaponScriptedAssign(weapon, script)` Assign a script to a scripted weapon.  
`_SWEPSetSound(weapon_index, action, sound)` Sets SWEP sound.  
`_SWEPUseAmmo(weapon_index, clip[0|1], amount)` Takes ammo from SWEP gun.  
`_SWEPUpdateVariables(weapon_index)` Re-reads all the 'fetch' variables. You should call this if you have changed the accuracy etc.  
`_SWEPRunString(weapon_index, string)` Runs a Lua string in the weapon's Lua instance.  
`_swep.GetClipAmmo(weapon_id, clip[0|1])` Get amount of ammo in a clip.  
`_swep.SetClipAmmo(weapon_index, clip[0|1], clip)` Get amount of ammo in a clip.  
`_swep.GetDeathIcon(weapon_index)` Gets death icon name.  


## Weapon-related
`_WeaponSetModel(weapon_name, model_type, model_name)` Sets weapon model.  
`_WeaponSetSlot(weapon_name, slot, pos)` - Sets weapon slot.  
`_WeaponSetSound(weapon_name action, sound)` - Sets weapon sound.  
`_WeaponSetFOV(weapon_name, fov)` - Sets a weapon's draw FOV.  
`_WeaponFlipHands(weapon_name, bool)` - Flips a weapon's hands.  
`_WeaponSetDamage(weapon_name, damage)` - Sets the damage that a bullet from this gun does.  
`_WeaponSetup(weapon_name, anim_prefix, clip_size_1, clip_size_2, default_ammo_1, default_ammo_2, primary_ammo, secondary_ammo)` - Sets animation prefix.  


## 'Deprecated'
`_IsLinux()` Would return true if running on a Linux server
