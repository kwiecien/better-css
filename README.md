# CSS

CSS3 and SASS examples from Pluralsight courses:

- https://app.pluralsight.com/library/courses/better-css/
- https://app.pluralsight.com/library/courses/css3-in-depth/

## A Better CSS: LESS and SASS

LESS and SASS can style sheets more readable, maintainable and easier to write.

### Examples

```scss
// mixins.scss
@mixin rounded-corners($size: 5px) {
  border-radius: $size;
  -moz-border-radius: $size;
  -webkit-border-radius: $size;
}
```

```scss
// My.scss
@import "mixins";
```

```scss
@function center-width($gutter) {
  @return $app-size - ($gutter * 2);
}
```

```scss
#container {
  @include rounded-corners;
  color: lighten($mainColor, 50%);
  width: center-width(100px);
}
```

```scss
@for $colNumber from 2 through 5 {
  .col-#{$colNumber} {
    width: ($app-size / $colNumber) - 10px;
  }
}
```

```scss
header h1
{
  @extend nav;
  font-size: 24px;
  font-family: 'Share', cursive;
  color: Blue;
}
nav
{
  ...
}
```

```scss
h1 {
  @if $size > 14px {
    color: Blue;
  } @else @if $size < 14px {
    color: Red;
  } @else {
    color: Green;
  }
}
```

## CSS3 In-Depth

Learn how deep the CSS3 rabbit hole goes in this jam-packed course with CSS
luminary Estelle Weyl. Estelle dives deep into the various components of CSS3
including: selectors, specificity, generated content, media queries, debugging,
colors,...
