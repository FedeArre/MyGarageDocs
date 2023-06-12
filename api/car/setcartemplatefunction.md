# [Car](api/car.md).SetCarTemplateFunction

*public void SetCarTemplateFunction(Action<GameObject> function)*

#### Description
Sets a function to be called after ModUtils finishes the car template setup process. Note that this function gets called twice (The empty and the fully built variant).

#### Example
```csharp
using SimplePartLoader;

ModInstance ThisMod;
public ModMain()
{
    ThisMod = ModUtils.RegisterMod(this);
    
    Car newCar = ThisMod.RegisterCar(carGenObj, emptyObj, transparentsObj);
    newCar.SetCarTemplateFunction(PostTemplate);
}

void PostTemplate(GameObject car)
{
    Debug.Log("Car template was setup for car " + car.name);
}
```