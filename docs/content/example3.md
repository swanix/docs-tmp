<figure class="hero" style="--hero-image:url(https://source.unsplash.com/g-YsyUUwT9M/1800x600);"></figure>

# Other

## Chinese characters

Data from https://hanzien.github.io/cards

<section class="grid list" style="filter: invert(1);">
{{#characters}}
<div class="grid-item">
  <div class="grid-item-body">
      <h2>{{hanzi}}</h2>
      <h3  class="pinyin">{{pinyin}}</h3>
      <span class="name">{{meaning}}</span>
  </div>
  <div class="grid-item-footer">
    <button class="button copy" data-clipboard-text="{{{hanzi}}}" aria-label="Copied!">Copy</button>
  </div>
</div>
{{/characters}}
</section>