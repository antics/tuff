tuff
====

This project is directly inspired by and based on [Tufte
CSS](https://github.com/edwardtufte/tufte-css) and [Acme from Plan
9](http://acme.cat-v.org/).

> Edward Tufte uses a distinctive style in his handouts: simple, with well-set typography, extensive sidenotes, and tight integration of graphics and charts. `tufte-css` brings that style to HTML documents.

Basically, I like the structure of the document and especially the side-notes.

![A screenshoot of tuff in action](https://github.com/antics/tuff/blob/gh-pages/screenshoot.png)

# Getting Started

To use tuff, just copy `tuff.css` to your project and add the following to your HTML doc's
head block:

```html
<link rel="stylesheet" href="tuff.css">
```

All other files in the repository can be ignored.

## Template

```html
<!DOCTYPE html>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<link rel="icon" href="data:,">
<link rel="stylesheet" href="tuff.css">

<title>Tuff means tough</title>

<article>
<section>
<h1>Tuff means tough</h1>

<address>
Author <a rel="author" href="https://mastodon.nu/@antics">@antics@mastodon.nu</a><br>
Last update: <time>2024-04-07</time>
</address>

<p>
Pray for a tough instructor to hear and act and stay within you.
We have been busy accumulating solace.
Make us afraid of how we were.
```

## Examples
Now, I'm no fan of using either classes or id's or unnecessary markup in hypertext. However, in this case we have none but this choice.

All spans must be within a `<p>` but not necessarily directly after. You put the sidenote inline in the text and in relation to where in the sidebar you want it to appear.

`.sn` Add a numbered reference sidenote; automatically counted with `.snn`
```html
<p>
Pray for a tough instructor<span class="snn"></span>
to hear and act and stay within you.
We have been busy accumulating solace.
Make us afraid of how we were.<span class="sn">Jalāl al-Dīn Muḥammad Rūmī - or simply Rumi</span>
```

`.mn` Jibberish note for jibberish.
```html
<p>
Flumbogoo wizzlefrazzled<span class="mn">flubberidoo</span>
the bimblywinks with zorgonified flibberflabber.
```

Add a picture as a sidenote `.mn`. But do not print it `.np`.
```html
<p>
<span class="mn np"><img src="vacilala.png"></span>
```

Use `.danger` to make the text red.
```html
<b class="danger">Attention!</b>
```

# Project Scope and Status

tuff is specifically a CSS-only solution for styling HTML for the web and print styles are included.

This project is maintained and under active development. Contributions are welcomed especially if they simplify code.

License
-
Released under the MIT license. See [LICENSE](https://github.com/antics/tuff/blob/gh-pages/LICENSE).
