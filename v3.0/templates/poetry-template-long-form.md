<!--
Template: poetry collection (not compliant, but looks nice)

Poetry collections no matter the length are typically formatted similarly to
a chapter-book, but a little different ...
- title page (same as a long-form prose)
- Table of contents chapter: .m-chapter.toc -> .m-scene
- The poems: empty .m-chapter -> m-poem m-poem m-poem ...
- Acknowledgements chapter: .m-chapter -> m-scene

This poetry collection does not meet industry spec just yet.
-->

<style>
    /*
    @import url("https://toddwarner.io/pub/css/manuscript-css/manuscript-3.0.css");
    */
    @import url("../../manuscript-3.0.css");
</style>

<div id="vpage">
<article id="manuscript" class="long poetry">

<div id="m-contact">

Firstname Lastname

123 Elm Street

Example City, NC 12345 USA

firstname.lastname@example.com

+1 555-555-1212

</div>

<div class="m-header">

# Manuscript Formatting via CSS: A Poetry Collection

### by Editor Name, ed.

<div class="m-facts">

4 poems | NN lines

(_rev. 20250831_)

</div></div>

<section class="m-chapter toc">
<div class="m-header" style="width: 100%">

# Table of Contents

</div>
<section class="m-scene">

##### Chapter Theme 1

  - Poem 1.1
  - Poem 1.2

##### Chapter Theme 2

  - Poem 2.1
  - Poem 2.2

</section></section>


<section class="m-chapter">
<div class="m-header">

# Chapter Theme 1

</div>
<section class="m-poem">
<div class="m-header">

# Poem 1.1

### by Firstname Lastname

<div class="m-facts">

NN lines

</div></div>

```plaintext
Lorem ipsum dolor sit amet consectetur adipiscing elit.
  Quisque faucibus ex sapien vitae pellentesque sem placerat.
In id cursus mi pretium tellus duis convallis.
    Tempus leo eu aenean sed diam urna tempor.
```
```plaintext
In id cursus mi pretium tellus duis convallis.
  Tempus leo eu aenean sed diam urna tempor.
Pulvinar vivamus fringilla lacus nec metus bibendum egestas.
```
```plaintext
. . .
```

</section> <!-- end poem -->
<section class="m-poem">
<div class="m-header">

# Poem 1.2

### by Firstname Lastname

<div class="m-facts">

NN lines

</div></div>

```plaintext
Lorem ipsum dolor sit amet consectetur adipiscing elit.
  Quisque faucibus ex sapien vitae pellentesque sem placerat.
In id cursus mi pretium tellus duis convallis.
    Tempus leo eu aenean sed diam urna tempor.

In id cursus mi pretium tellus duis convallis.
  Tempus leo eu aenean sed diam urna tempor.
Pulvinar vivamus fringilla lacus nec metus bibendum egestas.

. . .
```

</section> <!-- end poem -->
</section> <!-- end chapter -->


<section class="m-chapter">
<div class="m-header">

# Chapter Theme 2

</div>
<section class="m-poem">
<div class="m-header">

# Poem 2.1

### by Firstname Lastname

<div class="m-facts">

NN lines

</div></div>

```plaintext
Lorem ipsum dolor sit amet consectetur adipiscing elit.
  Quisque faucibus ex sapien vitae pellentesque sem placerat.
In id cursus mi pretium tellus duis convallis.
    Tempus leo eu aenean sed diam urna tempor.
```
```plaintext
In id cursus mi pretium tellus duis convallis.
  Tempus leo eu aenean sed diam urna tempor.
Pulvinar vivamus fringilla lacus nec metus bibendum egestas.
```
```plaintext
. . .
```

</section> <!-- end poem -->
<section class="m-poem">
<div class="m-header">

# Poem 2.2

### by Firstname Lastname

<div class="m-facts">

NN lines

</div></div>

```plaintext
Lorem ipsum dolor sit amet consectetur adipiscing elit.
  Quisque faucibus ex sapien vitae pellentesque sem placerat.
In id cursus mi pretium tellus duis convallis.
    Tempus leo eu aenean sed diam urna tempor.

In id cursus mi pretium tellus duis convallis.
  Tempus leo eu aenean sed diam urna tempor.
Pulvinar vivamus fringilla lacus nec metus bibendum egestas.

. . .
```

</section> <!-- end poem -->
</section> <!-- end chapter -->


<section class="m-chapter">
<div class="m-header">

# Acknowledgments

</div>
<section class="m-scene">

The editors of this poetry collection sould like to acknowledge the good graces
of many people. In particular …

</section> <!-- end "scene" -->
</section> <!-- end chapter -->

</article> <!-- end manuscript -->
</div>     <!-- end vpage -->
