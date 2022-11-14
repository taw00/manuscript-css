# Structure summary of a manuscript drafted in markdown

### Example 1: The document beginning - default format and behavior

_Note that "manuscript.css" here is a stand-in for
"/path/to/manuscript-css/manuscript.css". Or if you decide to host it on some
webserver, "https://yourwebsite.com/pub/css/manuscript-css/manuscript.css"._

```markdown
<!-- Formatting: US letter, 1in margins, short-form narrative -->
<style>
    @import "manuscript.css";
</style>
<div id="vpage">
<article id="manuscript">
... your manuscript ...
```

### Example 2: The document beginning - same as above with behavior adjustments

```markdown
<!-- Formatting: A4, 1in margins, long-form non-narrative          -->
<!--             I.e. All the big prose switches reversed from the default. -->
<style>
    @import "manuscript.css";
    @page { size: A4 portrait; margin: 1in; }
</style>
<div id="vpage" class="A4">
<article id="manuscript" class="long non-narrative">
... your manuscript ...
```

### Example 3: The high-level containers

`manuscript.css` structures the document into parts, chapters, and scenes. And
if poetry, parts, chapters and poems. In the end, parts and chapters are not
absolutely required. The meat of your manuscript lives either in a scene or a
poem. Most short stories, for example, only use scenes. Often only one scene
container.

Let's look at the containers in summary, and then we'll dive into a little
depth afterward.

# The containers in summary (prose-focused)...

```markdown
<style>
    @import "manuscript.css";
</style>
<div id="vpage">
<article id="manuscript" class="prose narrative">

<!-- suggested: contact name, address, email, phone -->
<div id="m-contact">
</div>

<!-- suggested: title, subtitle, by Author, wordcount/genre facts, and
     epigraph -->
<div class="m-header">
<div id="m-facts">
</div>
</div>

<!-- optional: part - parts contain chapters -->
<section class="part">
<!-- suggested: part title - rare: subtitle, by Author, epigraph -->
<div class="m-header">
</div>

<!-- optional: chapter - chapters contain scenes (or poems) -->
<section class="chapter">
<!-- suggested: chapter title - rare: subtitle, by Author, epigraph -->
<div class="m-header">
</div>

<!-- required (for prose): scene - scenes contain your prose
     An example of three scenes -->
<section class="scene">
<!-- unusual: scene title, subtitle, by Author, epigraph -->
<div class="m-header">
</div>
</section>

<section class="scene">
<div class="m-header">
</div>
</section>

<section class="scene">
<div class="m-header">
</div>
</section>

</section></section>
</article>
</div>
```


### The container `<div id="m-contact">`

The `m-contact` container is for your author or agent contact info. Example:

```markdown
<div id="m-contact">

Todd Warner

123 Main St

Example Town, NC 27560

email@example.com | +1 555-555-1212

</div>
```

### The container `<div class="m-header">`

One exists at the top level for the title and whatnot of the work. Then each
part, chapter, and scene can also optionally also have titles and things.

Within this container, `h1` (`#` in markdown), `h2` (`##`), `h3`
(`###`), and `blockquote` (`>`) are overloaded to represent ...

```markdown
<div id="m-header">

# Title of Story

## Subtitle of Story

### by Firstname Lastname

> An epigraph for my story. _There is nothing to writing. All you do is sit
> down at a typewriter and bleed._ —Ernest Hemingway

<div id="m-facts">

2000 words

Literary Fiction

(_draft rev. 20221029_)

</div>
```

**What's an epigraph you ask?** <https://en.wikipedia.org/wiki/Epigraph_(literature)>

Note, the `m-header`s in the parts, chapters, and scenes don't usually have `m-facts`.

# Fonts / Typefaces

The default fonts used by the manuscript are ones selected to conform to what
is expected—namely Times New Roman close equivalents, but also Arial and
Courier New, depending on need.

You really don't need to import new typefaces (your computer should know how to
handle a request for any one of those), but if you want to explore my open
source font recommendations, just add these imports to the top of your
manuscript (adding the path as needed, of course):

```markdown
<style>
    @import "typeface/typeface-serif-termes.css";
    @import "typeface/typeface-serif-tinos.css";
    @import "typeface/typeface-sans-arimo.css";
    @import "typeface/typeface-mono-cousine.css";
    @import "manuscript.css";
</style>
```

# Poetry!

To insert a poem in a document arbitrarily, it will be structured like this:

    <div class="x-poem">

    ```plaintext
       Poem stanza
           Here.
    ```
    ```plaintext
       Poem stanza
           Here.
    ```
    </div>

- If your document is a manuscript for a single poem, `#manuscript` will be of
  `class="short poetry"` and instead of a `.m-chapter` + `.m-scene`, you will
  have an _empty_ `.m-chapter` + a solitary `.m-poem` filled with ```plaintext
  stanzas similar to `.x-poem` above.

- If your document is a manuscript for a single poem, `#manuscript` will be of
  `class="short poetry"` and instead of a `.m-chapter` + `.m-scene`, you will
  have an _empty_ `.m-chapter` + a solitary `.m-poem` filled with
  ````plaintext` stanzas similar to `.x-poem` above.

## Good luck!

Check out the example manuscripts in this repository and I think how everything
works with `manuscript.css` becomes obvious.

Good luck. Now, quit fooling around on the internet and write something.

Copyright (c) Todd Warner <t0dd@protonmail.com>
This work is licensed under Attribution 4.0 International. To view a copy
of this license, visit http://creativecommons.org/licenses/by/4.0/
