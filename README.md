# Scoop bucket for Smia

[Smia](https://smia.leifericf.com) builds technical books as PDF, EPUB, and a
static site on the JVM.

Install:

```
scoop bucket add java
scoop bucket add smia https://github.com/leifericf/scoop-smia
scoop install smia
```

The manifest installs the release jar and a `smia` shim, and pulls a Temurin
JRE from the `java` bucket as a dependency.

The manifest pins one release by URL and hash. New Smia releases bump
`version`, `url`, and `hash` in `bucket/smia.json` (the checksum is printed by
the release workflow in the main repository); `checkver`/`autoupdate` keep the
manifest current when run with Scoop's tooling.
