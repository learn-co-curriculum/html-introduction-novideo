# TODO: Add descriptive and succinct title

## Problem Statement

How do we go about writing text that is designed for viewing on the web? And
how does that differ from the text that one might write into a plain old text
file? We're going to explore how these things differ in this README.

## Objectives

1. Define what a file is
2. Recognize plain text versus markup text
3. Label primary components of a HyperText Markup Language (HTML) text file
4. Discern between material that describes _markup_ versus _content_
5. Recognize the difference between source text and text as viewed in a browser


## Define what a file is

While you may have used these computers for years, you might not have ever
considered what a "file" is. You've certainly downloaded them, saved them,
deleted them.  In the earliest days of computing, the ancestors of modern
computers recognized two primary types of files: plain text files and binary
files. This primary distinction has come to us in our current day.

**Plain text** (or, "plaintext") files are designed for _humans_ to read and write
with editors like LearnIDE, Atom, Sublime Text, vim, or emacs (notably, not
Microsoft Word or TextEdit - more on those in a moment!).

**Binary** files are designed for _computers_ to read and run (or "execute"). These
are instructions, written in binary (the format computers think in) that
describe how to do something. In general if the computer is doing something
very computer-y (turning a file into music, turning a file into a movie,
turning a file into a game) it's going to be a _binary file_. Every video game
every DVD is effectively _one large file_ written on a disc (or downloaded)
that a player plays back. Think of it! A Playstation of an Xbox is what it is
simply because it knows how to turn a special file of binary data into a game.
It's a plain ol' computer with just a _little_ extra knowledge.

Word processing programs (Microsoft Word, on your computer, for example),
provide a confusing case. While you're _seeming_ to edit text, Word stores your
text _as well as information_ about how to undo 2 changes, which words are
bolded, what lines are bullet lists, etc. A "word doc" file is _actually_
a binary file.

Many file types have an "extension" that comes after a `.` which suggests what
type of program works with the file or what kind of data lie inside. For
example "LetterToGrandma.doc" is a *doc*. The file "LetterToGrandma.txt" is a
*txt* file. The "CarletonDance.gif" suggests an image, possibly animated.

Here's a table to help train your instincts in seeing text- files versus
binary-files:

|File | Plaintext or Binary | Use |
|-----|---------------------|-----|
| `beethoven_09_01_chorale.mp3` | Binary | Music |
| `CarletonDance.gif` | Binary | Image |
| `fibonacci_printer.py` | Plaintext | A Python program written in text; executable by the `python` _binary_ file |
| `index.html` | Plaintext | An HTML File |
| `LetterToGrandma.doc` | Binary | A binary file for Microsoft Word |
| `minaswan.rb` | Plaintext | A Ruby program file written in text; executable by the `ruby` _binary_ file |
| `cannonball.mov` | Binary | A Quicktime movie showing someone jumping into a swimming pool|

## Recognize plain text versus markup text

You might be thinking that plaintext file seem pretty, well, boring. Games,
movies, music, a picture of a rabbit stealing cookies from a plate, all of
those are binary files.

What good are "plain text" files? Well, every email you've ever received is a
text file. Every web page you've ever viewed is a text file. Every journal
you've read to do a research paper was (likely) a text file. Think momentarily
of the ancient computers of the 1960's. A professor might key in the grades for
their students in a text file and then use a program to calculate the averages
and grades. An astronomer might key in historical notes on star positions and
calculate the angle for a telescope that might point to some amazing phenomenon
that happened billions of years ago. Text quite often gains exponential power
when it is "processed" in some way.

Let's consider what happens if text is _not_ processed at all. Looking at the
document `dj_set.html`:

```text
* "Love Will Tear Us Apart "
* "Everybody Knows"
* "Somewhere on the Moon"
* "Fast Car"
* "Girlfriend In a Coma"
```

If we view this in our web server we see....exactly what we put in. But these
songs all have a theme. I'd like to put a heading on top "Quiet Late-Night"
music.

```text
"Quiet Late-Night"
* "Love Will Tear Us Apart "
* "Everybody Knows"
* "Somewhere on the Moon"
* "Fast Car"
* "Girlfriend In a Coma"
```

Well, that doesn't display _quite_ right, I really want to see my header
more...header-like. Let's add some extra blank lines.

```text
"Quiet Late-Night"


* "Love Will Tear Us Apart "
* "Everybody Knows"
* "Somewhere on the Moon"
* "Fast Car"
* "Girlfriend In a Coma"
```

What happened? Are you surprised by this? Ask a friend or a guide and explain
your theory about why nothing changed. Maybe discuss it with a friend.

