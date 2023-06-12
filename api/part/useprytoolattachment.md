# [Part](api/part.md).UsePrytoolAttachment

*public void UsePrytoolAttachment()*

#### Description
Makes a part use the prytool attachment system from the game.

#### Example
```csharp
using SimplePartLoader;

ModInstance ThisMod;

public ModMain()
{
    ThisMod = ModUtils.RegisterMod(this);
    
    Part example_part = ThisMod.Load(MyAssetBundle, "ExamplePart");
    example_part.UsePrytoolAttachment();

    // Note that if a part has any WeldCut / HexNut / FlatNut / BoltNut it will be deleted.
}
```