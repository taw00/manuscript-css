<!--
Convert this to PDF (reference README.md on how to do that).

NOTE: this is experimental! This will likely change.

Short-form manuscript for poetry:
- one poem per document
- m-contact, main title block (title, byline and m-facts), and one m-poem 
  -- that's it.
- Alternatively, .m-contact, main title block (title, byline and .m-facts), and
  then empty-.m-chapter + one .m-poem, then .m-chapter entitled
  "Acknowledgement", and an .m-scene.foothang with an acknowledge of prior
  publication.

(c) Copyright 2022 Todd Warner
This work is licensed under Attribution 4.0 International. To view a copy
of this license, visit http://creativecommons.org/licenses/by/4.0/
-->

<style>
    /*
    @import "https://toddwarner.io/pub/css/manuscript-css/manuscript.css";
    */
    @import "../manuscript.css";
    :root {
        --m-pagination-header: "Lastname / Short-form Poetry / " counter(page);
    }
</style>

<div id="vpage">
<article id="manuscript" class="short poetry">

<div id="m-contact">

Firstname Lastname

123 Elm Street

Example City, NC 12345 USA

firstname.lastname@example.com

+1 555-555-1212

</div>

<div class="m-header">

# I Wandered Lonely as a Cloud

### by William Wordsworth

<div class="m-facts">

24 lines

</div></div>

<section class="m-chapter">
<section class="m-poem">

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
</section> <!-- end chapter --> 

<section class="m-chapter force-break-before">
<div class="m-header">

# Acknowledgment

</div>
<section class="m-scene foothang">

Woodsworth, William. 1807. (Revised 1815.) "I Wandered Lonely as a Cloud." In *Poems, in Two Volumes*. London: Longman, Hurst, Rees, and Orms.

</section> <!-- end "scene" -->
</section> <!-- end chapter -->

</article> <!-- manuscript -->
</div> <!-- vpage -->
