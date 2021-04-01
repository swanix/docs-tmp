<figure class="hero" style="--hero-image:url(https://source.unsplash.com/g-YsyUUwT9M/1800x600);"></figure>

# Example 3

## Colors

Elements from file `colors.json` using Docsify Mustache plugin:

<style>
  .colors.grid {
    grid-gap: 24px 24px;
  }

  .colors .grid-item {
    box-shadow: 1px 2px 5px 0px rgba(0, 0, 0, 0.1);
    border-radius: 8px;
  }

  .colors .grid-item-header {
    width:100%; 
    height:140px;
    border-radius: 8px 8px 0 0;
  }

  .colors .grid-item-body {
    padding: 16px 16px;
    align-items: start;
    font-size:14px; 
    border-top:#EDEDED solid 1px;
  }
</style>

### Greyscale

<section class="grid colors">
{{#grey}}
<div class="grid-item">
  <div class="grid-item-header" style="background-color:{{{codeHex}}}">
  </div>
  <div class="grid-item-body">
      <span>{{name}}</span>
      <span>{{codeHex}}</span>
      <span>{{codeRgb}}</span>
  </div>
  <div class="grid-item-footer">
    <button class="button copy" data-clipboard-text="{{{codeHex}}}" aria-label="Copied!">Copy HEX</button>
    <button class="button copy" data-clipboard-text="{{{codeRgb}}}" aria-label="Copied!">Copy RGB</button>
  </div>
</div>
{{/grey}}
{{^grey}}
No hay colores disponibles.
{{/grey}}
</section>

### Grey Blue

<section class="grid colors">
{{#greyBlue}}
<div class="grid-item">
  <div class="grid-item-header" style="background-color:{{{codeHex}}}">
  </div>
  <div class="grid-item-body">
      <span>{{name}}</span>
      <span>{{codeHex}}</span>
      <span>{{codeRgb}}</span>
  </div>
  <div class="grid-item-footer">
    <button class="button copy" data-clipboard-text="{{{codeHex}}}" aria-label="Copied!">Copy HEX</button>
    <button class="button copy" data-clipboard-text="{{{codeRgb}}}" aria-label="Copied!">Copy RGB</button>
  </div>
</div>
{{/greyBlue}}
</section>

#### Mustache template (greyBlue)

{{=<% %>=}}
```
<section class="grid colors">
{{#greyBlue}}
<div class="grid-item">
  <div class="grid-item-header" style="background-color:{{{codeHex}}}">
  </div>
  <div class="grid-item-body">
      <span>{{name}}</span>
      <span>{{codeHex}}</span>
      <span>{{codeRgb}}</span>
  </div>
  <div class="grid-item-footer">
    <button class="button copy" data-clipboard-text="{{{codeHex}}}" aria-label="Copied!">Copy HEX</button>
    <button class="button copy" data-clipboard-text="{{{codeRgb}}}" aria-label="Copied!">Copy RGB</button>
  </div>
</div>
{{/greyBlue}}
</section>

```
<%={{ }}=%>

#### Mustache template (grey)

{{=<% %>=}}
```
<section class="grid colors">
{{#grey}}
<div class="grid-item">
  <div class="grid-item-header" style="background-color:{{{codeHex}}}">
  </div>
  <div class="grid-item-body">
      <span>{{name}}</span>
      <span>{{codeHex}}</span>
      <span>{{codeRgb}}</span>
  </div>
  <div class="grid-item-footer">
    <button class="button copy" data-clipboard-text="{{{codeHex}}}" aria-label="Copied!">Copy HEX</button>
    <button class="button copy" data-clipboard-text="{{{codeRgb}}}" aria-label="Copied!">Copy RGB</button>
  </div>
</div>
{{/grey}}
</section>

```
<%={{ }}=%>


#### External JSON file

<a href="content/data/colors.json" target="_blank">File colors.json</a>

```json
{
"grey": [
  { "name": "grey1", 
    "codeHex":"#FAFAFA", 
    "codeRgb":"rgb(255,255,255)"
  },
  { "name": "grey2", 
    "codeHex":"#F7F7F7", 
    "codeRgb":"rgb(255,255,255)"
  },
  { "name": "grey3", 
    "codeHex":"#EDEDED", 
    "codeRgb":"rgb(255,255,255)"
  },
  { "name": "grey4", 
    "codeHex":"#CCCCCC", 
    "codeRgb":"rgb(255,255,255)"
  },
  { "name": "grey5", 
    "codeHex":"#B3B3B3", 
    "codeRgb":"rgb(255,255,255)"
  },
  { "name": "grey6", 
    "codeHex":"#707070", 
    "codeRgb":"rgb(255,255,255)"
  },
  { "name": "grey7", 
    "codeHex":"#474747", 
    "codeRgb":"rgb(255,255,255)"
  },
  { "name": "grey8", 
    "codeHex":"#262626", 
    "codeRgb":"rgb(255,255,255)"
  },
  { "name": "grey9", 
    "codeHex":"#1A1A1A", 
    "codeRgb":"rgb(255,255,255)"
  }
],
"greyBlue": [
  { "name": "greyblue1", 
    "codeHex":"#F4F5FB", 
    "codeRgb":"rgb(255,255,255)"
  },
  { "name": "greyblue2", 
    "codeHex":"#F0F2FA", 
    "codeRgb":"rgb(255,255,255)"
  },
  { "name": "greyblue3", 
    "codeHex":"#E4E9F6", 
    "codeRgb":"rgb(255,255,255)"
  },
  { "name": "greyblue4", 
    "codeHex":"#C2C9D6", 
    "codeRgb":"rgb(255,255,255)"
  },
  { "name": "greyblue5", 
    "codeHex":"#A3ADC2", 
    "codeRgb":"rgb(255,255,255)"
  },
  { "name": "greyblue6", 
    "codeHex":"#8592AD", 
    "codeRgb":"rgb(255,255,255)"
  },
  { "name": "greyblue7", 
    "codeHex":"#47536B", 
    "codeRgb":"rgb(255,255,255)"
  },
  { "name": "greyblue8", 
    "codeHex":"#29303D", 
    "codeRgb":"rgb(255,255,255)"
  },
  { "name": "greyblue9", 
    "codeHex":"#1F242E", 
    "codeRgb":"rgb(255,255,255)"
  }
]
}
```

## Icons

Loop from file `icons.json` using Docsify Mustache plugin:

<!-- Swanix icons assets -->
<link href="https://cdn.jsdelivr.net/gh/swanix/icons/dist/swanix-icons.css" rel="stylesheet" />

<!-- Mustache section loop -->
<section class="grid five-columns">
{{#icons}}
<div class="grid-item">
  <div class="grid-item-body">
    <svg class="icon huge">
      <use href="assets/images/swanix-icons.svg#{{{name}}}"></use>
    </svg>
    <span>{{{name}}}</span>
  </div>
  <div class="grid-item-footer">
    <button class="button copy" data-clipboard-text="{{{name}}}" aria-label="Copied!">Copy</button>
  </div>
</div>
{{/icons}}
{{^icons}}
No icons
{{/icons}}
</section>

#### External file `icons.json`

```json
{"icons": [
  { "name": "home" },
  { "name": "menu" },
  { "name": "settings" },
  { "name": "arrow-left" },
  { "name": "arrow-right" },
  { "name": "plus" },
  { "name": "minus" },
  { "name": "close" },
  { "name": "edit" },
  { "name": "search" },
  { "name": "email" },
  { "name": "caret-up" },
  { "name": "caret-down" },
  { "name": "upload" },
  { "name": "download" },
  { "name": "delete" },
  { "name": "code" },
  { "name": "help" },
  { "name": "check" },
  { "name": "info" },
  { "name": "view-grid" },
  { "name": "sync" },
  { "name": "social-instagram" },
  { "name": "social-youtube" },
  { "name": "social-linkedin" },
  { "name": "social-whatsapp" },
  { "name": "social-twitter" },
  { "name": "social-facebook" },
  { "name": "social-vimeo" },
  { "name": "social-pinterest" },
  { "name": "social-github" },
  { "name": "social-dribbble" }
]
}
```