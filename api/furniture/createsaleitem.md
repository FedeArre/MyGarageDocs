# [Furniture](api/furniture.md).CreateSaleItem

*public SaleFurniture CreateSaleItem(Vector3 position, Vector3 rotation)*

#### Description
Creates a sale item of your furniture for the mod shop.

#### Example
```cs
using SimplePartLoader;

ModInstance ThisMod;

public ModMain()
{
    ThisMod = ModUtils.RegisterMod(this);

    AssetBundle MyBundle = AssetBundle.LoadFromMemory(Properties.Resources.Bundle);

    Furniture exampleFurniture = ThisMod.LoadFurniture(Bundle, "MyFurniture");
    exampleFurniture.CreateSaleItem(SaleFurniture.DEFAULT_MODSHOP_LOCATION, Vector3.zero);

    MyBundle.Unload(false);
}
```