You see, as a human, you recognize the convention that "vertical space" between
a collection of words at the top of a document (or plaintext file) _means_
something like "a heading." Years of social conditioning have taught you this:
grocery lists, train time tables, picture books you saw in kindergarten,
graffitti wall art, most movie introductions, etc. _But a computer doesn't know
anything about these rules!_ It never lived a human life such that it could
learn these rules. Therefore we have to tell the displaying program (the
browser) what these bits of text _mean_ so that it knows how to treat them.

We'll fill out the text a bit more:

```text
"Quiet Late-Night"

British post-punk, American folk, and some Americana for help when writing
curriculum late at night.


* "Love Will Tear Us Apart"
* "Everybody Knows"
* "Somewhere on the Moon"
* "Fast Car"
* "Girlfriend In a Coma"
```

With our _human_ intelligence we see a "heading" a "paragraph" and an
"unordered ('bullet') list." Let's tell the browser to treat these bits of
content as such.

```html
<h1>"Quiet Late-Night"</h1>

<p>British post-punk, American folk, and some Americana for help when writing
curriculum late at night.</p>

<ul>
  <li>"Love Will Tear Us Apart"</li>
  <li>"Everybody Knows"</li>
  <li>"Somewhere on the Moon"</li>
  <li>"Fast Car"</li>
  <li>"Girlfriend In a Coma"</li>
</ul>
```

Now when the browser sees a plaintext file, with an HTML extension it will
apply "display rules" or "rendering rules" and, instead of showing the `<p>`
_markup_ will use that information to start tracking that the _content_  that
should be shown as a **p**aragraph between the `<p>` and `</p>` markup. These
angle-bracket bits of text are known as "tags." Experienced HTML writers would
say that "the content of the paragraph is defined between the opening (`<p>`)
and closing (`</p>`) p-tags."

This is, essentially, the work of learning to write HTML. You will grow more
familiar with tags, what they do, and how they display in a browser.
Nevertheless the essential lesson of HTML is this:

1. You edit a plaintext file
2. You add _content_
3. You add _markup_ around that _content_ to tell browsers _how_ to display the
   content
4. Browsers do the rest!

It's worth celebrating. Every web page: Netflix, Facebook, Twitter, Google, The
NRC Handelsblad, Le Monde &mdash; _every single one uses the standard that
**you** just worked with to inform and change lives every day_. Welcome to the
club!

## Label primary components of a HyperText Markup Language (HTML) text file
## Discern between material that describes _markup_ versus _content_
## Recognize the difference between source text and text as viewed in a browser

## Conclusion

In this lesson we saw that by editing a plain text file and by filling it with
special "markup" characters we can provide HTML (Remember that the "M" is for
"markup") reading programs ("browsers") _content_ for display _as well ass_
instructions on _how_ to show the _content_. We saw that the primary components
of an HTML file are the `<header>` and the `<body>` and that the `<body>` is
usually full of tags that help the readability of the document. HTML documents,
when rendered by browsers provide a richer display than a plain text document
could provide.

In future lessons, we'll learn more about how HTML provides the ability to
shape the presentation of your content in ever more engaging and fun ways. You
might be starting with paragraphs today, but soon you'll be including video,
inserting opinions multi-column layouts, and making sure the site works equally
well on a web-enabled refrigerator as well as smartphone.


## Lesson

### Integrating Review

So far we've covered many concepts in small pieces to help you focus your
learning. This lesson reviews some previously-seen concepts, but will focus on
_integrating_ them, not _introducing_ them.

### What is HTML?

HTML, or HyperText Markup Language, is a markup language which describes the
structure and semantic meaning of web pages. Web browsers, such as Mozilla
Firefox, Internet Explorer, and Google Chrome interpret the HTML code and use
it to render output. Unlike Ruby, JavaScript and other programming languages,
markup languages like HTML don't have any logic behind them. Instead, they
simply surround the content to convey structure and meaning.

Every web page you've ever visited is structured using HTML code. Being able to
read and understand an HTML document is one of the most essential tools in a
developer's toolbox.

### HTML Syntax

HTML consists of different elements. Each element consists of tags, which wrap
around content. For example, say we wanted `Hello World` to appear as a
paragraph. We could use the `p` element, which consists of an opening `p` tag
and a closing `p` tag.

```html
<p>Hello World</p>
```

Elements, like our `p` tags above, won't be displayed in the browser. Instead,
they affect how the content itself is displayed. Techonologists might say that
the tags "affect how the content is rendered by the browser."

We can also alter any number of attributes inside of the opening tags. For
example, the `a` element, which is used for links, has an `href` attribute to
specify the destination address of the link. If we wanted to link to
www.flatironschool.com, we could do so as follows:

