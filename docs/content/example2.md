<figure class="hero" style="--hero-image:url(https://source.unsplash.com/g-YsyUUwT9M/1800x600);"></figure>

# Mustache

Examples using Docsify Mustache plugin to create visual content from external data `colors.json` and `icons.json`

```js
// Add to Docsify configuration
window.$docsify = {
  // ...
  mustache: {
    data: [
      'path/to/colors.json',
      'path/to/icons.json'
    ]
  }
};
```


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

## Colors

<!-- tabs:start -->

#### ** Result **

<section class="grid colors">
{{#grey}}
<div class="grid-item">
  <div class="grid-item-header" style="background-color:{{{codeHex}}}">
  </div>
  <div class="grid-item-body">
      <h4 id="color-{{{name}}}">{{name}}</h4>
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

#### ** Mustache **

{{=<% %>=}}
```
<section class="grid colors">
{{#grey}}
<div class="grid-item">
  <div class="grid-item-header" style="background-color:{{{codeHex}}}">
  </div>
  <div class="grid-item-body">
      <h4 id="color-{{{name}}}">{{name}}</h4>
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

#### ** JSON **

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
]
}
```
<!-- tabs:end -->

## Icons

<!-- tabs:start -->

#### ** Result **

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
</section>

#### ** Mustache **

{{=<% %>=}}
```
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
</section>

```
<%={{ }}=%>

#### ** JSON **

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

<!-- tabs:end -->