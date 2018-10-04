# GridKit

Lightweight Sass grid framework.

## Installation

```shell
npm install gridkit
```

Import the main file into your project to use the available tools:

```scss
@import "./node_modules/gridkit/core/gridkit";
```

**Optional:** Import the utility classes into your project:

```scss
@import "./node_modules/gridkit/core/utilities";
```

See **Usage** below for instructions on how to override defaults.

## Usage

### Variables

The following variables can be overidden in your project. If using the utility classes, these variables should be changed before the utility classes are imported:

```scss
$breakpoint: 896px !default;
$gutter: 20px !default;
```

The column width variables should not be overridden:

```scss
$one-half: calc((100% - (#{$gutter} * 1)) / 2);
$one-third: calc((100% - (#{$gutter} * 2)) / 3);
$one-fourth: calc((100% - (#{$gutter} * 3)) / 4);
$one-fifth: calc((100% - (#{$gutter} * 4)) / 5);
$one-sixth: calc((100% - (#{$gutter} * 5)) / 6);
$one-seventh: calc((100% - (#{$gutter} * 6)) / 7);
$one-eighth: calc((100% - (#{$gutter} * 7)) / 8);
$one-ninth: calc((100% - (#{$gutter} * 8)) / 9);
$one-tenth: calc((100% - (#{$gutter} * 9)) / 10);
$one-eleventh: calc((100% - (#{$gutter} * 10)) / 11);
$one-twelfth: calc((100% - (#{$gutter} * 11)) / 12);
$two-thirds: calc(#{$one-third} * 2 + #{$gutter});
$two-fourths: calc(#{$one-fourth} * 2 + #{$gutter});
$two-fifths: calc(#{$one-fifth} * 2 + #{$gutter});
$two-sixths: calc(#{$one-sixth} * 2 + #{$gutter});
$two-sevenths: calc(#{$one-seventh} * 2 + #{$gutter});
$two-eighths: calc(#{$one-eighth} * 2 + #{$gutter});
$two-ninths: calc(#{$one-ninth} * 2 + #{$gutter});
$two-tenths: calc(#{$one-tenth} * 2 + #{$gutter});
$two-elevenths: calc(#{$one-eleventh} * 2 + #{$gutter});
$two-twelfths: calc(#{$one-twelfth} * 2 + #{$gutter});
$three-fourths: calc(#{$one-fourth} * 3 + (#{$gutter} * 2));
$three-fifths: calc(#{$one-fifth} * 3 + (#{$gutter} * 2));
$three-sixths: calc(#{$one-sixth} * 3 + (#{$gutter} * 2));
$three-sevenths: calc(#{$one-seventh} * 3 + (#{$gutter} * 2));
$three-eighths: calc(#{$one-eighth} * 3 + (#{$gutter} * 2));
$three-ninths: calc(#{$one-ninth} * 3 + (#{$gutter} * 2));
$three-tenths: calc(#{$one-tenth} * 3 + (#{$gutter} * 2));
$three-elevenths: calc(#{$one-eleventh} * 3 + (#{$gutter} * 2));
$three-twelfths: calc(#{$one-twelfth} * 3 + (#{$gutter} * 2));
$four-fifths: calc(#{$one-fifth} * 4 + (#{$gutter} * 3));
$four-sixths: calc(#{$one-sixth} * 4 + (#{$gutter} * 3));
$four-sevenths: calc(#{$one-seventh} * 4 + (#{$gutter} * 3));
$four-eighths: calc(#{$one-eighth} * 4 + (#{$gutter} * 3));
$four-ninths: calc(#{$one-ninth} * 4 + (#{$gutter} * 3));
$four-tenths: calc(#{$one-tenth} * 4 + (#{$gutter} * 3));
$four-elevenths: calc(#{$one-eleventh} * 4 + (#{$gutter} * 3));
$four-twelfths: calc(#{$one-twelfth} * 4 + (#{$gutter} * 3));
$five-sixths: calc(#{$one-sixth} * 5 + (#{$gutter} * 4));
$five-sevenths: calc(#{$one-seventh} * 5 + (#{$gutter} * 4));
$five-eighths: calc(#{$one-eighth} * 5 + (#{$gutter} * 4));
$five-ninths: calc(#{$one-ninth} * 5 + (#{$gutter} * 4));
$five-tenths: calc(#{$one-tenth} * 5 + (#{$gutter} * 4));
$five-elevenths: calc(#{$one-eleventh} * 5 + (#{$gutter} * 4));
$five-twelfths: calc(#{$one-twelfth} * 5 + (#{$gutter} * 4));
$six-sevenths: calc(#{$one-seventh} * 6 + (#{$gutter} * 5));
$six-eighths: calc(#{$one-eighth} * 6 + (#{$gutter} * 5));
$six-ninths: calc(#{$one-ninth} * 6 + (#{$gutter} * 5));
$six-tenths: calc(#{$one-tenth} * 6 + (#{$gutter} * 5));
$six-elevenths: calc(#{$one-eleventh} * 6 + (#{$gutter} * 5));
$six-twelfths: calc(#{$one-twelfth} * 6 + (#{$gutter} * 5));
$seven-eighths: calc(#{$one-eighth} * 7 + (#{$gutter} * 6));
$seven-ninths: calc(#{$one-ninth} * 7 + (#{$gutter} * 6));
$seven-tenths: calc(#{$one-tenth} * 7 + (#{$gutter} * 6));
$seven-elevenths: calc(#{$one-eleventh} * 7 + (#{$gutter} * 6));
$seven-twelfths: calc(#{$one-twelfth} * 7 + (#{$gutter} * 6));
$eight-ninths: calc(#{$one-ninth} * 8 + (#{$gutter} * 7));
$eight-tenths: calc(#{$one-tenth} * 8 + (#{$gutter} * 7));
$eight-elevenths: calc(#{$one-eleventh} * 8 + (#{$gutter} * 7));
$eight-twelfths: calc(#{$one-twelfth} * 8 + (#{$gutter} * 7));
$nine-tenths: calc(#{$one-tenth} * 9 + (#{$gutter} * 8));
$nine-elevenths: calc(#{$one-eleventh} * 9 + (#{$gutter} * 8));
$nine-twelfths: calc(#{$one-twelfth} * 9 + (#{$gutter} * 8));
$ten-elevenths: calc(#{$one-eleventh} * 10 + (#{$gutter} * 9));
$ten-twelfths: calc(#{$one-twelfth} * 10 + (#{$gutter} * 9));
$eleven-twelfths: calc(#{$one-twelfth} * 11 + (#{$gutter} * 10));
```

### Mixins

#### Grid

```scss
.grid {

    @include grid();
}
```

Outputs:

```css
.grid {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;

    > div {
        margin-right: 0;
        margin-left: 0;
    }
}
```

#### Column

```scss
.column {

    @include column(one-third);
}
```

Outputs:

```css
.column {
    width: calc((100% - (#{$gutter} * 1)) / 2);
}
```


## Contributing

Command to compile Sass:

```shell
sass core/__index.scss:gridkit.css --style compressed
```