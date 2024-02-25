# RoState

# Overview

The Roblox State Framework is a modular system designed to help developers manage and organize game states within Roblox Studio projects. States are fundamental to controlling the flow and behavior of games, and this framework provides a flexible and efficient way to implement them.

## Features

Easy state management: Quickly switch between different game states.
Customizable state behaviors: Define unique actions and properties for each state.
Modular design: Add or remove states easily to suit your game's needs.
Event-driven architecture: Execute specific actions when entering or exiting states.

# Usage

## Setup
Import the StateFramework module into your Roblox Studio project.
Require the StateFramework module in your scripts where you need to manage states.
```lua
Copy code
local RoState = require(game:GetService("ReplicatedStorage"):WaitForChild("RoState"))
-- Initialize the state machine with the defined states
local NewState = RoState.new()
NewState:Set("Blue")
print(NewState:Get()) --Prints "Blue"
local Connection = NewState:Changed(function(newvalue)
    print("State Value Changed To: "..newvalue)
end)
State:Set(true) Prints "State Value Changed To: true"
Connection:Disconnect()
if NewState:Is(true) then
    print("NewState") --Prints
end


```
## Contributing


Contributions are welcome! If you have suggestions for improvements or new features, please submit a pull request or open an issue on GitHub.

### License

This project is licensed under the MIT License - see the LICENSE file for details.


