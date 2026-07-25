---
"@biomejs/biome": patch
---

The HTML formatter now formats the value of a `style` attribute as CSS, the same way it already formatted a `<style>` element. The declarations stay on the tag's line while they fit there, and break onto their own lines once they do not:

```diff
- <div style="color:#fFf;  background:red"></div>
+ <div style="color: #fff; background: red"></div>
```

A value that is not a list of declarations is left exactly as written, which covers an interpolation such as `style="{{ dynamic }}"` and a prop that happens to be called `style`.
