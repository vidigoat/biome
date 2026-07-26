---
"@biomejs/biome": patch
---

Fixed `.editorconfig` numeric ranges with negative bounds, such as `[{-1..1}.txt]`. Biome now expands them as ranges and matches `-1.txt`, `0.txt`, and `1.txt`, instead of treating the section header as a literal file name.
