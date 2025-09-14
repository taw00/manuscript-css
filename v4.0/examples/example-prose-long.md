<!--
Long-form prose example with chapters and scenes.

Copyright (c) Todd Warner
This work is licensed under Attribution 4.0 International. To view a copy of
this license, visit <http://creativecommons.org/licenses/by/4.0/>.
-->

<style>
    /*
    @import url("https://toddwarner.io/pub/css/manuscript-css/manuscript-4.0.css");
    @import url("/full/path/to/the/repository/for/manuscript-css/manuscript-4.0.css");
    */
    @import url("../../manuscript-local-4.0.css");

    /* Examples of overloading some CSS variables. Uncomment the font-weight
       variable to flip the title to bold. Uncomment the other to turn off the
       dotted like page-break simulator when presenting the document on the
       web. */
    :root {
        /*
        --m-font-weight-title: bold;
        --m-page-break-simulated-long: 0;
        */
        --m-marginalia: "Lastname / Long-form Prose / " counter(page);
    }
</style>

<div id="vpage">
<article id="manuscript" class="long narrative">




<!-- --------------------------- TITLE PAGE ------------------------------- -->




<div class="m-page-header">
<div class="m-contact">

Firstname Lastname

123 Elm Street

Example City, NC 12345 USA

firstname.lastname@example.com

+1 555-555-1212


</div></div> <!-- /.m-contact, /.m-page-header -->




<div class="m-title-header">


# Manuscript Formatting via CSS: A Long-Form Example (typical)

## A Compliant Manuscript with Chapters and Scenes

### by Author Name

> This is an [epigraph](https://en.wikipedia.org/wiki/Epigraph_(literature)).
> Some stories, parts, chapters, and even scenes will kick off with an epigraph.
>
> <div class="x-poem">
>
> ```
> A dreamer is one who can only find his way by moonlight, and his
> punishment is that he sees the dawn before the rest of the world.
>                                                              Oscar Wilde, 1888
> ```
>
> </div>


<div class="m-facts">


95,000 words

Contemporary Fiction

(_draft rev20221024_)


</div> <!-- /.m-facts -->
</div> <!-- (/title strings), /.m-facts, /.m-title-header -->




[comment]: / "---------------------- CHAPTER & SCENES ------------------------"




<section class="m-chapter">
<div class="m-title-header">


# Chapter 1


</div>




<section class="m-scene">

This document templates a long-form narrative that is divided into the more
typical chapters and scenes (no parts). Most short stories are just a series of
scenes. Most books-length (long-form) manuscripts are divided into chapters and
scenes w/o parts. But some books are also divided into books or parts. Of the
three components, only scenes are required. But here, we demo the long-form
typical: chapters and scenes.

Side note: the dotted lines in the HTML view are simulalated page breaks. They
can be turned off by setting the `--m-page-break-simulated-long` to `0`. If you
look in the `<style>...</style>` block above, I have that commented out.
Uncomment it to see the change. HTML doesn't "page break" so we put in an
indicator as an approximation of the behavior.

The only time I turn off the page break similation is when I am sharing the 
document as an HTML page. I.e., when the HTML becomes the primary end artifact.

</section> <!-- end scene -->
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

</section> <!-- end scene -->
<section class="m-scene">

Nam pharetra fermentum lectus nec malesuada. Nulla facilisi. Pellentesque
volutpat odio vitae sapien convallis hendrerit. Nunc eu tincidunt quam. Praesent
at urna molestie, tincidunt mi vitae, dapibus nulla.

Sed suscipit mauris in dolor faucibus, et tempus dui placerat. Nam ultricies,
quam quis ultrices sollicitudin, neque augue dapibus diam, at sodales justo
diam eu massa. Duis id ex vitae sem tempus auctor non at est. Aenean
ullamcorper orci vel massa volutpat hendrerit. Phasellus dui ex, efficitur in
elementum a, efficitur auctor ipsum. Aenean sit amet nisi eu nibh imperdiet
efficitur. Vestibulum molestie aliquam magna, et iaculis leo porttitor ac.

</section> <!-- end scene -->
</section> <!-- end chapter -->




[comment]: / "---------------------- CHAPTER & SCENES ------------------------"




<section class="m-chapter">
<div class="m-title-header">


# Chapter 2


</div>




<section class="m-scene">

Only one scene for chapter 2 because I think you get the idea.

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam a placerat lorem,
a sagittis risus. Curabitur erat risus, congue in lacinia ac, viverra molestie
tellus. Morbi convallis velit non sem venenatis consectetur. Nam congue posuere
magna nec vulputate. Donec sodales nisl id mi fringilla elementum. Donec in
feugiat mauris, quis laoreet lorem. Suspendisse non mi velit.

Nunc sed massa lacinia, accumsan est at, laoreet neque. Integer vestibulum eget
eros eu molestie. Quisque facilisis molestie elit at suscipit. Cras et felis
tortor. Morbi mi libero, luctus ut scelerisque at, cursus ac ex. Proin
tristique ligula sed neque dapibus, quis fermentum dui faucibus. In consectetur
sapien non rhoncus fermentum. Etiam sit amet leo dolor. Donec eget velit cursus
mauris suscipit mattis ac sit amet purus.


</section> <!-- end scene -->
</section> <!-- end chapter -->




[comment]: / "---------------------- CHAPTER & SCENES ------------------------"




<section class="m-chapter">
<div class="m-title-header">


# Epilogue


</div>




<section class="m-scene">

You get the idea. I am ending this manuscript with this scene.

Also, did you notice the `#` [dinkuses](https://en.wikipedia.org/wiki/Dinkus)
between the scenes? And the `The End` at the end? That's a typographical marker
called a [-30-](https://en.wikipedia.org/wiki/-30-). You can turned them off or
change them by redefining CSS variabbles `--m-dinkus` and `--m-30-`. For
example, set `--m-dinkus` to an empty string `""` to turn it off and set
`--m-30-` to "La Fin" just because you think your critique readers reviewers
will be impressed with your French.


</section> <!-- end scene -->
</section> <!-- end chapter -->


</article></div> <!-- ----------------------------- end of manuscript ---- -->

