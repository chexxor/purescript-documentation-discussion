
## Source: Teach Don't Tell

http://stevelosh.com/blog/2013/09/teach-dont-tell/

Main ideas:

- Reading the Source code is not the same as reading documentation: **it's only useful once you already know how to use the code.**
- Reading the Tests' code is not the same as reading documentation: **it's only useful once you already know how to use the code.**
- Using literate programming tools don't help.
- Using wikis as a way to document things are horrible because
    1. there is no coherent voice (multiple authors that often times fight/correct one another)
    2. it allows the excuse, "If you don't understand it yourself, you can write the content and fix it!"
    3. there is no version control (even GitHub wikis aren't good for this since they are separate from the project/code)

Critique: This presumes a single person is writing the entire documentation. Larger projects don't have this luxury.

### Purpose of Documention

> The purpose of technical documentation is to take someone who has never seen your project, teach them to be an expert user of it, and support them once they become an expert.

> You can’t look at the finished product and understand the perspective and ideas that went into it without additional guidance. That’s a job for documentation.

> If you want to write better documentation, you need to practice teaching.

> As programmers, we almost never get this (face-to-face conversation) kind of feedback about our documentation. We don’t see that the person on the other end of the wire is hopelessly confused and blundering around because they’re missing something we thought was obvious (but wasn’t). Teaching someone in person helps you learn to anticipate this, which will pay off (for your users) when you’re writing documentation.

There are 4 types of documentation: 1st contact, the black triangle, the hairball, the reference

### First Contact

Basically, a "high-level overview and purpose statement"

Answers questions like "What is this thing, why would I care about it, why would I not care about it, and why is it worth my effort to learn how to use it?"

### Black Triangle

> First, it lets the user verify that yes, this collection of bytes is actually going to run and do something on their machine. It’s a quick sanity check that the project hasn’t bit rotted and is still viable to use at that point in time. More importantly, it lets your prospective user get some paint on the canvas.

Basically a "getting started guide"

If it's up-to-date, then the reader knows the library/code isn't stale or out-of-date

It doesn't teach everything someone needs to know, just enough to start being productive. For example, a guitar teacher teaches enough chords to play a song, not all possible chords at once before ever starting.

### Hairball

Basically, the "explanation" part of docs

> The “hairball” is the twisted, tangled maze of teaching that is going to take these novices and turn them into expert users. It’s going to mold their brains, one nudge at a time, until they have a pretty good understanding of how your project works.

> You should have a table of contents that lists each section of the “hairball”. And then each section should have its own table of contents that lists the sections inside it. 

### Recommended approach to teaching something new to a person

> The process needs to go something like this:
> 1. Figure out what they already know. (identity start point)
> 2. Figure out what you want them to know after you finish. (identity end point)
> 3. Figure out a single idea or concept that will move state 1 a little bit closer to state 2. (figure out path)
> 4. Nudge the student in the direction of that idea. (instruct/guide using path)
> 5. Repeat until state 1 becomes state 2.

> Too often I see documentation that has very carefully considered step 2, and then simply presents it to the reader as a pronouncement from God. That isn’t teaching. That’s telling. People don’t learn by being told, they learn by being taught.

- The above is a less clearly-defined version of the GTD-modified methodology we're using here.
