# A Better CSS: LESS and SASS

LESS and SASS can style sheets more readable, maintainable and easier to write.

- https://app.pluralsight.com/library/courses/better-css/

# Examples

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
