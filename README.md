# ModTemplate
Repository Template for a Parkitect Mod.

mod.json options
----------------

Your mod.json file for a mod with the following directory structure could be found below:
- /
  - mod.json
  - YourMod.sln
    - YourModFolder/
      - Main.cs
      - YourMod.csproj
      - SomeMoreCode.cs
            
```
{
	"BaseDir": "YourModFolder",
	"EntryPoint": "YourMod.Main",
	"IsDevelopment": true,
	"Name": "Your First Mod",
	"Project": "YourMod.csproj"
}
```

Your mod.json file for a mod with the following directory structure could be found below:
- /
  - mod.json
  - Main.cs
  - SomeMoreCode.cs
            
```
{
	"EntryPoint": "YourMod.Main",
	"IsDevelopment": true,
	"Name": "Your First Mod",
	"CodeFiles": ["Main.cs", "SomeMoreCode.cs"],
	"ReferencedAssemblies": ["System", "Assembly-CSharp", "UnityEngine"]
}
```

All available mod.json options are:

- `AssetBundleDir` (string): The path to the mod's asset bundles. (optional)
- `AssetBundlePrefix` (string): A unqiue prefix for this mod's asset bundles. (optional)
- `BaseDir` (string): The path to the directory which contains your `.csproj` file. (optional)
- `CompilerVersion` (string): . The default value is `"v4.0"`. (optional)
- `CodeFiles` (string[]): . The default value is `[]`. \* (optional)
- `EntryPoint` (string): The name (including namespaces) of your entry point class. This class must implement `IMod`. (required)
- `IsDevelopment` (boolean): Set to true to let the client recompile this mod at every launch. While set to true the mod can't be uninstalled either. (optional)
- `Name` (string): The name of your mod. (optional)
- `Project` (string): The name of your `.csproj` file. \* (optional)
- `ReferencedAssemblies` (string[]): . \* (optional)

\*: If `Project` is null, `CodeFiles` and `ReferencedAssemblies` *must* be set.
