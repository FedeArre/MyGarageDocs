# CarProperties (WIP)

Component used in car parts to determinate what exactly does the part

# Properties <!-- {docsify-ignore} -->

Attribute | Type | Observation
--------- | ---- | -----------
PartName | string | The part name to be displayed in-game. Can be overriden by localization
PartNameExtension | string | An extension to the part name. Generally used by engines (i4, v8, etc)
PrefabName | string | Unique identifier for the prefab name. Used in saving
Type | int | Used in rims and hubs. Must match to bolt Type attribute to be able to bolt the part
Type2 | int | TBR
ObjectNumber | int | Temporal "unique" identificator on game saving / load
ChildrenNumber | int | TBR
NumberPlate | bool | If the part is a license plate
One | Material | Material of the first number/letter of the license plate
Two | Material | Material of the second number/letter of the license plate
There | Material | Material of the third number/letter of the license plate
Four | Material | Material of the fourth number/letter of the license plate
Five | Material | Material of the fifth number/letter of the license plate
Six | Material | Material of the sixth number/letter of the license plate
Nr1 | string | Number/letter in the first place of the license plate
Nr2 | string | Number/letter in the second place of the license plate
Nr3 | string | Number/letter in the third place of the license plate
Nr4 | string | Number/letter in the fourth place of the license plate
Nr5 | string | Number/letter in the fifth place of the license plate
Nr6 | string | Number/letter in the sixth place of the license plate
WearWorking | bool | If the part should wear while the engine is running
WearDriving | bool | If the part should wear while the vehicle is being driven (Speed > 5km/h)
WearByTime | bool | If the part should wear with time. Condition decreases every ~100s (Has to be attached in a car)
WearSpeed | float | Works as a multiplier in WorkWorking and WorkDriving. The formula used for condition is -0.0001f * (0.1f * wearSpeed)
triger | bool | Indicates if the part is using triger-collider method (As specified on car parts guide)
Differentmesh | Mesh | Specify a different mesh for the part. Not recommended to use
tight | bool | Indicates if the part is bolted / welded. Does not seem to work well
SavePosition | int | The current save position of the object. Explained on car parts guide
JunkSpawnChance | int | Fully explained on car parts guide
Owner | string | Owner of the part (Generally Client, Player, Junkyard), set by game
SinglePart | bool | TBR (Awaiting mbdriver response)
PREFAB | GameObject | Not really used. Has to be set to any GameObject or part will not save
InBarn | bool | TBR
ConditionDebug | bool | TBR
NormalMesh | Mesh | Default mesh of object (Used only when DMGdeformMesh is set)
RemovedDifferentMesh | Mesh | If set, this mesh will be used when part is not attached. Note that the attached mesh is set by ChildrenMesh on transparent!
VisualObject | GameObject | Used in certain objects that require to move like crankshaft or camshaft.
MainProperties | MainCarProperties | TBR
exp | VehicleController | TBR
started | bool | Indicates if a part got a Start() call at least once (Game can call Start() at CarProperties multiple times)
Attached | bool | TBR
picked | bool | TBR (iirc did not work)
isCopy | bool | TBR
RustChangeCounter | P3dChangeCounter | Set by game if exists. Rust paint counter
RepairDecal | P3dPaintDecal | Set by game. Used for part repairing (Mesh damage)
RustRepairDecal | P3dPaintDecal | Set by game. Used for rust fixing
RustRepairedDecal | P3dPaintDecal | Set by game. Used for rust fixing
PaintRemoveDecal | P3dPaintDecal | Set by game. Used for rust fixing
WashDecal | P3dPaintDecal | Set by game. Used for car washing
Chromed | bool | If part has been chromed
ChromeMat | Material | If set, part will be chromable on the Chrome station. This material will be set to index 0 of the part material
unmountedWheel | GameObject | TBR
WheelController | GameObject | TBR
FRSuspensionPosition | GameObject | TBR
FLSuspensionPosition | GameObject | TBR
RRSuspensionPosition | GameObject | TBR
RLSuspensionPosition | GameObject | TBR
AudioParent | GameObject | Set by game on part start
MaterialParent | GameObject | Set by game on part start
HandBrake | bool | If part is a Handbrake
HandBrakeCable | bool | If part is a Handbrake cable
MeshRepairable | bool | If part has a fixable mesh (Generally used with DMGdeformMesh)
Tintable | bool | TBR
TintLevel | bool | TBR
CantRust | bool | TBR?
Paintable | bool | If part has painting support (PaintIn3D proper setup)
Washable | bool | If part has washing support (PaintIn3D proper setup)
Fairable | bool | If part has body filler support (Readable mesh)
Interior | bool | If is an interior part. Note that this will enable interior colors on the part. The color Material is always set to index 0
OriginalInterior | int | TBR
StartOption1 | GameObject | Explained on Cars guide
StartOption2 | GameObject | Explained on Cars guide
StartOption3 | GameObject | Explained on Cars guide
StartOption4 | GameObject | Explained on Cars guide
StartOption5 | GameObject | Explained on Cars guide
VisualWheel | bool | TBR
NonRotatingVisualWheel | bool | TBR
RealWheel | bool | TBR
Hub | bool | If part is a wheel hub
tireObject | bool | TBR
Tire | bool | If part is a tyre
TirePressure | float | The current pressure of a tyre
TireType | float | TBR
forwSlipCoef | float | TBR
forwForcCoef | float | TBR
sideForcCoef | float | TBR
sideForcCoef | float | TBR
TireValve | bool | TBR
Spring | bool | If part is a spring
Damper | bool | If part is a damper (Shock absorber)
SuspensionPart | bool | TBR

# Methods <!-- {docsify-ignore} -->

Method | Description
----- | -----------
[SetCarTemplateFunction](api/car/setcartemplatefunction.md) | Set a function to be called after ModUtils does the template setup of the car. Only one function can be set
[SetPostBuildFunction](api/car/setpostbuildfunction.md) | Set a function to be called after ModUtils finishes building the car. Only one function can be set
