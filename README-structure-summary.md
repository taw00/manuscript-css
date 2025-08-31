# Structure summary of a manuscript drafted in markdown

### Example 1: The document beginning

_Note that "./manuscript.css" here is a stand-in for
"/path/to/manuscript-css/manuscript.css". Or if you decide to host it on some
webserver, "https://yourwebsite.com/pub/css/manuscript-css/manuscript.css"._

```markdown
<!-- Default Formatting: US letter, 1in margins, short-form narrative -->
<style>
    @import url("./manuscript.css");
</style>
<div id="vpage">
<article id="manuscript">
... your manuscript ...
```

### Example 2: The document beginning - w/ alterations

```markdown
<!-- Formatting: A4, 2.54cm margins, long-form nonnarrative                 -->
<style>
    @import url("./manuscript.css");
</style>
<div id="vpage" class="A4">
<article id="manuscript" class="long nonnarrative">
... your manuscript ...
```

### Example 3: the high-level containers

`manuscript.css` structures the document into parts, chapters, and scenes. And
if poetry, parts, chapters and poems. In the end, parts and chapters are not
absolutely required. The meat of your manuscript lives either in a scene or a
poem. Most short stories, for example, only use scenes. Often only one scene
container.

The containers, in summary:  
(*Note: section blocks can be repeated infinite times.*)

```html
<div id="vpage">                                            <!-- 1 required -->
    <article id="manuscript">                               <!-- 1 required --> 
        <div id="m-contact"></div>                   <!-- 0 or 1 is allowed -->
        <div class="m-header">                       <!-- 0 or 1 is allowed -->
            <div class="m-facts"></div></div>        <!-- 0 or 1 is allowed -->
        <section class="m-part">              <!-- 0 to many allowed --------->
            <div class="m-header"></div>             <!-- 0 or 1 is allowed -->
            <section class="m-chapter">       <!-- 0 to many allowed --------->
                <div class="m-header"></div>         <!-- 0 or 1 is allowed -->
                <section class="m-scene">     <!-- 1 required; many allowed -->
                    <div class="m-header"></div>     <!-- 0 or 1 is allowed -->
                </section
            </section>
        </section>
    </article>
</div>
```



### A fuller example (*also see templates in the templates folder*)

This is a truncated example of a short story. It's three scenes contained
within one chapter, and that chapter within one part. But you can have many parts containing many chapters containing many scenes.



```markdown
<style>
    @import url("./manuscript.css");
</style>

<div id="vpage">
<article id="manuscript">

<!-- contact name, address, email, phone --
  -- (note: m-contact is optional)       -->
<div id="m-contact">

Edgar Allan Poe

Coates Street, Philadelphia, PA 19079 USA

telleroftales@example.com

</div>

<!-- title, subtitle, author byline, and epigraph --
  -- then wordcount and genre facts               -->
<div class="m-header">

# The Tell-Tale Heart

# … a subtitle if there were one …

### by Edgar Allan Poe

> They heard!—they suspected!—they knew!

<!-- notice that .m-facts in contained within .m-header -->

<div id="m-facts">

2200 words

Gothic Horror

</div>
</div>

<!-- "section.part"s contain "section.chapter"s -->
<section class="part">

<!-- the part's title (and could have, subtitle, author byline, & epigraph) -->
<div class="m-header">

# Part 1

</div>

<!-- "section.chapter"s contain section.scene"s (or "section.poem"s) -->
<section class="chapter">

<!-- the chapter's  title, subtitle, author byline, epigraph -->
<div class="m-header">

# Chapter 1

</div>

<!-- "section.scene"s contain your prose - an example of three scenes -->
<section class="scene">

<!-- scene title, subtitle, author byline, epigraph
     (I rarely use m-headers in scenes) -->
<div class="m-header">

# My Scene Title

### Contributing Author: Joe Blough

</div>

True!—nervous—very, very dreadfully nervous I had been and am; but why *will*
you say that I am mad? The disease had sharpened my senses—not destroyed—not
dulled them. Above all was the sense of hearing acute. I heard all things in
the heaven and in the earth. I heard many things in hell. How, then, am I mad?
Hearken! and observe how healthily—how calmly I can tell you the whole story.

It is impossible to say how first the idea entered my brain; but once
conceived, it haunted me day and night. Object there was none. Passion there
was none. I loved the old man. He had never wronged me. He had never given me
insult. For his gold I had no desire. I think it was his eye! [ … ]

</section>

<section class="scene">

Upon the eighth night I was more than usually cautious in opening the door. A
watch's minute hand moves more quickly than did mine. Never before that night
had I *felt* the extent of my own powers—of my sagacity. I could scarcely
contain my feelings of triumph. To think that there I was, opening the door,
little by little, and he not even to dream of my secret deeds or thoughts. I
fairly chuckled at the idea; and perhaps he heard me; for [ … ]

</section>

<section class="scene">

It was open—wide, wide open—and I grew furious as I gazed upon it. I saw it
with perfect distinctness—all a dull blue, with a hideous veil over it that
chilled the very marrow in my bones; but I could see nothing else of the old
man's face or person: for I had directed the ray as if by instinct, precisely
upon the damned spot.

And have I not told you that what you mistake for madness is but over-acuteness
of the sense?—now, I say, there came to my ears [ … ]

</section>

</section></section>
</article>
</div>
```

# Poetry!

To insert a poem in a document arbitrarily, it will be structured like this:

~~~markdown

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
~~~

- If your document is a manuscript for a single poem, `#manuscript` will be of
  `class="short poetry"` and a `.m-poem` instead of a `.m-scene`, you will have
  a solitary `.m-poem` filled with ```plaintext stanzas similar to `.x-poem`
  above.

- If your document is a manuscript of many poems, `#manuscript` will be of
  `class="long poetry"` and then many `.m-poem`s filled with ````plaintext`
  stanzas similar to `.x-poem` above. For long-form poetry, you probably want to
  add the `no-header` class to the `div#vpage` element: `<div id="vpage" class="no-header">`

## Good luck!

Check out the example manuscripts in this repository and I think how everything
works with `manuscript.css` becomes obvious.

Good luck. Now, quit fooling around on the internet and write something.

Copyright (c) Todd Warner <t0dd@protonmail.com>
This work is licensed under Attribution 4.0 International. To view a copy
of this license, visit http://creativecommons.org/licenses/by/4.0/
