# Document Switches to Customize your Manuscript (the beta version)

Copying a template and filling in the blanks is all you really need to know,
but there are a number of switches at your disposal the customize the end
result if you need to tweak the formatting.

Also included are theme switches. These only effect the rendered view, not the
PDF export. Namely, a bunch of "dark modes" so that if you working at night,
you can make your intimediary preview of your manuscript not blind you.

## `#vpage` switches - switches associated to the page itself

To turn these on, you add them to the class attribute of the vpage div:
```html
<div id="vpage" class="add-switch-here and-here-is-another-one">
```

&ZeroWidthSpace;

### `div#vpage` Switches to Theme Your Document Preview

<dl>
    <dt>dim</dt>
    <dd>Easier on the eyes, but not dark mode.</dd>
    <dt>dimmer</dt>
    <dd>Even easier on the eyes, but not yet dark mode.</dd>
    <dt>dark</dt>
    <dd>Dark mode! A very light gray on dark background.</dd>
    <dt>dark yellow</dt>
    <dd>Dark mode! But yellow themed.</dd>
    <dt>dark green</dt>
    <dd>Dark mode! But green themed.</dd>
    <dt>dark cyan</dt>
    <dd>Dark mode! But cyan themed.</dd>
    <dt>dark blue</dt>
    <dd>Dark mode! But blue themed.</dd>
    <dt>dark purple</dt>
    <dd>Dark mode! But purple themed.</dd>
    <dt>dark pink</dt>
    <dd>Dark mode! But pink themed.</dd>
    <dt>dark red</dt>
    <dd>Dark mode! But red themed.</dd>
    <dt>dark amber</dt>
    <dd>Dark mode! But amber themed.</dd>
    <dt>hide-jcloud-navbar</dt>
    <dd>Joplin (Joplin Cloud) specific. If you absolutely must hide the navbar
    when you publish to Joplin Cloud, this switch will enable that. It leaves
    the footer in place so that the Joplin Cloud service is appropriately
    acknowledged.</dd>
</dl>

&ZeroWidthSpace;

### `div#vpage` Switches Governing Papersizes and Orientation

<dl>
    <dt>US</dt>
    <dd>US Letter sized (the default): 8.5in x 11in (216mm x 279mm) with 1in (25.4mm) margins</dd>
    <dt>USh</dt>
    <dd>US half-letter sized: 5.5in x 8.5in (140m x 216mm) with 1/2in (12.7mm) margins</dd>
    <dt>A4</dt>
    <dd>A4 sized: 210mm x 297mm (8.3in x 11.7in) with 25.4mm (1in) margins</dd>
    <dt>A5</dt>
    <dd>A5 sized: 148mm x 210mm (5.8in x 8.3in) with 12.7mm (1/2in) margins</dd>
    <dt>A6</dt>
    <dd>A6 sized: 106mm x 148mm (4.1in x 5.8in) with 6.35mm (1/4in) margins</dd>
    <dt>portrait</dt>
    <dd>(The default) Height is longer than width.</dd>
    <dt>landscape</dt>
    <dd>The reverse: width is longer than height.</dd>
    <dt>—marginalia (lastname / story title / page-number) switches—</dt>
    <dt>no-marginalia</dt>
    <dd>Turns off marginalia. (The default if the `poetry` class is set for `#manuscript` (see below).)</dd>
    <dt>no-marginalia</dt>
    <dd>Turns off page marginalia.</dd>
    <dt>top-right-marginalia</dt>
    <dd>Margin header will be set to appear at the top right corner of the page. This is the default for prose.</dd>
    <dt>top-left-marginalia</dt>
    <dd>Margin header will be set to appear at the top left corner of the page.</dd>
    <dt>top-center-marginalia</dt>
    <dd>Margin header will be set to appear at the top center of the page.</dd>
    <dt>bottom-right-marginalia</dt>
    <dd>Margin header will be set to appear at the bottom right corner of the page.</dd>
    <dt>bottom-left-marginalia</dt>
    <dd>Margin header will be set to appear at the bottom left corner of the page.</dd>
    <dt>bottom-center-marginalia</dt>
    <dd>Margin header will be set to appear at the bottom center of the page.</dd>
</dl>

### Configuring the content of the margin header

