# Basic Syntax

> The Markdown elements outlined in the original design document.  
> There are minor variations and discrepancies between Markdown processors.

## *Headings*

| Markdown | HTML | Rendered Output |
|---|---|---|
| `# Heading level 1` | `<h1>Heading level 1</h1>` | <h1>Heading level 1</h1> |
| `## Heading level 2` | `<h2>Heading level 2</h2>` | <h2>Heading level 1</h2> |

## *Alternate Syntax*

| Markdown | HTML | Rendered Output |
|---|---|---|
| `Heading level 1 ===` | `<h1>Heading level 1</h1>` | <h1>Heading level 1</h1> |
| `## Heading level 2 ---` | `<h2>Heading level 2</h2>` | <h2>Heading level 1</h2> |

## Heading Best Practices

For compatibility, always put a space between the number sings and the heading name.

| Do this | Don't do this |
| --- | --- |
| # Here's a Heading | #Here's a Heading |

You Shoul also put blanck lines before and after a heading for compatibility.

## Paragraphs

To create paragraphs, use a blank line to separate one or more lines of text.

## Paragraph Best Practices

Unless the paragraph is in a list, don´t indent paragraphs with spaces or tabs.

## Line Breaks

To Create a line break or new line (`<br>`), end a line with two or more spaces, and then type return.

## Emphasis

Tou can add emphasis by making text bold or italic.

## Bold

To bols text, add two asterisks or underscores before and after a word or phrase. To bols the middle of a word for emphasis, add two asterisks without spaces around the letters.

| Markdown | HTML | rendered Output |
|---|---|---|
| I just love `**`bold text`**`. | I just love `<strong>`bold text`</strong>`. | I just love **bold text** |
| I just love `__`bold text`__`. | I just love `<strong>`bold text`</strong>`. | I just love **bold text** |
| Love`**`is`**`bold. | Love`<strong>`is`</strong>`bold. | Love**is**bold. |

## Bold Best Practices

Markdown applications don´t agree on how to handle underscores in the middle of a word. For compatibility, use asterisk to bold the middle of a word for emphasis.

| Do this | Don't do this |
|---|---|
| Love`**`is`**`bold | Love`__`is`__`bold |

## Italic

To italicize text, add one asterisk or underscore before and after a word or phrase. To italicize the middle of a word for emphasis, add one asterisk without spaces around the letters.

| Markdown | HTML | Rendered Output |
|---|---|---|
| Italicized text is the `*`cat's meow`*`. | Italicized text is the `<em>`cat's meow`</em>`. | Italicized text is the *cat's meow*. |
| Italicized text is the `_`cat's meow`_`. | Italicized text is the `<em>`cat's meow`</em>`. | Italicized text is the *cat's meow*. |
| A`*`cat`*`meow. | A`<em>`cat`</em>`meow. | A*cat*meow. |

## italic Best Practices

Markdown applications don't agree on how to handle undescores in the middle of a word. For compatibility, use asterisk to italicize the middle of a word for emphasis.

| [x] Do this | [] Don't do this |
|---|---|
| A`*`cat`*`meow | A`_`cat`_`meow |

## Bold and Italic

To emphasize text with bold and italics at te same time, add three asterisks or underscores before and after a word or phrase. To bold and italicize the middle of a word for emphasis, add three asterisks without spaces around the letters.

| Markdown | HTML | Rendered Output |
|---|---|---|
| this text is `***`really important`***`.| This text is `<em><strong>`really important`</strong></em>`. | this text is ***really important***. |
| this text is `___`really important`___`.| This text is `<em><strong>`really important`</strong></em>`. | this text is ***really important***. |
| this text is `__*`really important`*__`.| This text is `<em><strong>`really important`</strong></em>`. | this text is ***really important***. |
| this text is `**_`really important`_**`.| This text is `<em><strong>`really important`</strong></em>`. | this text is ***really important***. |
| This is really`***`very`***`important text. | This is really`<em><strong>`very`</strong></em>`. | This is really***very***important text. |

> Note: The order of the "em" and "strong" tags might be reversed depending on the Markdown processor you're using.

## Bold and Italic Best Practices

