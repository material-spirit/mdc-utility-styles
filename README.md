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

CSS&nbsp;Class&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | Description
--- | ---
`mdx-d--<VALUE>`<br>`mdx-d--<VALUE>-<DEVICE>` | Change the value of the `display` CSS property.<br>VALUE: none, inline, inline-block, block, grid, table, table-cell, table-row, flex, inline-flex.<br><br>Examples:<br>`mdx-d--flex`<br>`mdx-d--flex-tablet`<br><br>Bootstrap Docs: [Display](https://getbootstrap.com/docs/5.0/utilities/display/)
`mdx-p--<N>`<br>`mdx-p--<N>-<DEVICE>`<br>`mdx-pt--<N>`<br>`mdx-pt--<N>-<DEVICE>`<br>`mdx-pr--<N>`<br>`mdx-pr--<N>-<DEVICE>`<br>`mdx-pb--<N>`<br>`mdx-pb--<N>-<DEVICE>`<br>`mdx-pl--<N>`<br>`mdx-pl--<N>-<DEVICE>`<br>`mdx-px--<N>`<br>`mdx-px--<N>-<DEVICE>`<br>`mdx-py--<N>`<br>`mdx-py--<N>-<DEVICE>`<br> | Classes that set `padding`.<br>N - value from 0 to 5. Each step is **8px**.<br><br>Examples:<br>`mdx-p--2`<br>`mdx-p--2-tablet`<br>`mdx-pt--1`<br>`mdx-pt--1-desktop`<br>`mdx-px--2`<br>`mdx-px--2-desktop`<br><br>Bootstrap Docs: [Spacing. Margin and padding](https://getbootstrap.com/docs/5.0/utilities/spacing/#margin-and-padding)
`mdx-m--<N>`<br>`mdx-m--<N>-<DEVICE>`<br>`mdx-mt--<N>`<br>`mdx-mt--<N>-<DEVICE>`<br>`mdx-mr--<N>`<br>`mdx-mr--<N>-<DEVICE>`<br>`mdx-mb--<N>`<br>`mdx-mb--<N>-<DEVICE>`<br>`mdx-ml--<N>`<br>`mdx-ml--<N>-<DEVICE>`<br>`mdx-mx--<N>`<br>`mdx-mx--<N>-<DEVICE>`<br>`mdx-my--<N>`<br>`mdx-my--<N>-<DEVICE>`<br> | Classes that set `margin`.<br>N - value from 0 to 5. Each step is **8px**.<br><br>Examples:<br>`mdx-m--2`<br>`mdx-m--2-tablet`<br>`mdx-mt--1`<br>`mdx-mt--1-desktop`<br>`mdx-mx--2`<br>`mdx-mx--2-desktop`<br><br>Bootstrap Docs: [Spacing. Margin and padding](https://getbootstrap.com/docs/5.0/utilities/spacing/#margin-and-padding)
`mdx-border--<SIDE>`<br>`mdx-border--<SIDE>-<DEVICE>` | Classes to add or remove an element’s borders. Border is always 1px solid. Color equals to Data table's stroke color.<br>SIDE: bottom, top, left, right.<br><br>Examples:<br>`mdx-border--top`<br>`mdx-border--bottom-tablet`<br><br>Bootstrap Docs: [Borders](https://getbootstrap.com/docs/5.0/utilities/borders/)
`mdx-theme--<COLOR_STYLE>-<EMPHASIS>` | MDC has a set of classes to set text color: `mdc-theme--primary`, `mdc-theme--secondary`, etc. These new classes extend the set with variations of main theme colors: high, medium, disabled. It is achieved by applying [emphasis opacity](https://github.com/material-components/material-components-web/tree/master/packages/mdc-theme#themetext-emphasisemphasis) on target color.<br>COLOR_STYLE: primary, on-primary, secondary, on-secondary, on-surface.<br>EMPHASIS: high, medium, disabled.<br><br>Examples:<br>`mdx-theme--primary-medium`<br>`mdx-theme--secondary-disabled`


Flex utility CSS classes

CSS&nbsp;Class&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | Description
--- | ---
`mdx-flex-grow--<VALUE>`<br>`mdx-flex-grow--<VALUE>-<DEVICE>` | Use these utilities to toggle a flex item’s ability to grow to fill available space.<br>VALUE: 0 or 1.<br><br>Examples:<br>`mdx-flex-grow--1`<br>`mdx-flex-grow--0`<br>`mdx-flex-grow--0-tablet`<br><br>Bootstrap Docs: [Grow and shrink](https://getbootstrap.com/docs/5.0/utilities/flex/#grow-and-shrink)
`mdx-flex-shrink--<VALUE>`<br>`mdx-flex-shrink--<VALUE>-<DEVICE>` | Use these utilities to toggle a flex item’s ability to shrink if necessary.<br>VALUE: 0 or 1.<br><br>Examples:<br>`mdx-flex-shrink--1`<br>`mdx-flex-shrink--0`<br>`mdx-flex-shrink--0-tablet`<br><br>Bootstrap Docs: [Grow and shrink](https://getbootstrap.com/docs/5.0/utilities/flex/#grow-and-shrink)
`mdx-align-items--<ALIGN>`<br>`mdx-align-items--<ALIGN>-<DEVICE>` | ALIGN: start, end, center, baseline, stretch.<br><br>Examples:<br>`mdx-align-items--center`<br>`mdx-align-items--center-phone`


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


