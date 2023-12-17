# String literals
String literals are any form of text used in RePack files. Syntax:
```rs
"this is a string literal"
'this is also a string literal'

"this is an invalid string literal'
"this is a string literal containing a \" quote character"
"this is a string literal with a \n new line, \t tab"
"string literals can also have \b backspace, \f form feed, \r carriage return"
"as well as escaped \u0061 unicode literals"
"or ascii literals \65"
"to use backslashes, they also need to be escaped \\"
```

## Multiline string literals (planned)
String literals defined across multiple lines are not usable yet, but they are planned for the future. Possible syntax:
```rs
"""
this is a multiline string literal.
text can be written across multiple lines here without using the \n character.
this can be useful for writing files with $(placeholders) directly.
"""

"current strings
cannot go across multiple
lines, so this is invalid."
```

## Placeholders
To see how to use placeholders for definitions in string literals, see
![the definitions page](/docs/feature/definitions.md).