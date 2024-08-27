# Dash.css

## Overview

**Dash.css** is a simple, lightweight (31 KB gzip) , and highly configurable CSS framework designed to streamline web development. It can be utilized as both a CSS framework and an SCSS framework. This file provides an overview of the available utility classes, organized by their functionality.

To get started, simply copy the `dist/css/dash.min.css` file into your project and embark on your development journey! You can customize the configuration by editing the `src/config.scss` file. For instance, you can change the `$-prefix` variable from `-` to `_`, adjust color names, and more.

To apply your changes, run the following command:

```cmd
npm start
```

Please note that this command will not alter the development file located at `dist/css/dash.css`; instead, it generates a new version of `dist/css/dash.min.css` based on your configurations.

## Version

**Current Version**: 1.0.2

## Utility Classes

### Responsive design

**Description**: Some utility classes can be prefixed with a screen size indicator.

Prefixes: `-sm`, `-md`, `-lg`, `-xl`, `-xxl`

Without prefix: X-Small devices (portrait phones, _Applies to all screen sizes_)

`-sm`: Small devices (landscape phones, _576px and up_)

`-md`: Medium devices (tablets, _768px and up_)

`-lg`: Large devices (desktops, _992px and up_)

`-xl`: X-Large devices (large desktops, _1200px and up_)

`-xxl`: XX-Large devices (larger desktops, _1400px and up_)

### Unstyled Elements

**Description**: Removes default styles from elements, making them appear as normal text.

**Class**: `-unstyled`

```css
.-unstyled,
.-unstyled * {
  text-decoration: none;
  font-weight: normal;
  color: black;
  cursor: default;
  background: transparent;
  box-sizing: border-box;
  box-shadow: none;
  text-shadow: none;
  border: none;
  list-style: none;
  margin: 0;
  padding: 0;
  background-clip: border-box;
  scroll-behavior: smooth;
}
```

### Link

**Classes**: `-link`, `-link-hover`, `-link-focus`

```css
.-link,
.-link-hover:hover,
.-link-focus:focus {
  text-decoration: none;
  cursor: pointer;
  color: #fc598f;
  font-weight: bold;
  display: block;
}
```

### Text Formatting

**Bold Text**: `-t-bold`, `-t-bold-hover`, `-t-bold-focus`

```css
.-t-bold,
.-t-bold-hover:hover,
.-t-bold-focus:focus {
  font-weight: bold;
}
```

**Italic Text**: `-t-italic`, `-t-italic-hover`, `-t-italic-focus`

```css
.-t-italic,
.-t-italic-hover:hover,
.-t-italic-focus:focus {
  font-style: italic;
}
```

**Text Decorations**: `-t-underline`, `-t-overline`, `-t-overline-hover`, `-t-line-through-focus`

```css
.-t-underline,
.-t-underline-hover:hover,
.-t-underline-focus:focus {
  text-decoration: underline;
}
```

### Text Transformations

**Classes**: `-t-lowercase`, `-t-uppercase`, `-t-capitalize`

```css
.-t-lowercase,
.-t-lowercase-hover:hover,
.-t-lowercase-focus:focus {
  text-transform: lowercase;
}
```

### Direction

**Classes**: `-ltr` (_Left to Right_), `-rtl` (_Right to Left_)

```css
.-ltr {
  direction: ltr;
}
.-rtl {
  direction: rtl;
}
```

### Clear

**Clear Classes**: `-clear`, `-clear-right`, `-clear-left`, `-clear-none`, `-clearfix`

```css
.-clearfix:before {
  content: "";
  display: table;
}
.-clearfix:after {
  clear: both;
  content: ".";
  display: block;
  font-size: 0;
  height: 0;
  visibility: hidden;
}
.-clearfix {
  zoom: 1;
  clear: both;
  width: 100%;
  min-height: 0.01px;
}
```

### Box Sizing

**Classes**: `-box-content`, `-box-border`

```css
.-box-content,
.-box-content * {
  box-sizing: content-box;
}
.-box-border,
.-box-border * {
  box-sizing: border-box;
}
```