Markdown applications don't agreee on how to handle underscores in the middle of a word. For compatibility, use asterisk to bold and italicize the middle of a word for emphasis.

| [x] Do this | [] Don't do this |
|---|---|
| This is really`***`very`***` important text. | This is really`___`very`___`important text. |

## Blockquotes

To create a blockquote, add a > in front of a paragraph.

> This's a blockquote

## Blockquotes with Multipple Paragraphs

Blockquotes can contain multiple paragraphs. Add a > on the blank lines between the paragraphs.

> First paragraph.
>
> Second paragraph.

## Nested Blockquotes

Blockquotes can be nested. Add a >> in front of the paragraph you want to nest.

> Paragraph.
>
>> Nested paragraph.

## Blockquotes with Other Elements

Blockquotes can contain other Markdown formatted elemnts. Nota all elements can be used --- you'll need to experiment to see whick ones work.

> `####` The quarterly results look great!
>
> `-` Revenue was ooff the chart.
> `-` Profits were higher than ever.
>
> `*`Everything`*` is going acording to `**`plan`**`.

### Output

> #### The quarterly results look great!
>
> - Revenue was ooff the chart.
> - Profits were higher than ever.
>
> *Everything* is going acording to **plan**.

## Blockquotes Best Practices

For compatibility, put blank lines vefore and after blockquotes.

| [x] Do this | [] Don't do this |
|---|---|
| Try to put a blank line before ... | Without black lines, this might not loock right. > This is a blockquote Don't do this! |
|   
| >This is a blockquote  |
|  
| ...and after a blockquote. |

## List

Yout can organize items into ordered and unordered lists.

## Ordered Lists

To create an ordered list, add line items with number followed by periods. The numbers don't have to be in numerical order, but the list should start with the number one.

| Markdown | HTML | Render Output |
|---|---|---|
| 1. First item | `<ol> <li>First item</li> </ol>` | 1. First item |

Indented

``` Markdownd
1. First item
    1. Fisrt item indented.
```

## Ordered List Best Practices

CommonMark and a few other lightweight markup languages let you use a parenthesis ()) as a delimiter (e.g., 1) First item), but no tall Markdown applications support this, so it isn't a great option from a compatibility perspective. For compatibility, use periods only.

| [x] Do this | [] Don't do this |
|---|---|
| 1. fisrt item | 1) First item |

## Unordered Lists

To create an unordered list, add dashes (-), asterisk (*), or plus signs (+) in front of line items. Indent one or more items to create a nested list.

| Markdown | HTML | Rendered Output |
|---|---|---|
| `-` First item | `<ul> <li>`First item`</li> </ul>` | <ul> <li>First item</li> </ul> |
| `*` First item | `<ul> <li>`First item`</li> </ul>` | <ul> <li>First item</li> </ul> |
| `+` First item | `<ul> <li>`First item`</li> </ul>` | <ul> <li>First item</li> </ul> |

Indented

- First item
    - Indented item

## Starting Unordered List Items With Numbers

If you need to start an unordered list item with a number followed by a period, you can use a backslah (\) to scape the period.

| Markdown | HTML | Rendered Output |
|---|---|---|
| - 1968\. A great year! | `<ul> <li>`1968. A great year!`</li> </ul>` | - 1968\. A great year! |

## Unordered List Best Practices

Markwoen applications don't agrre on how to handle different delimiters in the same list. For compatibility, don't mix and match delimiters in the same list ---- pick one and stick with it.

| [x] Do this | [] Don't do this |
|---|---|
| - First item | - First item |
| - Second item | * Second item |
| - Third item| + Third item|
| - Four item | - Fourt item|

## Addding Elements in Lists

To add another element in a list while preserving th continuity of the list, indent the element four spaces or one tab, as shown in the following examples.

### Paragraphs

- This is the first list item.
- Here's the second list item.

    I need to add another paragraph below the second list item.

- And here's the third list item.

### Blockquotes

- This is the first list item.
- Here's the second list item.

    > A blockquote would look great below the second list item.

- And here's the third list item.

## Code Blocks

Code blocks are normally indented four spaces or one tab. When they're in a list, indente then eith spaces or two tabs.

