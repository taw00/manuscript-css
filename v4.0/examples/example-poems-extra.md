<!--
Poetry submission packet example, but with extra stuff.
(may/may not be acceptable for submission; as always, check the requirements)

Poetry manuscripts, no matter the length, are typically formatted as a series
of poems without a title page or table of contents. Each page has a page
header and facts, as well as a title, and then the poem.

This one has a title page.

- title-page stuff: the opening .m-page-header and .m-title-header
  Note: this required me adding 'long' to the #manuscript classes.
- the poems (each with their own page-header and line-count)
- citation scene, for show

Copyright (c) Todd Warner
This work is licensed under Attribution 4.0 International. To view a copy of
this license, visit <http://creativecommons.org/licenses/by/4.0/>.
-->

<style>
    /*
    @import url("https://toddwarner.io/pub/css/manuscript-css/manuscript.css");
    @import url("/full/path/to/the/repository/for/manuscript-css/manuscript.css");
    */
    @import url("../../manuscript.css");

    :root {
        /*
        --m-page-break-simulated-long: 0;
        --m-font-weight-title: bold;
        --m-font-weight-title-chapter: bold;
        --m-font-weight-title-poem: bold;
        */
        --m-marginalia: "Lastname / Long-form Poetry / " counter(page);
    }
</style>

<div id="vpage" class="no-header">
<article id="manuscript" class="poetry">




[comment]: / "-------------------------- TITLE PAGE --------------------------"
[comment]: / "----------------- (often not used with poetry) -----------------"




<div class="m-page-header">
<div class="m-contact">


Editor Name

123 Elm Street

Example City, NC 12345 USA

editor@example.com

+1 555-555-1212


</div></div> <!-- /.m-contact, /.m-page-header -->




<div class="m-title-header">


# A Poetry Collection

### by Editor Name, ed.

<div class="m-facts">

2 poems | 72 lines

(_draft rev20250910_)


</div></div>




[comment]: / "-------------------------- TOC SCENE ---------------------------"
[comment]: / "----------------- (often not used with poetry) -----------------"




<section class="m-scene toc">
<div class="m-title-header">


# Table of Contents


</div>


- I Wandered Lonely as a Cloud, by William Wordsworth (24 lines)

- Jabberwocky, by Lewis Carroll (48 lines)


</section>




[comment]: / "---------------------------- POEMS -----------------------------"




<section class="m-poem">
<div class="m-page-header">
<div class="m-contact">


William Wordsworth

123 Main St

Everyville, NM 32145

will.i.am@example.com


</div> <!-- /.m-contact -->
<div class="m-facts">


24 lines


</div> <!-- /.m-facts -->
</div> <!-- /.m-title-header -->


<div class="m-title-header">


# I Wandered Lonely as a Cloud


</div> <!-- /.m-title-header -->


```
I wandered lonely as a cloud
That floats on high o'er vales and hills,
When all at once I saw a crowd,
A host, of golden daffodils;
Beside the lake, beneath the trees,
Fluttering and dancing in the breeze.
```
```
Continuous as the stars that shine
And twinkle on the milky way,
They stretched in never-ending line
Along the margin of a bay:
Ten thousand saw I at a glance,
Tossing their heads in sprightly dance.
```
```
The waves beside them danced; but they
Out-did the sparkling waves in glee:
A poet could not but be gay,
In such a jocund company:
I gazed—and gazed—but little thought
What wealth the show to me had brought:
```
```
For oft, when on my couch I lie
In vacant or in pensive mood,
They flash upon that inward eye
Which is the bliss of solitude;
And then my heart with pleasure fills,
And dances with the daffodils.
```


</section> <!-- /.m-poem -->




<section class="m-poem">
<div class="m-page-header">
<div class="m-contact">


Charles Lutwidge Dodgson

The Mount Cemetery

Guildford, England

United Kingdom


</div><div class="m-facts">


48 lines


</div></div>


<div class="m-title-header">


# Jabberwocky

### by Lewis Carroll


</div>


```
’Twas brillig, and the slithy toves
   Did gyre and gimble in the wabe;
All mimsy were the borogoves,
   And the mome raths outgrabe.
```
```
“Beware the Jabberwock, my son
   The jaws that bite, the claws that catch!
Beware the Jubjub bird, and shun
   The frumious Bandersnatch!”
```
```
He took his vorpal sword in hand;
   Long time the manxome foe he sought—
So rested he by the Tumtum tree,
   And stood awhile in thought.
```
```
And, as in uffish thought he stood,
   The Jabberwock, with eyes of flame,
Came whiffling through the tulgey wood,
   And burbled as it came!
```
```
One, two! One, two! And through and through
   The vorpal blade went snicker-snack!
He left it dead, and with its head
   He went galumphing back.
```
```
“And hast thou slain the Jabberwock?
   Come to my arms, my beamish boy!
O frabjous day! Callooh! Callay!”
   He chortled in his joy.
```
```
’Twas brillig, and the slithy toves
   Did gyre and gimble in the wabe;
All mimsy were the borogoves,
   And the mome raths outgrabe.
```


</section> <!-- /.m-poem -->




[comment]: / "------ CITATION CHAPTER + SCENE (used only for example) --------"




<section class="m-chapter">
<div class="m-title-header">


# Acknowledgments


</div>


<section class="m-scene foothang">


Woodsworth, William. 1807. (Revised 1815.) "I Wandered Lonely as a Cloud." In *Poems, in Two Volumes*. London: Longman, Hurst, Rees, and Orms.

Carroll, Lewis. "Jabberwocky." 1871. In *Through the Looking-Glass*. London: Macmillan and Co.


</section></section> <!-- end chapter + specialized scene -->


</article></div> <!-- ------------------------------ end of manuscript ---- -->

