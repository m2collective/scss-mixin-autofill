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

.demo {
    @include autofill((active, hover, focus)) {
        box-shadow: 0 0 0 9999px white inset !important;
        -webkit-text-fill-color: black !important;
    }
}

// Return

.demo:autofill{
    -webkit-text-fill-color:#000!important;
    box-shadow:inset 0 0 0 9999px #fff!important
}

.demo:autofill:active{
    -webkit-text-fill-color:#000!important;
    box-shadow:inset 0 0 0 9999px #fff!important
}

.demo:autofill:focus{
    -webkit-text-fill-color:#000!important;
    box-shadow:inset 0 0 0 9999px #fff!important
}

.demo:autofill:hover{
    -webkit-text-fill-color:#000!important;
    box-shadow:inset 0 0 0 9999px #fff!important
}
```

## Mixins

The package contains the following mixins to use:

| Name                    | Variables      |
|-------------------------|----------------|
| autofill                | actions        |
| autofillDisable         | actions        |
| autofillBackgroundColor | color, actions |
| autofillTextColor       | color, actions |

## License

The MIT License (MIT). Please see the [License file](LICENSE.txt) for more information.
