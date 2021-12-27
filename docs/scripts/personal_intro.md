# Personal Introduction #

Hi!  My name is Stephen Czetty.  I have been a software engineer for more than twenty years
working in industries ranging from E-Commerce to Legal to Healthcare to Financial Services.

My first exposure to programming was when I was very young, perhaps five or six years old.
Way back in the 80's, my father brought home a Compaq "luggable" from work.  As a side-project,
he was working on a program in basic that drew the logo of his company on the screen, with an
on-screen "laser", complete with a sparkle at the drawing point.  I was hooked.

I remember him showing me his program, and teaching me some of the basics.  Before long, I
was writing simple basic programs, most of which amounted to asking canned questions and
expecting very specific responses.

By the time I was in 5th or 6th grade, I found a book in my school library that contained the
source code for a Zork-like adventure game, written in basic.  I probably renewed that book
for the entire school year as I copied it, line for line.  In retrospect, it was a highly
tedious endeavour, but I learned all about concepts like functions, complex conditionals,
even some simple text parsing.

In 7th grade, I was at a flea market (or something like it) with my parents looking through
a pile of books when I came across a relatively small (considering the topic) book entitled
"Teach yourself C".  I remember begging my father to buy it for me, though I don't think that
he really put up much of a fight.  I spent the next month reading it cover-to-cover before
asking for a C compiler so I could practice my new knowledge.

That summer, I put my first line of code into production.  I was visiting my father at work and
one of his co-workers was having trouble tracking down a bug in her code.  Looking over her
shoulder, I spotted the issue and pointed it out to her.  A couple of years later, I found myself
with a job as a junior programmer at that very same company.

I suppose that it was pre-destined that I would attend an engineering school and major in
computer science.  After graduation, I moved to Troy, New York (just outside of Albany) to
attend Rensselaer Polytechnic Institute.  I did well, not great, and graduated in 1999 after
taking a semester off for an internship at the Jet Propulsion Labs in Pasadena, California.

Working at NASA/JPL was the first "real" job of my career, where I had the unique opportunity
to work directly with the Linux kernel's networking subsystem with the goal of improving
communication over long latency connections.  Think, connections from Mars and beyond.  So, yes,
some of my code is on Mars.

After graduation, I moved to Austin, Texas to work for a startup during what turned out to be
the end of the dot-com boom of the 90's.  I was writing code in the hot language at the time, Perl, and I think I was pretty good at it.  I left as a lead developer when their funding fell
through shortly after the 9/11 attacks.

I floundered for a bit looking for solid work during the next couple of years until I finally
found a gig in the legal industry.  Starting with basic data analysis and the maintenance of
their legacy Visual Basic applications, I moved on to the relatively new .net framework, though
it was still in VB.  On the side, I started teaching myself C# and preferred that immensely.

Eventually, C# became my go-to language, and I moved on to a new position in the healthcare
industry.  When the project I was working on was cancelled, they did not want to let me go,
but they also did not have any real work for me to do.  It was a paycheck for doing very little,
but it was excruciatingly boring, so I moved on to another healthcare company.

A few years ago, I was asked to move to a new team that would be doing its development in Python.
I had never programmed in Python before, so I decided that it would make sense to find a
personal project that I could use to teach myself.  I did just that, writing a fairly simple
program that combined a series of audio files into a single one.  Then I moved on to a more
complex one for controlling some aspects of my personal virtual machine box.

I stayed with that company, through several different projects and an acquisition until
very recently.  I am now working for a company in the financial services industry, but that
position is too new to tell much about it yet.

## The Go Project ##

Since a personal project worked so well to teach myself Python, I have decided to do something
similar to learn Go.  That will be the subject of the videos I intend to publish over the
course of the next several weeks.

The project is somewhat ambitious, and I hope it will allow me to explore most if not all of
the major features of Go.  In a nutshell, I would like to build a utility that hides
arbitrary data inside of an OPUS-formatted audio file.  Doing this will require me to
work directly with the binary format and rewrite it.  I do not intend to write an actual
encoder (I can leave that to ffmpeg), but instead I intend to write something that
repackages the encoded audio with the secret data included.

It should be fun.

