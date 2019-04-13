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

- [What is "Good" Documentation Anyway?](#what-is-good-documentation-anyway)
  - [The Types of Documentation](#the-types-of-documentation)
  - [The Documentation's Intended Audience](#the-documentations-intended-audience)
  - [Maintaining Documentation's Accuracy](#maintaining-documentations-accuracy)
    - [The "Size" of a Change](#the-size-of-a-change)
    - [The "Frequency" of a Change](#the-frequency-of-a-change)
    - [How to Make Maintenance Easier](#how-to-make-maintenance-easier)
  - [Criteria for "Good" Documentation](#criteria-for-good-documentation)
  - [Evaluating PureScript's Documentation](#evaluating-purescripts-documentation)
- [Why is PureScript's Documentation Lacking and How Do We Improve It?](#why-is-purescripts-documentation-lacking-and-how-do-we-improve-it)
- [New Learners: What is the Best Way to Learn PureScript?](#new-learners-what-is-the-best-way-to-learn-purescript)
- [PureScript Documentation Writers: What is the Best Way to Write Documentation in this Context?](#purescript-documentation-writers-what-is-the-best-way-to-write-documentation-in-this-context)
- [Core Contributors: ???](#core-contributors-)


## What is "Good" Documentation Anyway?

There are 5 types of documentation that target specific phases of a learner's experience (as explained in [What Nobody Tells You About Documentation](https://www.divio.com/blog/documentation/) and [Teach, Don't Tell](http://stevelosh.com/blog/2013/09/teach-dont-tell/))

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

Note: this section is sourced from only two blog posts, [What Nobody Tells You About Documentation](https://www.divio.com/blog/documentation/) and [Teach, Don't Tell](http://stevelosh.com/blog/2013/09/teach-dont-tell/). Understand these as a starting point for defining a criteria for "good" documentation, not a final "there's nothing more to say" conclusion.

### Evaluating PureScript's Documentation

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

## Why is PureScript's Documentation Lacking?

Here's the short version. Each paragraph will have a link that explains its summary in more detail.

It is difficult to define what are FP's "best practices / design patterns." The issues explained below are mostly situational; they will improve in time. However, this "best practices" issue is hard to address because it is subjective in nature, requires a lot of expertise, and requires a great communicator. [further explained here]()

PureScript is not _currently_ trying to be the next "mainstream language." Rather, it values "power" over "popularity" and so works towards those ends. [further explained here]()

While developing the language, core contributors incurred a lot of responsibility (e.g. library maintenance, documentation updates, updating Pursuit and other related sites, etc.). Over time, they became spread thin and one even burned out. [further explained here]()

Thus, they cannot quickly respond to most people's questions or contributions. With the small amount of time they do have, they are focusing on adding new language features, not improving the documentation situation. The language's development is steady (6-week release cycle) but slow. [further explained here]()

However, it seems they are (wisely) postponing "breaking changes" until all can be done at once. Otherwise, they will ~spend~ waste even more of their time updating the ecosystem to account for the breaking changes. There is also some disagreement about when those changes should be done. [further explained here]()

Due to the looming "breaking changes," those who want to improve the documentation situation are often discouraged from improving it. They tend to think, "Why invest many hours into something that will be outdated in a few months? Why not invest those hours into something else, like an interesting project or learning something new?" [further explained here]()

Fixing this situation is not as simple as it sounds. You can't "just delegate" their work to anyone. Others attempted to fund core contributors. However, the effort was likely stopped due to not having a clear idea of how the funds would be spent. [further explained here]()

Moreover, there are other factors independent of the "breaking changes" issues.
1. Until recently (it's fixed now), an OOM error was preventing some popular libraries from uploading their API docs. Even those familiar with the language had difficulty knowing how to use some libraries. [further explained here]()
2. The current support system doesn't build towards structured, persistent documentation. In some ways, it's like trying to get out of quicksand. [further explained here]()

### Some libraries cannot publish their docs due to OOM error

From [pulp version runs out of memory (fatal exception) - Issue 351](https://github.com/purescript-contrib/pulp/issues/351):
- Context: Bower is used to produce the "resolutions file" that the compiler expects
    - > The compiler expects a “resolutions file” in a similar format to the output of this problematic bower command. We only need a very small portion of the information produced by that command though; for each dependency, if the bower.json specifies anything other than a version range for it, we need to know so that we can produce a warning about that. Otherwise, we need to know which version bower’s solver picked. If I remember correctly that’s everything. Unfortunately I’m not aware of a more sensible variant of bower list which produces all the information we need. [comment in issue, paragraph 2](https://github.com/purescript-contrib/pulp/issues/351#issuecomment-395611759)
- Problem: Bower throws a `RangeError` when attempting to `JSON.stringify` an object that includes a massive dependency tree due to duplicate transitive dependencies:
    - > Bower builds a log object, which has our dependency tree. When they try to JSON.stringify this object, it throws RangeError: Invalid string length [comment in issue](https://github.com/purescript-contrib/pulp/issues/351#issuecomment-395605607)

The proposed solution: change the compiler's "resolution file" schema. Unfortunately, this is a breaking change (tracking issue: [Simplify `purs publish` resolution format](https://github.com/purescript/purescript/issues/3499)):
    - > To clarify, the course of action I'm suggesting is that we have `pulp` actually look through the filesystem and collect the resolutions data, and we then pass that information to the compiler. It would make our lives easier if we could also change the compiler so that it accepts this information using a more sensible schema than that of `bower list --offline --json` (and this is what I'm suggesting in that issue ([comment in issue](https://github.com/purescript-contrib/pulp/issues/351#issuecomment-450465708))).

Thus, a heavily-used library like `Halogen` cannot publish its `v4.0.0` or `v5.0.0` docs on Pursuit. Unfortunately, there's nothing they can do about it.

### The current support system doesn't build towards structured, persistent documentation

Because the documentation is lacking, many are encouraged to ask their questions on the `#purescript` channel in the FP Slack. Many have greatly benefited from the quick answers they receive.

There are two issues with this approach:
1. Such answers cannot be easily found because they are hidden in a chatroom's length conversation.
2. These questions and their answers do not persist. After so much time, Slack will delete them.

Thus, people with the same already-answered questions can't find their answers. They ask the same questions and receive the same answers. This takes time away from other contributors and developers.

@chexxor has made some effort to address these issues by cross-posting such discussions in the Discourse forum. This accounts for the second issue.

However, the format is poor. One must read through a (sometimes) lengthy conversation to find the answer.
Contrast that with an StackOverflow question and answer that appears in a Google search.

(Related interpretation section: [PureScript's Mediums of Communication](https://github.com/chexxor/purescript-documentation-discussion/blob/master/01-Sources-and-Interpretation/All-Interpretations.md#purescripts-mediums-of-communication))

### But Is There Hope? Yes!

This small change will address the FP Slack persistence issue:
- When a question on the `#purescript` Slack channel gets answered, request the person who asked it to post the question on StackOverflow and link to the question in the chatroom.
- Then, let someone (whether the answerer or someone who saw it) "answer" that question and give credit it to the answerer.

People are making an assumption that has not been tested. **Are all documentation efforts always affected by a breaking change?** I doubt it. Certainly there are some things that need better documentation which won't be affected by breaking changes. Why not identify what those are and start improving them?

Such efforts will likely need to be "unofficial." We (non-core-contributors / users of PS) do not want to steal time away from the core contributors by distracting them with documentation PRs. Let them focus on the language's development. Stabilizing the language sooner means an improved documentation situation sooner.

Rather, we (non-core-contributors / users of PS) can focus on answering questions like these:
- What are the libraries that need to have their documentation improved?
    - If documented, will breaking changes outdate such documentation?
    - How hard would it be to write a small code example that shows how to use them? For example
        - [Jordan's example for how to create a tree via `purescript-tree`](https://github.com/JordanMartinez/purescript-jordans-reference/blob/latestRelease/22-Projects/src/11-Table-of-Contents/04-Tree/01-Syntax.purs#L31-L64)
        - [Jordan's example of the "hello world" program via the ReaderT design pattern](https://github.com/JordanMartinez/purescript-jordans-reference/blob/latestRelease/21-Hello-World/08-Application-Structure/src/11-Hello-World/02-ReaderT.purs)
        - [Halogen's "basic button component" example](https://github.com/slamdata/purescript-halogen/blob/master/examples/basic/src/Button.purs)
- What are "best practices" for various topics/areas? For example:
    - Guidelines for writing a good bindings library
        - How should a library author analyze the library to which they want to write bindings?
        - What are common problems such people face and their possible solutions?
- What are some of the clearest explanations of FP concepts?
    - How hard is it to port their code examples to PureScript?
    - Have people written an explanation that "walks one through" an FP paper's ideas in a clear way?
- What are common solutions to build-related problems? Where is a centralized resource that can store all of these?
    - Integrating PureScript to work with JS build tools?
    - Integrating PureScript with CI (Travis, AppVeyor, etc.)?
    - Possible "tree-shaking" approaches to PureScript and their tradeoffs?

## New Learners: What is the Best Way to Learn PureScript?

First, PureScript is mainly used for front-end work, not back-end work. While it is used for the back-end in some situations, most tend to use Haskell or another language, even if PureScript would be a better language in some situations. These languages already have mature libraries with people maintaining them. So, the incentives to improve this situation are not quite there.

Second, your language background affects how easy or hard it is to learn PureScript. There are likely other learning paths besides the ones covered below, but here's what we found in our research:

![Learner Paths "Learner Paths"](./learner-paths-to-ps.png)

| If your language background is... | ... then try these learning resources... | ... and these PureScript libraries |
| -- | -- | -- |
| JavaScript / OO languages | [Make the Leap from JavaScript to PureScript (Tutorial Series)](https://medium.com/@kelleyalex/index-make-the-leap-from-javascript-to-purescript-a1566d657e9c)<br><br>[An Outsider's Guide to Statically Typed Functional Programming (Book)](https://leanpub.com/outsidefp)<br><br>[Haskell: From First Principles](http://haskellbook.com/) | --
| Elm | [An Outsider's Guide to Statically Typed Functional Programming (Book)](https://leanpub.com/outsidefp) | --
| Haskell | [Introduction to PureScript (PDF)](http://code.adriansieber.com/adrian/adriansieber-com/src/branch/master/posts/_2018-11-01_introduction_to_purescript_for_haskell_developers/main.pdf)<br><br>[Differences from Haskell](https://github.com/purescript/documentation/blob/master/language/Differences-from-Haskell.md) | --

## PureScript Documentation Writers: What is the Best Way to Write Documentation in this Context?

## Core Contributors: ???

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



The following
    - Evaluate PureScript's documentation using that criteria
    - Explain why PureScript's documentation is lacking and what is being done to improve it
    - Address various audience's possible concerns or questions centered on these themes:
        - New learners - How should I learn PureScript?
        - PureScript documentation writers - How should I write good maintainable documentation for others?
        - Core Contributors -

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
