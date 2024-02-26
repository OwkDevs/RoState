# RoState

# Overview

RoState is a modular system designed to help developers manage and organize game states within Roblox Studio projects. States are fundamental to controlling the flow and behavior of games, and this framework provides a flexible and efficient way to implement them.

## Features

Easy state management: Quickly switch between different game states.
Customizable state behaviors: Define unique actions and properties for each state.
Modular design: Add or remove states easily to suit your game's needs.
Event-driven architecture: Execute specific actions when entering or exiting states.

# Usage

## Setup
Import the RoState module into your Roblox Studio project.
Require the RoState module in your scripts where you need to manage states.
```lua
local RoState = require(path.to.rostate)

-- Initialize the state machine with the defined states
local testState = RoState.new()

testState:Set("Blue")
print(testState:Get()) -- Blue

local connection = testState:Changed(function(newValue)
    print(`State value changed to: {newValue}`)
end)

testState:Set(1) -- outputs "State value changed to: true"
print(testState:Is(1)) -- prints true (Is function returns true/false)

connection:Disconnect() -- Disconnects the connection we made earlier
```
## Contributing


Contributions are welcome! If you have suggestions for improvements or new features, please submit a pull request or open an issue on GitHub.

### License

This project is licensed under the MIT License - see the LICENSE file for details.


