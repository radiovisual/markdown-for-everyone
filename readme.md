# Markdown For Everyone

Use this cheatsheet as a way of demonstrating specific Github-flavored Markdown (GFM) features. View this file in "raw" plaintext view to see the specific markdown formatting. This cheatsheet is intially based off of [this nice gist](https://gist.githubusercontent.com/jonschlinkert/5854601/raw/4cb53c02691e32930865fa2dafecf8ed359e057c/markdown.md) by [jonschlinkert](https://github.com/jonschlinkert), but will soon evolve to read like a "Markdown for Dummies."

# Typography 

## Headings

Headings from `h1` through `h6` are constructed with a `#` for each level:

``` markdown
# h1 Heading
## h2 Heading
### h3 Heading
#### h4 Heading
##### h5 Heading
###### h6 Heading
```

Renders to:

# h1 Heading
## h2 Heading
### h3 Heading
#### h4 Heading
##### h5 Heading
###### h6 Heading


<br>
<br>


## Horizontal Rules

The HTML `<hr>` element is for creating a "thematic break" between paragraph-level elements. In markdown, you can create a `<hr>` with any of the following:

`___`: three consecutive underscores  
`---`: three consecutive dashes  
`***`: three consecutive asterisks

which renders to:

___

---

***


<br>
<br>


## Body Copy 

Body copy written as normal, plain text will be wrapped with paragraph tags `<p></p>` in the rendered HTML.

So this body copy:

``` markdown
Lorem ipsum dolor sit amet, graecis denique ei vel.
```
renders to this HTML:

``` html
<p>Lorem ipsum dolor sit amet, graecis denique ei vel.</p>
```


<br>
<br>


## Emphasis

### Bold
For emphasizing a snippet of text with a heavier font-weight.

To create bold (emphasized) text, use double underscores or double astericks:

``` markdown
**rendered as bold text with double underscores**
**rendered as bold text with double astericks**
```

which renders to:

**rendered as bold text with double underscores**
**rendered as bold text with double astericks**


### Italics
For emphasizing a snippet of text with italics.

The following snippets of text are _rendered as italicized text_ by wrapping either single underscores or single astericks:

``` markdown
_rendered as italicized text with underscores_
*rendered as italicized text with single astericks*
```

which renders to:

_rendered as italicized text with underscores_  
*rendered as italicized text with single astericks*

### strikethrough
In Github-Flavored Markdown (GFM) you can do strikethroughs by wrapping the text with double tildes: 

``` markdown
~~Strike through this text.~~
```
Which renders to:

~~Strike through this text.~~


<br>
<br>


## Links

### Basic link

``` markdown
[Assemble](http://assemble.io)
```

Renders to (hover over the link, there is no tooltip):

[Assemble](http://assemble.io)

HTML:

``` html
<a href="http://assemble.io">Assemble</a>
```


### Add a title

``` markdown
[Upstage](https://github.com/upstage/ "Visit Upstage!")
```

Renders to (hover over the link, there should be a tooltip):

[Upstage](https://github.com/upstage/ "Visit Upstage!")

HTML:

``` html
<a href="https://github.com/upstage/" title="Visit Upstage!">Upstage</a>
```

### Named Anchors

Named anchors enable you to jump to the specified anchor point on the same page. For example, each of these chapters:

```markdown
# Table of Contents
  * [Chapter 1](#chapter-1)
  * [Chapter 2](#chapter-2)
  * [Chapter 3](#chapter-3)
```
will jump to these sections:

```markdown
## Chapter 1 <a id="chapter-1"></a>
Content for chapter one.

## Chapter 2 <a id="chapter-2"></a>
Content for chapter one.

## Chapter 3 <a id="chapter-3"></a>
Content for chapter one.
```
**NOTE** that specific placement of the anchor tag seems to be arbitrary. They are placed inline here since it seems to be unobtrusive, and it works.


<br>
<br>


## Blockquotes
For quoting blocks of content from another source within your document.

Add `>` before any text you want to quote. 

``` markdown
Add `>` before any text you want to quote. 
```

Renders to:

> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.

Blockquotes can also be nested:

``` markdown
> Donec massa lacus, ultricies a ullamcorper in, fermentum sed augue. 
Nunc augue augue, aliquam non hendrerit ac, commodo vel nisi. 
>> Sed adipiscing elit vitae augue consectetur a gravida nunc vehicula. Donec auctor 
odio non est accumsan facilisis. Aliquam id turpis in dolor tincidunt mollis ac eu diam.
>>> Donec massa lacus, ultricies a ullamcorper in, fermentum sed augue. 
Nunc augue augue, aliquam non hendrerit ac, commodo vel nisi. 
```

Renders to:

> Donec massa lacus, ultricies a ullamcorper in, fermentum sed augue. 
Nunc augue augue, aliquam non hendrerit ac, commodo vel nisi. 
>> Sed adipiscing elit vitae augue consectetur a gravida nunc vehicula. Donec auctor 
odio non est accumsan facilisis. Aliquam id turpis in dolor tincidunt mollis ac eu diam.
>>> Donec massa lacus, ultricies a ullamcorper in, fermentum sed augue. 
Nunc augue augue, aliquam non hendrerit ac, commodo vel nisi. 


<br>
<br>


## Lists

### Unordered
A list of items in which the order of the items does not explicitly matter.

You may use any of the following symbols to denote bullets for each list item:

```markdown
* valid bullet
- valid bullet
+ valid bullet
```

For example

``` markdown
+ Lorem ipsum dolor sit amet
+ Consectetur adipiscing elit
+ Nulla volutpat aliquam velit
  - Phasellus iaculis neque
  - Purus sodales ultricies
+ Faucibus porta lacus fringilla vel
```
Renders to:

+ Lorem ipsum dolor sit amet
+ Consectetur adipiscing elit
+ Nulla volutpat aliquam velit
  - Phasellus iaculis neque
  - Purus sodales ultricies
+ Faucibus porta lacus fringilla vel

### Ordered

A list of items in which the order of items does explicitly matter.

``` markdown
1. Lorem ipsum dolor sit amet
2. Consectetur adipiscing elit
3. Integer molestie lorem at massa
4. Facilisis in pretium nisl aliquet
```
Renders to:

1. Lorem ipsum dolor sit amet
2. Consectetur adipiscing elit
3. Integer molestie lorem at massa
4. Facilisis in pretium nisl aliquet

**TIP**: If you just use `1.` for each number, GitHub will automatically number each item. For example:

``` markdown
1. Lorem ipsum dolor sit amet
1. Consectetur adipiscing elit
1. Integer molestie lorem at massa
1. Facilisis in pretium nisl aliquet
```

Renders to:

1. Lorem ipsum dolor sit amet
1. Consectetur adipiscing elit
1. Integer molestie lorem at massa
1. Facilisis in pretium nisl aliquet


<br>
<br>


## Tables
Tables are created by adding pipes as dividers between each cell, and by adding a line of dashes (also separated by bars) beneath the header. Note that the pipes do not need to be vertically aligned.


``` markdown
| Option | Description |
| ------ | ----------- |
| data   | path to data files to supply the data that will be passed into templates. |
| engine | engine to be used for processing templates. Handlebars is the default. |
| ext    | extension to be used for dest files. |
```

Renders to:

| Option | Description |
| ------ | ----------- |
| data   | path to data files to supply the data that will be passed into templates. |
| engine | engine to be used for processing templates. Handlebars is the default. |
| ext    | extension to be used for dest files. |


### Right aligned text

Adding a colon on the right side of the dashes below any heading will right align text for that column.

``` markdown
| Option | Description |
| ------:| -----------:|
| data   | path to data files to supply the data that will be passed into templates. |
| engine | engine to be used for processing templates. Handlebars is the default. |
| ext    | extension to be used for dest files. |
```

| Option | Description |
| ------:| -----------:|
| data   | path to data files to supply the data that will be passed into templates. |
| engine | engine to be used for processing templates. Handlebars is the default. |
| ext    | extension to be used for dest files. |


<br>
<br>


## Images
Images have a similar syntax to links but include a prepended exclamation point.

``` markdown
![Minion](http://octodex.github.com/images/minion.png)
```
![Minion](http://octodex.github.com/images/minion.png)

or
``` markdown
![Alt text](http://octodex.github.com/images/stormtroopocat.jpg "The Stormtroopocat")
```
![Alt text](http://octodex.github.com/images/stormtroopocat.jpg "The Stormtroopocat")

Like links, Images also have a footnote style syntax

``` markdown
![Alt text][id]
```
![Alt text][id]

With a reference later in the document defining the URL location:

[id]: http://octodex.github.com/images/dojocat.jpg  "The Dojocat"


    [id]: http://octodex.github.com/images/dojocat.jpg  "The Dojocat"


<br>
<br>


## Code

### Inline code
Wrap inline snippets of code with a single accent grave character (aka "tick mark") `` ` ``.

For example, this markup:

``` html
Render these section tags as inline code: `<section></section>`
```

will render to:

Render these section tags as inline code: `<section></section>`


### Indented code

Or indent several lines of code by at least four spaces, as in:

``` js
    // Some comments
    line 1 of code
    line 2 of code
    line 3 of code
```

    // Some comments
    line 1 of code
    line 2 of code
    line 3 of code


### Block code "fences"

Use "fences"  ```` ``` ```` to block in multiple lines of code. 

<pre>
``` html
Sample text here...
```
</pre>


```
Sample text here...
```

HTML:

``` html
<pre>
  <p>Sample text here...</p>
</pre>
```

### Syntax highlighting

GFM, or "GitHub Flavored Markdown" also supports syntax highlighting. To activate it, simply add the file extension of the language you want to use directly after the first code "fence", ` ``` js `, and syntax highlighting will automatically be applied in the rendered HTML. For example, to apply syntax highlighting to JavaScript code:

<pre>
``` javascript
grunt.initConfig({
  assemble: {
    options: {
      assets: 'docs/assets',
      data: 'src/data/*.{json,yml}',
      helpers: 'src/custom-helpers.js',
      partials: ['src/partials/**/*.{hbs,md}']
    },
    pages: {
      options: {
        layout: 'default.hbs'
      },
      files: {
        './': ['src/templates/pages/index.hbs']
      }
    }
  }
};
```
</pre>

Renders to:

``` javascript
grunt.initConfig({
  assemble: {
    options: {
      assets: 'docs/assets',
      data: 'src/data/*.{json,yml}',
      helpers: 'src/custom-helpers.js',
      partials: ['src/partials/**/*.{hbs,md}']
    },
    pages: {
      options: {
        layout: 'default.hbs'
      },
      files: {
        './': ['src/templates/pages/index.hbs']
      }
    }
  }
};
```
