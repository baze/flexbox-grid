# Flexbox Grid
- Dynamic flexbox based grid system using CSS custom properties, breakpoints and NO media-queries.
- 1.81kb minified. 
- Very much inspired by @heydonworks' article: http://www.heydonworks.com/article/the-flexbox-holy-albatross

## 1. Configuring the grid

```css
:root {
/*grid configuration*/
--columns: 12;
--margin: 12px;
--maxwidth: 40em;
--multiplier: calc( var(--maxwidth) - 100%); /*this is your breakpoint without media queries */
}
```

## 2. Usage

### Case 1: equally sized items

```html
<div class="grid-container grid-4">
	<div class="some-item"></div>
	<div class="some-item"></div>
	<div class="some-item"></div>
	<div class="some-item"></div>
	<div class="some-item"></div>
	<div class="some-item"></div>
	<div class="some-item"></div>
	<div class="some-item"></div>
	<div class="some-item"></div>
	<div class="some-item"></div>
	<div class="some-item"></div>
	<div class="some-item"></div>
</div>
```
### Case 2: differently sized items

```html
<div class="grid-container">
<!-- half size -->
	<div class="some-item columns-6"></div>
	<div class="some-item columns-6"></div>
<!-- one-third -->
	<div class="some-item columns-4"></div>
	<div class="some-item columns-4"></div>
	<div class="some-item columns-4"></div>
<!-- one sixth -->
	<div class="some-item columns-2"></div>
	<div class="some-item columns-2"></div>
	<div class="some-item columns-2"></div>
	<div class="some-item columns-2"></div>
	<div class="some-item columns-2"></div>
	<div class="some-item columns-2"></div>
<!-- full size -->
	<div class="some-item columns-12"></div>
</div>
```