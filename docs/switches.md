# Document Switches to Customize your Manuscript

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

### Themed Preview Switches

<dl>
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
</dl>

### Papersizes and Orientation Switches

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
</dl>


## `#manuscript` switches - switches more associated to the document as a whole

To turn these on, you add them to the class attribute of the manuscript
article:
```html
<div id="vpage" class="US dark">
<article id="manuscript" class="add-switch-here and-here-is-another-one">
```


### Prose Switches

<dl>
    <dt>short</dt>
    <dd>For short works of prose, like short stories (the default. Will alter
    how the 1st page is structured (where the facts-block lands, really) and
    the spacing of that page and others.</dd>
    <dt>long</dt>
    <dd>For longer works (novels, novellas, etc). Again, it will alter the
    exported manuscript to match the shunn.net novel spec.</dd>
    <dt>narrative</dt>
    <dd>(The default) Serif font (Times New Roman, by default). Paragraphs are
    1st line indented with no spacing between.</dd>
    <dt>nonnarrative</dt>
    <dd>Sans serif font (Aria, by default). Paragraphs are space separated and
    without indent.</dd>
</dl>

### Poetry Switches

<dl>
    <dt>poetry</dt>
    <dd>Formats the manuscript appropriately, stripping out things the default
    poetry manuscript doesn't need. Note, that if you wish a more prose format
    (1st page title and such) you can choose 'long' instead then add your poems
    within. You will have to experiment.</dd>
</dl>

### Simplification Switches

<dl>
    <dt>simple</dt>
    <dd>(prose only) Strips out the 1st page contact and all facts. Great for
    sharing with friends and family who don't need to see that formal element
    of your manuscript.</dd>
    <dt>text-only</dt>
    <dd>(prose only) Strips out all contact info, all facts, all dinkuses,
    and the ending -30- marker. Gives you are "just show me the words"
    view.</dd>
    <dt>no-dinkuses</dt>
    <dd>(prose only) Strips out all of the dinkuses.</dd>
    <dt>no-30-</dt>
    <dd>(prose only) Strips out the ending -30- marker. (The End or ###
    etc.)</dd>
</dl>

---

## `.m-book`, `.m-chapter`, `.m-scene`, `.m-poem` switches - switches shared between these structural elements

Switches usable by all of these elements. For example:

```html
<div id="vpage" class="US dark">
<article id="manuscript" class="long">

[ . . . ]

<div class="m-chapter add-your-switch-here">
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

## `.m-scene` switches - switches associated to prose content

Switches available to a scene beyond what has been mentioned previously.

```html
<div id="vpage" class="US dark">
<article id="manuscript" class="long">

[ . . . ]

<div class="m-scene add-your-switch-here">
```

<dl>
    <dt>no-break</dt>
    </dd>See above description.</dd>
    <dt>force-break-before</dt>
    </dd>See above description.</dd>
    <dt>force-break-after</dt>
    </dd>See above description.</dd>
    <dt>no-indent</dt>
    <dd>Remove paragraph indenting. This does not add between-paragraph spacing
    and it does not change the font to sans-serif. A 'nonnarrative' override
    does not exist yet. If you are need that functionality, just let me
    know.</dd>
    <dt>foothang</dt>
    <dd>Convert all paragraphs in the scene to hanging indent format. Useful
    for endnotes, citation, and the like. Note: You can also wrap paragraphs
    in a `<div class="foothang"> [ . . . ]</div>` if you like so that only
    a portion of your `.m-scene` needs to be formated as such.</dd>
    <dt>no-dinkus</dt>
    <dd>Will not add a dinkus at the end of the scene if one would normally be
    placed there.</dd>
</dl>


## `.m-poem` switches - switches associated to poem content

Switches available to a poem beyond what has been mentioned previously. Note
that poems have a title header that can have a prose element where the above
prose-oriented switches can have an effect.

```html
<div id="vpage" class="US dark">
<article id="manuscript" class="poetry">

[ . . . ]

<div class="m-poem add-your-switch-here">
```

<dl>
    <dt>no-break</dt>
    </dd>See above description.</dd>
    <dt>force-break-before</dt>
    </dd>See above description.</dd>
    <dt>force-break-after</dt>
    </dd>See above description.</dd>
</dl>

