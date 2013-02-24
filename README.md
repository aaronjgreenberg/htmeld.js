# htmeld.js

Here's a JavaScript that allows you to meld Markdown and HTML in a single HTML file.  My rationale for creating this script is that I want to be able to write and edit articles in static web pages without having to manually convert back and forth between Markdown.  Using this script, you can write Markdown directly into your HTML and have your browser render it as HTML.  In your editor, it will still be clean, readable Markdown.

## Usage

It's very simple to use.  Just include the `htmeld.js` script in your HTML file:

```html
<script type="text/javascript" src="/path/to/htmeld.js"></script>
```

You should add that script at the end of your HTML so it doesn't run until all the elements are loaded.  Then, any HTML element with a Markdown class will have its contents converted into HTML in the browser.

```html
<div class="markdown">

# Article Title

Lorem ipsum dolor...

</div>
```

becomes

```html
<div class="markdown">

<h1>Article Title</h1>

<p>Lorem ipsum dolor...</p>

</div>
```

## Installation

Also pretty simple.

```
$ curl -S https://raw.github.com/aaronjgreenberg/htmeld.js/master/htmeld.min.js > htmeld.js
```

## License

Licensed under the MIT license.

Also important: this software is pretty much just a slim wrapper around John Fraser's Showdown, which is a JavaScript port of John *Gruber's* Markdown.  Fraser holds the copyright on Showdown; Gruber hold's the copyright on Markdown.

## Thanks
To John Fraser, John Gruber, and [Corey Innis](https://github.com/coreyti/showdown), for hosting a Showdown repository on GitHub.

:metal:
