# mdc-css-utils

This package is inspired by [Bootstrap utility styles](https://getbootstrap.com/docs/5.0/utilities/borders/) and implements very similar set of CSS classes for 
[Material Components for web (MDC)](https://material.io/develop/web).


## Class naming

Class names are basically the same as in Bootstrap, with a little bit of MDC flavor - `mdx-d--flex-desktop`

1. Class name starts with `mdx-` prefix. _mdx_ stands for _Material Design Extensions_. Having prefix makes it easy finding all usages of this package.
2. After prefix we have actual utility class name. In example above it is `d--flex` which corresponds with Bootstrap's [display utilities](https://getbootstrap.com/docs/5.0/utilities/display/). Only we follow BEM naming and separate modifier _flex_ with double dash. BEM naming is used to be inline with main MDC packages.
3. At the end there is optional `-desktop`, `-tablet` or `-phone`. It is basically similar to `lg`, `md` and `sm` in Bootstrap, but follows MDC pattern for naming such classes.



