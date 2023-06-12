# [Car](api/car.md).SetPostBuildFunction

*public void SetPostBuildFunction(Action<GameObject> function)*

#### Description
Sets a function to be called after ModUtils finishes the car building process. You generally will do the fixes (Like broken fluids references) or other stuff here.

#### Example
```csharp
using SimplePartLoader;

ModInstance ThisMod;
public ModMain()
{
    ThisMod = ModUtils.RegisterMod(this);
    
    Car newCar = ThisMod.RegisterCar(carGenObj, emptyObj, transparentsObj);
    newCar.SetPostBuildFunction(PostBuild);
}

void PostBuild(GameObject car)
{
    Debug.Log("Car was builded!");
}
```