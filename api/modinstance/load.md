# [ModInstance](api/modinstance.md).Load

*public Part Load(AssetBundle bundle, string prefabName)*

#### Description
Loads a new part into the game. Automatically detects if is a full part, dummy with prefab gen. or dummy part.

#### Example
```csharp
using SimplePartLoader;

ModInstance ThisMod;
Part fullPart, dummyPart;

public ModMain()
{
    ThisMod = ModUtils.RegisterMod(this);

    AssetBundle Bundle = AssetBundle.LoadFromMemory(Properties.Resources.exampleBundle);

    fullPart = ThisMod.Load(Bundle, "partWithCarprops");
    dummyPart = ThisMod.Load(Bundle, "partWithPrefabGen");

    Bundle.Unload(false);
}
```