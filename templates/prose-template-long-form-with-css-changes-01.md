<!--
Convert this to PDF (reference README.md on how to do that).

This example:
- we are using parts (and chapters and scenes)
- we are using automated title generation for parts and chapters (but not
  scenes). We are using the default configuration where the titles will look
  like: Part 1, Chapter 3, etc.
- included examples of typeface imports that match the default fontstacks
  defined in _manuscript-config.css.

(c) Copyright 2022 Todd Warner
This work is licensed under Attribution 4.0 International. To view a copy
of this license, visit http://creativecommons.org/licenses/by/4.0/
-->

<style>
    /*
    @import "https://toddwarner.io/pub/css/manuscript/manuscript.css";
    @import "https://toddwarner.io/pub/css/manuscript/manuscript-counters.css";
    @import "https://toddwarner.io/pub/css/manuscript/typefaces/typeface-serif-termes.css";
    @import "https://toddwarner.io/pub/css/manuscript/typefaces/typeface-serif-tinos.css";
    @import "https://toddwarner.io/pub/css/manuscript/typefaces/typeface-sans-arimo.css";
    @import "https://toddwarner.io/pub/css/manuscript/typefaces/typeface-mono-cursor.css";
    @import "https://toddwarner.io/pub/css/manuscript/typefaces/typeface-mono-cousine.css";
    ...or...
    @import "../manuscript.css";
    @import "../manuscript-counters.css";
    @import "../typefaces/typeface-serif-termes.css";
    @import "../typefaces/typeface-serif-tinos.css";
    @import "../typefaces/typeface-sans-arimo.css";
    @import "../typefaces/typeface-mono-cursor.css";
    @import "../typefaces/typeface-mono-cousine.css";
    */
    @import "../manuscript.css";
    @import "../manuscript-counters.css";
    @import "../typefaces/typeface-serif-termes.css";
    @import "../typefaces/typeface-serif-tinos.css";
    @import "../typefaces/typeface-sans-arimo.css";
    @import "../typefaces/typeface-mono-cursor.css";
    @import "../typefaces/typeface-mono-cousine.css";

    /* Examples of overloading some CSS variables. Uncomment the font-weight
       variable to flip the title to bold. Uncomment the other to make a fancy
       -30- end marker (not a typical decision for a manuscript, of course). */
    :root {
        /*
        --m-font-weight-title: bold;
        --m-page-break-simulated-long: 0;
        --m-30-: var(--m-marker31) "2022 Firstname Lastname | All rights reserved.";
        */
        --m-append-to-scene-off: "";
    }
</style>

<div id="vpage">
<article id="manuscript" class="long narrative">

<div id="m-contact">

Firstname Lastname

123 Elm Street

Example City, NC 12345 USA

firstname.lastname@example.com

+1 555-555-1212

</div>

<div class="m-header">

# Manuscript Formatting via CSS: A Long-Form Example (atypical)

## Parts and Chapters and Scenes - and a (_mostly_) Compliant Manuscript

### by Author Name

> Also, parts and chapters have auto-titling enabled.
>
> <div class="x-poem">
>
> ```plaintext
>                  My epitaphs.
>                    Overflow with bad rhyme.
>                       Here this poem ends. Can anyone spare a dime?
>                  —todd warner, all rights reserved (not really)
> ```
>
> </div>

<div class="m-facts">

95,000 words

Contemporary Fiction

(_draft rev20221024_)

</div></div>

<section class="m-part">
<div class="m-header">

#

</div>
<section class="m-chapter">
<div class="m-header">

#

</div>
<section class="m-scene">

This document templates a narrative that is divided into parts, chapters, and
scenes. Most short stories are just a series of scenes. Most books-length
(long-form) manuscripts are divided into chapters and scenes. But some books
are also divided into books or parts. Of those divisions, only scenes are
required for this manuscript to template out correctly. But here, we demo all
the major bits.

_War and Peace_ by Leo Tolstoy, for example, is divided into 15 books with two 
epilogues and many many chapters. _At the Mountains of Madness_, a novella by
H.P. Lovecraft is a series of chapters with only one scene each. That novella is
included as an example in this repository.

Side note: the dotted lines in the HTML view are simulalated page breaks. They
can be turned off by setting the `--m-page-break-simulated-long` to `0`. If you
look in the `<style>...</style>` block above, I have that commented out.
Uncomment it to see the change. HTML doesn't "page break" so we put in an
indicator as an approximation of the behavior.

The only time I turn off the page break similation is when I am sharing the 
document as an HTML page. I.e., when the HTML becomes the primary end artifact.

</section>
<section class="m-scene">

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis lacinia neque
ultricies erat ullamcorper, non semper ex molestie. Duis sed odio at mauris
ornare imperdiet nec ac turpis. Praesent ac tristique nunc, nec sodales ante.
Sed posuere, risus nec molestie suscipit, velit massa volutpat sem, nec
elementum leo eros ac felis. Fusce luctus tincidunt libero, vitae eleifend
neque iaculis a. Curabitur molestie lobortis gravida. In eget tincidunt erat.

