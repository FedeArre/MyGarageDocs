# [ModUtils](api/modutils.md).RegisterEngineCategory

*public static void RegisterEngineCategory(string name)*

#### Description
Registers a new engine category on the in-game catalog.

#### Example
```csharp
using SimplePartLoader;

ModInstance ThisMod;

public ModMain()
{
    ThisMod = ModUtils.RegisterMod(this);

    ModUtils.RegisterEngineCategory("NewGreatEngine");
}
```