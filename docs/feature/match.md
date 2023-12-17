# Match statements
Match statements are used to set textures that are usually set with the Optifine 
![cit properties](https://github.com/sp614x/optifine/blob/master/OptiFineDoc/doc/cit_single.properties). This means
they are only supported by Optifine users. Syntax:
```rs
match {
    "nbt.display.Name" = "\'{\"text\":\"hello\"}\'" 
    // this is the place to put any form of cit properties
} replace {
    items {
        "*_glass_pane" = "textures/demo.png" 
        // all glass panes with the name "hello" will have their 
        // texture replaced with the demo.png file
    }
}
```
This can be used to easily change the texture of a lot of items at once or even add new items to the game.
```rs
match {
    "nbt.CustomItem" = "raw_uranium" 
    // matching for a custom nbt tag lets you create 
    // infinitely many custom items without mods
} replace {
    items {
        "feather"
        "clock"
        "redstone" 
        // these 3 items will all have the same texture as seen below
        // if, and only if, they have the nbt tag defined above
    } = "assets/minecraft/textures/raw_uranium.png"
}
```

## Future
Other features like setting armor, elytra, etc textures are planned for the future, which is why the 'items' keyword
is used in the replace {} scope.