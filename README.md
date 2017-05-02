# Modular Scale Tool

The Modular Scale tool contains a function that helps you create sizes based on modular scale.


### Installation

```
npm install --save iotacss-tools-ms
```


### Options

```scss
$iota-ms-base   : 15px !default;
$iota-ms-ratio  : 1.2 !default;
$iota-ms-digits : 3 !default;
```


### Function Syntax

```sass
@include iota-ms($increment,
  $base   : $iota-ms-base,
  $ratio  : $iota-ms-ratio,
  $digits : $iota-ms-digits
);
```


### Parameters

* increment: unitless number - Number of steps to increment up or down the scale
* base: number - The base value the scale starts at. Defaults to  $iota-ms-base;
* ratio: unitless number - The ratio the scale is built on. Defaults to $iota-ms-ratio.
* digits: unitless number - Number of digits the ms value will be rounded to. Defaults to $iota-ms-digits.


## Examples


### Modular scale with 16px base, 1.5 ratio rounded to 2 digits

You can either adjust the default options:

```sass
$iota-ms-base   : 16px;
$iota-ms-ratio  : 1.5;
$iota-ms-digits : 2;

.h1 {
  font-size: iota-ms(2); // 36px
}
```

or you can just pass the options directly to the function:

```css
.h1 {
  font-size: iota-ms(2, 16px, 1.5, 2); // 36px
}
```
