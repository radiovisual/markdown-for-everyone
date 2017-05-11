# Markdown For Everyone

Markdown is an incredibly simple and hassle-free alternative to HTML. Markdown accomplishes the same thing as HTML, but Markdown uses a simple, easy-to-learn syntax that allows you to add a variety of styling options to your plain-text without all the hassle of opening and closing tags.

Use this cheatsheet as a way of demonstrating specific Markdown features. Because this document was written using Markdown, you can alternatively view this file's [raw plaintext](https://raw.githubusercontent.com/radiovisual/markdown-for-everyone/master/readme.md) to see more of the specific markdown formatting used in this document.

**Note:** Markdown used on Github resources differs slightly in its feature set then Markdown used elsewhere, but once you learn the basics of Github-flavored Markdown, you are ready to write Markdown everywhere. 


---

# Table of Contents

- [Typography](#typography)
  - [Headings](#headings)
  - [Horizontal Rules](#horizontal-rules)
  - [Body Copy](#body-copy)
  - [Linebreaks](#linebreaks)
  - [Empahsis](#emphasis)
      - [Bold](#bold)
      - [Italics](#italics)
      - [Strikethrough](#strikethrough)
- [Links](#links)
  - [Basic Link](#basic-link)
  - [Add a Title](#add-a-title)
  - [Named Anchors](#named-anchors)
- [Blockquotes](#blockquotes)
  - [Nested Blockquotes](#nested-blockquotes) 
- [Lists](#lists)
  - [Unordered](#unordered)
  - [Ordered](#ordered)
- [Tables](#tables)
  - [Right Aligned Text](#right-aligned-text)
- [Task List](#task-list)
- [Images](#images)
- [Code](#code)
  - [Inline Code](#inline-code)
  - [Indented Code](#indented-code)
  - [Block Code "Fences"](#block-code-fences)
  - [Syntax Highlighting](#syntax-highlighting)
- [Keyboard Keys](#keyboard-keys)
- [Emojis](#emojis)
- [Credit](#credit)

---


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


## Linebreaks

To add a linebreak to your body copy, you need to put **two spaces** at the end of the text where you want the linebreak to occur.

So this body copy with two spaces at the end (spaces are being represented as '⃞'):

``` markdown
Putting two spaces at the end of this line ⃞⃞
will cause this line to appear on the line below.  
```
renders to this HTML:

``` html
Putting two spaces at the end of this line <br/>will cause this line to appear on the line below. 
```

which will be seen in your markdown files as:

Putting two spaces at the end of this line    
will cause this line to appear on the line below.  

**Note:** This "two spaces" trick often trips up new users of Markdown, because spaces are invisible, so the rule is not obvious when reading Markdown files.

**Note:** If you want to add your own linebreaks without having to manage invisible space characters in your file, then you can simply add the `<br />` tag wherever you want to add a linebreak, and your Markdown parser will honor it. 

<br>
<br>


## Emphasis

### Bold
For emphasizing a snippet of text with a heavier font-weight.

To create bold text, use double underscores or double asterisks:

``` markdown
**rendered as bold text with double underscores**
**rendered as bold text with double asterisks**
```

which renders to:

**rendered as bold text with double underscores**  
**rendered as bold text with double asterisks**  


### Italics
For emphasizing a snippet of text with italics.

The following snippets of text are _rendered as italicized text_ by wrapping either single underscores or single asterisks:

``` markdown
_rendered as italicized text with underscores_
*rendered as italicized text with single asterisks*
```

which renders to:

_rendered as italicized text with underscores_  
*rendered as italicized text with single asterisks*

### Strikethrough
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


### Add a Title

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

## Nested Blockquotes

Blockquotes can be nested by using an incremental number of greater-than signs (`>`). For example, you will use one `>` for a 
blockquote at the first level. To nest a blockquote, simply use two `>>`, to nest a third blockquote, use three `>>>`, and so on. 

Here is an example:

``` markdown
> Donec massa lacus, ultricies a ullamcorper in, fermentum sed augue. 
Nunc augue augue, aliquam non hendrerit ac, commodo vel nisi. 
>> Sed adipiscing elit vitae augue consectetur a gravida nunc vehicula. Donec auctor 
odio non est accumsan facilisis. Aliquam id turpis in dolor tincidunt mollis ac eu diam.
>>> Donec massa lacus, ultricies a ullamcorper in, fermentum sed augue. 
Nunc augue augue, aliquam non hendrerit ac, commodo vel nisi. 
```

Which renders to:

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


### Right Aligned Text

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

## Task List
Task lists are a handy way of making lists where items can be "checked" on or off. Like a "To-Do" List.
To create a task list, you will use a hyphen, angle brackets and the letter "x". 

So the following task list syntax:
 
``` markdown
- [ ] This item is unchecked
- [x] This item is checked
```

will render to:

- [ ] This item is unchecked
- [x] This item is checked


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

### Inline Code
Wrap inline snippets of code with a single accent grave character (aka "tick mark") `` ` ``.

For example, this markup:

``` markdown
Render these section tags as inline code: `<section></section>`
```

will render to:

Render these section tags as inline code: `<section></section>`


### Indented Code

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


### Block Code "Fences"

Use "fences", which are made up of three accent grave marks (aka "tick marks")  ```` ``` ```` to block in multiple lines of code. Notice how the "fences" wrap the code with three accent graves at the start of the code block and three accent graves at the end of the code block: 

<pre>
``` 
This text is surrounded by a "fence", so it will get treated like a block of code.

```
</pre>

Which renders to:

```
This text is surrounded by a "fence", so it will get treated like a block of code.
```

### Syntax Highlighting

GitHub-Flavored Markdown (GFM) also supports syntax highlighting. To activate it, simply add the file extension (or full name of the language) you want to use directly after the first code "fence", and language-specific syntax highlighting will automatically be applied in the rendered HTML.

For example, to apply syntax highlighting to JavaScript code, both of these formats will render the exact same output:

<pre>
``` javascript
// javascript code here ...
```

``` js
// javascript code here ...
```
</pre>

Here is a full example:
<pre>
``` javascript
// javascript code here ...
const b = stampit().init(function() {
  const priv = 'b';
  this.getB = () => {
    return priv;
  };
});
```
</pre>

Which renders to:

``` javascript
// javascript code here ...
const b = stampit().init(function() {
  const priv = 'b';
  this.getB = () => {
    return priv;
  };
});
```


<br>
<br>


### Keyboard Keys

Github-Flavored Markdown (GFM) allows you to render pretty keyboard keys which are particularly useful when instructing your readers on keyboard shortcuts, commands or hotkeys.

For example, the following markdown can be used to display the shortcut for "Copy" and "Paste" on a Mac:

```markdown
To copy, press <kbd>Cmd</kbd> + <kbd>C</kbd>  
To paste, press <kbd>Cmd</kbd> + <kbd>V</kbd>
```

Which renders to:

To copy, press <kbd>Cmd</kbd> + <kbd>C</kbd>  
To paste, press <kbd>Cmd</kbd> + <kbd>V</kbd>


<br>
<br>


### Emojis

Github-Flavored Markdown (GFM) supports Emojis! :bowtie: :heart_eyes: :smile: :boom: :dog2:

To add an emoji in GFM, just surround the emoji name with colons, like this:

```markdown
:hamburger: :pizza: :beer: :sushi: :tropical_drink:
```

Which renders to:

:hamburger: :pizza: :beer: :sushi: :tropical_drink:

**Tip:** For a full list of supported emojis, check out [emoji-cheat-sheet.com](http://www.emoji-cheat-sheet.com/)


<br>
<br>


### Credit

This cheatsheet was initially inspired by [this nice gist](https://gist.githubusercontent.com/jonschlinkert/5854601/raw/4cb53c02691e32930865fa2dafecf8ed359e057c/markdown.md) by [jonschlinkert](https://github.com/jonschlinkert), but has since evolved with added content, in hopes to one day read like a "Markdown for ~~Dummies~~ Everyone."