### Object Fit

**Classes**: `-fit-cover`, `-fit-fill`, `-fit-none`, `-fit-scale-down`

```css
.-fit-cover {
  object-fit: cover;
}
```

### Aspect Ratios

**Classes**: `-aspect-ratio`, `-aspect-video`, `-aspect-square`,

`-aspect-2-1`, `-aspect-3-2`, `-aspect-4-3`, `-aspect-34-21`,

`-aspect-1-2`, `-aspect-2-3`, `-aspect-3-4`, `-aspect-21-34`

```css
.-aspect-ratio {
  aspect-ratio: auto;
}
.-aspect-video {
  aspect-ratio: 16/9;
}
.-aspect-square {
  aspect-ratio: 1/1;
}
.-aspect-2-1 {
  aspect-ratio: 2/1;
}
```

### Positioning

**Classes**: `-pos-absolute`, `-pos-relative`, `-pos-static`, `-pos-fixed`, `-pos-sticky`,

`-pos-l`, `-pos-r`, `-pos-t`, `-pos-b`, `-pos-lt`, `-pos-rt`, `-pos-lb`, `-pos-rb`,

`-pos-0`, `-pos-center`,

`-pos-10`, `-pos-20`, ..., `-pos-100`

```css
.-pos-absolute {
  position: absolute;
}
.-pos-l {
  object-position: left;
}
.-pos-rt {
  object-position: right top;
}
.-pos-0 {
  left: 0;
  right: 0;
  top: 0;
  bottom: 0;
}
.-pos-center {
  margin-left: auto;
  margin-right: auto;
  left: 0;
  right: 0;
  text-align: center;
}
.-pos-10 {
  left: 10%;
  -webkit-transform: translate(-90%, 0);
  transform: translate(-90%, 0);
}
```

### Display Properties

**Classes**: `-d-inline`, `-d-inline-block`, `-d-list-item`, `-d-grid`,

`-sm-d-flex`, `-md-d-blank`, `-lg-d-hidden`, `-lx-d-collapse`

```css
.-d-inline {
  display: inline;
}
/* Ghost element */
.-d-blank,
.-d-blank-hover:hover,
.-d-blank-focus:focus {
  visibility: hidden;
}
/* Hidden element. */
/* For Example, hides a row of a table without resizing its columns. */
.-d-collapse,
.-d-collapse-hover:hover,
.-d-collapse-focus:focus {
  visibility: collapse;
}
```

### Cursor Styles

**Classes**: `-cursor-default`, `-cursor-pointer`, `-cursor-auto`, `-cursor-none`,

`-cursor-help`, `-cursor-progress`, `-cursor-wait`, `-cursor-crosshair`, `-cursor-text`,

`-cursor-row-resize`, `-cursor-col-resize`

```css
.-cursor-default {
  cursor: default;
}
```

### Text Formatters

**Classes**: `-t-break`, `-t-nowrap`, `-t-ellipsis`, `t-single-row`

```css
.-t-ellipsis {
  text-overflow: ellipsis;
}
```

### Font Families

**Classes**: `-font-sans-serif`, `-font-arial`, `-font-helvetica`, `-font-verdana`, `-font-tahoma`,

`-font-arial-black`, `-font-comic-sans-ms`, `-font-trebuchet-ms`, `-font-impact`,`-font-courier`,

`-font-courier-new`, `-font-andale-mono`, `-font-georgia`, `-font-times`, `-font-times-new-roman`,

`-font-palatino`, `-font-century-schoolbook`, `-font-bookman`, `-font-garamond`, `-font-avant-garde`

```css
.-font-arial {
  font-family: arial, helvetica, sans-serif;
}
```

### Ribbon

**Class**: `-ribbon`

```css
.-ribbon {
  overflow: hidden;
  height: 4px;
  font-size: 0;
}
```

### Responsive Images

**Class**: `-img-responsive`

```css
.-img-responsive {
  max-width: none;
}
```

### Background Properties

**Classes**: `-bg-cover`, `-bg-fixed`

```css
.-bg-cover {
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}
.-bg-fixed {
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}
```

