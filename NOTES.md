# good to know

You'll want to configure your working directory such that it can find the quake assets.

On my machine, this was done by updating the project settings, resulting in the following file:
```xml
<!-- WinQuake\HandmadeQuake\HandmadeQuake.vcxproj.user -->
<?xml version="1.0" encoding="utf-8"?>
<Project ToolsVersion="14.0" xmlns="http://schemas.microsoft.com/developer/msbuild/2003">
  <PropertyGroup Condition="'$(Configuration)|$(Platform)'=='Debug|Win32'">
    <LocalDebuggerCommandArguments>-startwindowed</LocalDebuggerCommandArguments>
    <DebuggerFlavor>WindowsLocalDebugger</DebuggerFlavor>
    <!-- This is the important line! -->
    <LocalDebuggerWorkingDirectory>C:\Program Files (x86)\Steam\steamapps\common\Quake</LocalDebuggerWorkingDirectory>
  </PropertyGroup>
  <PropertyGroup Condition="'$(Configuration)|$(Platform)'=='Release|Win32'">
    <LocalDebuggerCommandArguments>-startwindowed</LocalDebuggerCommandArguments>
    <DebuggerFlavor>WindowsLocalDebugger</DebuggerFlavor>
  </PropertyGroup>
</Project>
```

# Things to check out

- game loop
- input
- rendering
- network code
- where do they send stuff and how?


# What's this?

```c
SV_Physics
```

```c
qsocket_t	*net_activeSockets = NULL;
qsocket_t	*net_freeSockets = NULL;
```