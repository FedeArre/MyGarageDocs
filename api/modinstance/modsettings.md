# ModSettings

Allows to change various settings about the mod

# Properties <!-- {docsify-ignore} -->

Type | Default value | Property | Description
---- | ------------ | -------- | -----------
bool | false | Enable developer log | If developer log is enabled, more debug information about the mod is shown. Recommended to enable while developing a mod (Disable before releasing!)
bool | false | Enable immediate destroys | Forces ModUtils to use GameObject.DestroyImmediate instead of GameObject.Destroy for your mod. Required when working with cars
bool | true | Precise cloning | Uses a better cloning method. Is not recommended to use the old method, setting exists to preserve mod compatibility
string[] | null | Automatic fits to car | If set, all the parts loaded with the mod will use this as their Partinfo.FitsToCar
string[] | null | Automatic fits to engine | If set, all the parts loaded with the mod will use this as their Partinfo.FitsToEngine
[PartPaintResolution](api/paintingsystem.md# Paint resolution enum) | Low | Painting resolution | The paint resolution to be used on loaded parts that use PaintIn3D
bool | Cull shader | On prefab generator parts, forces the bodymat to render the opposite of the mesh normals