Curabitur at tellus ac sapien blandit ullamcorper. Etiam tortor sapien,
dignissim vel tempor sagittis, efficitur eget magna. Vestibulum ante ipsum
primis in faucibus orci luctus et ultrices posuere cubilia curae; Quisque
eleifend, nulla ac bibendum tristique, massa lacus tincidunt risus, finibus
lacinia sem magna id leo. Ut porttitor nulla nisl, et dictum nisi efficitur a.
Aliquam tellus nulla, faucibus a luctus id, vestibulum nec enim. Nulla egestas
pellentesque porttitor. In ac mollis arcu. Etiam est nulla, faucibus et tellus
nec, congue sagittis metus.

</section>
<section class="m-scene">

Nam pharetra fermentum lectus nec malesuada. Nulla facilisi. Pellentesque
volutpat odio vitae sapien convallis hendrerit. Nunc eu tincidunt quam. Praesent
at urna molestie, tincidunt mi vitae, dapibus nulla.

Ut porttitor nulla nisl, et dictum nisi efficitur a.
Aliquam tellus nulla, faucibus a luctus id, vestibulum nec enim. Nulla egestas
pellentesque porttitor. In ac mollis arcu. Etiam est nulla, faucibus et tellus
nec, congue sagittis metus.

</section> <!-- scene -->
</section> <!-- chapter -->

<section class="m-chapter">
<div class="m-header">

#

</div>
<section class="m-scene">

All work and no play makes Jack a dull boy. All work and no play makes Jack a
dull boy. All work and no play makes Jack a dull boy. All work and no play makes
Jack a dull boy. All work and no play makes Jack a dull boy. All work and no
play makes Jack a dull boy. All work and no play makes Jack a dull boy. All work
and no play makes Jack a dull boy. All work and no play makes Jack a dull boy.

All work and no play makes Jack a dull boy. All work and no play makes Jack a
dull boy. All work and no play makes Jack a dull boy. All work and no play makes
Jack a dull boy. All work and no play makes Jack a dull boy. All work and no
play makes Jack a dull boy. All work and no play makes Jack a dull boy. All work
and no play makes Jack a dull boy. All work and no play makes Jack a dull boy.

All work and no play makes Jack a dull boy. All work and no play makes Jack a
dull boy. All work and no play makes Jack a dull boy. All work and no play makes
Jack a dull boy. All work and no play makes Jack a dull boy. All work and no
play makes Jack a dull boy. All work and no play makes Jack a dull boy. All work
and no play makes Jack a dull boy. All work and no play makes Jack a dull boy.

</section> <!-- end scene -->
<section class="m-scene">

All work and no play makes Jack a dull boy. All work and no play makes Jack a
dull boy. All work and no play makes Jack a dull boy. All work and no play makes
Jack a dull boy. All work and no play makes Jack a dull boy. All work and no
play makes Jack a dull boy. All work and no play makes Jack a dull boy.

All work and no play makes Jack a dull boy. All work and no play makes Jack a
dull boy. All work and no play makes Jack a dull boy. All work and no play makes
Jack a dull boy. All work and no play makes Jack a dull boy. All work and no
play makes Jack a dull boy. All work and no play makes Jack a dull boy. All work
and no play makes Jack a dull boy. All work and no play makes Jack a dull boy.
All work and no play makes Jack a dull boy. All work and no play makes Jack a
dull boy.

All work and no play makes Jack a dull boy. All work and no play makes Jack a
dull boy. All work and no play makes Jack a dull boy. All work and no play makes
Jack a dull boy. All work and no play makes Jack a dull boy. All work and no
play makes Jack a dull boy. All work and no play makes Jack a dull boy. All work
and no play makes Jack a dull boy. All work and no play makes Jack a dull boy.

</section> <!-- end scene -->
</section> <!-- end chapter -->
</section> <!-- end part 1 -->

<section class="m-part">
<div class="m-header">

#

## A new beginning.

### by Second Author

> A second author? Maybe this is an anthology or a collaboration. This is one
> way of doing it. Each of these `section` component can have their own
> `m-header` with a title (in this case the title is `Part 2` and subtitle and
> author. Even an epitath (this `blockquote`) and `m-facts`.

</div>
<section class="m-chapter">
<div class="m-header">

#

</div>
<section class="m-scene">

I think you get the idea. I am ending this manuscript with this scene.

Also, did you notice the `#` [dinkuses](https://en.wikipedia.org/wiki/Dinkus)
between the scenes? And the `The End` at the end? That's a typographical marker
called a [-30-](https://en.wikipedia.org/wiki/-30-). You can turned them off or
change them by redefining CSS variabbles `--m-dinkus` and `--m-30-`. For
example, set `--m-dinkus` to an empty string `""` to turn it off and set
`--m-30-` to "La Fin" just because you think your critique readers reviewers
will be impressed with your French.

</section> <!-- scene -->
</section> <!-- chapter -->
</section> <!-- part 2 -->

</article> <!-- manuscript -->
</div> <!-- vpage -->
