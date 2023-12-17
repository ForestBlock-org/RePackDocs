# Character statements
Character statements are used to set the texture of any character in the minecraft font to any image. Syntax:
```cpp
char "\uAAAA" "textures/characters/custom_character.png" {
    "ascent" = "7"
}
```
The above example will replace the character \uAAAA with the provided texture and set its y offset to 7. It will be
stored in the default font (`assets/minecraft/font/default.json`).

## Texture splitting
The maximum texture size for custom characters is 256x256 pixels, however this can be easily bypassed by splitting the
texture into 256x256 splices and using a full string with 
![custom spaces](https://github.com/AmberWat/NegativeSpaceFont) to display the texture ingame. The exact string will be
automatically generated and shown in the log output when compiling the RePack workspace. This is especially useful for
creating custom GUIs using the GUI title.
