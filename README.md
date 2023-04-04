# Sass-BEM-Responsive-Design-4-hr-beginners-course-

## what is Sass

syntactically awesome style sheets

```css sass
html
    box-sizing: border-box
    font-size: 100%
```

```scss
html {
  box-sizing: border-box;
  font-size: 100%;
}
```

## sass partials

name the partial file with "\_"
and import it into the main \_index.scss file in the same folder with

```scss
@forward "fileNmeWithOut_orScss";
```

and import it into the main scss file with

```scss
@forward "folderName";
```

## sass variables

set the variables at the root to override all variables

to set the variable

```css
:root {
  --background-color: hsl(0, 0%, 11%);
}
```

to call or load a variable

```css
body {
  background-color: var(--background-color);
}
```

or with scss

to set the variable

```scss
$font: "Open Sans", sans-serif;
```

to call or load a variable

```css
@use "../util" as u;
body {
  font-family: u.$font;
}
```

## scss nesting

```scss
.grid {
  &__main {
  }
}
```

for

```scss
.grid {
  .grid__main {
  }
}
```

## mixins and builtIn modules

to make mixin

```scss
// 700px(43.75em) ,900px(56.25em),1440px(90em)
$breakpoints-up: (
  "medium": 43.75em,
  "large": 56.25em,
  "xlarge": 90em,
);

@mixin breakpoint($size) {
  @media (min-width: map-get($breakpoints-up,$size)) {
    @content;
  }
}
```

to use mixin

```scss
@use "../util" as u;
@include u.breakpoint(large) {
}
```
