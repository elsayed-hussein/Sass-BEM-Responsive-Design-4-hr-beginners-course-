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

```scss
:root {
  --background-color: hsl(0, 0%, 11%);
}
```

to call or load a variable

```scss
body {
  background-color: var(--background-color);
}
```
