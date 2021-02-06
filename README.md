# mdc-css-utils

This package is inspired by [Bootstrap utility styles](https://getbootstrap.com/docs/5.0/utilities/borders/) and implements very similar set of CSS classes for 
[Material Components for web (MDC)](https://material.io/develop/web).

Why not use Bootstrap's utility styles? Or some stand-alone package?

Nothing prevents from using some other utility styles package because MDC is highly compatible with other frameworks. However there are these reasons why you might need this package:
1. Often Material design apps don't use Bootstrap, but you still need those utility styles.
2. Other packages has their own breakpoints system.


- [Styles](#styles)
  - [Class naming](#class-naming)
  - [Display](#display)


## Styles


### Class naming

Class names are basically the same as in Bootstrap, with a little bit of MDC flavor. Lets review an example: `.mdx-d--flex-desktop`:

1. Class name starts with `.mdx-` prefix. _mdx_ stands for _Material Design Extensions_. Having prefix makes it easy finding all usages of this package.
2. `d--flex` corresponds with Bootstrap's [`d-flex`](https://getbootstrap.com/docs/5.0/utilities/display/). But since we follow BEM naming, we separate `flex` with double dash. BEM naming is used to be inline with other MDC packages.
3. At the end there is optional `-desktop`, `-tablet` or `-phone`. It is basically similar to `lg`, `md` and `sm` in Bootstrap, but follows MDC pattern for naming such classes.


Breakpoints:
- `phone`
- `tablet`
- `desktop`

Classes without breakpoint apply to all breakpoints.

Styles behavior is very similar to [Bootstrap's Utility](https://getbootstrap.com/docs/5.0/utilities/borders/) styles with a few differences:

- in Bootstrap class with breakpoint applies to the breakpoint and above breakpoints. In MDC class with breakpoint applies to specified breakpoint only.

Here is list of CSS classes:

CSS Class | Description | Example
--- | --- | ---
`mdx-d--<DISPLAY_VALUE>`<br>`mdx-d--<DISPLAY_VALUE>-<TYPE_OF_DEVICE>` | DISPLAY_VALUE: none, inline, inline-block, block, grid, table, table-cell, table-row, flex, inline-flex. | `mdx-d--flex`<br>`mdx-d--flex-tablet`
`mdx-align-items--<ALIGN_TYPE>`<br>`mdx-align-items--<ALIGN_TYPE>-<TYPE_OF_DEVICE>` | ALIGN_TYPE: start, end, center, baseline, stretch. | `mdx-align-items--center`<br>`mdx-align-items--center-phone`
`mdx-p--<N>`<br>`mdx-p--<N>-<TYPE_OF_DEVICE>`<br>`mdx-pt--<N>`<br>`mdx-pt--<N>-<TYPE_OF_DEVICE>`<br>`mdx-pr--<N>`<br>`mdx-pr--<N>-<TYPE_OF_DEVICE>`<br>`mdx-pb--<N>`<br>`mdx-pb--<N>-<TYPE_OF_DEVICE>`<br>`mdx-pl--<N>`<br>`mdx-pl--<N>-<TYPE_OF_DEVICE>`<br>`mdx-px--<N>`<br>`mdx-px--<N>-<TYPE_OF_DEVICE>`<br>`mdx-py--<N>`<br>`mdx-py--<N>-<TYPE_OF_DEVICE>`<br> | &lt;N&gt;: value from 0 to 5. Each step is **8px**. | `mdx-p--2`<br>`mdx-p--2-tablet`<br>`mdx-pt--1`<br>`mdx-pt--1-desktop`<br>`mdx-pr--0`<br>`mdx-pr--0-phone`<br>`mdx-pb--2`<br>`mdx-pb--2-phone`<br>`mdx-pl--3`<br>`mdx-pl--3-phone`<br>`mdx-px--2`<br>`mdx-px--2-desktop`<br>`mdx-py--1`<br>`mdx-py--1-phone`
`mdx-m--<N>`<br>`mdx-m--<N>-<TYPE_OF_DEVICE>`<br>`mdx-mt--<N>`<br>`mdx-mt--<N>-<TYPE_OF_DEVICE>`<br>`mdx-mr--<N>`<br>`mdx-mr--<N>-<TYPE_OF_DEVICE>`<br>`mdx-mb--<N>`<br>`mdx-mb--<N>-<TYPE_OF_DEVICE>`<br>`mdx-ml--<N>`<br>`mdx-ml--<N>-<TYPE_OF_DEVICE>`<br>`mdx-mx--<N>`<br>`mdx-mx--<N>-<TYPE_OF_DEVICE>`<br>`mdx-my--<N>`<br>`mdx-my--<N>-<TYPE_OF_DEVICE>`<br> | &lt;N&gt;: value from 0 to 5. Each step is **8px**.

### Display

Change the value of the `display` property. The classes are named using the format:

- `.mdx-d--{value}`
- `.mdx-d--{value}-{breakpoint}`

Where value is one of:
- `none`
- `inline`
- `inline-block`
- `block`
- `grid`
- `table`
- `table-cell`
- `table-row`
- `flex`
- `inline-flex`

Examples: `.mdx-d--flex .mdx-d--none-desktop` - sets `display:flex`, but hides the element on desktop screen size.


