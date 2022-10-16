# Manuscript Formatting for Markdown for Writers

_Draft your novel or short story in markdown, then export to industry standard
manuscript format._

Are you a writer? In particular a narrative writer? (Fiction, narrative
non-fiction, memoir, personal narratives, etc.) Do you draft in markdown? And
do you wish to share your drafts in a professional manner without having to
jump tools? Save the fancy office suites like LibreOffice or Google Docs or
Word for submission finalization. Now you can present your working drafts in a
professional manner for review, critique, or whatever.

Importing this `manuscript.css` stylesheet plus leveraging a bit of HTML in
your markdown document will configure your work to render in and export to a
generalized industry standard manuscript format.

How to use: TL;DR - Check out the sample manuscripts in this repository.

> Just remember, when you submit to an editor, they will likely have very
> specific requirements for the format of your manuscript. The rule is: submit
> in whatever format they demand. This is not for that.

> Do you need to produce a book from your markdown? This is not that. But if
> you do want to do that, check out [Bookdown](https://www.bookdown.org/).
> Bookdown, though very intriguing, also looks rather daunting and geared for
> the science community.

### Supported formatting:

1. A generalized manuscript format for prose.
2. US Letter- or A4-dimensioned artifacts.
3. Short-form (e.g. short stories) and long-form (novel and book-sized) works.
4. Narrative and non-narrative prose.
5. A lot of customization if you know your CSS.

### What this does not support:

- Nuanced out-of-the-box customization.
- No 'Lastname / Short Title / Page number' in the headers of page 2 and onward.
  Not yet anyway.
- There is a bug with page breaking. The CSS is configured to disallow
  page breaking in weird places, like between a chapter title and the prose, but
  those rules are ignored. I don't know why.

### Completely untested:

- Tables
- I have also done no styling for images. If you want to add images to your
  document, you are on your own. For now. I'll probably play with that in the
  future.
- I have tested manuscript.css with only a couple markdown editors and
  renderers. Some editors change the look and feel of certain elements, so just
  be aware. Since I overload the purpose of Joplin when I draft, I had to
  create a set of CSS to squash all of its Joplinisms when I render the
  document. Let me know what you see out there in the wild.
- Using this with HTML instead of markdown. Well, it should just work, I just
  haven't tried it. I mean, markdown, in the end, is really just HTML with a bit
  of varnish.

### My writer's workflow:
1. 0-draft: either in markdown or hand-written
2. work-in-progress: markdown drafting via the Joplin desktop application
   <https://joplinapp.org>. (_Joplin is a note-taking software application that
   also serves as an excellent general purpose markdown editor._)
3. review by other: I periodic share drafts or portion of a drafts with critique
   partners, alpha readers, and beta readers. For this, I also use Joplin's
   excellent Joplin Cloud service which has a really convenient "publish to the
   web" feature.
4. submission for publication: I port my markdown over to LibreOffice writer. I
   developed a manuscript template and it doesn't take me long to convert my
   markdown to LibreOffice, do a final proofread, and then submit a .docx file.

### For the Future
- The one big missing feature is, as I mentioned above, support for a per-page
  header with LASTNAME / SHORT TITLE / PAGENUMBER in the upper-righthand
  corner. If I can get that working (via javascript maybe?) I may be able to
  never leave markdown, even for submissions (assuming they accept PDF).

### Structure summary of a manuscript drafted in markdown

```markdown
<style>
    @import "manuscript-core.css";
</style>
<div id="vpage"><div id="manuscript">

<div id="m-contact">
... your name, address, email, cell, and date ...
</div>

<div class="m-header">
... title, subtitle, author ...
<div id="m-facts">
... wordcount, genre ...  
</div>
... an epigraph if you like ...
</div></div>

<!-- Note that there can be many scenes w/in a chapter, many chapters w/in a
     part, and many parts w/in a manuscript. Chapters & parts are optional.
     And, though titling and such are supported for scenes, it's something
     commonly done. Useful for embedded draft notes into a manuscript. -->

<section class="m-part">
<div class="m-header">
... part title, etc ...
</div>
<section class="m-chapter">
<div class="m-header">
... chapter title, etc ...
</div>
<section class="m-scene">
<div class="m-header">
... scene title, etc ...
</div>
... this scene's prose ...
</section>
<section class="m-scene">
<div class="m-header">
... scene title, etc ...
</div>
... this scene's prose ...
</section>

###### \#

<section class="m-scene">
... the next scene, etc ...
</section>
<section class="m-chapter">
... chapter 2 and its scenes, then chapter 3, etc ...
</section>
<section class="m-part">
... part 2 and its chapters, then part 3, etc ...
</section>

###### The End

</div></div>
<!-- the end of the manuscript -->
```

That top bit can be tweaked. For example, if I wanted to format the manuscript
as a long-form, non-narrative work destined to produce A4-dimensioned
artifacts, I would just have to edit a few things:

```markdown
<!-- the beginning of markdown file -->
<style>
    @import "manuscript.css";
    @page { size: A4 portrait; margin: 25.4mm; }
</style>
<div id="vpage"><div id="manuscript" class="A4 long non-narrative">
    ... your manuscript ...
```

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
</style>
```

Good luck. Now, quit fooling around on the internet and get back to writing.

Copyright (c) Todd Warner <t0dd@protonmail.com>
This work is licensed under Attribution 4.0 International. To view a copy
of this license, visit http://creativecommons.org/licenses/by/4.0/

