# [ModUtils](api/modutils.md).RegisterMod

*public static ModInstance RegisterMod(Mod mod)*

#### Description
Registers a new mod into ModUtils. Used to load parts and furnitures.

#### Example
```csharp
using SimplePartLoader;

ModInstance ThisMod;

public ModMain()
{
    ThisMod = ModUtils.RegisterMod(this);

    // Now ModUtils knows about our mod and we can start adding parts or furnitures into the game.
}
```