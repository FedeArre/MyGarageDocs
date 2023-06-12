# [ModInstance](api/modinstance.md).LoadFurniture

*public Furniture LoadFurniture(AssetBundle bundle, string prefabName)*

#### Description
Loads a new furniture into the game. It has to be setup with the Furniture Generator.

#### Example
```csharp
using SimplePartLoader;

ModInstance ThisMod;
Furniture myFurniture;

public ModMain()
{
    ThisMod = ModUtils.RegisterMod(this);

    AssetBundle Bundle = AssetBundle.LoadFromMemory(Properties.Resources.exampleBundle);

    myFurniture = ThisMod.LoadFurniture(Bundle, "greatShelf");

    Bundle.Unload(false);
}
```