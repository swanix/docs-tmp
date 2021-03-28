<figure class="hero" style="--hero-image:url(https://source.unsplash.com/g-YsyUUwT9M/1800x600);"></figure>

# Example 3

## Colors

Loop from external file `colors.json` using Docsify Mustache plugin:

<section class="grid">
{{#colors}}
<div class="grid-item">
<div class="grid-item-body" style="background-color:{{{codeHex}}}">
  <h4 class="{{{labelText}}}">{{codeHex}}</h4>
  <span class="{{{labelText}}}">{{sassVar}}</span>
</div>
<div class="grid-item-footer">
  <button class="copy" data-clipboard-text="{{{codeHex}}}">Copy HEX</button>
  <button class="copy" data-clipboard-text="{{{codeRgb}}}">Copy RGB</button>
  <button class="copy" data-clipboard-text="{{{sassVar}}}">Copy Sass</button>
</div>
</div>
{{/colors}}
{{^colors}}
No icons
{{/colors}}
</section>

#### External file `colors.json`

```json
{"colors": [
  { "name": "Brand-1", "sassVar":"$brand-1", "codeHex":"#4D62A4", "codeRgb":"rgb(255,255,255)", "labelText":"text-light" },
  { "name": "Brand-2", "sassVar":"$brand-2", "codeHex":"#87A2BD", "codeRgb":"rgb(255,255,255)", "labelText":"text-light" },
  { "name": "Brand-3", "sassVar":"$brand-3", "codeHex":"#4A5374", "codeRgb":"rgb(255,255,255)", "labelText":"text-light" },
  { "name": "Brand-4", "sassVar":"$brand-4", "codeHex":"#9AA4BF", "codeRgb":"rgb(255,255,255)", "labelText":"text-light" },
  { "name": "Brand-5", "sassVar":"$brand-5", "codeHex":"#04C29C", "codeRgb":"rgb(255,255,255)", "labelText":"text-light" },
  { "name": "Brand-6", "sassVar":"$brand-6", "codeHex":"#38445C", "codeRgb":"rgb(255,255,255)", "labelText":"text-light" }
]
}
```


## Icons

Loop from external file `icons.json` using Docsify Mustache plugin:

<section class="grid five-columns">
{{#icons}}
<div class="grid-item">
<div class="grid-item-body">
  <svg class="icon huge">
  <use href="#{{{name}}}"></use>
  </svg>
  <span>{{{name}}}</span>
</div>
<div class="grid-item-footer">
  <button class="copy" data-clipboard-text="{{{name}}}">Copy name</button>
  <!-- <button>Download</button> -->
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