# Markdown Cheat

The following lists the way I edit markdown. There are sometimes more than one way in markdown, I'll list only the one I typically use.

Markdown is depending on the renderer, the following should work at least with GitHub and Visual Studio Code (using the "Markdown Preview Enhanced" extension).

## References

The following is based on:

* https://www.markdownguide.org/basic-syntax/
* https://www.markdownguide.org/extended-syntax
* https://www.markdownguide.org/hacks

---
---

## Headings

> \# Heading Level 1
> \#\# Heading Level 2
> \#\#\# Heading Level 3

# Heading Level 1
## Heading Level 2
### Heading Level 3

> :bulb: **Tip:** Put blank lines before and after headings.

## Horizontal Rules

> \---

---

> :bulb: **Tip:** Put blank lines before and after horizontal rules.

## Bold

> \*\*Bold text\*\*

**Bold Text**

## Italic

> \*Italicized text\*

*Italicized Text*

## Strikethrough

> \~~This was wrong~~ This is right.

~~This was wrong~~ This is right.

## Subscript

> H\~2~O

H~2~O

## Superscript

> X\^2^

X^2^

## Color

### Font (HTML !)

> \<font color="red">This text is red!\</font>

<font color="red">This text is red!</font>

### CSS (HTML !)

> \<span style="color:black; background-color:white">black on white\</span>

<span style="color:black; background-color:white">black on white</span>

> :warning: **Warning:** Doesn't work with GitHub!.

## Blockquotes

> \> Block quote

> Block quote

> :bulb: **Tip:** Put blank lines before and after block quotes.

## Ordered List

> 1. first
> 1.1. subitem
> 2. second

1. first
1.1. subitem
2. second

TODO: Hmmm, character escaping doesn't work here

## Unordered List

> \* first
> &nbsp;&nbsp;\* subitem
> \* second

* first
  * subitem
* second

> :bulb: **Tip:** Use two spaces before subitems.

## Task List

> \- [x] Task 1
> \- [ ] Task 2

- [x] Task 1
- [ ] Task 2

## Code

### Inline e.g. for Commands

> Enter \`\`\`ps -A\`\`\` to list all processes.

Enter ```ps -A``` to list all processes.

### Fenced Code Blocks

> :bulb: **Tip:** Use three backticks.

> \`\`\`
> This is my code block
> \`\`\`

```
This is my code block
```

### Syntax highlighting

> \`\`\`c
> void main() {
>     printf("Hello World!");
> }
> \`\`\`

```c
void main() {
    printf("Hello World!");
}
```

Languages: c, cpp, json, ...

List of supported languages (but depends on renderer): https://github.com/jincheng9/markdown_supported_languages

## Links

> :bulb: **Tip:** Avoid spaces (use %20) and such in links (and local filenames).

### URL

> https://duckduckgo.com

https://duckduckgo.com

OR

> \[Duck Duck Go](https://duckduckgo.com)

[Duck Duck Go](https://duckduckgo.com)

### Link with Tooltip

> \[Duck Duck Go](https://duckduckgo.com "This is my duck tooltip")

[Duck Duck Go](https://duckduckgo.com "This is my duck tooltip")

### Open Link in new tab (HTML !)

> \<a href="https://www.markdownguide.org" target="_blank">Learn Markdown!\</a>

<a href="https://www.markdownguide.org" target="_blank">Learn Markdown!</a>

### Link to #headings on the same page

> \[Text for Headings Link](#headings)

[Text for Headings Link](#headings)

### Link to a different "local" page / file

> \[Text for README.md Link](README.md)

[Text for README.md Link](README.md)

## Images

> \![Tape]\(/ptouch/images/cassette_side.jpg)

OR with optional tooltip:

> \![Tape]\(/ptouch/images/cassette_side.jpg "Tape Tooltip")

![Tape](/ptouch/images/cassette_side.jpg "Tape Tooltip")

### Image with caption

> \![Tape]\(/ptouch/images/cassette_side.jpg)
> \*My caption*

![Tape](/ptouch/images/cassette_side.jpg)
*My caption*

### Image resized (HTML !)

> \<img src="/ptouch/images/cassette_side.jpg" width="200">

<img src="/ptouch/images/cassette_side.jpg" width="200">

TODO: Add hints for image.drawio.svg

## Emojis

List of emojis: https://gist.github.com/rxaviers/7360908

> \:thumbsup:
> \:thumbsdown:
> \:question:
> \:warning:
> \:bulb:
> \:memo:

:thumbsup: Good / Pros
:thumbsdown: Bad / Cons
:question: Question
:warning: Warning
:bulb: Tip
:memo: Note

## Tables

> \| Title 1 | Title 2 |
> \| --- | --- |
> \| Cell 1 | Cell 2 |

| Title 1 | Title 2 |
| --- | --- |
| Cell 1 | Cell 2 |

### Alignment

> \| Title 1         | Title 2        | Title 2          |
> \| :---            |    :----:      |             ---: |
> \| Left 1          | Mid 1          | Right 1          |
> \| Text for left 2 | Text for mid 2 | Text for right 2 |

| Title 1         | Title 2        | Title 2          |
| :---            |    :----:      |             ---: |
| Left 1          | Mid 1          | Right 1          |
| Text for left 2 | Text for mid 2 | Text for right 2 |

## Footnotes

See: https://www.markdownguide.org/extended-syntax/#footnotes

## Admonitions

> \> \:warning: \*\*Warning:** This is a warning, red alert emergency

> :warning: **Warning:** This is a warning, red alert emergency

## Character Escaping

See: https://www.markdownguide.org/basic-syntax/#escaping-characters
