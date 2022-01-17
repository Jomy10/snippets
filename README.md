# Snippets file format
The snippet file format is a file format for storing and retrieving pieces of text (strings).

## Table of contents
- [Specification](#format-specification)
- [Parsers](#parsers)
- [Contributing](#contributing)
- [License](#license)

## Format specification
The format is very simple and made to both generate using code or write it manually.

Strings are separated as follows:
```snippet
-- title --
Some string that can be
multiple lines.
-- end --
```

Start a new string using `-- title --`, where `title` is an identifier for your string, which can contain spaces and any utf-8 supported character.

The string is ended with `-- end --`.

When you get the above example with a parser, you will get back: "Some string that can be\nmultiple lines.".

Comments can be added on lines that are not part of a snippet, since these lines are simply ignored.

### File extension
The file extension for a snippet file is either `.snippet` or `.snip`.

## Parsers
Parsers should be able to read a file and seperate the individual snippets seperated by `-- title --` and `-- end --`.

## List of parsers
If you implement a parser in a new language, just open a pull request to add them to the list.

- [Rust](https://github.com/jomy10/snippets-rs)

## Contributing
If you have improvements for the file format, feel free to open an issue. If you have made a parser, feel free to open a pull request.

## License
The file format is licensed under the [MIT License]((LICENSE).

