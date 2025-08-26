<!--
Convert this to PDF (reference README.md on how to do that).

NOTE: this is experimental! This will likely change.

Poetry collections no matter the length are typically formatted similarly to
a chapter-book, but a little different ...
- title page (same as a long-form prose)
- Table of contents chapter: .m-chapter.toc -> .m-scene
- The poems: empty .m-chapter -> m-poem m-poem m-poem ...
- Acknowledgements chapter: .m-chapter -> m-scene

(c) Copyright 2022 Todd Warner
This work is licensed under Attribution 4.0 International. To view a copy
of this license, visit http://creativecommons.org/licenses/by/4.0/
-->

<style>
    /*
    @import "https://toddwarner.io/pub/css/manuscript-css/manuscript.css";
    */
    @import "../manuscript.css";
    @import "../pagination/none.css";

    :root {
        /*
        --m-page-break-simulated-long: 0;
        --m-font-weight-title: bold;
        --m-font-weight-title-chapter: bold;
        --m-font-weight-title-poem: bold;
        --m-pagination-header: "Lastname / Long-form Poetry / " counter(page);
        */
    }
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

2 poems | 72 lines

(_draft rev20221027_)

</div></div>

<section class="m-chapter toc">
<div class="m-header">

# Table of Contents

</div>
<section class="m-scene">

- I Wandered Lonely as a Cloud, William Wordsworth

- Jabberwocky, Lewis Carroll

</section></section>
<section class="m-chapter">
<section class="m-poem">
<div class="m-header">

# I Wandered Lonely as a Cloud

### by William Wordsworth

<div class="m-facts">

24 lines

</div></div>

```plaintext
I wandered lonely as a cloud
That floats on high o'er vales and hills,
When all at once I saw a crowd,
A host, of golden daffodils;
Beside the lake, beneath the trees,
Fluttering and dancing in the breeze.
```
```plaintext
Continuous as the stars that shine
And twinkle on the milky way,
They stretched in never-ending line
Along the margin of a bay:
Ten thousand saw I at a glance,
Tossing their heads in sprightly dance.
```
```plaintext
The waves beside them danced; but they
Out-did the sparkling waves in glee:
A poet could not but be gay,
In such a jocund company:
I gazed—and gazed—but little thought
What wealth the show to me had brought:
```
```plaintext
For oft, when on my couch I lie
In vacant or in pensive mood,
They flash upon that inward eye
Which is the bliss of solitude;
And then my heart with pleasure fills,
And dances with the daffodils.
```

</section> <!-- end poem -->
<section class="m-poem">
<div class="m-header">

# Jabberwocky

### Lewis Carroll

<div class="m-facts">

48 lines

</div></div>

```plaintext
’Twas brillig, and the slithy toves
   Did gyre and gimble in the wabe;
All mimsy were the borogoves,
   And the mome raths outgrabe.
```
```plaintext
“Beware the Jabberwock, my son
   The jaws that bite, the claws that catch!
Beware the Jubjub bird, and shun
   The frumious Bandersnatch!”
```
```plaintext
He took his vorpal sword in hand;
   Long time the manxome foe he sought—
So rested he by the Tumtum tree,
   And stood awhile in thought.
```
```plaintext
And, as in uffish thought he stood,
   The Jabberwock, with eyes of flame,
Came whiffling through the tulgey wood,
   And burbled as it came!
```
```plaintext
One, two! One, two! And through and through
   The vorpal blade went snicker-snack!
He left it dead, and with its head
   He went galumphing back.
```
```plaintext
“And hast thou slain the Jabberwock?
   Come to my arms, my beamish boy!
O frabjous day! Callooh! Callay!”
   He chortled in his joy.
```
```plaintext
’Twas brillig, and the slithy toves
   Did gyre and gimble in the wabe;
All mimsy were the borogoves,
   And the mome raths outgrabe.
```

</section> <!-- end poem -->
</section> <!-- end chapter -->

<section class="m-chapter">
<div class="m-header">

# Acknowledgments

</div>
<section class="m-scene foothang">

Woodsworth, William. 1807. (Revised 1815.) "I Wandered Lonely as a Cloud." In *Poems, in Two Volumes*. London: Longman, Hurst, Rees, and Orms.

Carroll, Lewis. "Jabberwocky." 1871. In *Through the Looking-Glass*. London: Macmillan and Co.

</section> <!-- end "scene" -->
</section> <!-- end chapter -->

</article> <!-- manuscript -->
</div> <!-- vpage -->
