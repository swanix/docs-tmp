<figure class="hero-large" style="--hero-image:url(https://source.unsplash.com/g-YsyUUwT9M/1800x600);"></figure>

# Tool Docs

#### Quick start

Crea un archivo `index.html` con el siguiente código HTML para iniciar la documentación, adicionalmente crea una carpeta con nombre `content` donde incluirás todos los archivos markdown de tu documentación.

```
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="robots" content="noindex, nofollow">
  <title>Swanix</title>
  <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <!-- Favicon -->
  <link rel="shortcut icon" href="assets/images/favicon.ico">
  <!-- Styles -->
  <link rel="stylesheet" href="dist/tool-docs.min.css">
</head>
<body>
<div id="app"></div>
<script>
  window.$docsify = {
    name: "Tool Docs",
    // themeColor: 'royalblue',
    basePath: 'content/',
    // onlyCover: true,
    // coverpage: '_site-cover.md',
    autoHeader: true,
    homepage: '_site-home.md',
    loadNavbar: '_site-navbar.md',
    loadSidebar: '_site-menu.md',
    subMaxLevel: 1,
    auto2top: true,
    relativePath: true,
    notFoundPage: true,
    tabs: {
      persist    : false,      
      sync       : false,     
      theme      : 'classic',
      tabHeadings: true
    },
    'flexible-alerts': {
      style: 'flat'
    },
    pagination: {
      previousText: 'Previous',
      nextText: 'Next',
      crossChapter: true
    }
  };
</script>

<!-- Swanix - Tool Docs -->
<script src="menu.js"></script>
<script src="dist/tool-docs.min.js"></script>
</body>
</html>

```


## Créditos

Tool Docs está basado en diferentes librerías open source:

#### Docsify:

- **Docsify** https://docsify.js.org/
- **Docsify Pagination** https://github.com/imyelo/docsify-pagination
- **Docsify Tabs** https://jhildenbiddle.github.io/docsify-tabs/
- **Docsify Copy Code**  https://github.com/jperasmus/docsify-copy-code
- **Docsify Mustache** https://docsify-mustache.github.io/

#### Otras Librerías

- **Clipboard.js** https://clipboardjs.com/
- **Hint.css** https://github.com/chinchang/hint.css