```html
<a href="http://www.flatironschool.com">Flatiron School</a>
```

This would render as:

[Flatiron School](http://www.flatironschool.com)

We can also nest elements inside of each other. To have a link displayed as a
separate paragraph, we could nest an `a` element inside of a `p`.

```html
<p>This <a href="http://www.google.com">link</a> will be a part of a separate paragraph.</p>
```

### Basic HTML Document Structure

All HTML documents begin with a "doctype declaration" tag, which tells our web
browser which version of HTML to use. HTML is a language that is currently
evolving &mdash; just like English. When we open "Romeo and Juliet," our
expectation is that the "doctype" is "Elizabethan English." In the same way
"Elizabethan English" has changed to a more modern form, HTML 1.0 was
_essentially_ the same as modern HTML5 but had some tags we don't use any more
and was lacking some tags we use often today.

Since it's not wrapping any content, our doctype declaration doesn't require a
closing tag. To use HTML5, the current up-to-date version, we can simply
declare `<!DOCTYPE html>`.

```html
<!DOCTYPE html>

```

Next, we add an opening and closing `html` tag. This tells the web browser to
interpret everything inside the tags as HTML code.

```html
<!DOCTYPE html>
<html>


</html>
```

Every HTML page is made up of two primary sections: a `head` and a `body`. The
`head` element contains metadata about the HTML document and other information
for the browser, while the `body` element contains the actual content.

```html
<!DOCTYPE html>
<html>
    <head>
        <!-- metadata about the HTML document as a whole -->

    </head>

    <body>
        <!-- content of our page will be here! -->

    </body>
</html>
```

#### Comments

Let's also take a brief moment to recognize how to add comments into an HTML
document.  These won't get rendered to the browser at all: they're just helpful
notes for the author.

```html
<!-- NYC Pizza is world-famous, cheap, and loved by both vermin and human like! -->
<p>Top 5 Pizza Places in NYC</p>
```

### Common HTML Elements

We've already looked at some common HTML elements, such as `a` and `p`. Let's
take a look at some more HTML elements.

#### Headers

HTML gives us access to different header elements, ranging from `h1` to `h6`,
with `h1` being the largest and `h6` being the smallest.

```html
<h1>Dogs!</h1>
<h3>Why Dogs are Great</h3>

<h6>Different Breeds</h6>
```

In addition to changing how the text is displayed, search engines use headers
to help determine what a web page is about. Remember, as Avi pointed out, when
we provide _semantic_ markup, machines can infer the "main points" of a page. A
well structured article will generally have its principle arguments bracketed
by low-number header tags -- this very document does exactly that!

#### Images

We can embed images on our web pages using the `img` element. The `img` element
doesn't have a closing tag. The `src` attribute tells the browser where to find
the image. The `alt` attribute will be displayed if an image can't be loaded,
and also describes the image to search engines.

The `alt` tag presents a moment to talk about an important principle behind Tim
Berners-Lee's vision for the Web: it is _inclusive_. If you're using assistive
technologies because you have a sight impairment, it's helpful to know what's
being displayed. If you're in a remote community where internet access is
expensive, you might choose to disable images and only pay to download those
which you _absolutely need_. So while an `img` will inject an image and "work,"
honoring the Web's vision for openness and inclusivity requires that we provide
the `alt` tag as well.

`<img src="URL_TO_IMAGE" alt="Picture of a Dog">`

#### Lists

Some other useful HTML elements are lists. We can make bulleted, or unordered
lists, using opening and closing `ul` tags. Inside, we can nest an `li`, or
"list item" element for each item on our list.

```html
<h5>My Favorite Things in No Particular Order</h5>
<ul>
    <li>Coffee</li>
    <li>Vinyl Records</li>
    <li>Pickling</li>
</ul>
```

This would render as:

____

<h5>My Favorite Things in No Particular Order</h5>
<ul>
    <li>Coffee</li>
    <li>Vinyl Records</li>
    <li>Pickling</li>
</ul>
____

We can also make a numbered, or ordered list, using an `ol` tag.

```html
<h5>Top 5 Pizza Places in NYC</h5>
<ol>
    <li>DiFara Pizza</li>
    <li>Lucali's</li>
    <li>Sal and Carmine's</li>
    <li>Juliana's</li>
    <li>Joe's</li>
</ol>
```
Would render as:

____

<h5>Top 5 Pizza Places in NYC</h5>
<ol>
    <li>DiFara Pizza</li>
    <li>Lucali's</li>
    <li>Sal and Carmine's</li>
    <li>Juliana's</li>
    <li>Joe's</li>
</ol>
____
