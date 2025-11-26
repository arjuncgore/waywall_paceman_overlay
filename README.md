# Waywall Paceman Overlay

A paceman statistics overlay for [Waywall](https://github.com/tesselslate/waywall)

---

## Installation
- Clone the repository into your waywall config folder
```bash
cd ~/.config/waywall
git clone https://github.com/arjuncgore/waywall_paceman_overlay.git
```

## Setup
### 1. Import the module

Add this line to your `init.lua` file

```lua
local pm_overlay = require("waywall_paceman_overlay.pm_overlay")
```

### 2. Change your username

Replace the placeholder "goreay" at the top of `pm_overlay.lua` with your own

## Customization
Edit these lines to your desired statistics and look.
```lua
-- ==== CONFIG ====
local username = "goreay"
local hours = 12
local hoursBetween = 1
local header = "PACEMAN STATS\n"

local look = {
    X = 300,
    Y = 1000,
    color = '#000000',
    bold = true,
    size = 3
}

local info = {
    { tag = "Nethers",           enabled = true,  key = "nether" },
    { tag = "Bastions",          enabled = true,  key = "bastion" },
    { tag = "Fortresses",        enabled = true,  key = "fortress" },
    { tag = "First Structures",  enabled = false, key = "first_structure" },
    { tag = "Second Structures", enabled = false, key = "second_structure" },
    { tag = "First Portals",     enabled = false, key = "first_portal" },
    { tag = "Strongholds",       enabled = false, key = "stronghold" },
    { tag = "End Enters",        enabled = false, key = "end" },
    { tag = "Completions",       enabled = false, key = "finish" },
}
```
IMPORTANT: Do not change or remove the key values in the info table. You may enable each split and/or change its tag to whatever you like.

---
## Preview
<p align="center">
  <img src="./preview.png" width="1000">
</p>
*Example of my personal wall with session statistics from paceman*

---

## Credits

- **Tesselslate** – creator of the original Waywall
- **Arsoniv** – inspired the origin of this overlay
- **Paceman Devs** - created the paceman tracker and api endpoints necessary https://github.com/PaceMan-MCSR
- **David Heiko Kolf and others** - creator of the json lua library https://github.com/LuaDist/dkjson

---
