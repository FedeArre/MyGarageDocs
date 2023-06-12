# [Part](api/part.md).UseHandAttachment

*public void UseHandAttachment()*

#### Description
Makes a part use the hand attachment system from the game.

#### Example
```csharp
using SimplePartLoader;

ModInstance ThisMod;

public ModMain()
{
    ThisMod = ModUtils.RegisterMod(this);
    
    Part example_part = ThisMod.Load(MyAssetBundle, "ExamplePart");
    example_part.UseHandAttachment();

    // Note that if a part has any WeldCut / HexNut / FlatNut / BoltNut it will be deleted.
}
```