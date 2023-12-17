# RePack Basics
RePack works by compiling a RePack workspace to a minecraft texture pack.

## Workspaces
A workspace consists out of pack files (.rpk), which can be structured in any desired way. Any other file extension
is ignored unless used in some form by a pack file.

## Pack files
Pack files consist out of a set of statements which tell RePack exactly what your texture pack should look like.
Their syntax is specified in detail in this documentation. Important to note is that RePack does not require statement
separators like semicolons nor newlines or tabs like in python; the syntax is designed to feel as free as possible.

## Features
Currently, there are not a lot of features, though there are enough to make a fully functional texture pack.
RePack lets you use:
- ![Global and local definitions](/docs/feature/definitions.md)
- ![Match statements to set item textures](/docs/feature/match.md)
- ![Write / copy statements](/docs/feature/writecopy.md)
- ![Character statements](/docs/feature/character.md)
- ![Language statements](/docs/feature/lang.md)
- ![Templates](/docs/feature/templates.md)

### More help
For simple syntax help, check out:
- ![File path help](/docs/basics/filepaths.md)
- ![String literal help](/docs/basics/stringliterals.md)