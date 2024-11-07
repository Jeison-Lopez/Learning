# Extended Sintax

## Overview

The basic syntax outlined in the original Markdown design document added many of the elements needed on a day-to-day basis, but it wasn’t enough for some people. That’s where extended syntax comes in.

Several individuals and organizations took it upon themselves to extend the basic syntax by adding additional elements like tables, code blocks, syntax highlighting, URL auto-linking, and footnotes. These elements can be enabled by using a lightweight markup language that builds upon the basic Markdown syntax, or by adding an extension to a compatible Markdown processor.

## Availability

Not all Markdown applications support extended syntax elements. You’ll need to check whether or not the lightweight markup language your application is using supports the extended syntax elements you want to use. If it doesn’t, it may still be possible to enable extensions in your Markdown processor.

## Tables

To add a talbe, use three or more hyphens (---) to create each column's header, and use pies (|) to separate each column, For compatibility, you should alse addd a pipe on either end of the row.

| Synctax | Description |
| --- | --- |
| Header | Title |
|Paragraph | Text |

## Alignment

You can akling text in the columns to the left, right, or center by adding a colon (:) to the left, right, or on both side of the hyphens wihtin the deader row.

| Syntax | Description | Test Text |
| :--- | :---: | ---: |
| Header | Tile | Here's this |
| Paragraph | Text | And more |

## Formatting Text in Tables

