# Dash CSS Framework

## Overview

**Dash** is a simple, lightweight, and highly configurable CSS framework designed to streamline web development. This documentation provides an overview of the available utility classes, organized by their functionality. Dash can be utilized as both a CSS framework and an SCSS framework.

To get started, simply copy the `dist/css/index.min.css` file into your project and embark on your development journey! You can customize the configuration by editing the `src/config.scss` file. For instance, you can change the `$-prefix` variable from `-` to `_`, adjust color names, and more.

To apply your changes, run the following command:

```cmd
npm start
```

Please note that this command will not alter the development file located at `dist/css/index.css`; instead, it generates a new version of `dist/css/index.min.css` based on your configurations.

## Version

**Current Version**: 1.0.1

## Utility Classes

### Unstyled Elements

**Description**: Removes default styles from elements, making them appear as normal text.

**Class**: `-unstyled`

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

**Text Decorations**: `-t-underline`, `-t-overline`, `-t-overline-hover`, `-t-line-through-focus`, etc

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

**Classes**: `-ltr` (Left to Right), `-rtl` (Right to Left)

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

**Classes**: `-aspect-ratio`, `-aspect-video`, `-aspect-square`, `-aspect-3-2`, etc

```css
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

**Classes**: `-pos-absolute`, `-pos-relative`, `-pos-static`, `-pos-fixed`, `-pos-sticky`

```css
.-pos-absolute {
  position: absolute;
}
```

### Display Properties

**Classes**: `-d-inline`, `-d-inline-block`, `-d-grid`, `-md-d-block`, `-lg-d-hidden`, etc

```css
.-d-inline {
  display: inline;
}
```

### Cursor Styles

**Classes**: `-cursor-default`, `-cursor-pointer`, `-cursor-auto`, etc

```css
.-cursor-default {
  cursor: default;
}
```

### Text Formatters

**Classes**: `-t-break`, `-t-nowrap`, `-t-ellipsis`, `t-single-row`, etc

```css
.-t-ellipsis {
  text-overflow: ellipsis;
}
```

### Font Families

**Classes**: `-font-sans-serif`, `-font-arial`, `-font-georgia`, etc

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

**Classes**: `-b-rounded-full`, `-b-rounded-0`, `-b-rounded-2-hover`, etc

```css
.-b-rounded-full {
  border-radius: 50%;
}
```

### Effects and Animations

**Rotation Effects**: `-effect-rotate-z-0`, `-effect-rotate-x-30deg`, `-effect-rotate-y-ccw-150deg`, etc

```css
.-effect-rotate-z-0 {
  -webkit-transform: rotate(0deg);
  transform: rotate(0deg);
}
```

**Flip**: `-effect-flip-hz`, `-effect-flip-vt`, etc

```css
.-effect-flip-hz,
.-effect-flip-hz-hover:hover,
.-effect-flip-hz-focus:focus {
  transform: scale(-1, 1);
}
```

**Filter**: `-effect-filter-gray`, `-effect-filter-blur-3`, etc

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

**Duration**: `-effect-duration`

```css
.-effect-duration-1 {
  transition-duration: 0.3s;
}
.-anim-duration-2 {
  animation-duration: 0.5s;
}
```

**Timing Functions**: `-effect-timing-linear`, `-anim-timing-ease`, `-effect-timing-ease-in-out`, etc

```css
.-effect-timing-linear {
  transition-timing-function: linear;
}
.-anim-timing-linear {
  transition-timing-function: linear;
}
```

**Effects**: `-effect-grow-2`, `-effect-float-3`, `-effect-skew-ccw-1`, `-effect-underline`,
`-effect-dim`, `-effect-glow`, etc

```css
.-effect-float-1 {
  transform: translateY(-0.125rem);
}
```

**Animations**: `-anim-background`, `-anim-spin-ccw-7`, `-anim-up-down`, `-anim-left-right`,
`-anim-move-tlbr`, `-anim-move-trbl`, etc

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

**Description**
The `-t` prefix means `text color`.
Values:
`blue`, `aqua`, `cyan`, `teal`, `green`, `lime`, `olive`, `yellow`, `orange`, `brown`,
`red`, `pink`, `fuchsia`, `purple`, `maroon`, `black`, `gray`, `white`

**Color**: `-t-green-4`, `-xl-t-red-1-hover`, `-t-blue-3-focus`, `-t-transparent`

**Background Color**: `-bg-green-4`, `-xl-bg-red-1-hover`, `-t-blue-3-focus`, `-t-transparent`

**Border Color**: `-b-green-4`, `-xl-b-red-1-hover`, `-b-blue-3-focus`, `-b-transparent`

**Gradient Color**: `-gr-lime-yellow`, `-gr-orange-pink-lime`, `-gr-yellow-lime`, `-gr-pink-lime-aqua`

**Selection Color**: `-t-selection-aqua`, `-bg-selection-lime`

### Smooth Scrolling

**Smooth Scrolling**: `-scroll-smooth`

```css
.-scroll-smooth {
  scroll-behavior: smooth;
}
```

### Flexible Box And Grid System

**Classes**: `-container`, `-f`, `-f-item`, `f-dir-row`, `f-wrap-reverse`, `f-center`,
`f-content-stretch`,`f-row-gap`, `f-items-start`, `f-item-grow`, `f-item-order`

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

### Scroll Bar

**Classes**: `-scroll-hidden`, `-scroll-x`, `-scroll-y`, `-scroll`

### Float

**Classes**: `-float-left`, `-float-right`, `-float-none`

### Font Size

**Classes**: `-font-1`, `-font-3`

### Line Height

**Classes**: `-line-1`, `-line-3`

### Display

**Classes**: `-d-hidden`, `-d-block`, `-d-blank`,, `-d-flex`, `-d-grid`, etc

### Opacity

**Classes**: `-opacity-transparent`, `-opacity-5`, `-opacity-15-hover`, `-opacity-35-focus`, etc

### Shadow

**Classes**: `-shadow-1`, `-md-shadow-2-hover`, `-shadow-rt-4-focus`,
`-shadow-lt-6`, `-md-shadow-rb-3`, etc

### Border

**Classes**: `-b`, `-b-none`, `-bt`, `-bb`, `-br`, `-bl`, `-bx`, `-by`,
`-b-1`, `-b-3`, `-b-dashed`, `-b-dotted`, `-b-solid`, etc

### Outline

**Classes**: `-outline`, `-outline-none`, `-outline-1`, `-outline-3`,
`-outline-offset-3`, `-outline-dashed`, etc

### Height And Width

**Width**: `-md-w-hover-3`, `-w-100px-hover`, etc

**Max-Width**: `-md-mw-focus-3`, `-mw-100px-hover`, etc

**Height**: `-md-h-hover-3`, `-h-100px-focus`, etc

**Automatic Width And Height**: `-w-auto-1`, `-h-auto-3`

```css
w-auto-1 {
  width: calc(100% - 10px);
}
```

### Margin And Padding

**Margin**: `-m-1`, `-md-mt-2`, `-mb-2`, `-mr-3`, `-lg-ml-5`, `-mx-4`, `-my-4`, etc

**Padding**: `-p-1`, `-lx-pt-2`, `-pb-2`, `-pr-3`, `-sm-pl-5`, `-px-4`, `-py-4`, etc

## Conclusion

**Dash** CSS Framework provides a comprehensive set of utility classes that facilitate rapid and efficient web design. By utilizing these classes, developers can create responsive, visually appealing layouts with minimal effort.
