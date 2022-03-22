# Set up git with a Unity Project

Follow these instructions if you wish to version a Unity project using git.  

Assuming you already created a Unity project:  
* Add a proper `.gitignore` file at your project files root. [You can use this one](./.gitignore).  
* Configure Unity
    * In **Edit > Project Settings**, category **Version Control**, turn the **Mode** to **Visible Meta Files**
    * Still in **Project Settings** but in the **Editor** category, within **Asset Serialization** switch the **Mode** to **Force Text**
    * Save the project

*([source](https://thoughtbot.com/blog/how-to-git-with-unity))*
