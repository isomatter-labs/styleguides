---
title: Markdown Style Guide
author: 'Isomorph Research Laboratories :: Dept of the Unreal'
date: 2 October 2021
---

# Flavors of markdown
Accepted flavors of markdown are as follows, in order of preferrence:

  1. pandoc markdown
  2. GitHub markdown [^1]

[^1]: GitHub markdown is preferred for ReadMe documents distributed with source code.

# Title Block [^2]
It is preferred to use YAML frontmatter blocks to store information regarding
tile, authors, and date, following the format:
```yaml
---
title: title
author: semicolon; separated; authors
date: day month year
---
```
[^2]: If title YAML blocks are rendered by GitHub markdown, it will be rendered as a table.

# Sections
Top-Level sections should be used for any top level topics discussed in the
document, as well as title and author information if not using a pandoc
tile block.

Section titles, contrary to many styleguides for markdown, should not be wrapped
by empty lines, but instead be preceded by exactly one empty line
(or a parent section), and followed immediately by the content of the section,
or a subsection title.

For example:
```markdown
# H1
Here is H1 level content

## H2
### H3
Content for subsection.

### H3-2
Content for second subsection.
```

# Column Width (Line Length)
Lines should be no more than 80 characters long, with the one exception of
footnotes. If a line will exceed the 80-char limit be even one character,
insert a newline before the last word in the line, and continue on the next
line. It is advised that you set a vertical ruler at both 80 and 100 character
column widths in your editor of choice, as these are the most common limits
in Isomorph Research Laboratories style guides.

# Footnotes
Footnotes should always be in the form of full, readable sentences, with proper
capitalization and punctuation. Footnotes are preferred for all asides, as they
are less intrusive to reading than inline notes. For examples regarding correct
use of footnotes, refer to the footnotes contained within this document.

# Text Formatting
## Bold
Bold excerpts should use the double-asterisk (`**word**`) form of notation
in all cases. Double underscores should never be used for bolding, in order to
allow for easier unrendered reading, since the presence of asterisks can be used
to interperet boldness, rather than requiring a count of asterisks present.

## Italics
Italic excerpts should use the single-underscore (`_word_`) form of notation
in all cases. Single asterisks should never be used for italics, in order to
allow for easier unrendered reading, since the presence of underscores can then
always be used to interpret boldness, rather than requiring a count of
underscores present.

## Bold and Italics
In the case where something is bolded and italicized, the bold should be the
inner formatting, while the italization should be the outer formatting
(`_**word**_`). Note that only asterisks are used for bolding, and underscores
for italics, as prescribed earlier.

## Verbatim
Verbatim should be used only to refer to terms that may be confusing when
formatted otherwise, such as variable names or filenames. Verbatim is almost
always used to format things that should be entered into a computer or other
piece of equipment verbatim, hence the name.

Verbatim should _never_ be used for code blocks. In cases of code, always prefer
code blocks, as they allow syntax highlighting for easier parsing.

## Code Blocks
Code blocks should only be used for code snippets (even one-liners), or other
compiled/interpreted text. Markdown allows for syntax highlighting in code
blocks, by following the initial three backticks with the name of the language
being used in the code block. If you are unsure how this language is
abbreviated for markdown, it is easily google-able.

Use of a code block for both a single line and section of C++:

```cpp
void printUserId(int id, char mode);
```

```cpp
void printUserId(int id, char mode) {
  if (mode == 'd') {
    std::cout << "=<< USER ID: " << id << " >>=" << std::endl;
  }
  return;
}
```