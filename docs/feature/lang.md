# Language statements
Language statements are used to change texts of a minecraft language file. Syntax:
```rs
lang {
    "en_*" 
    // wildcards are supported; this matches en_pt, en_ud, en_us, en_ca, en_gb, en_nz
    // matching for "*" would replace every language file.
} replace {
    "container.inventory" = "" // removes the Inventory text in every inventory gui
    // here wildcards are not supported yet, but will be in the future
}
```