# [Container](https://github.com/RbxscrIptConnectinG/Container)
such a way - such a shame.

heyaaa..
as you can see.
Container moved from [UselessStuff](https://github.com/RbxscrIptConnectinG/UselessStuff) to its own repository

there's many reasons why, for example:
1. hi.
2. maybe publishing it to.. *GULP* [wally](https://wally.run/)..

# API

# new Container
```lua
    Container.new(preAddTable: { [any]: any} ) -> ContainerType
```

# Add
Adds value with or without custom index ( #table+1 used as index if customIndex is nil )
```lua
    -- NewContainer.Add -> (self, any, any) -> (any, any)
    NewContainer:Add(
        value : any, 
        customIndex : any | nil
    ) 
    -> 
    (
        value : any,
        newOrCustomIndex : any | number
    )
```

# Remove
Just removes value from table
```lua
    -- NewContainer.Remove -> (self, ...any) -> nil
    NewContainer:Remove(...indexes) -> nil
```

# RemoveAndDestroy
The evil twin of **Remove**, it not only removes a value from the table, but also destroys it if it can do so.
```lua
    -- NewContainer.RemoveAndDestroy -> (self, ...any) -> nil
    NewContainer:RemoveAndDestroy(...indexes) -> nil
```

# RemoveAllIn
**Remove** but does job to everything in selected table
```lua
    -- NewContainer.RemoveAllIn -> (self, string) -> nil
    NewContainer:RemoveAllIn(locationName: "Connections" | "Any" | "Both") -> nil
```

# RemoveAndDestroyAllIn
The evil twin of **RemoveAllIn** blah blah... you know the drill.
```lua
    -- NewContainer.RemoveAndDestroyAllIn -> (self, string) -> nil
    NewContainer:RemoveAndDestroyAllIn(locationName: "Connections" | "Any" | "Both") -> nil
```

# GetPlainTable
returns plain table.
```lua
    -- NewContainer.GetPlainTable -> (self, string) -> nil
    NewContainer:GetPlainTable(locationName: "Connections" | "Any" | "Both") -> { [any]: any }
```

*unlisted LocationNames: "YieldedThreads","All"*

# IsIt
Type checking. stupid...
```lua
    -- NewContainer.IsIt -> (self, any, string) -> boolean
    NewContainer:IsIt(index: any, type: string) -> boolean
```

# IsItIn
checks if index is in certain table, then gives boolean (is it found) and value
```lua
    -- NewContainer.IsItIn -> (self, any, string) -> (boolean, any)
    NewContainer:IsItIn(index: any, locationName: "Connections" | "Any") -> (boolean, any)
```

# Set
replaces index with same index but with different value
```lua
    -- NewContainer.Set -> (self, any, any, boolean) -> (any, any, any | nil, any | nil)
    NewContainer:Set(index: any, value: any, destroyOldValue: boolean) -> (newValue, newIndex, oldIndex, oldValue)
```

# Get
Get values from indexes
```lua
    -- NewContainer.Get -> (self, ...any) -> (...any)
    NewContainer:Get(...indexes) -> (...values)
```

# Validate
Checks if index exists
```lua
    -- NewContainer.Validate -> (self, ...any) -> (...any)
    NewContainer:Validate(...indexes) -> (...booleans)
```

# WaitFor
Waiting for certain index to be added.
```lua
    -- NewContainer.WaitFor -> (self, any) -> (any, any)
    NewContainer:WaitFor(index: any) -> (index: any, value: any)
```

# Destroy
Activates SemiDestroy functions and clears self
```lua
    -- NewContainer.Destroy -> (self) -> nil
    NewContainer:Destroy() -> nil
```

# Shortcut functions

# DisconnectAll
RemoveAndDestroyAllIn("Connections")
```lua
    -- NewContainer.DisconnectAll -> (self) -> nil
    NewContainer:DisconnectAll()
```

# DestroyAllAny
RemoveAndDestroyAllIn("Any")
```lua
    -- NewContainer.DestroyAllAny -> (self) -> nil
    NewContainer:DestroyAllAny()
```

# SemiDestroy
RemoveAndDestroyAllIn("All")
```lua
    -- NewContainer.SemiDestroy -> (self) -> nil
    NewContainer:SemiDestroy()
```