### Tables

**Classes**: `-table`, `-table-striped`, `-table-bordered`

```css
.-table {
  width: 100%;
  border-spacing: 0;
  border-collapse: collapse;
  text-align: center;
}
.-table th {
  border-bottom: 2px #d1d1d1 solid;
  padding: 8px 12px;
}
.-table td {
  border-bottom: 1px #d4d4d4 solid;
  padding: 8px 12px;
}
.-table-striped tr:nth-child(2n + 1) {
  background-color: #f3f3f3;
}
.-table-bordered,
.-table-bordered td,
.-table-bordered th {
  border: 1px #ccc solid;
}
```

### Rounded Border

**Classes**: `-b-rounded-full`, `-b-rounded-0`, `-b-rounded-2-hover`

Default values: `1`, `2`, ..., `10`

```css
.-b-rounded-full {
  border-radius: 50%;
}
```

### Effects and Animations

**Rotation Effects**: `-effect-rotate-x-0`, `-effect-rotate-y-30deg`, `-effect-rotate-z-ccw-150deg`

Default degrees: `30`, `45`, `60`, `90`, `120`, `135`, `150`, `180`

```css
.-effect-rotate-z-0 {
  -webkit-transform: rotate(0deg);
  transform: rotate(0deg);
}
```

**Flip**: `-effect-flip-hz`, `-effect-flip-vt`

```css
/* Flip horizontal */
.-effect-flip-hz {
  -webkit-transform: scale(-1, 1);
  transform: scale(-1, 1);
}
/* Flip vertical */
.-effect-flip-vt {
  -webkit-transform: scale(1, -1);
  transform: scale(1, -1);
}
```

**Filter**: `-effect-filter-gray`, `-effect-filter-none`, `-effect-filter-blur-1`

Blur values: `1`, `2`, `3`, `4`

```css
.-effect-filter-gray {
  filter: grayscale(1);
}
.-effect-filter-blur-1,
.-effect-filter-blur-1-hover:hover,
.-effect-filter-blur-1-focus:focus {
  -webkit-filter: blur(1px);
  filter: blur(1px);
}
```

**Transition**: `-effect-transition`

```css
.-effect-transition {
  transition-property: all;
}
```

**Duration**: `-effect-duration-3`, `-anim-duration-2`

values: `1`, `2`, ..., `10`

```css
.-effect-duration-1 {
  transition-duration: 0.3s;
}
.-anim-duration-2 {
  animation-duration: 0.5s;
}
```

**Timing Functions**: `-effect-timing-linear`, `-effect-timing-ease`, `-effect-timing-ease-in`,

`-effect-timing-ease-out`, `-effect-timing-ease-in-out`, `-effect-timing-circle`,

`-effect-timing-overshoots`, `-effect-timing-2-pow-10`, `-effect-timing-sine`,

`-effect-timing-pow-2`, `-effect-timing-pow-3`, `-effect-timing-pow-4`, `-effect-timing-pow-5`,

`-anim-timing-linear`, `-anim-timing-ease`, `-anim-timing-ease-in`,

`-anim-timing-ease-out`, `-anim-timing-ease-in-out`, `-anim-timing-circle`,

`-anim-timing-overshoots`, `-anim-timing-2-pow-10`, `-anim-timing-sine`,

`-anim-timing-pow-2`, `-anim-timing-pow-3`, `-anim-timing-pow-4`, `-anim-timing-pow-5`

```css
.-effect-timing-linear {
  transition-timing-function: linear;
}
.-anim-timing-linear {
  transition-timing-function: linear;
}
```

**Simple Effects**: `-effect-grow-2`, `-effect-float-3`, `-effect-skew-ccw-1`

values: `1`, `2`, ..., `5`

```css
.-effect-float-1 {
  transform: translateY(-0.125rem);
}
```

**Complex Effects**: `-effect-underline`, `-effect-dim`, `-effect-glow`

```css
.-effect-float-1 {
  transform: translateY(-0.125rem);
}
```

**Animations**: `-anim-background`, `-anim-spin-5`, `-anim-spin-ccw-7`,

