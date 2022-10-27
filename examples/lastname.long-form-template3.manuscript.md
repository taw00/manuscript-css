<!--
Convert this to PDF (reference README.md on how to do that).

This example:
- we are using parts (and chapters and scenes)
- we are using automated title generation for parts and chapters and scenes.
  we turned on full-depth enumeration. This is helpful if you are sharing the
  document with reviewers. In lieu of page numbers they can reference part,
  chapter, and scene numbers.
- turned off the dinkus in this because we have scene titles and that renders
  moot the need for a dinkus scene separator.

(c) Copyright 2022 Todd Warner
This work is licensed under Attribution 4.0 International. To view a copy
of this license, visit http://creativecommons.org/licenses/by/4.0/
-->

<style>
    /*
    @import "https://toddwarner.io/pub/css/manuscript/manuscript.css";
    @import "https://toddwarner.io/pub/css/manuscript/manuscript-counters.css";
    ...or...
    */
    @import "../manuscript.css";
    @import "../manuscript-counters.css";
    :root {
        /*
        --m-font-weight-title: bold;
        --m-page-break-simulated-long: 0;
        */
        --m-30-: var(--m-marker9) "2022 Firstname Lastname | All rights reserved.";
		--m-autotitle-leaf-off: ""; /* turned off showing leaf values */
		--m-autotitle-depth-off: unset; /* turned on full-depth enumeration */
		--m-dinkus: unset;
    }
</style>

<div id="vpage">
<article id="manuscript" class="long narrative">

<div id="m-contact">

Firstname Lastname

North Carolina Piedmont, USA

firstname.lastname@example.com

+1 555-555-1212

</div>
<div class="m-header">

# Manuscript Formatting via CSS

## A Long-Form Example w/ Parts & AutoTitling

### by Author Name

> <div class="poem">
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

(_draft rev 20221024_)

</div>
</div>

<section class="m-part">
<div class="m-header">

#

</div>
<section class="m-chapter">
<div class="m-header">

#

</div>
<section class="m-scene">
<div class="m-header">

#

</div>

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

This is a scene. This is a scene. This is a scene. This is a scene.
This is a scene. This is a scene. This is a scene. This is a scene.

This is a scene. This is a scene. This is a scene. This is a scene.
This is a scene. This is a scene. This is a scene. This is a scene.
This is a scene. This is a scene. This is a scene. This is a scene. 

</section>
<section class="m-scene">
<div class="m-header">

#

</div>

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis lacinia neque
ultricies erat ullamcorper, non semper ex molestie. Duis sed odio at mauris
ornare imperdiet nec ac turpis. Praesent ac tristique nunc, nec sodales ante.
Sed posuere, risus nec molestie suscipit, velit massa volutpat sem, nec
elementum leo eros ac felis. Fusce luctus tincidunt libero, vitae eleifend
neque iaculis a. Curabitur molestie lobortis gravida. In eget tincidunt erat.

This is a scene. This is a scene. This is a scene. This is a scene.
This is a scene. This is a scene. This is a scene. This is a scene.

This is a scene. This is a scene. This is a scene. This is a scene.
This is a scene. This is a scene. This is a scene. This is a scene.
This is a scene. This is a scene. This is a scene. This is a scene. 

</section>
<section class="m-scene">
<div class="m-header">

#

</div>

Nam pharetra fermentum lectus nec malesuada. Nulla facilisi. Pellentesque
volutpat odio vitae sapien convallis hendrerit. Nunc eu tincidunt quam. Praesent
at urna molestie, tincidunt mi vitae, dapibus nulla.

This is a scene. This is a scene. This is a scene. This is a scene.
This is a scene. This is a scene. This is a scene. This is a scene.

This is a scene. This is a scene. This is a scene. This is a scene.
This is a scene. This is a scene. This is a scene. This is a scene.
This is a scene. This is a scene. This is a scene. This is a scene. 

</section>
</section>
<section class="m-chapter">
<div class="m-header">

#

</div>
<section class="m-scene">
<div class="m-header">

#

</div>

[SCENE TEXT]

</section> <!-- end scene -->
<section class="m-scene">
<div class="m-header">

#

</div>

This is a scene. This is a scene. This is a scene. This is a scene.
This is a scene. This is a scene. This is a scene. This is a scene.

This is a scene. This is a scene. This is a scene. This is a scene.
This is a scene. This is a scene. This is a scene. This is a scene.
This is a scene. This is a scene. This is a scene. This is a scene. 

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
<div class="m-header">

#

</div>

This is a scene. This is a scene. This is a scene. This is a scene.
This is a scene. This is a scene. This is a scene. This is a scene.

This is a scene. This is a scene. This is a scene. This is a scene.
This is a scene. This is a scene. This is a scene. This is a scene.
This is a scene. This is a scene. This is a scene. This is a scene. 

</section> <!-- end scene -->
<section class="m-scene">
<div class="m-header">

#

</div>

This is a scene. This is a scene. This is a scene. This is a scene.
This is a scene. This is a scene. This is a scene. This is a scene.

This is a scene. This is a scene. This is a scene. This is a scene.
This is a scene. This is a scene. This is a scene. This is a scene.
This is a scene. This is a scene. This is a scene. This is a scene. 

</section> <!-- end scene -->
</section> <!-- end chapter -->
</section> <!-- end part 2 -->

<section class="m-part">
<div class="m-header">

## Epilogue

> Here I override the part auto-titling by using the subtitle
as title-work-around.

</div>
<section class="m-scene">

Hey look! No chapters in this part. This is a scene! I also skipped having the
title auto-populate. Reviewers can just reference "Epilogue, paragraph X".

This is a scene. This is a scene. This is a scene. This is a scene.
This is a scene. This is a scene. This is a scene. This is a scene.

This is a scene. This is a scene. This is a scene. This is a scene.
This is a scene. This is a scene. This is a scene. This is a scene.
This is a scene. This is a scene. This is a scene. This is a scene. 

</section> <!-- scene -->
</section> <!-- part -->
</article> <!-- manuscript -->
</div>     <!-- vpage -->

