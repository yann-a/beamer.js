# beamer.js
A HTML+CSS+Js solution for creating slides distributed under MIT Licence (see LICENCE)

## Usage
This is a simple overview of the available features. To see more example, see the `examples` folder.

To create your own presentation, you'll need to insert your slides in the `#flides` div.

### Slides
A slide consists in a `.step` div, positioned with `data-x`, `data-y` and `data-z` arguments.\
Use `data-rotatex`, `data-rotatey` and `data-rotatez` to rotate the slide (works in 3D).\
`data-scale` is used to change scale of the slide.

Example:
```html
<div id="first_slide" class="step" data-x="1000" data-y="0">
    Content of slide
</div>
```

### Slide steps
A slide can contain several pieces of content that will be shown successively. This is achieved by putting each such piece in a `.slide_step` div.

Example:
```html
<div id="first_slide" class="step" data-x="1000" data-y="0">
    This is shown at entrance in slide. <br />
    <div class="slide_step">
        This is shown shortly after.
    </div>
</div>
```

### Transitions
The duration of transition to a given slide can be set via the `data-duration` argument of the slide.

### Footer
A footer is active by default, containing the name of the author (set from the `meta name="author"` element), the title (set from `meta name="description"`), the section and subsection if applicable and the number of the slide.

The footer can be hidden on a slide by giving it the `nofooter` class.

### Counter
All slides are counted by default (even if footer is not shown). A slide can be excluded from the counting system (i.e it will not increase the counter in bottom right corner, and the associated slot in footer will be left blank) by giving it the `uncounted` class.

### Sections and subsection
Sections (respectively subsections) are divs with the `section` (respectively `subsection`) class. To include a slide in a section, simply insert it in the said div.

### Overviews
Overviews only differ from regular slides by what is shown when in said slide. There are two types of overviews :
+ `#overview_intermediate` shows what's already been seen.
+ `#overview` shows everything.

### Math
Math support is assured by MathJax, that means you can enter math by inserting it between `$` `$` for inline display and `$$` `$$` for block display.

### Fixed slides
Fixed slides are excluded from the flow, and can only be entered by link (`<a href="#slide_id">`). They are indicated by the `data-fixed="1"` attribute.

# flides
This is a fork of Flides by Nathanaël Fijalkow, distributed under the following licence :

The MIT License (MIT)

Copyright (c) 2016 Nathanaël Fijalkow

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
