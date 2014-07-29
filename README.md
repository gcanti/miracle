# miracle

Mini fluid responsive less library

miracle includes a responsive, fluid grid system that appropriately scales up to 12 columns (or 20 columns if needed) as the device or viewport size increases.
Columns width are defined by percentages.

## Basic setup

    /* mystyle.less */
    @import "miracle.less";
    .miracle-container-max-width(940px);    // container max width (optional)
    .miracle-default(lg, 10px);             // desktops and unsupporting @media browsers (IE8)
    .miracle-breakpoint(768px, md, 5px);    // tablets
    .miracle-breakpoint(480px, sm, 2px);    // mobiles
    .miracle-img-responsive();              // (optional)


    <!-- mypage.html -->
    <!DOCTYPE html>
    <html>
        <head>
            <meta charset="utf-8" />
            <meta http-equiv="X-UA-Compatible" content="IE=edge">
            <meta name="viewport" content="width=device-width, initial-scale=1">
            <link type="text/css" rel="stylesheet" href="mystyle.css"/>
        </head>
        <body>
            <div class="container">
                <!-- grid here -->
            </div>
        </body>
    </html>

## mixins

### .miracle-container-max-width (@max-width)

Set the container max width for supported browsers that support @media.
Browsers that doesn't support @media the container width is fixed.  

### miracle-default (@name, @gutter)

Set the default grid system classes for large devices (desktops) and unsupporting @media browsers (IE8).
All columns classes follow the pattern `@name-<percentage>`.

### .miracle-breakpoint (@max-width, @name, @gutter)

Set the grid system classes for devices with viewport width up `@max-width`.
All columns classes follow the pattern `@name-<percentage>`.

### .miracle-img-responsive ()

Turn all images responsive.

## Copyright & License

Copyright (C) 2014 Giulio Canti - Released under the MIT License.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.