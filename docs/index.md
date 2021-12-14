## This is opus-steno

The Opus audio format has an interesting feature in the spec: padding.  The spec says that it should be left zeroed out, but also specifies that decoders
should ignore any data that is found in the padding.  This makes it ideal for stenography, or hiding other data in the file.

## Learning golang

This project is the one I picked for teaching myself golang.  I am starting with basically zero knowledge.

## Design

Creating this before I learn anything about Go.  As such, this is more of a high-level
architecture without knowing how best to arrange it in a way Go likes.

### Initial thoughts

- Need to learn how to structure a golang project ([#6](https://github.com/stephen-czetty/opus-steno/issues/6))
- Will write an opus header parser from scratch (even if a library exists, using it defeats the purpose of learning the language) ([#1](https://github.com/stephen-czetty/opus-steno/issues/1))
- Everything should have unit tests associated with it.  Don't know enough about Go yet to go TDD, but I plan to cover my work as I go.
- Will also need an ogg container parser ([#2](https://github.com/stephen-czetty/opus-steno/issues/2))
- Once the parsing works and all tests pass (with decent coverage, including failure paths), writing support needs to happen.
  - Given an opus stream, write a new one with different options (especially padding!) ([#3](https://github.com/stephen-czetty/opus-steno/issues/3))
  - Given an opus stream, place it into an ogg container ([#4](https://github.com/stephen-czetty/opus-steno/issues/4))
  - (Bonus) Muxer for opus plus a video stream ([#5](https://github.com/stephen-czetty/opus-steno/issues/5))

### References

- [Ogg Specification (RFC 3533)](reference/rfc3533-ogg-spec.html)
- [Opus Specification (RFC 6716)](reference/rfc6716-opus-spec.html)


### External Resources

- [Matroska container format](https://www.matroska.org/technical/basics.html)

### Episodes

#### [Getting started](scripts/episode1.md)

  - Building out the project structure
  - Basic Go syntax
  - Unit tests in Go

#### TDD

  - TDD in general, and why
  - 

#### Binary handling

  - Reading an ogg file, outputting statistics about it
  - Parsing the binary headers
  - Moving around in the file (finding frames, etc)

#### Coroutines

  - Not sure where they will fit in, but I imagine that they might need their own episode.
  - I guess this will come up whenever it comes up in the course of my implementation

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
  - Video stream support

### Testing

- Find a good audio file without copyright issues, and convert to opus.
  - This will be the baseline test.
  - First few tickets will not be modifying this file.
    - Well, nothing should modify this file.  The code should always output to a new file
  - 
