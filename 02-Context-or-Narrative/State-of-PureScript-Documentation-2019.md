# State of PureScript Documentation: 2019

This document is not meant to convince you to use PureScript, we assume that readers are already interested in it or using it.

Numerous parties within the PureScript community (e.g. [core contributors](), [users](), [new learners]()) believe that the documentation is lacking in some critical areas. As a result, @chexxor started the [PureScript documentation efforts in 2019](https://discourse.purescript.org/t/purescript-documentation-efforts-in-2019/524) Discourse thread to answer one question:
> How can we improve the PureScript documentation in 2019?

(Purpose) The following document tries to do the following things:
1. Provide a researched narrative of PureScript's documentation development and history.
2. Define the types of audiences of PureScript documentation and their expectations.
    - New learners (regardless of language background)
    - PureScript documentation writers
    - Core contributors
3. Summarize the current opinions of PureScript's documentation audiences.
4. Explore strategies for improving PureScript's documentation for its audiences.

<!-- https://imthenachoman.github.io/nGitHubTOC/ -->

- [State of PureScript Documentation: 2019](#state-of-purescript-documentation-2019)
  - [Current PureScript Documentation](#current-purescript-documentation)
    - [What is Documentation?](#what-is-documentation)
    - [What is PureScript's Documentation?](#what-is-purescripts-documentation)
    - [How Should Programming Strategies be Documented?](#how-should-programming-strategies-be-documented)
    - [Who is Writing PureScript's Documentation?](#who-is-writing-purescripts-documentation)
    - [How is Documentation Currently Generated?](#how-is-documentation-currently-generated)
  - [Documentation Desired by Specific Audiences](#documentation-desired-by-specific-audiences)
    - [Core Contributors](#core-contributors)
    - [New Learners](#new-learners)
    - [Documentation Writers](#documentation-writers)
  - [Documentation Improvement](#documentation-improvement)


## Current PureScript Documentation

### What is Documentation?

Did someone ever teach you how to write "good" documentation? Probably not - you likely just wrote what came to mind and hoped it was good enough.

Because of this, it's useful to learn a definition of good documentation and understand why it's defined that way.

Essentially, there are 3 factors that affect whether documentation is "good" or not.
1. Its intended audience
2. Its type: the question being answered, targeting a specific subsection of the audience
3. How accurately it reflects the desired version of the code/project

It's important to note that this section is sourced from only two blog posts, [What Nobody Tells You About Documentation](https://www.divio.com/blog/documentation/) and [Teach, Don't Tell](http://stevelosh.com/blog/2013/09/teach-dont-tell/). As we learn more this section might change in significant ways, so any conclusions we draw should be kept "flexible".

First, there are 5 types of documentation that target specific phases of a learner's experience (as explained in [What Nobody Tells You About Documentation](https://www.divio.com/blog/documentation/) and [Teach, Don't Tell](http://stevelosh.com/blog/2013/09/teach-dont-tell/))

| Learner's Phase | Type | Analogy | Characteristics
| -- | -- | -- | -- |
| Curious Outsider | The Hook | Selling a product to a potential customer | Answers these questions: <ul><li>What is this thing? / What problem does it solve?</li><li>Why whould I care? / How is this relevant to me for my purposes? / Who should not care?</li><li>How long will it take to learn it and how difficult is the learning curve?</li><li>Where do I go to get started / learn how to use this?</li></ul>
| Potential User | Getting Started | Teaching a child how to cook | <ul><li>Focuses on the learner 'doing' stuff, not 'explaining' stuff to the learner</li><li>Provides a small simple working example that teaches the basics</li><li>New learners experience an 'I can use this now!' moment by the end</li><li>Focuses on concrete tasks, not abstract concepts</li><li>Does not use jargon</li><li>Explains only what is necessary and cuts out all else</li><li>Avoids explaining deeper concepts or different ways of doing the same thing</li></ul>
| New User | How-To Guides | Following a cookbook's recipe | <ul><li>Achieves some goal or solves a problem</li><li>States the pre-requisites one needs to have before starting (not a Getting Started Guide)</li><li>The Guide follows a clearly-labeled step-by-step process</li><li>By following the steps, one reproduces the same results without fail</li><li>Explains the different ways one can achieve the same goal</li><li>Explains only what is necessary</li></ul>
| Active User | Reference | Reading an encyclopedia | <ul><li>Concise explanation of each piece of the code</li><li>The structure of the reference mirrors the structure of the code it documents</li><li>Formatting is consistent throughout the material</li></ul>
| Experienced User | Explanation | Listening to a CEO answer questions about his company | <ul><li>Explains the context/history</li><li>Explains the significant design decisions made, their alternativees, and the reasons one was chosen over another</li><li>Implies where things could be improved, expanded, refined, etc.</li></ul>

Moreover, there are clear examples of "bad" documentation (as explained in [Teach, Don't Tell](http://stevelosh.com/blog/2013/09/teach-dont-tell/)):

| Documentation Source | Why it's bad |
| -- | -- |
| Source Code | Only useful once you are already familiar with it
| Test Code | While it uses the code, it tends to focus on edge cases, not normal cases, and may not use all possible options/configurations.
| API docs | One must know the name of the function/value to be able to read its documentation. Most won't know the name until you teach it to them. Likewise, people don't learn by reading alphabetized lists of disconnected information
| Wiki | Content is usually not written by the code's authors, but by multiple 3rd-party people. There are often multiple disconnected voices throughout the material. It's like asking a student to write his own lesson plan.


TODO: links to separate file that includes full content of the rest of that section


### What is PureScript's Documentation?

Here was PureScript's documentation as of July 2018:

| Name | Type | Audience | Medium |
| -- | -- | -- | -- |
| The Documentation Repository | Getting Started + Explanation | New PS Learners | GitHub Repo
| Pursuit | Reference | All PS developers | API Docs website
| PureScript by Example | Getting Started + How To + Explanation | New PS Learners | Book
| PureScript Resources | Getting Started + Explanation | New PS Learners | Read The Docs
| Lens for the Mere Mortal: PureScript Edition | How To + Explanation | Intermediate PS Learners | Book
| -- | -- | -- | -- |
| Professor Frisby Introduces Composable Functional JavaScript | Getting Started + How to + Explanation | JavaScript developers who want to use JavaScript | Online Course
| An Outsider's Guide to Statically Typed Functional Programming | Hook + Getting Started + How to + Explanation | JavaScript developers who want to learn Elm but are exposed to PureScript at end | Book
| -- | -- | -- | -- |
| Elm to PureScript Cheatsheet | Reference | Elm developers considering PureScript | GitHub Repo
| Differences of PureScript from Elm | Reference | Elm developers consider PureScript (or vice versa) | GitHub Gist
| Documentation Repo's "Differences from Haskell" | Reference | Haskell developers considering PureScript | Markdown file

Here's what has been added to the above since then:

| Name | Type | Audience | Medium |
| -- | -- | -- | -- |
| Real World App | How To Guide? Reference? | PureScript developers | Code Example
| MultiPac | Reference? | PureScript developers | Code Example
| PureScript: Jordan's Reference | Hook + Getting Started + How to + Explanation + Reference | New Learners | GitHub Repo
| A Guide to the PureScript Numeric Hierarchy | Explanation | New Learners | Read the Docs
| Make the Leap from JavaScript to PureScript | Getting Started + Explanation | Javascript developers | Blog Post series

Where is PureScript's documentation **lacking**?

By looking at what exists, we can see that the following types of documentation are lacking:
- Hooks
- How-To Guides
- Explanations

Additionally, the following PureScript websites either are outdated or could be modified to improve the documentation situation. Who can merge PRs into the websites' repositories and redeploy them once these PRs are merged?

| Site | Write Privilege | Deploy Privelege | Source
| -- | -- | -- | -- |
| PureScript language website | Core Contributors | None. GitHub Pages | -
| Pursuit | Core Contributors | Phil Freeman | [The State of Things, point 2](https://discourse.purescript.org/t/the-state-of-things/282)
| Try PureScript | Core Contributors | Phil Freeman | [The State of Things, point 2](https://discourse.purescript.org/t/the-state-of-things/282)


### How Should Programming Strategies be Documented?

Coming from an Object-Oriented Paradigm, some have asked, "Why aren't the best practices / design patterns / idioms in Functional Programming explained/documented?"

What are FP's "design patterns" / "idioms" / "best practices" ? How would you define them?

FP's "best practices" are
- hard to define
    - Are `monads` a design pattern?
    - Are `lenses` a design pattern?
    - What is not a design pattern?
- things people assume everyone does (so why explain them?)
    - Functions compose. Didn't people realize that type class X and Y are often used together?
    - I used a recursive data type to model a domain. How else would I model it?
- unconscious habits ("Oh! I didn't realize this was a 'design pattern.'")
    - I used a List zipper to efficiently update an item in the list. What else would I use?

FP languages tend to draw people who are intellectually curious. These people tend not to be good at explaining FP's benefits and concepts. Knowledge get stuck in "silos."

(Related interpretation section: [FP "best practices" are not well-defined, are assumed, or are unconscious habits](https://github.com/chexxor/purescript-documentation-discussion/blob/master/01-Sources-and-Interpretation/All-Interpretations.md#fp-best-practices-are-not-well-defined-are-assumed-or-are-unconscious-habits), [FP's culture creates "knowledge silos"](https://github.com/chexxor/purescript-documentation-discussion/blob/master/01-Sources-and-Interpretation/All-Interpretations.md#fps-culture-creates-knowledge-silos))


### Who is Writing PureScript's Documentation?

While developing the language, core contributors incurred a lot of responsibility (e.g. library maintenance, documentation updates, updating Pursuit and other related sites, etc.). Over time, they became spread thin and one even burned out. [further explained here]()

With the small amount of time they do have, they are focusing on maintaining the language and adding features, not improving the documentation. The language's development is steady (6-week release cycle) but slow. [further explained here]()

There are people other than core contributors who want to contribute to the documentation, but it seems some need help finding the right place to contribute. [further explained here]()


### How is Documentation Currently Generated?

Because the documentation is lacking, many are encouraged to ask their questions on the `#purescript` channel in the FP Slack. Many have greatly benefited from the quick answers they receive.

There are two issues with this approach:
1. Such answers cannot be easily found because they are hidden in a chatroom's length conversation.
2. These questions and their answers do not persist. After so much time, Slack will delete them.

Thus, people with the same already-answered questions can't find their answers. They ask the same questions and receive the same answers. This takes time away from other contributors and developers.

@chexxor has made some effort to address these issues by cross-posting such discussions in the Discourse forum. This accounts for the second issue.

However, the format is poor. One must read through a (sometimes) lengthy conversation to find the answer.
Contrast that with an StackOverflow question and answer that appears in a Google search.

(Related interpretation section: [PureScript's Mediums of Communication](https://github.com/chexxor/purescript-documentation-discussion/blob/master/01-Sources-and-Interpretation/All-Interpretations.md#purescripts-mediums-of-communication))


## Documentation Desired by Specific Audiences

### Core Contributors

Please answer the below questions.

To help with consistency, copy the below questions and paste them into your comment box. Then, give a reply.

```
> What can the community do to encourage/support you in 2019?



> What are your general goals for the language/ecosystem in 2019?



> What are not your goals for the language/ecosystem in 2019? (i.e. things you know need additional work, but just don't have a high enough priority right now)



> What processes that are not automated could be automated to save you time / lower the maintenance cost?



> What kind of help do you want from the community in 2019 (e.g. maintainership, documentation, conbtributions, etc.)?



> What kind of help do you not want from the community in 2019 (e.g. maintainership, documentation, conbtributions, etc.)?



> How much support are you willing to provide to those who want to help and in what form?

```

### New Learners

First, PureScript is mainly used for front-end work, not back-end work. While it is used for the back-end in some situations, most tend to use Haskell or another language, even if PureScript would be a better language in some situations. These languages already have mature libraries with people maintaining them. So, the incentives to improve this situation are not quite there.

Second, your language background affects how easy or hard it is to learn PureScript. There are likely other learning paths besides the ones covered below, but here's what we found in our research:

![Learner Paths "Learner Paths"](./learner-paths-to-ps.png)

| If your language background is... | ... then try these learning resources... | ... and these PureScript libraries |
| -- | -- | -- |
| JavaScript / OO languages | [Make the Leap from JavaScript to PureScript (Tutorial Series)](https://medium.com/@kelleyalex/index-make-the-leap-from-javascript-to-purescript-a1566d657e9c)<br><br>[An Outsider's Guide to Statically Typed Functional Programming (Book)](https://leanpub.com/outsidefp)<br><br>[Haskell: From First Principles](http://haskellbook.com/) | --
| Elm | [An Outsider's Guide to Statically Typed Functional Programming (Book)](https://leanpub.com/outsidefp) | --
| Haskell | [Introduction to PureScript (PDF)](http://code.adriansieber.com/adrian/adriansieber-com/src/branch/master/posts/_2018-11-01_introduction_to_purescript_for_haskell_developers/main.pdf)<br><br>[Differences from Haskell](https://github.com/purescript/documentation/blob/master/language/Differences-from-Haskell.md) | --


### Documentation Writers

TODO [link to the file that (in this situation) now stores the full 'What is Good documentation anyway' section]()


## Documentation Improvement

Our purpose is clear: improve the documentation situation.

In doing so, we should abide by these principles:
- Show, don't tell: prefer heavily-commented compile-and-play code examples over written explanations
- Start unofficial documentation efforts: allowing core contributors to implement breaking changes sooner means we'll get out of this situation sooner. Let's not slow them down by bugging them with documentation PRs.
- Don't recreate the wheel: look into helping existing efforts before you consider starting your own
- Adhere to Good Docs Guidelines: we'll all be better for it

The outcomes we are striving to reach have yet to be defined.

Please share your idea for _what_ we should achieve, and only then share your idea for _how_ to achieve it.

| Example Type | Comment | Explanation
| - | - | - |
| Bad | We should send documentation PRs to specific libraries | Answers 'how to do something' not 'the reality that will be true when we are finished.'
| Good | Goal: The top 30 dependencies used in PS' ecosystem have examples and counterexamples in all of their Pursuit docs.<br>How: Perhaps we use a single "ACME" spago project that has all packages in the ecosystem in it. For packages that are lacking docs or are maintained by core contributors who won't respond quickly, we could use spago to override those packages with a version that includes more documentation. Then, via `spago docs`, would could create a local copy that has the updated docs. | States a goal but does not determine how that could be achieved. But a few ideas quicly come to mind for how.

[Our ideas](https://github.com/chexxor/purescript-documentation-discussion/blob/664347273e3e640931ce8ee1c6559b79f5388b36/02-Context-or-Narrative/State-of-PS-Docs/State-of-PureScript-Documentation-2019.md#everyone-how-should-we-improve-this-situation)
