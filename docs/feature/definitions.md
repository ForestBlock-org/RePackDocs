# Definitions
Definitions can be used to define and store string values per workspace or per pack file. They are not mutable and are
comparable to the #define feature of the C programming language.

## Local definitions
If a definition is not needed on a global level (everywhere in the workspace), local definitions are used. These are
only valid in the scope they were defined in (a pack file, or in a template). Syntax:
```py
def identifier = "value"
```

## Global definitions
This form of definitions is usable across the entire workspace. Syntax:
```py
global identifier = "value"
```

## Evaluating definitions
Definitions can be evaluated in any kind of string literals using a kind of placeholder syntax.
```py
def definition_1 = "hello"
def definition_2 = "$(definition_1) world"
```
Definition order is important however, so something like this will not work:
```py
def definition2 = "$(definition_1) world"
def definition1 = "hello"
```
Global definitions are created before local ones though, so this would work again:
```py
def definition2 = "$(definition_1) world"
global definition1 = "hello"
```