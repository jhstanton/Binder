# Binder

Binder is a tool that compiles notes into a single file.

## Current State

Binder currently compiles all markdown files with extension `.note` from the current directory and all subdirectories
into a single HTML file. In commit 8de0fb253e567ce5bac0ad8d208f69ffd976b1c7 the library switched from the
[markdown](http://www.haskell.org/hackage/package/markdown) package to
[pandoc](http://www.haskell.org/hackage/package/pandoc) to better support tables and math.

The HTML output is sorted by directories and last modified date (directories are sorted by last modified date as well). 

## Next Steps

Since pandoc is now used, the meta data in pandocs should be leveraged to update sorting (for example, by creation date rather
than last modification date).

Support for diagrams, ala [diagrams](http://www.haskell.org/hackage/package/diagrams), is desirable, possibly using 
[pandoc-diagrams](http://www.haskell.org/hackage/package/pandoc-diagrams).

Additional tooling is to be added for a yaml config file to include things such as additional styles to include, target
directory, etc.