If your document is a work of prose, page headers will be added to page 2 and
onward. If your document is a work of poetry, the header will not appear. It
will also not appear if you have added `no-marginalia` to the `#vpage` block
declaration: `<div id="vpage" class="no-marginalia">`.

If configure the header appropriately, you need to reset the value of the CSS
variable `--m-marginalia`. To do that, you add to the `<style> … </style>`
block at the top of your document. Replace `Penlastname` with your author last
name, of course, and `Story Title` with the title of your story. If the title
of your story is lengthy, use a truncated or shortened version of that title.

_(Note, there is debate about whether to use your legal last name in the page
headers or to use the last name of your pen name (author name). We are
defaulting to the assumption that it should be your last name used in your
byline (your pen name). Discuss this requirement with your agent.)_

```css
    --m-marginalia: "Penlastname / Story Title / " counter(page);
```

&ZeroWidthSpace;

&ZeroWidthSpace;

## `#manuscript` switches - switches more associated to the document as a whole

To turn these on, you add them to the class attribute of the manuscript
article:

```html
<div id="vpage">
<article id="manuscript" class="add-switch-here and-here-is-another-one">
```

&ZeroWidthSpace;

### `#manuscript` Switches Governing Prose (narratives)

<dl>
    <dt>short</dt>
    <dd>For short works of prose, like short stories (the default), this switch
    will alter how the 1st page is structured: the word count block in the
    upper right-hand corner or at the bottom, and the first page will not break
    after the title block.</dd>
    <dt>long</dt>
    <dd>For longer works (novels, novellas, etc). Again, this switch will alter
    the exported manuscript to match the shunn.net novel spec: word count on
    the bottom and centered, and a page-break after the novel title block.</dd>
    <dt>narrative</dt>
    <dd>(The default) Serif font (Times New Roman, by default). Paragraphs are
    1st line indented with no spacing between.</dd>
    <dt>nonnarrative</dt>
    <dd>Sans serif font (Aria, by default). Paragraphs are space separated and
    without indent.</dd>
    <dt>indent-first</dt>
    <dd>Force the first paragraph of prose to be indented. (This is the default
    behavior for narrative prose in manuscript-css.)</dd>
    <dt>unindent-first</dt>
    <dd>Force the first paragraph of prose to be unindented. (Industry standard
    manuscript format says to indent the first paragraphs of narrative
    prose.)</dd>
    <dt>indent-first-epigraph</dt>
    <dd>Force the first paragraph on an epigraph to be indented.</dd>
    <dt>unindent-first-epigraph</dt>
    <dd>Force the first paragraph on an epigraph to be unindented. (This is the
    default for narrative works in manuscript-css.)</dd>
    <dt>space-paragraphs</dt>
    <dd>Force nonnarrative-style paragraph spacing.</dd>
    <dt>unspace-paragraphs</dt>
    <dd>Force narrative-style paragraph spacing.</dd>
    <dt>narrative-spacing</dt>
    <dd>Force narrative-style indenting and paragraph spacing.</dd>
    <dt>nonnarrative-spacing</dt>
    <dd>Force nonnarrative-style indenting and paragraph spacing.</dd>
</dl>

&ZeroWidthSpace;

### `#manuscript` Switches for Poetry

<dl>
    <dt>poetry</dt>
    <dd>Formats the manuscript appropriately, stripping out things the default
    poetry manuscript doesn't need. Note, if you add title page elements,
    'poetry' documents are formatted like long narratives for that page.</dd>
</dl>

&ZeroWidthSpace;

### `#manuscript` Switches to Simplify the Appearance of Your Document

<dl>
    <dt>simple</dt>
    <dd>(prose only) Strips out andy contacts and word counts. Great for
    sharing with friends and family who don't need to see that formal element
    of your manuscript.</dd>
    <dt>text-only</dt>
    <dd>(prose only) Strips out all contact info, titles, word count, all
    dinkuses, and the ending -30- marker. Gives you are "just show me the
    words" view.</dd>
    <dt>no-dinkuses</dt>
    <dd>(prose only) Strips out all of the dinkuses.</dd>
    <dt>no-30-</dt>
    <dd>(prose only) Strips out the ending -30- marker. (The End or ###
    etc.)</dd>
    <dt>no-simulation</dt>
    <dd>(long narratives and poetry only) Strips out all simulated page-breaks
    (those dashed lines).</dd>
