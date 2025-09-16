<!--
Crepuscular Dreams, a poem
Copyright © 2019 Todd Warner

I wrote this in 2019. It's my favorite poem of mine. Hope you like it as
well.

In this, I used the manuscript CSS as a baseline to then modify the document
for presentation, not submission. It's an example of a few things you can do
if you are CSS-savvy.

Customizations:
- The page
  - A5 sized paper instead of US Letter.
  - I selected the 'dim' theme. (This only affects the preview and not the PDF
    or printed form of this document.)
- The document
  - Crimson Text as the baseline font (prettier)
  - font-size 14.5pt instead of 12pt
  - Shrank the content size to 73% of the page's width so that the poem
    looks more centered on the content.
  - Enabled the 'simple' flag to get rid of the contact information, poem
    facts, and to move the title to the top of the page.
- Title:
  - increased the size and left-aligned it
  - changed font to Overpass (a sans-serif font often used for display
    text). Notice, that I had to force the title header to be 100% of the
    width (usually it is set narrower and centered).
- Footnotes!
  The first content block is an 'm-poem' class <section>. The second content
  block is an 'm-scene' class <section>. But I wanted the content to be
  footnotes, and so …
  - 'no-break' switch enabled to remove the preceding page break that would
    normally occur if this were a manuscript.
  - 'foothang' switch enabled so that the text is formatted as hanging
    indents.
  - added a top margin to the scene to shove it away from the poem a bit.
  - reduced the font size by 60% because the content is not the focus of the
    work.

A note about footnotes and lines that begin with a number and a period. For
example our footnote begins with (2019) 2022. If that began with 2022, which in
the original version of this, it did, you would have to escape that period
using a backslash. I.e., it would be 2022\. instead. Why? Because markdown
thinks a number. means you want an enumerated (ordered) list there and not a
paragraph. Markdown is great, but sometimes it can catch you in an awkward
spot.
-->


<style>
    @import url("https://toddwarner.io/pub/css/tw-font-sans-overpass.css");
    @import url("https://toddwarner.io/pub/css/tw-font-serif-crimson.css");
    @import url("https://toddwarner.io/pub/css/manuscript-css/manuscript.css");
    /*
    @import url("../../manuscript-local.css");
    @import url("../../manuscript-local-beta.css");
    */
    h1 {
        font-size: 125% !important;
        text-align: left !important;
    }
    .m-poem > .m-title-header {
        font-family: overpass, sans-serif !important;
        max-width: 100% !important;
    }
    .m-scene {
        margin-block-start: .5in !important;
        font-size: 60%;
    }
    :root {
      --m-fontstack-serif: "Crimson Text", serif;
      --m-font-size: 14.5pt !important;
      --m-content-width: calc(var(--m-page-width) * .73);
    }
</style>

<div id="vpage" class="A5 dim">
<article id="manuscript" class="poetry simple">

<section class="m-poem">

<div class="m-page-header">
<div class="m-contact">

Todd Warner  
North Carolina Piedmont, USA  
todd@toddwarner.io

</div><div class="m-facts">

7 lines

</div></div>

<div class="m-title-header">

# Crepuscular Dreams

</div>


```
Night. Yet morning.
Crepuscular. Cool.
```

```
Half-awake. Half-asleep.
Quiet but for the whispered secrets of invertebrates.
```

```
Just then, an emergent glow.
```

```
As night surrenders to birdsong,
Dreamers wake and face the dawn.
```

```
     —Todd Warner
```

</section>
<section class="m-scene foothang no-break" style="font-size: 60%; margin-block-start: .5in;">

Copyright © 2019 Todd Warner

(2019) 2022\. In *County Lines*, Vol. 7 2020.
December 4, 2019. Louisburg, NC: Writers Guild, Franklin County Arts Council. Revised November 12, 2022.

</section>
</article>
</div>

