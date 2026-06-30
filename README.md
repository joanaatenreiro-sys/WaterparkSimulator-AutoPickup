# NoPushMod

A mod for **Waterpark Simulator** that stops your NPCs getting pushed over or hurt — so you can run around and use your tools without worrying about unhappy guests.

---

## What it does

The base game has two situations where NPCs get knocked over or hurt, which causes them to leave bad reviews:

- **Running** — if you run into a guest they get pushed over
- **Tools** — if you accidentally hit a guest with your hammer, sledgehammer, or mop they get hurt

This mod removes both of those reactions. Guests will no longer be affected when you bump into them while running or swing a tool near them. Everything else stays the same — guests still react normally to the waterpark itself, rides, and water guns.

---

## Requirements

- **BepInEx 6 (IL2CPP build)** installed on Waterpark Simulator — e.g. via the "BepInEx and MelonLoader" pack from [Nexus Mods](https://www.nexusmods.com/waterparksimulator/mods/62)

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

### Step 2 — Install NoPushMod

1. Download **NoPushMod.dll**
2. Copy it into the `BepInEx\plugins` folder inside your Waterpark Simulator install folder:
   ```
   Steam\steamapps\common\Waterpark Simulator\BepInEx\plugins\
   ```
3. Launch the game — the mod loads automatically, no further setup needed

### Step 3 — Confirm it worked

Open `BepInEx\LogOutput.log` (in your game folder) and look for these two lines:
```
[Info   :   NoPushMod] Patched PlayerTriggerPush.OnTriggerEnter — running push disabled.
[Info   :   NoPushMod] Patched HitNPCInteractable.HitNPC — tool hits on NPCs disabled.
```
If you see both, the mod is active. Run into an NPC or graze one with a tool in-game to confirm.

### Troubleshooting

- **Don't see the two lines above in the log at all** — BepInEx isn't loading the plugin. Double check `NoPushMod.dll` is directly inside `BepInEx\plugins\`, not in a subfolder.
- **See a "Could not find" warning instead** — the game was updated and an internal method name changed. Please report this on the mod page so it can be fixed.

---

## How to uninstall

Delete **NoPushMod.dll** from the `BepInEx\plugins` folder and restart the game.

---

## Version

| Field   | Value                 |
|---------|-----------------------|
| Version | 1.0.0                 |
| Author  | ShadowM00n81          |
| Game    | Waterpark Simulator   |
| Loader  | BepInEx 6 (IL2CPP)    |