</dl>

&ZeroWidthSpace;

### Other `#manuscript` Switches

<dl>
    <dt>no-links</dt>
    <dd>Disable all links in the document. Both for the rendered version and print/PDF export.</dd>
    <dt>no-links-export</dt>
    <dd>Disable all links when exporting (print/PDF) the document.
    (Bug alert! Chrome's export to PDF not honor our overrides to
    `pointer-events` or `cursor` (CSS). And so, the link still functions within
    the PDF. But at least it doesn't *look* like a link.)</dd>
    <dt>no-notes</dt>
    <dd>All notes will be hidden (for all presentations of the document). (By
    default, document notes are visible in preview and upon export, but not in
    Joplin Cloud.)</dd>
    <dt>show-notes</dt>
    <dd>Force all notes to be visible.</dd>
    <dt>no-notes-export</dt>
    <dd>Notes will not be included with the exported (print/PDF) document.</dd>
    <dt>show-notes-export (the default)</dt>
    <dd>Notes will be included with the exported (print/PDF) document.</dd>
    <dt>no-notes-jcloud (the default)</dt>
    <dd>Notes will not be included when viewing the document via Joplin
    Cloud</dd>
    <dt>show-notes-jcloud</dt>
    <dd>Notes will be included when viewing the document via Joplin
    Cloud</dd>
    <dt>classic</dt>
    <dd>You like that old-time monospaced Courier (now Courier Prime by
    default), don't you?</dd>
</dl>

&ZeroWidthSpace;

&ZeroWidthSpace;

---

&ZeroWidthSpace;

&ZeroWidthSpace;

## `.chapter`, `.scene`, `.poem` switches - switches shared between these structural elements

Switches usable by all of these elements. For example:

```html
<div id="vpage" class="US dark">
<article id="manuscript" class="long">

[ . . . ]

<div class="chapter add-your-switch-here">
```

<dl>
    <dt>no-break</dt>
    <dd>Removes the preceding page break if one exists.</dd>
    <dt>force-break-before</dt>
    <dd>Adds a page break before the element if it didn't exist
    previously.</dd>
    <dt>force-break-after</dt>
    <dd>Adds a page break after the element if it didn't exist previously.</dd>
</dl>

&ZeroWidthSpace;

&ZeroWidthSpace;

## `.scene` switches - switches associated to prose content

Switches available to a scene beyond what has been mentioned previously.

```html
<div id="vpage" class="US dark">
<article id="manuscript" class="long">

[ . . . ]

<div class="scene add-your-switch-here">
```

<dl>
    <dt>no-break</dt>
    </dd>See above description.</dd>
    <dt>break-before</dt>
    </dd>See above description.</dd>
    <dt>break-after</dt>
    </dd>See above description.</dd>
    <dt>unindent</dt>
    <dd>Remove paragraph indenting. This does not add between-paragraph spacing
    and it does not change the font to sans-serif. A 'nonnarrative' override
    does not exist yet. If you are need that functionality, just let me
    know.</dd>
    <dt>foothang</dt>
    <dd>Convert all paragraphs in the scene to hanging indent format. Useful
    for endnotes, citation, and the like. Note: You can also wrap paragraphs
    in a `<div class="foothang"> [ . . . ]</div>` if you like so that only
    a portion of your `.scene` needs to be formatted as such.</dd>
    <dt>no-dinkus</dt>
    <dd>Will not add a dinkus at the end of the scene if one would normally be
    placed there.</dd>
</dl>


&ZeroWidthSpace;

&ZeroWidthSpace;

## `.poem` switches - switches associated to poem content

Switches available to a poem beyond what has been mentioned previously. Note
that poems have a title header that can have a prose element where the above
prose-oriented switches can have an effect.

```html
<div id="vpage" class="US dark">
<article id="manuscript" class="poetry">

[ . . . ]

<div class="poem add-your-switch-here">
```

<dl>
    <dt>no-break</dt>
    </dd>See above description.</dd>
    <dt>break-before</dt>
    </dd>See above description.</dd>
    <dt>break-after</dt>
    </dd>See above description.</dd>
</dl>

