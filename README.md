# Manuscript Formatting for Markdown for Writers

_Draft your novel or short story in markdown, then export to industry standard
manuscript format._

Are you a writer? In particular a narrative writer? Fiction, narrative
non-fiction, memoir, personal narratives, etc.? Do you draft using a markdown
text editor? And do you wish to share your drafts in a professional manner
without having to jump toolchainss? Save the fancy office word processors like
LibreOffice or Google Docs or Word for submission finalization. Now, you can
stay in your favorite markdown editor and still have a means to present your
working drafts in a professional manner for review, critique, or whatever.

Importing this `manuscript.css` stylesheet plus leveraging a bit of HTML in
your markdown document will configure your work to render in and export to a
generalized industry standard manuscript format.

**TL;DR** - how to use: check out the sample manuscripts in this repository.

> Just remember, when you submit to an editor, they will likely have very
> specific requirements for the format of your manuscript. The rule is: submit
> in whatever format they demand. This is not for that.

> Do you need to produce a book from your markdown? This is not that. But if
> you do want to do that, check out [Bookdown](https://www.bookdown.org/).
> Bookdown, though very intriguing, also looks rather daunting and geared for
> the science community.

### Supported formatting

1. A generalized manuscript format for prose.
2. US Letter- or A4-dimensioned artifacts.
3. Short-form (e.g. short stories) and long-form (novel and book-sized) works.
4. Narrative and non-narrative prose.
5. A lot of customization if you know your CSS.

## What this does not support

- Nuanced out-of-the-box customization.
- No 'Lastname / Short Title / Page number' in the headers of page 2 and
  onward. Not yet anyway.
- There is a bug with page breaking. The CSS is configured to disallow page
  breaking in weird places, like between a chapter title and the prose, but
  those rules are ignored. I don't know why.

## What's completely untested

- Tables
- I have also done no styling for images. If you want to add images to your
  document, you are on your own. For now. I'll probably play with that in the
  future.
- I have tested `manuscript.css` with only a couple markdown environments. Some
  editors change the look and feel of certain elements, so just be aware. Since
  I overload the purpose of Joplin when I draft, I had to create a set of CSS
  to squash all of its Joplinisms when I render the document. Let me know what
  you see out there in the wild.
- Using this with HTML instead of markdown. Well, it should just work, I just
  haven't tried it. I mean, markdown, in the end, is really just HTML with a
  bit of varnish.

## For the Future

- The one big missing feature is, as I mentioned above, support for a per-page
  header with `LASTNAME / SHORT TITLE / PAGENUMBER` in the upper-right-hand
  corner. If I can get that working (via javascript maybe?) I may be able to
  never leave markdown, even for submissions (assuming they accept PDF). I
  mention this again because it annoys me.
- More options for the placement of `#m-facts`.

## My writer's workflow:

1. 0-draft: either in markdown or hand-written
2. work-in-progress: markdown drafting via the Joplin desktop application
   <https://joplinapp.org>. (_Joplin is a note-taking software application that
   also serves as an excellent general purpose markdown editor._)
3. review by other: I periodic share drafts or portion of a drafts with
   critique partners, alpha readers, and beta readers. For this, I also use
   Joplin's excellent Joplin Cloud service which has a really convenient
   publish-to-the-web feature.
4. submission for publication: I port my markdown over to LibreOffice writer. I
   developed a manuscript template and it doesn't take me long to convert my
   markdown to LibreOffice, do a final proofread, and then submit a .docx file.

## Structure summary of a manuscript drafted in markdown

### The `<style>` and first `vpage` and `manuscript` wrappers

These will be your first few lines of your markdown

#### Example 1: The default format and behavior

```markdown
<!-- Formatting: US letter, 1in margins, short-form narrative -->
<style>
    @import "manuscript.css";
</style>
<div id="vpage"><div id="manuscript">
... your manuscript ...
```

#### Example 2: The alternative high-level format and behavior adjustments

```markdown
<!-- Formatting: A4, 25.4mm margins, long-form non-narrative          -->
<!--             I.e. All the big switches reversed from the default. -->
<style>
    @import "manuscript.css";
    @page { size: A4 portrait; margin: 25.4mm; }
</style>
<div id="vpage"><div id="manuscript" class="A4 long non-narrative">
... your manuscript ...
```

> **A note about rendering a long-form manuscript.**  
> Manuscripts formatted for things like novels will page break for every
> part and chapter and place their title blocks 1/3rd of the way down the page.
> Well, you can't do that for regular screen output. Instead, I display a faint
> dashed line where the pagebreak would go, and skip the big margin all
> together. When you go to export the document to PDF or to the printer, those
> extra lines (and the manuscript border for that matter) will go away.

