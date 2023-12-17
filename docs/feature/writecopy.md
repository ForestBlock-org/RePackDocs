# Write statements
Write statements can be used to write UTF-8 text to the output of a RePack texture pack. Syntax:
```rs
write "path/to/file/in/output.txt" {
    "the content of the file"
    "multiple lines can be defined by writing several string literals after eachother."
    "this would be line 3 in the output"
    "placeholders can also be used $(some_placeholder_here)"
}
```

# Copy statements
To copy a file from the workspace to the output texture pack folder, copy statements can be used. This is useful for
when RePack does not support some kind of file directly (like shaders) and write statements are too much of a hassle.
Syntax:
```rs
copy "path/to/file/in/workspace/directory.txt" => "path/to/output/file.txt"
```
Copy statements like these only support UTF-8 files, because placeholders can be used (only of the scope the copy
statement was used in). To copy things like images, the raw copy is used instead:
```rs
raw copy "textures/pack-icon.png" => "pack.png"
```
Keep in mind that with raw copy statements, placeholders can NOT be used.