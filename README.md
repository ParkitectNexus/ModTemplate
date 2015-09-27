# ModTemplate
Repository Template for a Parkitect Mod.

mod.json options
----------------

Your mod.json file for a mod with the following directory structure could be found below:
- /
  - YourMod.sln
    - YourModFolder/
      - Main.cs
      - YourMod.csproj
      - SomeMoreCode.cs
            
```
{
	"BaseDir": "YourModFolder",
	"ClassName": "Main",
	"IsDevelopment": true,
	"Name": "Your First Mod",
	"NameSpace": "YourMod",
	"Project": "YourMod.csproj"
}
```

Your mod.json file for a mod with the following directory structure could be found below:
- /
  - Main.cs
  - SomeMoreCode.cs
            
```
{
	"ClassName": "Main",
	"IsDevelopment": true,
	"Name": "Your First Mod",
	"NameSpace": "YourMod",
	"CodeFiles": ["Main.cs", "SomeMoreCode.cs"],
	"ReferencedAssemblies": ["System", "Assembly-CSharp", "UnityEngine"]
}
```

All available mod.json options are:

- `BaseDir` (string): The path to the directory which contains your `.csproj` file. (optional)
- `ClassName` (string): The name of your entry point class. This class must implement `IMod`. (required)
- `CompilerVersion` (string): . The default value is `"v4.0"`. (optional)
- `CodeFiles` (string[]): . The default value is `[]`. \* (optional)
- `IsDevelopment` (boolean): Set to true to let the client recompile this mod at every launch. While set to true the mod can't be uninstalled either. (optional)
- `Name` (string): The name of your mod. (optional)
- `NameSpace` (string): The name of your entry point class' namespace. This class must implement `IMod`. (optional)
- `Project` (string): The name of your `.csproj` file. \* (optional)
- `ReferencedAssemblies` (string[]): . \* (optional)

\*: If `Project` is null, `CodeFiles` and `ReferencedAssemblies` *must* be set.
