# Timers

## Description
Timers are a way to make function run set amount of times every set amount of seconds  
To create a timer, use `AddTimer()` function. If you want to be able to stop a timer, you have to define a variable for storing timer's id. Then you can use `HaltTimer()`.  

## Syntax
### `AddTimer()`  
**Arguments:**  
`delay` - Controls after what time(in seconds) the function will be called again. Type: `number`  
`reps` - Controls amount of loops. Setting to `0` will result in an infinite loop. Type: `number`  
`func` - Is a function that will be called by timer. Type: `function`  
`...` - Additional arguments for `func`. Type: `any`  
**Returns:**  
`id` - ID of the timer. Type: `number`


### `HaltTimer()`  
**Arguments:**  
`timer` - ID of the timer you want to stop. Type: `number`  
**Returns:**  
Nothing

## Examples
### Spammy spam
```
function spam()
	_PrintMessageAll(HUD_PRINTTALK, "spammy spam")
end

-- Every 2 seconds, up to 5 times, spam function will be called
AddTimer(2, 5, spam)
```

### Virus
```
function virus()
	if _PlayerInfo(1, "health") > 0 then
		_PlayerSetHealth(1, _PlayerInfo(1, "health") - 1)
	elseif _PlayerInfo(1, "health") == 0 then
		-- We 'accidentally' killed player
		_PlayerKill(1)
		_PrintMessage(1, HUD_PRINTTALK, "Opps!")
		HaltTimer(timer)
	end
end

-- 0 means infinite loop
timer = AddTimer(0.01, 0, virus)
```

