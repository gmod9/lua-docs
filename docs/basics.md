# Basics
To mod GMod9 you need a basic understanding
of Lua language. Lua is one of the easiest
languages to learn. Here are basic things you
need to know if you are starting with Lua:

- Scripts end with .lua extension
- You can use any text editor to write Lua code
- You don't need to compile anything
- To load the script on the fly, use `lua_openscript` console command
- Puting your script in `lua/init` folder will make it load every time
- `;` are optional
- In `if` statements `()` are optional if not working with multiple things

You can find full Lua documentation here: <https://www.lua.org/manual/5.1/>  
*Note that GMod9 uses Lua 5.0 while documentation is only available for 5.1+, so some things might not exist*

And here's how you do basic stuff:

### Defining a function
```
function SayMyName(name)
	Msg("Your Name Is " .. name)
end
```

### Calling a function
```
SayMyName("garry")
```

### Commenting
```
-- Calling the function boss.
SayMyName("garry")
-- Called the function boss.
```

### If statement
```
if name == "garry" then
	SayMyName("garry")
end

if name == "MingeBag" then
	SayMyName("MingeBag")
end

if name ~= "garry" then
	SayMyName("NOT garry or MingeBag")
end

-- or

if name == "garry" then
	SayMyName("garry")
elseif name == "MingeBag" then
	SayMyName("MingeBag")
else
	SayMyName("NOT garry or MingeBag")
end
```

### For statements
```
for i = 0, 32 do
	Msg("Number " .. i)
end
```

### Variables
```
-- Locals only exist within the function in which they're defined
-- If you don't declare a variable as local it will exist globally by default

local name = "garry"


-- Tables are like arrays, they must be declared like so

PlayerNames = {}


-- and then you can fill them up like so

PlayerNames[0] = "david"
PlayerNames[1] = "andrew"

Msg( "Player 0's name is " .. PlayerNames[0] )


-- The index doesn't have to be a number

PlayerNames["test"] = "superdood";

Msg( "Player's name is " .. PlayerNames["test"] )
-- or
Msg( "Player's name is " .. PlayerNames.test )


-- Variables aren't a set type and can hold anything

Players = {}

Players[0] = {}
Players[0].name = "Garry"
Players[0].money = 1000
Players[0].age = 32


-- They can even hold functions since they're a legitimate variable type

function SayHello( )

     Msg ( "Hello" )

end

-- If we used SayHello() we would save the output the function instead of it
Players[0].intro = SayHello

Players[0].intro()


-- which means you can also pass them to functions

function SayPlayerHello ( in_function )

     in_function()

end

SayPlayerHello( Players[0].intro )

```

### Iterating over items in tables
```
local money = {
	garry = 999,
	nafrayu = 69,
	mingebag = 0
}

for name, amount in pairs(money) do
	Msg(name .. " has $" .. amount)
end
```

