# Structure summary of a manuscript drafted in markdown

It's generally easier to simply examine one of the templates in the template
folder, but, for those with a more analytical brain, here we present a
structural spec of sorts.

Note, all text that represents your words must be
bracketed by whitespace or it will not render correctly. That is a
markdown-mingling-with-html thing.

### Example 1: The document beginning

_Note that we use the locally imported url `"/path/to/manuscript.css"` here. If
you decided to host the repo on some webserver instead, it would be something
like: `"https://yourwebsite.com/pub/css/manuscript-css/manuscript.css"`._

```markdown
<!-- Default Formatting: US letter, 1in margins, short-form narrative -->
<style>
    @import url("/path/to/manuscript.css");
</style>
<div id="vpage">
<article id="manuscript">

... your manuscript ...

</article></div>
```

### Example 2: The document beginning - w/ alterations

```markdown
<!-- Formatting: A4, 2.54cm margins, long-form nonnarrative -->
<style>
    @import url("/path/to/manuscript.css");
</style>
<div id="vpage" class="A4">
<article id="manuscript" class="long nonnarrative">

... your manuscript ...

</article></div>
```

### Example 3: the high-level containers

`manuscript.css` structures the document into parts, chapters, and scenes. And
if poetry, parts, chapters and poems. In the end, parts and chapters are not
absolutely required. The meat of your manuscript lives either in a scene or a
poem. Most short stories, for example, only use scenes. Often only one scene
container. (Note, you can even add "book" sections do your document by
inserting `<div class="title-page"> … </div>` blocks where appropriate. Look
at `example-prose-long-and-complicated.md` for an example.)

The narrative or nonnarrative containers, in summary:  
(*Note: section blocks can be repeated infinite times.*)

```html
<style>
    @import url("/path/to/manuscript.css");
</style>
<div id="vpage">                                            <!-- 1 required -->
  <article id="manuscript" class="long">    <!-- 1 required (short or long) -->
    <div id="title-page">                                     <!-- 0 or 1 -->
        <div class="contact"></div>                           <!-- 0 or 1 -->
        <div class="count"></div>                             <!-- 0 or 1 -->
        <div class="title"></div>                             <!-- 0 or 1 -->
    </div>
    <section class="part">                          <!-- 0 to many --------->
      <div class="title"></div>                               <!-- 0 or 1 -->
      <section class="chapter">             <!-- 0 to many allowed --------->
        <div class="title"></div>                             <!-- 0 or 1 -->
        <section class="scene">            <!-- prose: 1 required to many -->
            <div class="title"></div>                         <!-- 0 or 1 -->

            [scene text in here]

        </section
        <section class="scene">            <!-- prose: 1 required to many -->
            <div class="title"></div>                         <!-- 0 or 1 -->

            [scene text in here]

        </section
        <section class="scene">            <!-- prose: 1 required to many -->
            <div class="title"></div>                         <!-- 0 or 1 -->

            [scene text in here]

        </section
      </section>
    </section>
  </article>
</div>
```


The poetry container, in summary:  
(*Note: section blocks can be repeated infinite times.*)

~~~html
<style>
    @import url("/path/to/manuscript.css");
