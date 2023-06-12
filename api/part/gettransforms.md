# [Part](api/part.md).GetTransforms

*public Transform[] GetTransforms()*

#### Description
Returns an array of Transform that includes the prefab transform and all the childrens from the prefab. Is equivalent to Part.Prefab.GetComponentsInChildren<Transform>().

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
    SPL.CopyPartToPrefab(example_part, "Roof07");
    
    // Checks for all the transforms of the prefab. If the name starts by Roofcol it gets deleted from the part.
    // Note that the transform of the prefab itself is also included!
    foreach(Transform t in example_part.GetTransforms())
    {
        if(t.name.StartsWith("Roofcol"))
        {
            GameObject.Destroy(t.gameObject);
        }
    }
}
```