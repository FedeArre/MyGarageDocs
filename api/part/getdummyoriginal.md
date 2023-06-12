# [Part](api/part.md).GetDummyOriginal

*public GameObject GetDummyOriginal()*

#### Description
Returns the reference to the original part that was copied to the part using CopyPartToPrefab or prefab generator. Returns null if the part is not a valid dummy part.

#### Example
```csharp
using SimplePartLoader;

Part example_part;
ModInstance ThisMod;

public ModMain()
{
    ThisMod = ModUtils.RegisterMod(this);
    
    example_part = ThisMod.Load(MyAssetBundle, "ExamplePart");
    
    SPL.FirstLoad += FirstLoad;
}

public void FirstLoad()
{
    SPL.CopyPartToPrefab(example_part, "HubCap");
    
    Debug.Log(example_part.GetDummyOriginal()); // Returns a reference to the original HubCap from the game.
}
```