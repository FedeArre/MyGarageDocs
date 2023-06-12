# [Part](api/part.md).AddTransparent

*public TransparentData AddTransparent(string attachesTo, Vector3 transparentLocalPos, Quaternion transaprentLocalRot, bool testingModeEnable = false)*

*public TransparentData AddTransparent(string attachesTo, Vector3 transparentLocalPos, Quaternion transaprentLocalRot, Vector3 scale, bool testingModeEnable = false)*

#### Description
Creates a transparent (Attachment point) in the indicated part on the given position. Returns a [TransparentData](api/transparentdata.md) instance.

If using dummy parts, this function has to be used AFTER the part creation has been done.

#### Parameters
Name | Description | Type | Default
---- | ---- | ----  | ---- 
attachesTo | Name of the game object that the transparent will be attached to | string | None
transparentLocalPos | The local position of the transparent | Vector3 | None
transparentLocalRot | The local rotation of the transparent | Quaternion | None
scale | The scale of the transparent. Is not recommended to change but may be required on certain scenarios. | Vector3 | Vector3.one
testingModeEnable | Enable the transparent in-game editor for the transparent | bool | false

#### Example
```csharp
using SimplePartLoader;

ModInstance ThisMod;

public ModMain()
{
    ThisMod = ModUtils.RegisterMod(this);

    Part example_part = ThisMod.Load(MyAssetBundle, "ExamplePart");
    example_part.SetupTransparent("TrunkDoor06", Vector3.up, Quaternion.identity);

    Part example_part2 = ThisMod.Load(MyAssetBundle, "ExamplePart2");
    TransparentData data = example_part2.SetupTransparent("TrunkDoor06", Vector3.up, Quaternion.identity);
    data.SavePosition = 1;
}
```