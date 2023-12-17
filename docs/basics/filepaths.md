# File paths
File paths are usually used in several places of a workspace like write statements, copy statements and more. It is
important to understand how these are evaluated.

## Root folders
File paths are evaluated relative to the root folder they will be used in. Usually this is the workspace directory.
If your workspace directory is stored on your computer in a directory like:
```
/home/username/Desktop/RePack/workspaces/mytexturepack
```
then a filepath in any pack file is evaluated with that directory as its parent, e.g. a file path like:
```
textures/pack-icon.png
```
will actually be inside `/home/username/Desktop/RePack/workspaces/mytexturepack/textures/pack-icon.png`.
This is important due to working together with other people and having the workspace also compile on their machine.

## Special file paths
Parent directory file paths are to be avoided if they go outside of the workspace directory, as the workspace might not 
compile on a different machine (e.g. `../some/directory/outside/of/the/workspace`). Avoid using any file that is not
found in your workspace directory.