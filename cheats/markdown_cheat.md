# Markdown Cheat

The following lists the way I edit markdown. There are sometimes more than one way in markdown, I'll list only the one I typically use.

Markdown is depending on the renderer, the following should work at least with GitHub repositories and Visual Studio Code (using the "Markdown Preview Enhanced" extension).

## Table of Contents

* [Sections](#sections)
* [Text](#text)
* [Lists](#lists)
* [Blocks](#blocks)
* [Tables](#tables)
* [Links](#links)
* [Images](#images)
* [Other](#other)

## References

The following is based on:

* https://www.markdownguide.org/basic-syntax/
* https://www.markdownguide.org/extended-syntax
* https://www.markdownguide.org/hacks

---

## Sections

### Headings

```
# Heading Level 1
```

# Heading Level 1

```
## Heading Level 2
```

## Heading Level 2

```
### Heading Level 3
```

### Heading Level 3

> :bulb: **Tip:** Put blank lines before and after headings.

### Horizontal Rules

```
---
```

---

> :bulb: **Tip:** Put blank lines before and after horizontal rules.

## Text

### Bold

```
**Bold Text**
```

**Bold Text**

### Italic

```
*Italicized text*
```

*Italicized Text*

### Strikethrough

```
~~This was wrong~~ This is right.
```

~~This was wrong~~ This is right.

### ~~Subscript~~

```
H\~2~O
```

H~2~O

> :warning: **Warning:** Doesn't work with GitHub!

### ~~Superscript~~

```
X\^2^
```

X^2^

> :warning: **Warning:** Doesn't work with GitHub!

### ~~Color~~

#### ~~Font (HTML)~~

```
<font color="red">This text is red!</font>
```

<font color="red">This text is red!</font>

> :warning: **Warning:** Doesn't work with GitHub!

#### ~~CSS (HTML)~~

```
<span style="color:black; background-color:white">black on white</span>
```

<span style="color:black; background-color:white">black on white</span>

> :warning: **Warning:** Works only in GitHub Pages, doesn't work with GitHub!

## Lists

### Unordered List

```
* first
  * subitem
* second
```

* first
  * subitem
* second

> :bulb: **Tip:** Use two spaces before subitems.

### Ordered List

```
1. first
  1.1. subitem
2. second
```

1. first
1.1. subitem
2. second

> :bulb: **Tip:** Use two spaces before subitems.

### Task List

```
- [x] Task 1
- [ ] Task 2
```

- [x] Task 1
- [ ] Task 2

## Blocks

### Blockquotes

```
> Block quote
```

> Block quote

> :bulb: **Tip:** Put blank lines before and after block quotes.

### Code

#### Inline e.g. for Commands

```
Enter ```ps -A``` to list all processes.
```

Enter ```ps -A``` to list all processes.

#### Fenced Code Blocks

> :bulb: **Tip:** Use three backticks.

````
```
This is my code block
```
````

```
This is my code block
```

#### Syntax highlighting

````
```c
void main() {
    printf("Hello World!");
}
```
````

```c
void main() {
    printf("Hello World!");
}
```

Languages: c, cpp, json, ...

List of supported languages (but depends on renderer): https://github.com/jincheng9/markdown_supported_languages

## Tables

```
| Title 1 | Title 2 |
| --- | --- |
| Cell 1 | Cell 2 |
```

| Title 1 | Title 2 |
| --- | --- |
| Cell 1 | Cell 2 |

### Table Alignment

```
| Title 1         | Title 2        | Title 2          |
| :---            |    :----:      |             ---: |
| Left 1          | Mid 1          | Right 1          |
| Text for left 2 | Text for mid 2 | Text for right 2 |
```

| Title 1         | Title 2        | Title 2          |
| :---            |    :----:      |             ---: |
| Left 1          | Mid 1          | Right 1          |
| Text for left 2 | Text for mid 2 | Text for right 2 |

## Links

> :bulb: **Tip:** Avoid spaces (use %20) and such in links (and local filenames).

### URL

```
https://duckduckgo.com
```

https://duckduckgo.com

OR

```
[Duck Duck Go](https://duckduckgo.com "Optional tooltip")
```

[Duck Duck Go](https://duckduckgo.com "Optional tooltip")

### Link to #headings on the same page

```
[Text for Headings Link](#headings)
```

[Text for Headings Link](#headings)

### Link to a different "local" page / file

```
[Text for python_cheat.md Link](python_cheat.md)
```

[Text for python_cheat.md Link](python_cheat.md)

### ~~Open Link in new tab (HTML)~~

```
<a href="https://www.markdownguide.org" target="_blank">Learn Markdown!</a>
```

<a href="https://www.markdownguide.org" target="_blank">Learn Markdown!</a>

> :warning: **Warning:** Doesn't work with GitHub!

## Images

```
![Tape]\(/ptouch/images/cassette_side.jpg "Optional Tooltip")
*Image with caption and (optional) tooltip*
```

![Tape](/ptouch/images/cassette_side.jpg "Optional Tooltip")
*Image with caption and (optional) tooltip*

### Image resized (HTML)

```
<img src="/ptouch/images/cassette_side.jpg" width="200">
```

<img src="/ptouch/images/cassette_side.jpg" width="200">

### Draw.io

Draw.io / diagrams.net drawings in SVG format can be directly edited in Visual Studio Code with the "Draw.io Integration" extension and displayed in the git repo on GitHub.

> :bulb: **Tip:** This enables a seamless drawing experience without exporting an intermediate png or such

```
![Example](/example.drawio.svg "Example Draw.io drawing (in svg format)")
```

![Example](/example.drawio.svg "Example Draw.io drawing (in svg format)")

> :memo: **Note:** Unfortunately, displaying the .svg in GitHub sometimes fails

### Emojis

List of emojis: https://gist.github.com/rxaviers/7360908

| Emoji | Code | Remark |
| --- |--- |--- |
| :thumbsup: | `:thumbsup:` | Good / Pros |
| :thumbsdown: | `:thumbsdown:` | Bad / Cons |
| :smile: | `:smile:` | Smile |
| :wink: | `:wink:` | Wink |
| :rage: | `:rage:` | Angry |
| :worried: | `:worried:` | Worried |
| :heart: | `:heart:` | Heart |
| :star: | `:star:` | Star |
| :question: | `:question:` | Question |
| :exclamation: | `:exclamation:` | Exclamation |
| :warning: | `:warning:` | Warning |
| :bulb: | `:bulb:` | Tip |
| :memo: | `:memo:` | Note |
| :no_entry: | `:no_entry:` | No entry |
| :construction: | `:construction:` | Under construction |
| :x: | `:x:` | Not Done |
| :heavy_check_mark: | `:heavy_check_mark:` | Ok / Check (there is no better emoji) |
| :zzz: | `:zzz:` | Sleep |
| :hourglass: | `:hourglass:` | Wait |

### Admonitions

```
> :warning: **Warning:** This is a warning, red alert emergency
```

> :warning: **Warning:** This is a warning, red alert emergency

## Other

### Footnotes

See: https://www.markdownguide.org/extended-syntax/#footnotes

### Character Escaping

See: https://www.markdownguide.org/basic-syntax/#escaping-characters
