# Mod settings

New structure allowed for per-mod settings, here is the full list and what does every one of them.

```cs
using SimplePartLoader;

ModInstance ThisMod;

public ModMain()
{
    ThisMod = ModUtils.RegisterMod(this);

    // Here you setup the settings of your mod.
}
```
# Developer log

Disabled by default.
Enables extra information related to the mod loading. Should be only used for testing

```cs
ThisMod.Settings.EnableDeveloperLog = true;
```

# Enable immediate destroys

Disabled by default. 
When enabled, all destroys done internally (Destroying childs, development components) is done immediately. This is useful when working on stuff that happens on same frame (like car-building).

```cs
ThisMod.Settings.EnableImmediateDestroys = true;
```

# PreciseCloning

Enabled by default.
When enabled, makes dummy part use a more precise cloning system. Can be disabled for certain compatibility stuff but generally is not a good idea to disable it.

```cs
ThisMod.Settings.PreciseCloning = true;
```

# Automatic fits to car

Not setup by default.
When setup, it sets the "FitsToCar" property on Partinfo to the value of the setting for all your parts.

```cs
string[] carList = { "F100", "F350" };
ThisMod.Settings.AutomaticFitsToCar = carList;
```

# Automatic fits to engine

Not setup by default.
When setup, it sets the "FitsToEngine" property on Partinfo to the value of the setting for all your parts.

```cs
string[] engineList = { "i4", "v8" };
ThisMod.Settings.AutomaticFitsToEngine = engineList;
```

# Paint resolution

Low by default.
Default paint resolution for paintable parts.

```cs
ThisMod.Settings.PaintResolution = PaintingSystem.PartPaintResolution.High;
```

# Use backface shader

Disabled by default.
When enabled, the base material of the painting system will render only the flipped normals of it.

```cs
ThisMod.Settings.UseBackfaceShader = true;
```