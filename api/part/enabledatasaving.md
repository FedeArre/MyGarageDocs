# [Part](api/part.md).EnableDataSaving

*public void EnableDataSaving()*

#### Description
Makes a part use the data saving feature. Saved data can be accesed through the SaveData component that is added to the prefab.

#### Example
```csharp
using SimplePartLoader;

ModInstance ThisMod;

public ModMain()
{
    ThisMod = ModUtils.RegisterMod(this);
    
    Part example_part = SPL.LoadPart(MyAssetBundle, "ExamplePart");
    example_part.EnableDataSaving();

    // If you are using dummy parts, use EnableDataSaving AFTER copying an object into your dummy!
    // Example:
    // SPL.CopyPartToPrefab(example_part, "TrunkDoor06");
    // example_part.EnableDataSaving();
}
```