`-anim-up-down`, `-anim-left-right`, `-anim-move-tlbr`, `-anim-move-trbl`

Spin values: `1`, `2`, ..., `10`

```css
.anim-up-down {
  animation: -anim-up-down 2s ease-in-out infinite;
}
@keyframes -anim-up-down {
  0% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(15px);
  }
  100% {
    transform: translateY(0);
  }
}
```

### 3D Text

**Classes**: `-t-3d-white`, `-t-3d-black`, `-t-3d-gray`

```css
.-t-3d-white {
  color: #fff;
  text-shadow: -3px -3px 0 #222, 3px -3px 0 #222, -3px 3px 0 #222, 3px 3px 0
      #222, 4px 4px 0 #fff, 5px 5px 0 #fff, 6px 6px 0 #fff, 7px 7px 0 #fff;
  line-height: 0.8em;
  letter-spacing: 0.1em;
  transform: scaleY(0.7);
}
```

### Pushy Button

**Class**: `-btn-pushy`

### Color

**Color**: `-t-green-4`, `-lg-t-red-1-hover`, `-t-blue-3-focus`, `-t-transparent`

**Background Color**: `-bg-green-4`, `-xxl-bg-red-1-hover`, `-t-blue-3-focus`, `-t-transparent`

**Border Color**: `-b-green-4`, `-sm-b-red-1-hover`, `-b-blue-3-focus`, `-b-transparent`

**Gradient Color**: `-gr-lime-yellow`, `-gr-orange-pink-lime`, `-gr-yellow-lime`, `-gr-pink-lime-aqua`

**Selection Color**: `-t-selection-aqua`, `-bg-selection-lime`

Colors: `blue`, `aqua`, `cyan`, `teal`, `green`, `lime`, `olive`, `yellow`, `orange`, `brown`,

`red`, `pink`, `fuchsia`, `purple`, `maroon`, `black`, `gray`, `white`, `transparent`

Brightness values: `1`, `2`, ..., `5`

### Smooth Scrolling

**Smooth Scrolling**: `-scroll-smooth`

```css
.-scroll-smooth {
  scroll-behavior: smooth;
}
```

### Flexible Box And Grid System

**Classes**: `-container`, `-f`, `-f-item`, `f-dir-row`, `f-dir-col`,

`f-dir-row-reverse`, `f-dir-col-reverse`, `f-wrap`, `f-wrap-reverse`,`f-row-gap-2`, `f-col-gap-6`,

`f-start`, `f-end`, `f-center`, `f-between`, `f-around`, `f-evenly`,

`-f-content-start`, `-f-content-end`, `-f-content-center`,

`-f-content-stretch`, `-f-content-between`, `-f-content-around`, `-f-content-evenly`,

`-f-items-start`, `-f-items-end`, `-f-items-center`, `-f-items-stretch`, `-f-items-baseline`,

`-f-item-grow-5`, `-f-item-shrink-3`,

`.-f-item-order-0`, `-f-item-order-2-front`, `-f-item-order-4-back`

Gap values: `1`, `2`, ..., `10`

Order, Grow, and Shrink values: `1`, `2`, ..., `12`

**Example**:

```html
<div class="-container">
  <div class="-f">
    <div class="-f-item -span-auto -pr-3 -h-4 -bg-red-1">...</div>
    <div class="-f-item -span-auto -px-3 -h-4 -bg-blue-2">...</div>
    <div class="-f-item -span-auto -px-3 -h-4 -bg-green-3">...</div>
    <div class="-f-item -span-auto -pl-3 -h-4 -bg-yellow-4">...</div>
  </div>
  <div class="-f">
    <div class="-f-item -span-4 -xl-span-5 -px-5 -h-4 -w-3 -bg-red-2">...</div>
    <div class="-f-item -span-4 -xl-span-3 -px-5 -h-4 -w-3 -bg-blue-3">...</div>
    <div class="-f-item -span-4 -px-5 -h-4 -w-3 -bg-green-5">...</div>
  </div>
</div>
```

### Alignment

