# Test with gatsby-plugin-asset-path
This is a fresh gatsby site (generated with `gatsby new`). I have added a `assetPrefix` and the necessary setup for `gatsby-plugin-asset-path`. But when I build this project with `gatsby clean && gatsby build --prefix-paths`, the link to the manifest file is not correct:

```
<link rel="manifest" href="//manifest.webmanifest"/>
```

because the manifest is actually located here:
```
$ ls public/assets/manifest.webmanifest
public/assets/manifest.webmanifest
```
and not here:
```
$ ls public/manifest.webmanifest
ls: cannot access 'public/manifest.webmanifest': No such file or directory
```

Am i missing something?
