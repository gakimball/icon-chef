# Icon Chef

Cook up the most absurd navigation icons you can think of with icon chef.

## Compatability

Works with:

- Sass 3.3
- Sass 3.4

Haven't tested it in libsass yet, hang on! But you would need that list maps polyfill.

## Usage

```html
<div class="icon">
  <span></span>
</div>
```

```scss
.icon {
  @include hamburger($width, $height, $weight, $bars, $toppings, $bgColor, $hoverBg);
}
```

## Settings

- **$width:** Width of the icon.
- **$height:** Height of the icon.
- **$weight:** Height of each bar in the icon.
- **$bars:** Number of bars to use.
- **$toppings:** Spruce up your hamburger with fresh ingredients! (see below)
- **$bgColor:** Color of the icon.
- **$hoverBg:** Color of the icon when you hover over it.

### Toppings

The `$toppings` variable accepts a list of toppings which will be placed between two bars of fresh bread. Adding toppings will override the `$bars`, `$bgColor`, and `$hoverBg` settings. Current available toppings are:

- Bread
- Meat
- Lettuce
- Tomato
- Onion

Note that two slices of bread are added to the top and bottom automatically, so the below code will produce an icon with four bars:

```scss
  @include hamburger($toppings: meat lettuce);
```