You can format the text within tables, For example, you can add links, code (word or phrases in backticks(`) only, not code blocks), and emphasis.

You cant't use headings, blockquotes, list, horizontal rules, images, or most HTML tags.

> You can use HTML to create line breaks and add lists within table cells.

## Escaping Pipe Characters in Tables

You can display a pipe (|) character in a table by using its HTML character code (`&#124;`).

## Fenced Code Blocks

the basic Markdown syntax allows you to create code blocks by indenting lines by four spaces or one tab. if you find that inconvenient, try using fenced code blocks. Depending on you Markdown processor or editor, you'll use thre backticks(```) or three tildes (~~~) on the lines before and after the code block. The best part? You don't have to indent any lines!

``` js
{
    "firstName": "Jeison",
    "lastName": "Smith",
    "age": 25
}
```

## Syntax Highlighting

Many Markdown processors support syntax highlighting for fenced code blocks. This feature allows you to add color highlighting for whatever language your code was written in. To add syntax highlighting, specify a language next to the backticks before the fenced code block.

```json
{
    "firstName": "John",
    "lastName": "Smith",
    "age": 25
}
```

## Footnotes

Footnotes allow you to add notes and references without cluttering the body of the document. When you create a footnote, a superscript number with a link appears where you added the footnote reference. Readers can click the link to jump to the content of the footnote at the bottom of the page.

To create a footnote reference, add a caret and an identifier inside brackets ([^1]). Identifiers can be numbers or words, but they can’t contain spaces or tabs. Identifiers only correlate the footnote reference with the footnote itself — in the output, footnotes are numbered sequentially.

Add the footnote using another caret and number inside brackets with a colon and text ([^1]: My footnote.). You don’t have to put footnotes at the end of the document. You can put them anywhere except inside other elements like lists, block quotes, and tables.

### Example

Here's a simple footnote,[^1] and here's a longer one.[^bignote]

[^1]: This is the first footnote.

[^bignote]: Here's one with multiple paragraphs and code.

Indent paragraphs to include them in the footnote.

`{ my code }`

Add as many paragraphs as you like.

## Heading IDs

Many Markdown preocessors support custom IDs for headings -- some Markdown processors automatically add them. Adding custom IDs allows you to link directly to headings and modify them with CSS. To add a custom heading ID, enclose the custom ID in curly braces on the same line as the heading.

`### My Great Heading {#custom-id}`

### HTML

`<h3 id="custom-id2">My Great Heading</h3>`

## Linking to Heading IDs

You can link to headings with custom IDs in the file by creating a standar link with a number sing (#) followed by the custom heading ID. These are commonly referred to as anchor links.

| Markdown | HTML | Rendered Output |
| --- | --- | --- |
| `[Heading IDs](#heading-ids)` |`<a href="#heading-ids">Heading IDs</a>` | [Heading IDs](#heading-ids) |

Other websites can link to the heading by adding the custom heading ID to the full URL of the webpage (e.g, `[Heading IDs](https://www.markdownguide.org/extended-syntax#heading-ids)`)

## Definition lists

Some Markdown processors allow you to create definition lists of terms and theri corresponding definitios. To create a definition list, type the term on the first line. On the next line, type a colon followed by a space and the definition.

Fisrt Term  
: This is the definition of the first term.

Second Term
: This is one definition of the second term.
: This is another definition of the second term.

### HTML

``` HTML
<dl>
    <dt>First Term</dt>
    <dd>This is the definition of the first term.</dd>
    <dt>Second Term</dt>
    <dd>This is one definition of the second term. </dd>
    <dd>This is another definition of the second term.</dd>
</dl>
```

## Strikethrough

You can strikethrough word by puttin a horizontal line through the center of them. The result looks ~~like this~~. this feature allows you to indicate that certain words are a mistake not mean for inclusion in the document. to strikethroug word, use two tilde symbols(~~) before and after the words.

`~~The world is flat.~~ We now know that the world is round.`  

## Task List

Task list (aslse referred to as checklist and todo list) allow you to create a list of item with checboxes. In Markdown applications that support task list, checkboxes will be displayed next to the content. To create a task list, add dashes (-) and brackets with a space ([ ]) in front of task list item. To select a checkbox, add an x in between the brackets ([x]).

- [x] Write the press release  
- [ ] Update the website  
- [ ] Contact the media

## Emoji

There are two ways to add emoji to Markdown files: copy and paste the emoji into your Markdown-formatted text, or type emoki shorcodes.  

## Copying and Pasting Emoji

In most cases, you can simply copy an emoji from a source like [Emojipedia](https://emojipedia.org/) and paste it into you doucment. Many Markdown application will automatically display the emoji en Markdown-formatted tex. The HTML and PDF files you export from you Markdown application should display the emoji.

## Using Emoji Shortcodes

Some Markdown applications allw you to insert emoji by typing emoji shortcodes. These begin and end with a colon and include the name of an emoji.  

Gone camping! `:tent:` Be back soon.

That is so funny! `:joy:`

### Rendered output

Gone camping! :tent: Be back soon.

That is so funny! :joy:

### Resource

[List of emoji shortcodes](https://gist.github.com/rxaviers/7360908)

## Hitghlight

This isn't common, by some Markdown processors allow you to highlight text. The resul looks ==Like this==. To highlight words, use two equal signs (==) before and after the words.

`I need to highlight these ==very important words==.`

### HTML

`I need to highlight these <mark>very important words</mark>`

### Rendered output

I need to highlight these <mark>very important words</mark>

## Subscript

This isn't common, but some Markdown processors allow you to use subscript to position one or more characters slightly below the normal line of type. To create a subscript, use one tilde symbol (~) before and after the characters.

`H~2~O`

### HTML

`H<sub>2</sub>O`

### Rendered Output

H<sub>2</sub>O

## Superscript

This isn't common, but some Markdown processors allow you to use superscript to position one or more characters slightly above the normal line of type.

`X^2^`

### HTML

`X<sup>2</sup>`

### Rendered Output

X<sup>2</sup>

## Automatic URL Linking

Many Markdown processors automatically turn URLs into links. That meas if you type http://www.example.com, your Markdown processor will automatically turn it into a link even thugh you haven't used brackets.

## Disabling Automatica URL Linking

If you don't want a URL to be automatically linked, you can remove the link by denoting the URL as code with backticks.

`http://www.example.com`
