<div align="center">
	<h1>RoState</h1>
</div>

# Overview

RoState is a modular system designed to help developers manage and organize game states within Roblox Studio projects. States are fundamental to controlling the flow and behavior of games, and this framework provides a flexible and efficient way to implement them.

## Features

Easy state management: Quickly switch between different game states.
Customizable state behaviors: Define unique actions and properties for each state.
Modular design: Add or remove states easily to suit your game's needs.
Event-driven architecture: Execute specific actions when entering or exiting states.

<div align="center">
	<h1>Usage</h1>
</div>

## Setup
Import the RoState module into your Roblox Studio project.
Require the RoState module in your scripts where you need to manage states.
```lua
local RoState = require(path.to.rostate)

-- Initialize the state machine with the defined states
local testState = RoState.new() -- First Arg is starting state
```
### Changing States
```lua
local testState = RoState.new()

testState:set("OwkSoCool") -- Change the value of the state

print(testState) -- Prints OwkSoCool
```

### Connections

<details>
    <summary>Changed</summary>
    This connection is fired when a state is changed.


```lua
local testState = RoState.new()

local connection = testState:Changed(function(newValue)
    print(`State value changed to: {newValue}`)
end)

connection:Disconnect() -- Disconnects the connection we made earlier
```
</details>



## Contributing


Contributions are welcome! If you have suggestions for improvements or new features, please submit a pull request or open an issue on GitHub.

### License

This project is licensed under the MIT License - see the LICENSE file for details.


