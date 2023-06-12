# SPL

Static class that contains all the useful methods of SimplePartLoader

# Methods <!-- {docsify-ignore} -->

Method | Description
----- | -----------
[CopyPartToPrefab](api/spl/copyparttoprefab.md) | Clones a game's GameObject prefab into a [Part](api/part.md) that has been loaded using [LoadDummy](api/spl/loaddummy.md)
[ForcePartRegister](api/spl/forcepartregister.md) | Internally registers a part into SPL object list after SPL has been loaded. Used for parts that do not exist on both gamemodes
[UpdateTransparentsReference](api/spl/updatetransparentsreference.mdd) | It updates the DEPENDANTS and ATTACHABLES on the specified part to point to the correct transparents. Used on dummy parts.

# Events <!-- {docsify-ignore} -->

Event | Description
----- | -----------
[FirstLoad](api/spl/events/firstload.md) | Invoked on game's first load only. Used for calling [CopyPartToPrefab](api/spl/copyparttoprefab.md) and interacting with parts that were added using prefab generator
[LoadFinish](api/spl/events/loadfinish.md) | Invoked when game has finished loading. Used for calling [ForcePartRegister](api/spl/forcepartregister.md)
[DataLoaded](api/spl/events/dataloaded.md) | Invoked when SimplePartLoader finished loading custom data.