1. Open the file
2. Find the following code block on line 21:

        <html>
            <head>
                <title>Test</title>
            </head>
        </html>

3. Update the title to match the name of your website

## Images

1. Open the file containing the Linux mascot.
2. Marvel at its beauty

        ![Tux, the Linux mascot](/assets/images/tux.png)

3. Close the file.

## Lists

You can nest an unordered list in an ordered list, or vice versa.

1. Fisrt item
2. Second item
3. third item
    - Indented item
    - Indented item
4. Fourth item

## Code

To denote a word or phrase as code, enclose it in backticks (`).

| Markdown | HTML | Rendered Output |
|---|---|---|
| At the command prompt, type `nano`. | At the command prompt, type `<code>`nano`</code>`. | At the command prompt, type `none`. |

## Escaping Backticks

If the word phrase you want to denote as code includes one or more backticks, you can escape it by enclosing the word or phrase in double backticks (``).

| Markdown | HTML | Rendered Output |
|---|---|---|
| `` Use `code` in your Markdown file. `` | <code>Use `code` in your Markdown file.</code> | Use `code` in your Markdown file. |

## Code Blocks

To create code blocks, indent every line of the block by at least four spaces or one tab.

    <html>
        <head>
        </head>
    </html>

## Horizontal Rules

To create a horizontal rule, use three ormore asterisks(***), dashes (---), or underscores (___) on a line by themselves.

***
---
___
`***`
`---`
`___`

## Horizontal rule Best Practices

For compatibility, put blank lines before and after horixontal rules.

| [x] Do this | [] Don't do this |
|---|---|
| Try to put a blank line before... | Without blank lines, this would be a heading.|
| | --- |
| --- | Don't do this!|
| | |
| ... and after a hoeizontal rule. | |

Links

To create a link, enclose the link text in brackets (e.g., [Duck Duck Go]) and then follow it immediately with the URL in parantheses (e.g., (https.//duckduckgo.com)).

My favorite searck engine is [Duck Duck Go](hhtps://duckduckgo.com).

## Addding Titles

You can optionally add a title for a link, This will appear as a tooltip when the user hovers over the link. To add a title, enclose it in quotation marks after the URL.

My favorite searck engine is [Duck Duck Go](https://duckduckgo.com "This is the title").

## URLs and Email Addresses

To quickly turn a  URL or email address into a link, enclose it in angle brackets.

<https://www.markdownguide.org>  
<fake@example.com>

## Fromatting Links

To emphasize links, add asterisk before and after the brackets and parentheses. To denote links as code, add backticks in the brackets.

I love supportin the **[EFF](https://eff.org)**.  
This is the *[Markdown Guide](https://www.markdownguide.org)*.  
See the section on [`code`](#code)

## Reference-style Links

Reference-styyle links are a especial kind of link that make URLs easier to display and read in Markdown. Reference-style links are contructed in two parts: the part you keep inline with your text and the park you store somewhere else inthe file to keep the text easy to read.

## Formatting the First Part of the LInk

The fisrt par of a reference-style link is formatted with two sets of brackets. The first set of brackets surrounds the text that should appear linked. The second set of brackets displays a label used to point to the link you're storing elsewhere in your document.

Although not required, you can include a space between the first and second set of brackets. The label in the second set of brackets is not case sensitive and can include letters, numbers, spaces, or punctuation.

This means the following exapel formats are roughly equivalent for the first part of the link:

- [hobbit-hole][1]
- [hobbit-hole] [2]

## Formatting the Second Part of the Link

The second par of a reference-style link is formatted with the following attributes:

1. The label, in brackets, followed immediately by a colon and at least one space (e.g., [label]; ).
2. The URL for the link, whick you can optionally enclose in angle brackets.
3. The optional title for the link, whick you can encolse in double quotes, single quotes, or parentheses.

- `[3]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle`
- `[4]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle "Hobbit lifestyles"`
- `[5]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle 'Hobbit lifestyles'`
- `[6]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle (Hobbit lifestyles)`
- `[7]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> "Hobbit lifestyles"`
- `[8]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> 'Hobbit lifestyles'`
- `[9]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> (Hobbit lifestyles)`

### Instance 1

>`In a hole in the ground there lived a hobbit. Not a nasty, dirty, wet hole, filled with the ends
of worms and an oozy smell, nor yet a dry, bare, sandy hole with nothing in it to sit down on or to
eat: it was a [hobbit-hole](https://en.wikipedia.org/wiki/Hobbit#Lifestyle "Hobbit lifestyles"), and that means comfort.`

### Instance 2

>`In a hole in the ground there lived a hobbit. Not a nasty, dirty, wet hole, filled with the ends
>of worms and an oozy smell, nor yet a dry, bare, sandy hole with nothing in it to sit down on or to
>eat: it was a [hobbit-hole][1], and that means comfort.`  
>
>`[1]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> "Hobbit lifestyles"`

### HTML

`<a href="https.//wikipedia" title="Hobbit">Hobbits</a>`

## Link Best Practices

Markdown applications don't agreee on how to handle spaces in the middle of a URL. For compatibility, try to URL encode any spaces with %20. Alternatively, if your Markdown application support HTML, you coul use the a HTML tag.

| [x] Do this | [] Don't do this |
|---|---|
| `[link](https://www.example.com/my%20great%20page)` | `[link](https://www.example.com/my great page)` |
| `<a href="https://www.example.com/my great page">link</a>` | |

Parentheses in the middle of a URL can also be problematic. For compatibility, try to URL encode the opening parenthesis (() with %28 and the closing parenthesis()) with %29. Alternatively, if your Makdown application supports HTML, you could use the a HTML tag.

| [x] Do this | [] Don't do this |
|---|---|
| `[a novel](https://en.wikipedia.org/wiki/The_Milagro_Beanfiel_War_%28novel%29)` | `[a novel](https://en.wikipedia.org/wiki/The_Milagro_Beanfield_War_(novel))` |
| `<a href="https://en.wikipedia.org/wiki/The_Milagro_Beanfield_War_(novel)">a novel</a>` | |

## Images

To add an image, add an exclamation mark (!), followed by alt tex in brackets, and the path or URL to the image asset in parentheses. You can optionally add a title in quotation marks after the path or URL.

![Image](/assets/images/image.jpg "Title")

## Linking Images

To add a link to an image enclose the Markdown for the image in brackets, and then add the link in parentheses.

[![Image](/assets/images/image.jpg "Title")](https://www.google.com)

## Escaping Characters

To display a literal character that would otherwise be used to format texte in a Markdown document, add a backslash (\) in front of the character.

`\* Without the backslash, this would be a bullet in an unordered list.`

## Characters You Can Escape

Yo can use a backslash to escape the following characters.

| | |
|---|---|
| `\` | backslash |
| ` | backtick (see also escaping backticks in code) |
| `*` | asterisk |
| `_` | underscore |
| `{ }` | curly braces |
| `[ ]` | brackets |
| `< >` | angle brackets |
| `( )` | parentheses |
| `#` | pound sign |
| `+`	| plus sign |
| `-`	| minus sign (hyphen) |
| `.` | dot |
| `!`	| exclamation mark |
| l	| pipe (see also escaping pipe in tables) |

## HTML

Many Markdown applications allow you to use HTML tags in Markdown-formatted text. This is helpful if you prefer certain HTML tags to Markdown syntax. For example, some people find it easier to use HTML tags for images. Using HTML is also helpful when you need to change the attributes of an element, like specifying the color of text or changing the width of an image.

To use HTML, place the tags in the text of your Markdown-formatted file.

`This **word** is bold. This <em>word</em> is italic.`

## HTML Best Practices

>For security reasons, not all Markdown documents. Whteen id doubt, check your Markdown application's documentation. Some appliations support only a subset of HTML tag.
>
>Use blank lines to separate block-level HTML elements like `<div>`, `<table>`, `<pre>`, and `<p>` from the surrounding content. Try not to indent the tags with tabs or spaces -- that can interfere with the fromatting.
>
>Toy can't use Markdown syntax inside block-level HTML tag. for example, `<p>`italic and `**`bold`**</p>` won't work.
