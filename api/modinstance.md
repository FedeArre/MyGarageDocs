# ModUtils

Represents a registered mod in ModUtils

# Properties <!-- {docsify-ignore} -->

Property | Description
----- | -----------
Mod | A reference to the Mod that registered the ModInstance
[Settings](api/modinstance/modsettings.md) | A reference to the ModSettings object of the ModInstance. Used to change mod settings
Name | Equals to Mod.Name
CheckAllow | If the user is whitelisted to use the mod. Note that it takes some frames to do the check, but it always has the result when OnLoad is called

# Methods <!-- {docsify-ignore} -->

Method | Description
----- | -----------
[Load](api/modinstance/load.md) | Load a part into the game
[LoadFurniture](api/modinstance/loadfurniture.md) | Load a furniture into the game
[EnableEarlyAccessCheck](api/modinstance/enableearlyaccesscheck.md) | Makes the mod check if the user is whitelisted to use the mod
[GenerateThumbnails](api/modinstance/generatethumbnails.md) | Enables the thumbnail generator for all the loaded parts of the mod
[LoadCar](api/modinstance/loadcar.md) | Load a new car into the game
