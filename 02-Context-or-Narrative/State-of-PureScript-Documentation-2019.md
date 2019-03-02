# State of PureScript Documentation: 2019

## Why Read This Document?

This document is not meant to convince you to use PureScript. We assume that readers already believe in using PureScript instead of alternatives.

It is well-known among the PureScript community that its documentation is lacking in some critical areas. As a result, @chexxor started the [PureScript documentation efforts in 2019](https://discourse.purescript.org/t/purescript-documentation-efforts-in-2019/524) discourse thread to answer one question:
> How can we improve the PureScript documentation in 2019?

(Purpose) The following document tries to do two things:
1. Provide an answer to @chexxor's above question
2. Answer other related questions that various audiences will have:
    - new learners (regardless of language background)
    - PureScript documentation writers
    - Core Contributors

Outline
- Explain what is "good" documentation to define a criteria
- Evaluate PureScript's documentation using that criteria
- Explain why PureScript's documentation is lacking and what is being done to improve it
- Address various audience's possible concerns or questions centered on these themes:
    - New learners - How should I learn PureScript?
    - PureScript documentation writers - How should I write good maintainable documentation for others?
    - Core Contributors -

## What is "Good" Documentation Anyway?

Did someone ever teach you how to write "good" documentation? No, you likely just wrote what came to mind and hoped it was good enough.

So, it helps to understand what is "good" documentation and why.

Essentially, there are 4 factors that affect whether documentation is "good" or not.
1. The type of documentation
2. The intended audience
3. How up-to-date the documentation is
4. The medium in which the documentation appears

### The Types of Documentation

First, there are 5 types of documentation that target specific phases of a learner's experience (as explained in [What Nobody Tells You About Documentation](https://www.divio.com/blog/documentation/) and [Teach, Don't Tell](http://stevelosh.com/blog/2013/09/teach-dont-tell/))

| Type | Analogy | Characteristics
| -- | -- | -- |
| The Hook | Selling a product to a potential customer | <ul><li>Answers 'What is this thing? / What problem does it solve?'</li><li>Answers 'Why whould I care? / How is this relevant to me for my purposes?'</li><li>Answers 'Is learning how to use this thing worth it to me?'</li></ul>
| Getting Started | Teaching a child how to cook | <ul><li>Focuses on the learner 'doing' stuff, not 'explaining' stuff to the learner</li><li>Provides a small simple working example</li><li>New learners experience an 'I can use this now!' moment by the end</li><li>Focuses on concrete tasks, not abstract concepts</li><li>Does not use jargon</li><li>Explains only what is necessary and cuts out all else</li><li>Avoids explaining deeper concepts or different ways of doing the same thing</li></ul>
| How-To Guides | Following a cook book's recipe | <ul><li>Achieves some goal or solves a problem</li><li>States the pre-requisites one needs to have before starting (not a Getting Started Guide)</li><li>The Guide follows a clearly-labeled step-by-step process</li><li>By following the steps, one reproduces the same results without fail</li><li>Explains the different ways one can achieve the same goal</li><li>Explains only what is necessary</li></ul>
| Explanation | Listening to a CEO answer questions about his company | <ul><li>Explains the context/history</li><li>Explains the significant design decisions made, their alternativees, and the reasons one was chosen over another</li><li>Implies where things could be improved, expanded, refined, etc.</li></ul>
| Reference | Reading an encyclopedia | <ul><li>Concise explanation of each piece of the code</li><li>The structure of the reference mirrors the structure of the code it documents</li><li>Formatting is consistent throughout the material</li></ul>

Moreover, there are clear examples of "bad" documentation (as explained in [Teach, Don't Tell](http://stevelosh.com/blog/2013/09/teach-dont-tell/)):

| Statement | Why it's bad |
| -- | -- |
| Read the Source Code | Only useful once you are already familiar with it
| Read the Test Code | While it uses the code, it tends to focus on edge cases, not normal cases, and may not use all possible options/configurations.
| Read the API docs | One must know the name of the function/value to be able to read its documentation. Most won't know the name until you teach it to them. Likewise, people don't learn by reading alphabetized lists of disconnected information
| Read the Wiki | Content is usually not written by the code's authors, but by multiple 3rd-party people. There are often multiple disconnected voices throughout the material. It's like asking a student to write his own lesson plan.

### The Documentation's Intended Audience

Second, the number of intended audiences can vary greatly. For example, here are different ways of categorizing them:
- The language/paradigms they primarily use and think in (e.g. JavaScript, Ruby, Haskell; lazy, strict; OO, FP; etc.)
- The amount of experience they have (e.g. never coded before, junior, senior, etc.)
- The programs they are looking to create (e.g. games, financial applications, cryptography, etc.)

Writing documentation that targets JavaScript-background junior developers who want to write games will focus on some things, exclude others, and order its content in a way that makes most sense to that purpose.

As a result, others who read the resulting documentation will consider it "poor" in some aspect:
- If one comes from a non-JavaScript language, one might find references to features in JavaScript confusing: "They used the concept of 'prototypes' to explain something, but that left me even more confused..." ~ a Java developer
- If one comes from a different experience level, one might have unanswered questions: "They didn't even mention what the performance trade-offs for specific libraries were..." ~ a senior developer
- If one has a different goal in mind, some crucial libraries might never be covered: "They didn't explain how I can make my Bitcoin client cryptographically secure..."

### The Documentation's Accuracy

Third, documentation becomes inaccurate in two ways when breaking changes occur: usefulness (depends on 'size' of breaking change) and coherence (depends on 'frequency' of breaking change).

When **large** breaking changes occur, documentation can immediately become useless because:
- none of its examples work anymore
- old terms might mean something different now
- the order of explanations should appear in a different way now
- some explanations are no longer relevant

When breaking changes occur **frequently**, documentation can appear more like loosely-coupled snippets of ideas rather than a coherent explanation

In short, it is impossible to write "good" documentation for everyone that is up-to-date all the time. There's simply not enough manpower, time, and incentives to do that. Rather, it will be "good", "horrible", or "somewhere in-between" for diffent kinds of people and at different times/seasons.

### The Mediums of Documentation

Fourth, documentation can appear in a few mediums/formats:

| Code | Explanation | Example
| -- | -- | -- |
| Syntax-highlighted snippets | Long Essay | Blog Posts
| Intermixed | Intermixed | Literate Programming
| Actual code | Comments | Working Examples
| Actual code | Slides / Explanation | Walking through someone in a video

### Criteria for "Good" Documentation

Still, we can define our criteria for "good" documentation using these four factors:
- [Type]
    - It defines which type of documentation it is
    - If a Hook, then
    - If a Getting Started, then
    - If a How-To Guide, then
    - If a Reference, then
    - If a Explanation, then
- [Audience]
    - It states who the intended audience is
- [Accuracy]
    - It explains which version of the code it documents
        - If it's not the most recent version, it explains:
            - Where it is outdated
            - How to understand the outdated explanation in light of the new changes
    - It includes the date it was published and last updated

A few different audiences
- shared (things we should explain, no matter who reads this)
    - Why read this document (capture people's attention in less than 2 paragraphs)
    - What is good documentation for new learners? (defining our terminology and criteria)
    - How does PureScript fair in that regard? (use that criteria to judge PS' current documentation)
    - Why isn't it better? (explain the obstacles that prevent it from being better)
- new learners (address things new learners care about)
    - What should your expectations be when learning? (frustration arises when expectations are broken)
    - How are people currently trying to improve it? (explain current efforts that people can tag alongside of / help / give feedback on)
    - How can you help in this effort? (you are most motivated, so you'll drive the effort or help out in some situations)
- Documentation writers (address things they care about)
    - How do I write good documentation for new learners?
    - How do I write documentation that does not go out-of-date quickly?
    - How do I write maintainable documentation?
    - How should I bring awareness to my documentation efforts?
- PS core contributors (things they care about)
    - What processes could be automated to save you time / lower the maintenance cost?
    - Questions whose answers would be helpful for others to know
        - What 'qualifications', if any, would they prefer someone has before delegating a project to them?

Here's a quick overview of some of its benefits compared to other languages:
- PureScript provides certain guarantees by default that other web languages do not or cannot (e.g. JavaScript, TypeScript)
- PureScript is more powerful than similar alternatives (i.e. Elm)
- PureScript can be used to 'patch' existing code, enabling one to slowly migrate a large application to PureScript one component at a time (unlike Haskell's GHCJS).