</style>
<div id="vpage">                                            <!-- 1 required -->
  <article id="manuscript" class="poetry">                  <!-- 1 required -->
    <div id="title-page">           <!-- 0 or 1 - poetry collections only -->
        <div class="contact"></div>                           <!-- 0 or 1 -->
        <div class="count"></div>                             <!-- 0 or 1 -->
        <div class="title"></div>                             <!-- 0 or 1 -->
    </div>
    <section class="part">       <!-- 0 to many - poetry collections only -->
      <div class="title"></div>                        <!-- 0 or 1 -->
      <section class="chapter">  <!-- 0 to many - poetry collections only -->
        <div class="title"></div>                      <!-- 0 or 1 -->
        <section class="poem">            <!-- poetry: 1 required to many -->
            <div class="contact"></div>                       <!-- 0 or 1 -->
            <div class="count"></div>                         <!-- 0 or 1 -->
            <div class="title"></div>                         <!-- 0 or 1 -->

            [poetry stanzas in here in between ```'s]

        </section>
        <section class="poem">            <!-- poetry: 1 required to many -->
            <div class="contact"></div>                       <!-- 0 or 1 -->
            <div class="count"></div>                         <!-- 0 or 1 -->
            <div class="title"></div>                         <!-- 0 or 1 -->

            [poetry stanzas in here in between ```'s]

        </section>
        <section class="poem">            <!-- poetry: 1 required to many -->
            <div class="contact"></div>                       <!-- 0 or 1 -->
            <div class="count"></div>                         <!-- 0 or 1 -->
            <div class="title"></div>                         <!-- 0 or 1 -->

            [poetry stanzas in here in between ```'s]

        </section>
        <section class="scene">         <!-- prose: rarely, if ever, used -->
            <div class="title"></div>                         <!-- 0 or 1 -->

            [scene text in here]

        </section
      </section>
    </section>
  </article>
</div>
~~~

# A prose example (*also see templates in the templates folder*)

This is a truncated example of a novel manuscript. It's three scenes contained
within one chapter, and that chapter within one part. But you can have many
parts containing many chapters containing many scenes. Parts and chapters are
optional.

```markdown
<style>
    @import url("/path/to/manuscript.css");
</style>
<div id="vpage">
<article id="manuscript" class="long narrative">


<!-- ------------------ the title page ------------------ -->

<div class="title-page"><div class="contact">

Edgar Allan Poe

Coates Street, Philadelphia, PA 19079 USA

telleroftales\@example\.com

</div><div class="count">

2200 words

Gothic Horror

</div><div class="title">

# The Tell-Tale Heart

# … a subtitle if there were one …

### by Edgar Allan Poe

> They heard!—they suspected!—they knew!

</div></div>


<!-- ------------------ the story ----------------------- -->

<section class="part">
<div class="title">

# Part 1

</div>


<section class="chapter">
<div class="title">

# Chapter 1

### Contributing Editor: Joe Blough

</div>


<section class="scene">

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
</article></div>
```



# Poetry within prose!

To insert a poem in a document arbitrarily, it will be structured like this:

~~~markdown

<div class="x-poem">

```
   Poem stanza
       Here.
```
```
   Poem stanza
       Here.
```

</div>
~~~



# Poetry Manuscripts


- `#manuscript` will be of `class="poetry"` and we use `poem` instead of a `scene`
- Each `poem` will contain an `contact`, an `count`, an `title` and then
  stanzas of poetry wrapped in <pre>```</pre> preformatting marks, similar to
  `x-poem` above.
- Most submissions are three to five poems. You don't used a title page for
  those. If you are submitting a collection, it is structured much like a
  novel.
- Check out the example and templated poetry manuscripts. But here's a simple
  and very common, three poem manuscript …


~~~markdown
<style>
    @import url("/path/to/manuscript.css");
</style>
<div id="vpage">
<article id="manuscript" class="poetry">


<!-- ------------------ three poems --------------------- -->

<section class="poem">
<div class="contact">

Haiku Johnson

Elm Street, Somewherein, PA 19079 USA

haikuforyou\@example\.com

</div><div class="count">

3 lines

</div><div class="title">

# The Savannah Watch

</div>

```
Long necks reach for leaves,
Soft shadows graze on the plains,
Gentle giants watch.
```

</section>


<section class="poem">

<div class="contact">

Haiku Johnson

Elm Street, Somewherein, PA 19079 USA

haikuforyou\@example\.com

</div><div class="count">

3 lines

</div><div class="title">

# Sky-High Grazing

</div>

```
Yellow patched tower,
Quietly chews acacia,
World seen from above.
```

</section>


<section class="poem">
<div class="contact">

Haiku Johnson

Elm Street, Somewherein, PA 19079 USA

haikuforyou\@example\.com

</div><div class="count">

3 lines

</div><div class="title">

# The Desert Drink

</div>

```
Water is far down,
Slow legs spread out wide to drink,
Neck bends to the pool.
```

</section>


</article></div>
~~~



# Good luck!

Check out the example and template manuscripts within this repository and I
think how everything works with `manuscript.css` becomes obvious.

Good luck. Now, quit fooling around on the internet and write something.

Copyright (c) Todd Warner  
This work is licensed under Attribution 4.0 International. To view a copy
of this license, visit http://creativecommons.org/licenses/by/4.0/
