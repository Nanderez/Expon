## Expon UI


`Creating Windows`
```lua
local Window = Expon.CreateWindow("My UI Library")
```

`Creating Tabs`
```lua
local Tab = Window.CreateTab("Home")
```

`Creating Buttons`
```lua
Tab.CreateButton("Print something", function()
	print("Hello world")
end)
```

`Creating Toggles`
```lua
Tab.CreateToggle("Bool", function(bool)
	print(bool)
end)
```

`Creating Dropdowns`
```lua
Tab.CreateDropdown("Workspace", game.Workspace:GetChildren(), function(value, index)
	print("["..tostring(index).."] = "..tostring(value))
end)
```

`Creating Custom Display Dropdowns`
```lua
local Table = {
  Test = {
    displayName = "Something"
  }
}

Tab.CreateDropdown("Workspace", game.Workspace:GetChildren(), function(value, index)
	print("["..tostring(index).."] = "..tostring(value))
end, "displayName")
```
