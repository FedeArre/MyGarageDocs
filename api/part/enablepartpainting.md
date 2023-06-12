# [Part](api/part.md).EnablePartPainting

*public void EnablePartPainting(int materialIndex, string slotTextureType = "_MainTex")*

#### Description
Makes a part paintable if the part already has the proper materials for it (Unless the paint only type)

#### Parameters
Name | Description | Type | Default
---- | ---- | ----  | ---- 
type | The type of painting that the part will have | [PaintingSystem.Types](api/paintingsystem/types.md) | None
paintMaterial | The index of the material that will become paintable, only required if using only paint type | int | -1

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
    // The materials from PaintingSystem are only available after game load, so we can not use them on constructor

    Material[] partMaterials = example_part.Renderer.materials;
    partMaterials[0] = PaintingSystem.GetPaintRustMaterial();
    partMaterials[1] = PaintingSystem.GetDirtMaterial();
    partMaterials[2] = PaintingSystem.GetBodymatMaterial();
    example_part.Renderer.materials = partMaterials; // Has to be assigned back since Renderer.materials returns a copy of the materials array, not a reference.

    // You can also use PaintingSystem.SetMaterialsForObject to setup the materials

    example_part.MakePartPaintable(PaintingSystem.Types.FullPaintingSupport);
}
```