# Episode 1 #

## Getting started with Golang ##

Hi! This will be my first start with golang, and I will be recording this so that you can follow along.
Besides some initial research, I know basically zero about go and how to best use it.  That's the fun
part, though, and I hope that at by the end of this series, both you and I will have learned something.

The project I have in mind I hope will allow me to explore most of the features and syntax of Go by the
time it reaches its conclusion.  If it is actually useful in the real world, or if there is already
an existing and better project that does the same thing, well, that's not really important.  My main goal
is to learn and become proficient with Go as a programming language.
  
I hope this project can do that.  Maybe I'll have to do another one to explore other aspects of the language,
but I won't know that until I've progressed much farther than the zero I'm at right now.
  
So what do I want to write?  The basic idea is to write a utility that can hide arbritary data inside of
an OPUS-encoded audio file, without effecting audio quality.  OPUS makes that pretty easy, with the
support for padding at the end of each of its frames.  I would also like to explore another mode, by re-using
the least-signifigant bit of the encoded audio itself, and maybe a hybrid option of the two.  I will consider
the project a success if the first mode is working well, but will relish the challenge of modes two and three.
  
(Cut to OPUS documentation, describe the details, unscripted (?))

I intend to start with a test project and then get started with code to read and parse the header of an OGG
stream.  At this stage, I only want to be able to read the basic metadata stored in the header.  From there I will
go on to read the other embedded metadata.

So let's go ahead and jump right in.
