# unity-singleton
Adds singleton functionality to your Unity components. This allows components that inherit from the Singleton component (which itself derives from MonoBehaviour) to be the sole version that exists in the Unity scene. You can easily access this sole version of the component (the singleton) by calling T.Singleton (where T is the name of your class). The first time it's accessed a gameobject will be spawned that stores the singleton.

**Assembly:**\
com.gambit.singleton

**Namespace:**\
gambit.singleton

**ASMDEF File:**\
gambit.singleton

**Scripting Define Symbol:**\
GAMBIT_SINGLETON

------------------------------
USAGE INSTRUCTIONS
------------------------------
To use, have your monobehaviour class inherit from Singleton<T> (where T is the name of your class).\
  To call the singleton, call T.Instance (where T is the name of your class).
  
 The first time T.Instance is used, it will create a gameobject and attach your class to it. It will persist between scenes and further references to T.Instance will reference this gameobject and component.
  
Take a look at the [Singleton Pattern On Wikipedia](https://en.wikipedia.org/wiki/Singleton_pattern) for more information.

------------------------------
INSTALLATION INSTRUCTIONS
------------------------------
- Open your unity package manager manifest (YourProject/Packages/manifest.json)

- Add a new entry...\
  "com.gambit.singleton": "https://github.com/GambitGamesLLC/unity-singleton.git?path=Assets/Plugins/Package",

- If you want to keep up to date with this repo, then you're done.
- If you want a specific version, add #v1.0.0 to the end of the URL (replace with the released version you want)

- Check the [Unity manual](https://docs.unity3d.com/Manual/upm-git.html#subfolder) on installing plugins from the subfolder of a Git repo for more info.
