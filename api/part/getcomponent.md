# [Part](api/part.md).GetComponent

*public T GetComponent<T>()*

#### Description
A shortcut for Prefab.GetComponent<T>

#### Example
```csharp
using SimplePartLoader;

ModInstance ThisMod;

public ModMain()
{
    ThisMod = ModUtils.RegisterMod(this);
    
    Part example_part = ThisMod.Load(MyAssetBundle, "ExamplePart");

    // Both do the same!
    example_part.Prefab.GetComponent<MeshCollider>().trigger = false;
    example_part.GetComponent<MeshCollider>().trigger = false;
}
```