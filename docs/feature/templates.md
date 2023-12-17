# Templates
Templates are a key part of RePack and they are probably the most useful feature to increase texture pack creation
speed drastically. When used, they can run multiple statements all at once, given some parameters. Syntax:
```rs
template create_custom_item(require name, require replacement_item) {
    match {
        "nbt.CustomItem" = "$(name)"
    } replace {
        items {
            "$(replacement_item)"
        } = "$(ITEM_TEXTURES)/$(name).png"
    }
}

create_custom_item(name = "raw_uranium", replacement_item = "feather")
create_custom_item(name = "purified_uranium", replacement_item = "feather")

create_custom_item(replacement_item = "feather", name = "raw_aluminium")
// parameter order is not important

create_custom_item(name = "aluminium_ingot", replacement_item = "clock")
```
To create default parameters, the 'require' keyword can be discarded, e.g.
```rs
template create_custom_item(require name, replacement_item = "feather") { 
    // replacement_item will be "feather" by default, unless specified otherwise
    // ...
}

create_custom_item(name = "raw_uranium")
create_custom_item(name = "raw_aluminium")
create_custom_item(name = "purified_uranium")
create_custom_item(name = "aluminium_ingot", replacement_item = "clock")
```
Templates are also defined at a global level, meaning they can be used in any other pack file as well.