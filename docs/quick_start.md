# Quick Start

Add Slab to your Love 2D project with:
```lua
local Slab = require 'Slab'
```
In `love.load` initialise the library and set a background colour:
```lua
function love.load(args)
    love.graphics.setBackgroundColor(0.4, 0.88, 1.0)
    Slab.Initialize(args)
end
```
Create and render windows inside `love.update`:
```lua
function love.update(dt)
    Slab.Update(dt)
    Slab.BeginWindow('MyFirstWindow', {Title = 'My First Window'})
    Slab.Text('Hello World')
    Slab.EndWindow()
end
```
Finally call `Slab.Draw()` from `love.draw`:
```lua
function love.draw()
    Slab.Draw()
end
```
See [main.lua](../main.lua) for a full demo.
