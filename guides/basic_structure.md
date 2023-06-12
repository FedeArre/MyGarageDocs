# Basic mod structure and settings

ModUtils v1.2 introduced a new structure for the mods, old mods still work but the old structure is now deprecated. Converting old mods is very easy since structure is now easier. Let's look an example of a old mod and then see how it would be under new structure.

```cs
using SimplePartLoader;

Part examplePartOne, examplePartTwo;

public ModMain()
{
    AssetBundle Bundle = AssetBundle.LoadFromMemory(Properties.Resources.example);

    examplePartOne = SPL.LoadDummy(Bundle, "examplePartOne");
    examplePartTwo = SPL.LoadPart(Bundle, "examplePartTwo");

    Bundle.Unload(false);
}
```

With the new structure it will be like this

```cs
using SimplePartLoader;

Part examplePartOne, examplePartTwo;
ModInstance ThisMod;

public ModMain()
{
    ThisMod = ModUtils.RegisterMod(this);

    AssetBundle Bundle = AssetBundle.LoadFromMemory(Properties.Resources.example);

    examplePartOne = ThisMod.Load(Bundle, "examplePartOne");
    examplePartTwo = ThisMod.Load(Bundle, "examplePartTwo");

    Bundle.Unload(false);
}
```

Two differences on this snippet:
- You now have to register your mod
- The part loading happens through your mod instance rather than a global method.

This new structure allows to new features, like identifying which mod added which part, settings for the mod and more.

A full guide related to mod settings is available [here](guides/mod_settings.md).