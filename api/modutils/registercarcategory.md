# [ModUtils](api/modutils.md).RegisterCarCategory

*public static void RegisterCarCategory(string name)*

#### Description
Registers a new car category on the in-game catalog.

#### Example
```csharp
using SimplePartLoader;

ModInstance ThisMod;

public ModMain()
{
    ThisMod = ModUtils.RegisterMod(this);

    ModUtils.RegisterCarCategory("NewCar");
}
```