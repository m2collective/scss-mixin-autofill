# SCSS Mixin Autofill

A package for integrating a mixin for styling auto-completion of input fields.

![npm](https://img.shields.io/npm/v/@m2collective/scss-mixin-autofill?style=for-the-badge)

___

## Installation

You can install the package automatically using NPM:

```
npm i @m2collective/scss-mixin-autofill
```

## Usage

To use the package, import it into your project:

```scss
@use "@m2collective/scss-mixin-autofill" as *;
```

### Autofill

```scss
@use "@m2collective/scss-mixin-autofill" as *;

.demo {
    @include autofill((active, hover, focus)) {
        box-shadow: 0 0 0 9999px white inset !important;
        -webkit-text-fill-color: black !important;
    }
}

// Return

.demo:autofill{
    -webkit-text-fill-color: #000 !important;
    box-shadow: inset 0 0 0 9999px #fff !important
}

.demo:autofill:active{
    -webkit-text-fill-color: #000 !important;
    box-shadow: inset 0 0 0 9999px #fff !important
}

.demo:autofill:focus{
    -webkit-text-fill-color: #000 !important;
    box-shadow: inset 0 0 0 9999px #fff !important
}

.demo:autofill:hover{
    -webkit-text-fill-color:#000 !important;
    box-shadow: inset 0 0 0 9999px #fff !important
}
```

### AutofillDisable

```scss
@use "@m2collective/scss-mixin-autofill" as *;

.demo {
    @include autofillDisable((active, hover, focus));
}

// Return

.demo:autofill{
    box-shadow: inset 0 0 0 9999px #fff !important
}

.demo:autofill:active{
    box-shadow: inset 0 0 0 9999px #fff !important
}

.demo:autofill:focus{
    box-shadow: inset 0 0 0 9999px #fff !important
}

.demo:autofill:hover{
    box-shadow: inset 0 0 0 9999px #fff !important
}
```

### AutofillBackgroundColor

```scss
@use "@m2collective/scss-mixin-autofill" as *;

.demo {
    @include autofillBackgroundColor(white, (active, hover, focus));
}

// Return

.demo:autofill{
    box-shadow: inset 0 0 0 9999px #fff !important
}

.demo:autofill:active{
    box-shadow: inset 0 0 0 9999px #fff !important
}

.demo:autofill:focus{
    box-shadow: inset 0 0 0 9999px #fff !important
}

.demo:autofill:hover{
    box-shadow: inset 0 0 0 9999px #fff !important
}
```

### AutofillTextColor

```scss
@use "@m2collective/scss-mixin-autofill" as *;

.demo {
    @include autofillTextColor(black, (active, hover, focus));
}

// Return

.demo:autofill{
    -webkit-text-fill-color: #000 !important;
}

.demo:autofill:active{
    -webkit-text-fill-color: #000 !important;
}

.demo:autofill:focus{
    -webkit-text-fill-color: #000 !important;
}

.demo:autofill:hover{
    -webkit-text-fill-color: #000 !important;
}
```

## Changing the namespace

You can change the namespace during mixin import and use the mixin with a different namespace:

```scss
@use "@m2collective/scss-mixin-autofill" as mixin;

.demo {
    @include mixin.autofillDisable;
}

// Return

.demo:autofill{
    box-shadow: inset 0 0 0 9999px #fff!important
}
```

## License

The MIT License (MIT). Please see the [License file](LICENSE.txt) for more information.
