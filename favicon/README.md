
We have two SVG files for the favicon source (essentially the same file but with colours reversed).

Black text on white is used for low resolution files (128x128 and below).

The SVG files are resized in graphics software and exported to PNG files.

The smaller resoultion icons are combined into a .ico file.

```shell
icotool -c favicon-16x16.png favicon-32x32.png favicon-48x48.png favicon-64x64.png favicon-128x128.png -o favicon.ico
```

The files should be added to the website document root (or the webserver should be configured to find their location).

The following metadata should be added to the `<head/>` section of webpages.

```html
    <link rel="apple-touch-icon" sizes="1024x1024" href="/favicon-1024x1024.png"/>
    <link rel="apple-touch-icon" sizes="180x180" href="/favicon-180x180.png"/>
    <link rel="apple-touch-icon" sizes="167x167" href="/favicon-167x167.png"/>
    <link rel="apple-touch-icon" sizes="152x152" href="/favicon-152x152.png"/>
    <link rel="apple-touch-icon" sizes="80x80" href="/favicon-80x80.png"/>
    <link rel="apple-touch-icon" href="/favicon-152x152.png"/>
    <link rel="icon" sizes="32x32" href="/favicon-32x32.png"/>
```

