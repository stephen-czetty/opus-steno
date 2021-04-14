## This is opus-steno

The Opus audio format has an interesting feature in the spec: padding.  The spec says that it should be left zeroed out, but also specifies that decoders
should ignore any data that is found in the padding.  This makes it ideal for stenography, or hiding other data in the file.

## Learning golang

This project is the one I picked for teaching myself golang.  I am starting with basically zero knowledge.

## Resources

- [Opus File Format](https://tools.ietf.org/html/rfc6716) -- Look at padding
- [Ogg container format](https://xiph.org/ogg/doc/rfc3533.txt)
- [Matroska container format](https://www.matroska.org/technical/basics.html)

## Design

Creating this before I learn anything about Go.  As such, this is more of a high-level
architecture without knowing how best to arrange it in a way Go likes.

 ### Initial thoughts

- Will write an opus header parser from scratch (even if a library exists, using it defeats the purpose of learning the language) ([#1](https://github.com/stephen-czetty/opus-steno/issues/1))
- Everything should have unit tests associated with it.  Don't know enough about Go yet to go TDD, but I plan to cover my work as I go.
- Will also need an ogg container parser ([#2](https://github.com/stephen-czetty/opus-steno/issues/2))
- Once the parsing works and all tests pass (with decent coverage, including failure paths), writing support needs to happen.
  - Given an opus stream, write a new one with different options (especially padding!) ([#3](https://github.com/stephen-czetty/opus-steno/issues/3))
  - Given an opus stream, place it into an ogg container ([#4](https://github.com/stephen-czetty/opus-steno/issues/4))
  - (Bonus) Muxer for opus plus a video stream 

### Components

- Core
  - Exception classes
  - I/O helpers
  - Etc.
- Command-line
  - Entry point
  - Command-line parser
- Opus
  - Code to parse binary opus packets
  - Code for writing opus packets
- Ogg
  - Parsing ogg containers
  - Ogg container muxer