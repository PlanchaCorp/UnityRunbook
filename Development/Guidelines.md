# Project guidelines

## Naming Convention

We use **PascalCase** in most places.  
We use it for every files and folders *(ex: CrabMovement.cs, CrabDigging.png, Crab.prefab)*  
And for class names and properties - parameters or local variables are fine in *camelCase*.  
```
class PlayerMovement {
  public void Move(Vector2 direction) {
    float localVariable = ...;
  }
}
```

Try to find relevant names! Other people must be able to understand the purpose of your files by their names.  

## Project file structure

We try to be consistent with where we put our files.  
Here is a good enough file structure we can use:  

* **Assets**
  * **GameData**: *All instantiated scriptable objects (but not the classes!)*
  * **Graphics**: *Everything about graphical assets*
    * **Animations**
    * **Textures**
  * **Prefabs**
  * **Scenes**
  * **ScriptableObjects**: *Only the classes*
  * **Scripts**: *Structure the content of Scripts as best as you can*

## Keep a clean code 🧹

People will work on the same file as you do, so keep it clean!  
**Indentation** is not for the sake of being pretty, and **line breaks** serve a purpose when done well.   
