## Create Window
```lua
local Finity = loadstring(game:HttpGet("https://raw.githubusercontent.com/Auickcode/FinityLibNewLoadstring/refs/heads/main/FinityLib.lua"))()
local FinityWindow = Finity.new(true)
FinityWindow.ChangeToggleKey(Enum.KeyCode.Semicolon)
```

## Create Tab
```lua
local tab1 = FinityWindow:Category("Catching")
```

## Create Section
```lua
local tab1 = sec1:Sector("Magnets")
```

## Create Toggle
```lua
tab1:Cheat(
	"Customize Magnets", -- Type
	"Enable Magnets", -- Name
	function(State) -- Callback function
		print("Checkbox state changed:", State)
	end
)
```

## Create Slider
```lua
tab1:Cheat("Magnet Radius", "Catch Distance", function(Value)
	print("Silder value changed:", Value)
end, {min = 0, max = 25, suffix = " Radius"})
```
