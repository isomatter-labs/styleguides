% Embyr Technologies Markdown Style Guide
% Matthew Cooper Healy
% 8 April 2018

# Flavors of markdown
Accepted flavors of markdown are as follows, in order of preferrence:

  1. pandoc markdown
  2. GitHub markdown

# Title Block
It is preferred to use pandoc title blocks to store information regarding
tile, authors, and date, following the format:
```
% title
% semicolon; separated; authors
% day month year
```
#### Note: if this title block is rendered by markdown other than pandoc, it will be formatted incorrectly.

# Sections
Top-Level sections should be used for any top level topics discussed in the
document, as well as title and author information if not using a pandoc
tile block.

# Column Width (Line Length)
Lines should be no more than 80 characters long, with the one exception of
inline notes. If a line will exceed the 80-char limit be even one character,
insert a newline before the last word in the line, and continue on the next
line. It is advised that you set a vertical ruler at both 80 and 100 character
column widths in your editor of choice, as these are the most common limits
in Embyr Technologies style guides.

Inline notes may extend to up to 200 characters, although
brevity is preferred.

# Inline Notes
In the case where the current section-level is greater than four, notes
should have a section level one more than the curent section level.
In all other cases, notes should have a section level of four (i.e.
`#### Note: `). Notes should follow the form of the word "Note", followed
by a colon, then a space, then the note to be written.

Notes should always be in the form of full, readable sentences, with proper
capitalization and punctuation. Note that "Note: " begins the first sentence,
to the succeeding word need not be capitalized (see notes within this document
for reference).

# Text Formatting
## Bold
Bold excerpts should use the double-asterisk (`**word**`) form of notation
in all cases.

## Italics
Italic excerpts should use the single-underscore (`_word_`) form of notation
in all cases.

## Bold and Italics
In the case where something is bolded and italicized, the bold should be the
inner formatting, while the italization should be the outer formatting
(`_**word**_`).

## Verbatim
Verbatim should be used only to refer to terms that may be confusing when
formatted otherwise, such as variable names or filenames. Verbatim is almost
always used to format things that should be entered into a computer or other
piece of equipment verbatim, hence the name.
Verbatim should _never_ be used for code blocks.

## Code Blocks
Code blocks should only be used for code snippets (even one-liners), or other
compiled/interpreted text. Markdown allows for syntax highlighting in code
blocks, by following the initial three backticks with the name of the language
being used in the code block. If you are unsure how this language is
abbreviated for markdown, it is easily google-able. What follows is a proper
use of a code block for both a single line and section of C++:

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

#### Note: this is a living document and is updated regularly with new standards as they are required.