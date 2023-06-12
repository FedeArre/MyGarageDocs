# [ModInstance](api/modinstance.md).EnableEarlyAccessCheck

*public void EnableEarlyAccessCheck()*

#### Description
Enables the whitelist check for the mod. This is not intended for fully released mods but rather mods that are under testing. A more specific guide is available [here]()

#### Example
```csharp
using SimplePartLoader;

ModInstance ThisMod;
public ModMain()
{
    ThisMod = ModUtils.RegisterMod(this);
    
    ThisMod.EnableEarlyAccessCheck();
}
```