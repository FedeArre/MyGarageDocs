# [SPL](api/spl.md).UpdateTransparentsReference

*public static Part UpdateTransparentsReference(Part part)*

#### Description
Used on dummy parts. It updates the DEPENDANTS and ATTACHABLES on the specified part to point to the correct transparents.

#### Parameters
Name | Description | Type | Default
---- | ---- | ----  | ---- 
part | The part to update | [Part](api/part.md) | None

#### Example
```csharp
using SimplePartLoader;

ModInstance ThisMod;

public ModMain()
{
    ThisMod = ModUtils.RegisterMod(this);
    
    Part example_part = ThisMod.Load(MyAssetBundle, "ExamplePart");
    
    SPL.FirstLoad += OnFirstLoad;
}

public void OnFirstLoad()
{
    // For this case we are going to copy the LAD headliner to our dummy part.
    // The headliner is holded by the mirror through the ATTACHABLES.
    // When we do our clone, our part still points to the mirror transparent that is located on the original prefab instead of the clone, so we update the references.
    SPL.CopyPartToPrefab(example_part, "Headliner06");
    SPL.UpdateTransparentsReference("Headliner06");
}
```