**Text Alignment**: `-t-left`, `-t-right`, `-t-center`, `-t-justify`

**Center Of Box**: `-center`

**Vertical Alignment**: `-vertical-top`, `-vertical-middle`, `-vertical-bottom`

### Stretch

**Classes**: `-w-full`, `-w-screen`, `-h-full`, `-h-screen`, `-full`, `-screen`

```css
-w-screen {
  width: 100vw;
}
-h-full {
  height: 100%;
}
```

### Pressed

**Class**: `-pressed`

### Z-Index

**Classes**: `-z-1-front`, `-md-z-2-back`

Values: `1`, `2`, ..., `5`

### Scroll Bar

**Classes**: `-scroll-hidden`, `-scroll-x`, `-scroll-y`, `-scroll`

### Float

**Classes**: `-float-left`, `-float-right`, `-float-none`

### Font Size

**Classes**: `-font-1`, `-font-3`

Values: `1`, `2`, ..., `10`

### Line Height

**Classes**: `-line-1`, `-line-3`

Values: `1`, `2`, ..., `10`

### Display

**Classes**: `-d-hidden`, `-d-block`, `-d-blank`, `-d-collapse`, `-d-flex`, `-d-grid`

### Opacity

**Classes**: `-opacity-transparent`, `-opacity-5pc`, `-opacity-15pc-hover`, `-opacity-35pc-focus`

Values: `5pc`, `10pc`, `15pc`, `25pc`, `35pc`, `50pc`, `65pc`, `75pc`, `85pc`, `90pc`, `95pc`,

`transparent`, `full`

### Shadow

**Classes**: `-shadow-1`, `-md-shadow-2-hover`, `-shadow-rt-4-focus`, `-shadow-lt-6`, `-md-shadow-rb-3`

Values: `1`, `2`, ..., `6`

### Border

**Classes**: `-b`, `-b-none`, `-sm-bt`, `-md-bb`, `-lg-br`, `-bl`, `-bx`, `-by`, `-b-1`, `-md-b-3`,

`-b-solid`, `-xl-b-dashed`, `-xxl-b-dotted`, `-b-double`, `-b-ridge`, `-b-groove`

Values: `1`, `2`, ..., `6`

### Outline

**Classes**: `-outline`, `-sm-outline-none`, `-lg-outline-1`, `-outline-3`,
`-outline-offset-3`, `-lx-outline-dashed`

Values: `1`, `2`, ..., `6`

### Height And Width

**Width**: `-md-w-3-hover`, `-w-100px-hover`

**Max-Width**: `-md-mw-3-focus`, `-mw-100px-hover`

**Height**: `-md-h-3-hover`, `-h-100px-focus`

**Automatic Width And Height**: `-w-auto-1`, `-h-auto-3`

Width, max-width, and height values: `0`, `1`, `2`, ..., `10`, `1`, `2px`, `3px`, `5px`, `7px`,

`10px`, `15px`, `20px`, `25px`, `30px`, `35px`,`40px`, `45px`, `50px`, `60px`, `70px`, `80px`,

`90px`, `100px`, `120px`, `140px`, `160px`, `180px`,`200px`, `250px`, `300px`, `350px`, `400px`,

`450px`, `500px`, `sm`, `md`, `lg`, `xl`, `xxl`

Automatic width and hight values: `1`, `2`, ..., `10`

```css
w-auto-1 {
  width: calc(100% - 10px);
}
```

### Margin And Padding

**Margin**: `-m-1`, `-mx-4`, `-sm-my-4`, `-mt-2`, `-mb-2`, `-lx-ml-3`, `-lg-mr-5`

**Padding**: `-p-1`, `-px-4`, `-sm-py-4`, `-pt-2`, `-pb-2`, `-lx-pl-3`, `-lg-pr-5`

Margin values: `auto`, `1`, `2`, ..., `10`

Padding values: `1`, `2`, ..., `10`

## Conclusion

**Dash.css** provides a comprehensive set of utility classes that facilitate rapid and efficient web design. By utilizing these classes, developers can create responsive, visually appealing layouts with minimal effort.