### The high-level containers

This is great for quick reference. Just remember that, depending on the nature
of your prose, parts are not required, nor are chapters. But you will always
have to have scenes (duh). And per-container `m-header`s are not required
except for the main title and author section.

```markdown
<style>
    @import "manuscript.css";
</style>
<div id="vpage"><div id="manuscript">

<!-- required: contact name, address, email, phone -->
<div id="m-contact">
</div>

<!-- required: title, subtitle, by Author,
     wordcount/genre facts, and epigraph (optional) -->
<div class="m-header">
<div id="m-facts">
</div>
</div>

<!-- optional: part - parts contain chapters -->
<section class="part">
<!-- suggested: part title, subtitle, by Author, epigraph -->
<div class="m-header">
</div>

<!-- optional (for short prose): chapter - chapters contain scenes -->
<section class="chapter">
<!-- suggested: chapter title, subtitle, by Author, epigraph -->
<div class="m-header">
</div>

<!-- required: scene - scenes contain your prose (example, three scenes) -->
<section class="scene">
<!-- optional: scene title, subtitle, by Author, epigraph -->
<div class="m-header">
</div>
</section>

<!-- a between-scene dingus -->
###### \#

<section class="scene">
<div class="m-header">
</div>
</section>

###### \#

<section class="scene">
<div class="m-header">
</div>
</section>

</section>
</section>

<!-- the end of prose -30- marker -->
###### The End

</div></div>
```


### The `<div id="m-contact">`

#### at the top-level ...

`h1`, `h2`, `h3` represent Title, Subtitle, and by Author in this context. The
`m-facts` represents facts about your prose, namely word count and sometimes
genre, and audience (especially if not for adults). The `>` blockquote
represents a
[epigraph](https://en.wikipedia.org/wiki/Epigraph_(literature)) in this
context, though I think epigraphs are unusual for a manuscript at the main
title block.  But I use it at times.

<div id="contact">

# Title of Story

## Subtitle of Story

### by Firstname Lastname

<div id="m-facts">

2000 words

Literary Fiction

</div>

> _There is nothing to writing. All you do is sit down at a typewriter and
> bleed._ —Ernest Hemingway

</div>

#### `<div class="m-header">` at the part chapter and scene levels

It works just the same, except that there is no `m-facts` div-block.


### FONTS / TYPEFACES

The default fonts used by the manuscript are ones selected to conform to what
is expected—namely Times New Roman close equivalents, but also Arial and
Courier New, depending on need.

You really don't need to import new typefaces (your computer should know how to
handle a request for any one of those), but if you want to explore my open
source font recommendations, just add these imports to the top of your
manuscript:

```markdown
<style>
    @import "https://toddwarner.io/pub/css/m-font-serif-termes.css";
    @import "https://toddwarner.io/pub/css/m-font-serif-tinos.css";
    @import "https://toddwarner.io/pub/css/m-font-sans-arimo.css";
    @import "https://toddwarner.io/pub/css/m-font-mono-cousine.css";
    @import "manuscript.css";
</style>
```

## Good luck!

Check out the example manuscripts in this repository and I think how everything
you work with `manuscript.css` becomes obvious.

Good luck. Now, quit fooling around on the internet and write something.

Copyright (c) Todd Warner <t0dd@protonmail.com>
This work is licensed under Attribution 4.0 International. To view a copy
of this license, visit http://creativecommons.org/licenses/by/4.0/

---

## Addendum

### General manuscript formatting guidelines

Please note, again, that manuscript formatting is a loose standard and
ultimately governed by to whomever you are submitting. For example, if a
publishing house demands the typeface by Comic Sans, you format your manuscript
in Comic Sans.

Here are some general guidelines.

#### Novels

- <https://www.shunn.net/format/novel/>
- <https://graemeshimmin.com/manuscript-format-for-novel-submission/> A4!
- <https://blog.reedsy.com/guide/book-manuscript-format/>

#### Novellas

- <https://www.shunn.net/format/2009/03/proper_novella_format.html>

#### Short Narratives

- <https://www.shunn.net/format/story/>

#### Poetry!

Poetry is beyond the scope of this project, but it is doable by designating the
`.short` for the `#manuscript` div, setting `--m-indent` to 0 and managing
the physical layout of the poetry by hand. Markdown was not truly designed for
stuff like this, but if you want to maintain all of your writing drafts in a
single format, for example, it makes sense.

- <https://www.shunn.net/format/poetry/>

