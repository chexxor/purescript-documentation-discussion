# State of PureScript Documentation: 2019

This document is not meant to convince you to use PureScript, we assume that readers are already interested in it or using it.

It is well-known amongst the PureScript community that its documentation is lacking in some critical areas. As a result, @chexxor started the [PureScript documentation efforts in 2019](https://discourse.purescript.org/t/purescript-documentation-efforts-in-2019/524) Discourse thread to answer one question:
> How can we improve the PureScript documentation in 2019?

(Purpose) The following document tries to do three things:
1. Explain why documentation is currently lacking
2. Address specific audiences:
    - Core Contributors (Feedback): How should we support you in this context?
    - New Learners (Answers): What is the best way to learn PureScript in this context?
    - Documentation writers (Answers): How should I contribute documentation in this context?
3. Explore possible solutions to improving the documentation

## Why is PureScript's Documentation Lacking?

Here's the short version. Each paragraph will have a link that explains its summary in more detail.

PureScript is not _currently_ trying to be the next "mainstream language." Rather, it values "power" over "popularity" and so works towards those ends. [further explained here]()

While developing the language, core contributors incurred a lot of responsibility (e.g. library maintenance, documentation updates, updating Pursuit and other related sites, etc.). Over time, they became spread thin and one even burned out. [further explained here]()

Thus, they cannot quickly respond to most people's questions or contributions. With the small amount of time they do have, they are focusing on adding new language features, not improving the documentation situation. The language's development is steady (6-week release cycle) but slow. [further explained here]()

However, it seems they are (wisely) postponing "breaking changes" until all can be done at once. Otherwise, they will ~spend~ waste even more of their time updating the ecosystem to account for the breaking changes. There is also some disagreement about when those changes should be done. [further explained here]()

Due to the looming "breaking changes," those who want to improve the documentation situation are often discouraged from improving it. They tend to think, "Why invest many hours into something that will be outdated in a few months? Why not invest those hours into something else, like an interesting project or learning something new?" [further explained here]()

The following statement is not to blame people or point fingers. Rather, it summarizes our current reality:
> Core contributors are doing great and their pace is just fine. Still, we're in a sort of catch-22 situation. The longer the core contributors take to implement these breaking changes, the longer most documentation writers will wait to avoid unnecessary updates, and the longer we'll be in this situation.

Moreover, there are other factors independent of the "breaking changes" issues.
1. Until recently (it's fixed now), an OOM error was preventing some popular libraries from uploading their API docs. Even those familiar with the language had difficulty knowing how to use some libraries. [further explained here]()
2. The current support system doesn't build towards structured, persistent documentation. In some ways, it's like trying to get out of quicksand. [further explained here]()

Finally, it is difficult to define what are FP's "best practices / design patterns." This issue won't go away even if all 'breaking changes' have been implemented. [further explained here]()

Now, we'll address a few different audiences:
- Core Contributors - Feedback: Tell us how we can support you and when our 'help' is actually unhelpful
- New Learners - Answering your Question: What is the best way to learn PS in this situation?
- Documentation writers - Answering your Question: How should I write docs in this situation?
- Everyone - Brainstorming: How should we fix this situation?

## Core Contributors: How should we support you?

We consider you to be a 'core contributor' if you:
- have write access to the PureScript language or any of its websites (Pursuit, Try PureScript, etc.)
- have write access to `pulp`, `spago`, or any related build tools

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

## New Learners: What is the Best Way to Learn PureScript?

First, PureScript is mainly used for front-end work, not back-end work. While it is used for the back-end in some situations, most tend to use Haskell or another language, even if PureScript would be a better language in some situations. These languages already have mature libraries with people maintaining them. So, the incentives to improve this situation are not quite there.

Second, your language background affects how easy or hard it is to learn PureScript. There are likely other learning paths besides the ones covered below, but here's what we found in our research:

![Learner Paths "Learner Paths"](./learner-paths-to-ps.png)

| If your language background is... | ... then try these learning resources... | ... and these PureScript libraries |
| -- | -- | -- |
| JavaScript / OO languages | [Make the Leap from JavaScript to PureScript (Tutorial Series)](https://medium.com/@kelleyalex/index-make-the-leap-from-javascript-to-purescript-a1566d657e9c)<br><br>[An Outsider's Guide to Statically Typed Functional Programming (Book)](https://leanpub.com/outsidefp)<br><br>[Haskell: From First Principles](http://haskellbook.com/) | --
| Elm | [An Outsider's Guide to Statically Typed Functional Programming (Book)](https://leanpub.com/outsidefp) | --
| Haskell | [Introduction to PureScript (PDF)](http://code.adriansieber.com/adrian/adriansieber-com/src/branch/master/posts/_2018-11-01_introduction_to_purescript_for_haskell_developers/main.pdf)<br><br>[Differences from Haskell](https://github.com/purescript/documentation/blob/master/language/Differences-from-Haskell.md) | --

Third, we learned that there are [5 different types of documentation](). Each type addresses a different person at a different spot in their learning journey. To help you know how to navigate through the current PS documentation, we've tagged each of them with one of those types.

| Type | Audience | Name | Medium |
| -- | -- | -- | -- |
| Getting Started + How To + Explanation | New PS Learners | PureScript by Example | Book
| Hook + Getting Started + How to + Explanation + Reference | New Learners | PureScript: Jordan's Reference | GitHub Repo
| Getting Started + Explanation | New PS Learners | The Documentation Repository | GitHub Repo
| Getting Started + Explanation | New PS Learners | PureScript Resources | Read The Docs
| Reference | All PS developers | Pursuit | API Docs website
| Getting Started + How to + Explanation | JavaScript developers who want to use JavaScript | Professor Frisby Introduces Composable Functional JavaScript | Online Course
| Hook + Getting Started + How to + Explanation | JavaScript developers who want to learn Elm but are exposed to PureScript at end | An Outsider's Guide to Statically Typed Functional Programming | Book
| How To + Explanation | Intermediate PS Learners | Lens for the Mere Mortal: PureScript Edition | Book
| Reference | Elm developers considering PureScript | Elm to PureScript Cheatsheet | GitHub Repo
| Reference | Elm developers consider PureScript (or vice versa) | Differences of PureScript from Elm | GitHub Gist
| Reference | Haskell developers considering PureScript | Documentation Repo's "Differences from Haskell" | Markdown file
| How To Guide? Reference? | PureScript developers | Real World App | Code Example
| Reference? | PureScript developers | MultiPac | Code Example
| Explanation | New Learners | A Guide to the PureScript Numeric Hierarchy | Read the Docs
| Getting Started + Explanation | Javascript developers | Make the Leap from JavaScript to PureScript | Blog Post series

## PureScript Documentation Writers: What is the Best Way to Write Documentation in this Context?

See [Guidelines for Good Docs]()

## Everyone: How should we improve this situation?

Our purpose is clear: improve the documentation situation

In doing so, we should abide by these principles:
- **Show, don't tell**: prefer heavily-commented compile-and-play code examples over written explanations
- **Start unofficial documentation efforts**: allowing core contributors to implement breaking changes sooner means we'll get out of this situation sooner. Let's not slow them down by bugging them with documentation PRs.
- **Don't recreate the wheel**: look into helping existing efforts before you consider starting your own
-  **Adhere to Good Docs Guidelines**: we'll all be better for it

The outcomes we are striving to reach have yet to be defined.

We'll share ours soon, but we'd like your help.

Please share your idea for _what_ we should achieve, and only then share your idea for _how_ to achieve it.

| Example Type | Comment | Explanation
| - | - | - |
| Bad | We should send documentation PRs to specific libraries | Answers 'how to do something' not 'the reality that will be true when we are finished.'
| Good | Goal: The top 30 dependencies used in PS' ecosystem have examples and counterexamples in all of their Pursuit docs.<br>How: Perhaps we use a single "ACME" spago project that has all packages in the ecosystem in it. For packages that are lacking docs or are maintained by core contributors who won't respond quickly, we could use spago to override those packages with a version that includes more documentation. Then, via `spago docs`, would could create a local copy that has the updated docs. | States a goal but does not determine how that could be achieved. But a few ideas quicly come to mind for how.

### Idea for improving packages' documentations when they are maintained by core contributors

Purpose: allow anyone to update a package's documentation without taking time away from core contributors

Goal: The top 30 libraries used in PS' ecosystem have examples and counterexamples in all of their Pursuit docs.

How:
- We create a single community-wide "ACME" Spago project that has all packages in the ecosystem in it. This project is used solely for documentation, not as an actual package set.
- Anyone who wants to add documentation for a project (like one maintained by core contributors) can make make their own fork of the library, add the changes, and override the ACME's package set's entry for that package to use their version that includes the updated docs
- Anyone can clone the Spago project and generate local documentation that has the additional documentation via `spago docs`.
- Core contributors can later add the documentation to the original version at a later time.

### Idea for dealing with improving the current support system

Purpose: To get easily findable answers via Google in a well-presented format on SO

Goal: all Slack-based code-related questions and answers are "copied" to StackOverflow

How:
- When a question on the `#purescript` Slack channel gets posted, request the person who asked it to post the question on StackOverflow and link to the question in the chatroom.
- The question gets answered.
- Let someone (whether the answerer or someone who saw it) "answer" the corresponding StackOverflow question with the answer and give credit to the original answerer.

### Idea for documenting things that aren't affected by breaking changes

Context: people are making an assumption that has not been tested. **Are all documentation efforts always affected by a breaking change?** I doubt it. Certainly there are some things that need better documentation which won't be affected by breaking changes. Why not identify what those are and start improving them?

Purpose: to document things that aren't affected by breaking changes

Goal: How-to guides / best practices guides on various topics have been written

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