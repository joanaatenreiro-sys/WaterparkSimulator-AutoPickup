# AutoPickup Mod for Waterpark Simulator

Automatically collects science flasks and money piles as soon as they appear in your park, so you never have to run over and pick them up manually.

---

## What it does

**Science flasks** — When a SmartGuy visitor drops a science flask in your park, the mod picks it up automatically and gives you the research XP straight away.

**Money piles** — When a Magnate visitor drops a money pile in your park, the mod collects it automatically.

Both happen in the background every few seconds. You will still see the items appear briefly before they are collected.

---

## Requirements

- **BepInEx 6 (IL2CPP build)** installed on Waterpark Simulator — e.g. via the ["BepInEx and MelonLoader" pack on Nexus Mods](https://www.nexusmods.com/waterparksimulator/mods/62)

---

## How to install

### Step 1 — Install BepInEx (skip if you already have it)

This mod requires **BepInEx 6 (IL2CPP build)**. The easiest way to get it set up for Waterpark Simulator is the ["BepInEx and MelonLoader" pack on Nexus Mods](https://www.nexusmods.com/waterparksimulator/mods/62):

1. Download the pack
2. Extract its contents directly into your Waterpark Simulator install folder, e.g.:
   ```
   Steam\steamapps\common\Waterpark Simulator\
   ```
3. Launch the game once and let it sit at the main menu for a minute or two — BepInEx needs this first launch to generate its IL2CPP interop assemblies. This step only needs to be done once.

### Step 2 — Install AutoPickup

1. Download **AutoPickup.dll**
2. Copy it into the `BepInEx\plugins` folder inside your Waterpark Simulator install folder:
   ```
   Steam\steamapps\common\Waterpark Simulator\BepInEx\plugins\
   ```
3. Launch the game — the mod loads automatically, no further setup needed

### Step 3 — Confirm it worked

Open `BepInEx\LogOutput.log` (in your game folder) and look for these lines near the start:
```
PlayerCharacter resolved.
Interact method confirmed for ScienceEssenseIntertactable
Interact method confirmed for MoneyPileInteractable
Ready — scanning every 3 seconds.
```
Then, while playing, wait for a SmartGuy or Magnate visitor to drop an item. Within a few seconds you should see:
```
Auto-collected ScienceEssenseIntertactable
Auto-collected MoneyPileInteractable
```

### Troubleshooting

- **Don't see the startup lines above in the log at all** — BepInEx isn't loading the plugin. Double check `AutoPickup.dll` is directly inside `BepInEx\plugins\`, not in a subfolder.
- **See a "not found" warning during startup instead** — the game was updated and an internal name changed. Please report this on the mod page so it can be fixed.
- **Items aren't being collected during play** — the mod scans every 3 seconds, so allow a short delay. If nothing is ever collected even after a SmartGuy/Magnate visit, check the log for warnings around the time the item dropped.

---

## How to uninstall

Delete **AutoPickup.dll** from the `BepInEx\plugins` folder and restart the game.

---

## Version

| Field   | Value                |
|---------|----------------------|
| Version | 1.0.0                |
| Author  | ShadowM00n81         |
| Game    | Waterpark Simulator  |
| Loader  | BepInEx 6 (IL2CPP)   |
