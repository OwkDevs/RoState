<div align="center">
	<h1>RoState (In Dev)</h1>
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

## Example
```lua
local RoState = require(path.to.rostate)

-- Create a new RoState object, first argument is the starting value
local newState = RoState.new("Idle")

-- Creating a OnStateEnter connection
local StateEntered = newState:OnStateEnter("Walking",function(lastValue,newValue)
      if lastValue == "Idle" then
         print(`State changed from {lastValue} to {newValue}`
      end
end)

--Creating a Changed connection
local StateChanged = newState:Changed(function(lastValue,newValue)
      print("newState changed")
end)

newState:Set("Walking")
```
### Changing States

<details>
    <summary>Set State</summary>
    This function is used to set a state to any value.

```lua
local testState = RoState.new()

testState:set("OwkSoCool") -- Change the value of the state

print(testState) -- Prints OwkSoCool
```
</details>

### Connections

<details>
    <summary>Changed</summary>
    This connection is fired when a state is changed.

```lua
local testState = RoState.new()

local connection = testState:Changed(function(lastValue,newValue)
    print(`State value changed to: {newValue}`)
end)

connection:Disconnect() -- Disconnects the connection we made earlier
```
</details>

<details>
    <summary>OnStateEnter</summary>
    This connection is fired when a specific state is entered.

```lua
local testState = RoState.new()

local connection = testState:OnStateEnter(stateEntered,function(lastValue,newValue)
    print(`Entered the state: {newValue}`)
end)

connection:Disconnect() -- Disconnects the connection we made earlier
```
</details>

<details>
    <summary>OnStateExit</summary>
    This connection is fired when a specific state is exited.

```lua
local testState = RoState.new()

local connection = testState:OnStateExit(stateExited,function(lastValue,newValue)
    print(`Exited the state: {lastValue}`)
end)

connection:Disconnect() -- Disconnects the connection we made earlier
```
</details>


## Contributing


Contributions are welcome! If you have suggestions for improvements or new features, please submit a pull request or open an issue on GitHub.

### License

This project is licensed under the MIT License - see the LICENSE file for details.


