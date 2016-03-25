## Modern Sass BEM Grid for Foundation 6

A Modern Sass [BEM](http://getbem.com/) Grid for Zurb Foundation for Sites 6, inspired by [Avalanche](http://colourgarden.net/avalanche/).

### Features
- BEM (Block Element Modifier) logic.
- Fully compatible with [Foundation for Sites 6](https://github.com/zurb/foundation-sites/).
- Uses Zurb Foundation breakpoint convention
- No bloat. Only create the selectors you'll actually use
- No duplication. 1/2 == 2/4 so why create two selectors?
- No floats. No clears. No .last
- Nesting to infinity and beyond

## Installation

### Using Bower

`bower install --save foundation-bem-grid`

### Using NPM

`npm install --save foundation-bem-grid`

## Usage

Example of your main `app.scss` file:

```sass
@import "node_modules/foundation-bem-grid/scss/bem-grid";

@include foundation-bem-grid;
```

Example of a two column, responsive, centered grid. All grid layout classes and responsive width classes are modifiers.

```
<div class="grid grid--center">
  <div class="3/4 1/2--small grid__cell"></div>
  <div class="1/4 1/2--small grid__cell"></div>
</div>
```

## Settings

**`$grid-namespace`**  
Global prefix for layout and cell class names. Default: `grid`.

**`$grid-gutter`**  
Map of gutter width between cells for each breakpoint. To use just one size, set the variable to a number instead of a map. Default: `20px`.

**`$grid-width-class`**  
Prefix for width class names. Default: `''`.

**`$grid-width-class-style`**  
Naming style of width classes. Default: `'fraction'`. Options: `fraction` (1/2, 3/4 etc), `percentage` (25, 50 etc), `fragment` (1-of-3, 4-of-5 etc).  

**`$grid-widths`**  
Max width of the grid when used as --container. Default: `$global-width`.

**`$grid-responsive`**
Enable/disable the inclusion of responsive width classes. Default: `true`.
