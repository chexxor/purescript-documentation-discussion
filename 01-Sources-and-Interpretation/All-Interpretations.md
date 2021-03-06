Table of Contents
<!-- https://imthenachoman.github.io/nGitHubTOC/ -->
  - [Preface](#preface)
  - [What is Good Documentation?](#what-is-good-documentation)
    - [Purpose of Documentation](#purpose-of-documentation)
    - [Types of Documentation](#types-of-documentation)
      - [Inline with Code](#inline-with-code)
      - [Apart from Code](#apart-from-code)
        - [Long-form Essays](#long-form-essays)
    - [Code Examples are better than Written Explanations](#code-examples-are-better-than-written-explanations)
    - [Concerns relating to the order of information presented](#concerns-relating-to-the-order-of-information-presented)
    - [Centralized vs Decentralized Docs](#centralized-vs-decentralized-docs)
    - [How and why documentation becomes outdated](#how-and-why-documentation-becomes-outdated)
    - [Why don't developers write good documentation more often?](#why-dont-developers-write-good-documentation-more-often)
    - [Documentation does not replace 'true learning by doing'](#documentation-does-not-replace-true-learning-by-doing)
    - [How to teach someone something new](#how-to-teach-someone-something-new)
  - [Code as Examples Referenced in Discussions](#code-as-examples-referenced-in-discussions)
  - [Comparing Elm, PureScript, and Haskell: which language do I use?](#comparing-elm-purescript-and-haskell-which-language-do-i-use)
    - [General Statements](#general-statements)
    - [Specific statements about the langauges](#specific-statements-about-the-langauges)
    - [Arguments For PS](#arguments-for-ps)
      - [Compared to Elm](#compared-to-elm)
        - [Language is not bottlenecked/controlled by beneficial dictator](#language-is-not-bottleneckedcontrolled-by-beneficial-dictator)
        - [Better FFI Experiencee](#better-ffi-experiencee)
        - [PS has a more powerful type system (i.e. Type Classes)](#ps-has-a-more-powerful-type-system-ie-type-classes)
      - [Compared to Haskell](#compared-to-haskell)
        - [Easier setup process](#easier-setup-process)
        - [Less fragmented ecosystem](#less-fragmented-ecosystem)
        - [Removes some of Haskell's baggage](#removes-some-of-haskells-baggage)
        - [Provides better integration with JS ecosystem](#provides-better-integration-with-js-ecosystem)
        - [Miscellaneous](#miscellaneous)
    - [Comments specifically in favor of PS](#comments-specifically-in-favor-of-ps)
      - [Good for Front-End Applications](#good-for-front-end-applications)
      - [High Long-Term Potential](#high-long-term-potential)
      - [Easy Setup Process / Good Build Tools](#easy-setup-process--good-build-tools)
      - [Miscellaneous](#miscellaneous-1)
    - [Arguments Against using PS](#arguments-against-using-ps)
      - [Compared to Haskell](#compared-to-haskell-1)
      - [Compared to Elm](#compared-to-elm-1)
        - [Elm is easier to learn for JS developers due to a less-powerful / simpler type system](#elm-is-easier-to-learn-for-js-developers-due-to-a-less-powerful--simpler-type-system)
        - [Elm has an easy-to-understand Application Structure](#elm-has-an-easy-to-understand-application-structure)
        - [Elm has really great compiler errors](#elm-has-really-great-compiler-errors)
      - [Comments specifically against PS / for alternatives](#comments-specifically-against-ps--for-alternatives)
        - [Regarding OCaml / ReasonML / BuckleScript as an alternative](#regarding-ocaml--reasonml--bucklescript-as-an-alternative)
        - [Miscellaneous](#miscellaneous-2)
    - [Arguments against using OCaml / ReasonML / BuckleScript?](#arguments-against-using-ocaml--reasonml--bucklescript)
  - [Various "Learning Paths" to reach PureScript](#various-learning-paths-to-reach-purescript)
    - [From Nothing](#from-nothing)
    - [From JavaScript](#from-javascript)
    - [From Elm](#from-elm)
    - [From Haskell](#from-haskell)
    - [No Category](#no-category)
  - [Ideas for how to improve PS Docs](#ideas-for-how-to-improve-ps-docs)
    - [Things that need to be fixed](#things-that-need-to-be-fixed)
    - [Things that can be improved or better communicated](#things-that-can-be-improved-or-better-communicated)
    - [Providing Code Examples in Other Languages](#providing-code-examples-in-other-languages)
  - [Problems New Learners Face when Learning PS](#problems-new-learners-face-when-learning-ps)
    - [Baggage Learners Bring with Them](#baggage-learners-bring-with-them)
    - [Difficulty in understanding PureScript's Syntax](#difficulty-in-understanding-purescripts-syntax)
    - [Difficulty in understanding how to do X in PureScript](#difficulty-in-understanding-how-to-do-x-in-purescript)
    - [Miscellaneous](#miscellaneous-3)
  - [Ways to Improve New Learner Experience](#ways-to-improve-new-learner-experience)
    - [Clarify whether learning materials are up-to-date or not](#clarify-whether-learning-materials-are-up-to-date-or-not)
    - [Better explain how to use/write FFI](#better-explain-how-to-usewrite-ffi)
    - [Use Library Badges to indicate compiler compatibility](#use-library-badges-to-indicate-compiler-compatibility)
    - [Make Pursuit more 'beginner-friendly'](#make-pursuit-more-beginner-friendly)
    - [Provide Examples of Code Solving Some Problem](#provide-examples-of-code-solving-some-problem)
    - [Improve Compiler Error Messages](#improve-compiler-error-messages)
    - [Explain how PS integrates with other web build tools](#explain-how-ps-integrates-with-other-web-build-tools)
    - [Miscellaneous](#miscellaneous-4)
  - [PureScript's Mediums of Communication](#purescripts-mediums-of-communication)
    - [GitHub Issue Tracker](#github-issue-tracker)
    - [Slack](#slack)
    - [Discourse Forum](#discourse-forum)
    - [Things relating to Slack and Discourse mediums](#things-relating-to-slack-and-discourse-mediums)
    - [Inactive Mediums](#inactive-mediums)
  - [Why Previous Documentation Efforts Failed](#why-previous-documentation-efforts-failed)
    - [FP "Best Practices" are not well-defined, are assumed, or are unconscious habits](#fp-best-practices-are-not-well-defined-are-assumed-or-are-unconscious-habits)
    - [FP's Culture Creates "Knowledge Silos"](#fps-culture-creates-knowledge-silos)
    - [No well-defined criteria for which libraries count as 'core' libraries and ensuring their documentation is good/up-to-date](#no-well-defined-criteria-for-which-libraries-count-as-core-libraries-and-ensuring-their-documentation-is-goodup-to-date)
    - [Reviewing Documentation PRs can be just as difficult as code PRs](#reviewing-documentation-prs-can-be-just-as-difficult-as-code-prs)
    - [Limited Manpower / Not Enough Automation](#limited-manpower--not-enough-automation)
    - [Slow submitted-reviewed-merged timeline of documentation PRs kills documentation momentum](#slow-submitted-reviewed-merged-timeline-of-documentation-prs-kills-documentation-momentum)
    - [Knowing whom to trust with write access, defining best workflow procedures, and providing necessary support](#knowing-whom-to-trust-with-write-access-defining-best-workflow-procedures-and-providing-necessary-support)
    - [Core contributors have not provided, nor known about, the desired support that 'unofficial' documentation efforts wanted/expected](#core-contributors-have-not-provided-nor-known-about-the-desired-support-that-unofficial-documentation-efforts-wantedexpected)
    - [Breaking Changes Renders Documentation Outdated](#breaking-changes-renders-documentation-outdated)
    - [Lack of a clearly-defined community-wide mutually-held vision/goal](#lack-of-a-clearly-defined-community-wide-mutually-held-visiongoal)
    - [Miscellaneous](#miscellaneous-5)
  - [Why a "v1.0" PureScript release has not been made](#why-a-v10-purescript-release-has-not-been-made)
    - [Lack of a clearly-defined core-contributor-wide mutually-held language specification](#lack-of-a-clearly-defined-core-contributor-wide-mutually-held-language-specification)
    - [Keeping the motto of `Avoid "success at all costs"` and understanding its meaning](#keeping-the-motto-of-avoid-success-at-all-costs-and-understanding-its-meaning)
    - [Fear that people will misinterpret a "v1.0" compiler release for a "v1.0" ecosystem release](#fear-that-people-will-misinterpret-a-v10-compiler-release-for-a-v10-ecosystem-release)
  - [Things that have changed since 'The State of Things'](#things-that-have-changed-since-the-state-of-things)
  - [Unanswered Questions](#unanswered-questions)
  - [Things relating to breaking changes](#things-relating-to-breaking-changes)
    - [Compiler-Library-Ecosystem Things](#compiler-library-ecosystem-things)
    - [Dependency Managers](#dependency-managers)
    - [Communicating Changes in the Ecosystem](#communicating-changes-in-the-ecosystem)
  - [Unused Interpretations](#unused-interpretations)

## Preface

The following interpretations have been copied over from various sources. In some situations, they have been further edited or clarified when their meaning was not clear when read in isolation from other things. The bracketed content `[example_slug_name]` refers to the unqiue slug name of a source, defined in the Index.md file, so you can see the full context of that interpretation.

<hr>

## What is Good Documentation?

### Purpose of Documentation

- One person believes that documentation is the foundation of user experience. [Discussion_about_WNTYAD]
- Lack of documentation feels like a form of hazing [Discussion_about_WNTYAD]
- Being able to ask a good question presupposes an understanding of the domain / library / language. [Discussion_about_WNTYAD]
- One documentation writer believes his readers prefer to be one-on-one guided through their questions than to read documentation. This implies that his readers prefer personalized explanations than impersonal ones. [Discussion_about_WNTYAD]
- Documentation is really a way of thinking about design, but often done after the code has already been written according to some other design. [Discussion_about_WNTYAD]

### Types of Documentation

- In reality, there are more than 4 different types of documentation. Let's think of the many dimensions: [Discussion_about_WNTYAD]
    - The 4 normal types (intended audience based on goal): get started, how to do one thing, reference, explanation
    - The X audiences based on background / purpose (new core developers, plug-in developers, distributors, end-users).
- Putting the above idea [(i.e. 4 types of docs & total number of audiences based on background/purpose: core developers, plug-in developers, distributors, and end-users)] into terms of PS: [Discussion_about_WNTYAD]
    - audience based on background: Javascript, Haskell, Elm, TypeScript, other language entirely
    - audience based on purpose: front-end or back-end, each with these concerns (performance, complex logic, hitting quick deadline, migrating to better system, refactor-heavy due to prototypal nature)

#### Inline with Code

- Reading the Tests' code is not the same as reading documentation: **it's only useful once you already know how to use the code.** [Teach Don't Tell]

#### Apart from Code

- Using literate programming tools don't help. [Teach Don't Tell]

##### Long-form Essays

Wiki

- Using wikis as a way to document things are horrible because: [Teach Don't Tell]
    1. there is no coherent voice (multiple authors that often times fight/correct one another)
    2. it allows the excuse, "If you don't understand it yourself, you can write the content and fix it!"
    3. there is no version control (even GitHub wikis aren't good for this since they are separate from the project/code)
    - (Critique: This presumes a single person is writing the entire documentation. Larger projects don't have this luxury.)

- There are 4 types of documentation: 1st contact, the black triangle, the hairball, the reference [Teach Don't Tell]
    - First Contact (type of documentation) [Teach Don't Tell]
        - Basically, a "high-level overview and purpose statement"
        - Answers questions like "What is this thing, why would I care about it, why would I not care about it, and why is it worth my effort to learn how to use it?"
    - Black Triangle (type of documentation) [Teach Don't Tell]
        - Basically a "getting started guide"
        - If it's up-to-date, then the reader knows the library/code isn't stale or out-of-date
        - It doesn't teach everything someone needs to know, just enough to start being productive. For example, a guitar teacher teaches enough chords to play a song, not all possible chords at once before ever starting.
    - Hairball (type of documentation) [Teach Don't Tell]
        - Basically, the "explanation" part of docs

- Getting Started guides that do not distract with other important but not relevant-at-the-time matters are what new learners want [Discussion_about_WNTYAD]
- good documentation might just cover the 'basic idea' well and how to get started [Discussion_about_WNTYAD]
- Documentation should focus first on helping people solve real problems with practical bottom-up documentation. The theoretical top-down stuff can come later on once they realize the value of the abstraction. [Why_is_Elm_More_Popular_Than_PureScript]
- One person believes the difference between context and reference documentation is small, because "context" is wide umbrella. [Discussion_about_WNTYAD]

- Knowledge can at best be encoded into views that we call 'documentation.' Documentation is 'good' when one's view happens to correlate with what they need to 'see' at a given time. However, due to how 'views' work, they must explain the same concepts in different orders, show some content rather than other content based on what the reader needs, etc. [Discussion_about_WNTYAD]
- StackOverflow is its own form of documentation [Discussion_about_WNTYAD]
- Visual flow charts that adhere to the code might replace documentation...? One thought that comes to mind is [Teaching New Tricks to Old Programs](https://www.youtube.com/watch?v=vzLK_xE9Zy8&index=3&list=LL0RItGq_oLk-fvqppBpwtew&t=0s) which could literally visualize a program (see 34:00 and onward) [Discussion_about_WNTYAD]


### Code Examples are better than Written Explanations

- Examples of code are easier to maintain and are often better than some blog posts on the same matter. [Discussion_about_WNTYAD]
- (duplicate) working code examples are sometimes better than actual written content. [Discussion_about_WNTYAD]
- Examples speak clearer than documentation [Discussion_about_WNTYAD]
- Providing working examples of code that show how to properly use some subset of an API is better than making someone read through that API and figure out how to piece them together. (In some cases, this is not necessarliy true for PS because the type signatures are designed so that two functions work together) [Discussion_about_WNTYAD]
- While one can have code examples without written documentation, one cannot have written documentation without code examples. [Discussion_about_WNTYAD]
- Author could not find complex examples that helped author troubleshoot issues. [Exploring_the_MVI_Architecture_with_PureScript_Puzzler]

### Concerns relating to the order of information presented

- One person believes that an important aspect of the purpose of a piece of documentation is the order in which it presents information and references to related reading. [Discussion_about_WNTYAD]
- Part of the issue of documentation is the cultural aspects of it: the authors need to know effective ways of presenting information. [Discussion_about_WNTYAD]
- One person believes the presentation of various types of documentation is so different that there isn't value in working to normalize knowledge. [Discussion_about_WNTYAD]

### Centralized vs Decentralized Docs

- Having documentation in a centralized place is not what's important. Rather, the ease with which one navigates throughout an ecosystem's documentation is important. If the documentation can answer questions like "Does the user know where to find X knowledge given that they now/already know Y, and can they easily get there?" [Discussion_about_WNTYAD]
- One person believes that duplication of knowledge/communication in documentation produces fewer problems than having a normalized/de-duplicated documentation format. [Discussion_about_WNTYAD]
- One person believes it's natural to attempt to organize a documentation project in a piece-wise taxonomic way and generating the audience-facing documentation using templates. [Discussion_about_WNTYAD]
- 4 types are boundaries that are kept within the content of each type. One can still store them in the same overall project as long as there is a clear boundary between them. [Discussion_about_WNTYAD]
- One person believes it's useful to link between types of documentation. [Discussion_about_WNTYAD]

### How and why documentation becomes outdated

- Documentation, by nature, goes out of sync quickly because the code it documents changes. [Discussion_about_WNTYAD]
- Of the 4 types, 2 quickly go stale after 1 year and need updating [Discussion_about_WNTYAD]
- One person believes that documentation becomes less effective when it is refactored as a program is refactored. [Discussion_about_WNTYAD]
- One person believes that of all purposes of documentation, there are only two purposes that are maintainable and useful long-term: [Discussion_about_WNTYAD]
    - Documentation of functionality
    - Getting started tutorials
- closely integrated documentation is harder to maintain [Discussion_about_WNTYAD]
- loosely integrated documentation is easier to maintain [Discussion_about_WNTYAD]
- There is a huge list of things that can make documentation go out of date. Perhaps this is the real issue behind why no one wants to write documentation. Thus, it's worth asking which medium of documentation is easier to 'update' when they change or which is less vulnerable to such changes. [Discussion_about_WNTYAD]
- The last part of the issue of documentation is finding good ways to automate tedious tasks. [Discussion_about_WNTYAD]
- Documentation that explains things broadly and is less tied down to a specific version of some code tends to remain up-to-date longest. [Discussion_about_WNTYAD]
- The number of possible audiences complicates up-to-date documentation significantly. [Discussion_about_WNTYAD]
- One person writes documentation and finds users don't consult documentation even when they know they should. [Discussion_about_WNTYAD]

### Why don't developers write good documentation more often?

Writer-audience mismatch:

- People who write such guides might struggle to know what to include and exclude because they know what the trade-offs are. [Discussion_about_WNTYAD]
- Sometimes there is intent to write but not knowing what to say is the wall people hit right before giving up. [Discussion_about_WNTYAD]
- It's hard to write some documentation without a good problem to solve. Thinking of such problems is hard but very easy when someone else comes to you with one. [Discussion_about_WNTYAD]
- What you think is 'good' documentation is never 'good enough' in someone else's eyes. [Discussion_about_WNTYAD]
- Some writers get stopped at, "When is 'self-documenting' code via type signatures and the entity's name good enough and when should it be documented?" [Discussion_about_WNTYAD]
- Some developers might think "It's obvious what this code does. Why does it need documentation?" simply because they aren't looking at this with 'never seen it before' eyes. [Discussion_about_WNTYAD]

Not self-beneficial, hard work:

- Writing documentation isn't "fun", doesn't add new features / fix bugs, and doesn't use skills that a programming job requires [Discussion_about_WNTYAD]
- Writing documentation (for 3 of 4 types) is useless to the writer as long as the writer already knows it. [Discussion_about_WNTYAD]
- What's the point in writing documentation if you know that an upcoming breaking change will make it outdated? [Discussion_about_WNTYAD]
- Documentation of some code might require consulting 4 different developers to make an accurate change [Discussion_about_WNTYAD]
- One person believes that writing programs provides different rewards than writing documentation. This implies the two types of writing require two different personalities. [Discussion_about_WNTYAD]

Not a programmer responsibility:

- A good programmer does not need to be great at typing or other skills required for writing good docs. [Discussion_about_WNTYAD]
- Businesses do not give programmers an incentive to write documentation [Discussion_about_WNTYAD]
- (Duplicate) Businesses do not give programmers an incentive to write documentation [Discussion_about_WNTYAD]
- There's no "compiler error" (or other forms of compiler support that push the programmer towards doing things the 'right way') for writing documentation [Discussion_about_WNTYAD]
    - If the concept "your code is documented or it fails to compile" could be enforced, this would address this issue [Discussion_about_WNTYAD]
    - (duplicate) Making the build fail unless documentation is added could help documentation purposes [Discussion_about_WNTYAD]
- The next part of the issue of documentation is finding people who can write good documentation. [Discussion_about_WNTYAD]

### Documentation does not replace 'true learning by doing'

- This could reflect how people learn a human language - they learn by using it while socializing with other people. [Discussion_about_WNTYAD]
- True learning sometimes requires the person to actually figure things out for themselves. [Discussion_about_WNTYAD]
- Writing new docs or improving old ones is a good way to get started with a language. [The_State_of_Things]

### How to teach someone something new

- Recommended approach to teaching something new to a person [Teach Don't Tell]
    1. Figure out what they already know. (identity start point)
    2. Figure out what you want them to know after you finish. (identity end point)
    3. Figure out a single idea or concept that will move state 1 a little bit closer to state 2. (figure out path)
    4. Nudge the student in the direction of that idea. (instruct/guide using path)
    5. Repeat until state 1 becomes state 2.


## Code as Examples Referenced in Discussions

- The simple demo, `star-dodge-clone`, still assumes too much advanced background info for a new learner to understand it. People think 'simple' demos (like that above) don't require that much understanding. The "simple" demo above uses the following language features: [Elm_PureScript_In_Depth_Overview]
    - the `Eff` monad
    - a Graphics library
    - symbolic functions (e.g. `<$>` instead of `map`)
    - implicit monadic functions via the `<-` bind syntax
    - Type Classes
    - Type Aliases
    - algebraic data types
    - records and their accessor syntax
    - value assignments via `let`
    - FFI
    - pattern matching
    - pattern guards

## Comparing Elm, PureScript, and Haskell: which language do I use?

### General Statements

- The target / purpose for learning FP language should be the controlling factor. [Learn_PureScript_or_Haskell_First]
- Good summary of the learning curves of these languages: Elm is lowest, PS is next, Haskell is highest. [Learn_PureScript_or_Haskell_First]
- Learning one language or another does not matter since the type classes and general foundations apply equally to all of them. [Learn_PureScript_or_Haskell_First]
- PureScript is a more powerful language than Elm but provides less guidances as to how to write code [Elm_019_Broke_Us]
- Once the core ideas behind FP languages are learned, one can switch between them relatively easily. [Why_is_Elm_More_Popular_Than_PureScript]

### Specific statements about the langauges

- If one wants to do FP web development and get the full power of FP languages and is willing to pay the cost of a steeper learning curve, then they should start with PureScript. Still, this learning curve could be made less steep if there was more beginner-friendly documentation. [Learn_PureScript_or_Haskell_First]
- "PureScript focuses on Web, Haskell is more general, but in case you're only interested in playing with a functional language, I'd pick PureScript for that." [Learn_PureScript_or_Haskell_First]
- Good summary of the differences between Elm and PS' handling of partial functions: "Elm strive to be total and prevent you from shooting yourself in the foot in any way, while Purescript gives you more freedom, but you have to understand the consequences of what you’re doing." [Elm_PureScript_In_Depth_Overview]askell and Purescript, which one is easier to learn since both use the same concepts that translate easily between both languages (e.g. type classes, Functor, etc.)?" [Learn_PureScript_or_Haskell_First]
- One person believes that many people choose a language not based on what it *can* do, but based on what it *prevents* you from doing, because most people just want to avoid nightmare codebases. [Why_is_Elm_More_Popular_Than_PureScript]
- One person believes that PureScript is the right choice for people who want to use a general purpose Haskell-like language for web programming. [Why_is_Elm_More_Popular_Than_PureScript]
- One will be more productive overall in languages that have more mature ecosystem and active communities. However, if one wants to specifically do web programming and not use Haskell's solutions to that problem and needs something more powerful than Elm, then one seems limited to Purescript, Elixir, or Closure. [Learn_PureScript_or_Haskell_First]
- A number of usability issues (REPL slows to a crawl with 10+ packages; bower as package management with psc-package still a WIP) stopped one commentator from continuing choosing PS over Haskell as a language to learn FP. [Learn_PureScript_or_Haskell_First]
    - Addressing this comment, some have been resolved whereas some others have not. AFAIK, the REPL no longer responds that slowly. `psc-package` is that stack-like alternative mentioned above that is become more established. Moreover, `spago` addresses some of its shortcomings due to the tedious nature of modifying packaget sets. However, `spago` does not yet have as much support in various things as `psc-package`.
- A newcomer believes the PureScript community is friendly to beginners and contributors. [Elm_019_Broke_Us]
- Source believes that PureScript leaders do not care about documentation/standards/infrastructure of PS. The "leaders" are never defined here, but it probably refers to the core contributors. [Elm_019_Broke_Us]
- While PS can be used on the back-end, it's likely not as performant than other solutions because of the virtualization layers. Thus, it's likely only for the front-end [Why_is_Elm_More_Popular_Than_PureScript]
- Comparing Elm and PureScript is like comparing apples and oranges. Just realize that each language is a tool that better suits some people's use cases and preferences than others and leave it at that. People should know what the design decisions are and their tradeoffs and be able to make an informed decision. [Why_is_Elm_More_Popular_Than_PureScript]
- One person thought there really weren't any cons to PS, just some situations where it's not "ideal". For example, if you want lazy evaluation by default, PureScript is not ideal for you. [Why_use_Purescript]
- Haskellers will likely be unsatisfied with either language at some point because neither of them are Haskell. [Why_is_Elm_More_Popular_Than_PureScript]

### Arguments For PS

#### Compared to Elm

##### Language is not bottlenecked/controlled by beneficial dictator

- A PureScript user prefers PureScript over Elm because they don't like a language which dogmatically enforces a certain way of programming. [Hitchhikers_Guide_to_Elm]

##### Better FFI Experiencee

- A PureScript user believes PureScript's FFI is simpler than Elm. [Hitchhikers_Guide_to_Elm]
- A JavaScript/React/PureScript user believes PureScript's FFI is fairly easy and is better than ReasonML's and Elm's FFI. [Hitchhikers_Guide_to_Elm]
- A PureScript user believes PureScript compiles to smaller amounts of JS than Elm for the same thing, making pages load faster than Elm-written ones. [Hitchhikers_Guide_to_Elm]
- A PureScript user believes that using it is dead-simple because it compiles to JavaScript (because it is readable?). [Hitchhikers_Guide_to_Elm]

##### PS has a more powerful type system (i.e. Type Classes)

- A PureScript user believes that a language can limit what you can do and learn, and is reason for leaving the language. [Hitchhikers_Guide_to_Elm]
- A PureScript user feels limited by Elm's type system. [Hitchhikers_Guide_to_Elm]
- PS has type classes whereas Elm does not: one reason why one might want to use PS instead of Elm. [Elm_PureScript_In_Depth_Overview]
- PS is more precise and powerful at a lower level than Elm. [Elm_PureScript_In_Depth_Overview]
- Elm is a not a bad 'first step' but one quickly realizes its limitations when someone tries to do something outside of its intended scope. [Author_Venting_About_Book]
- 50k app and the "abstraction ceiling" has not been hit yet. App does require a lot of boilerplate-y code, but it works and solves the business problem at the end of the day. [Why_is_Elm_More_Popular_Than_PureScript]
- Haskellers who know of better abstractions were restricted by Elm's lack of features. Moreover, Elm did not allow their hacks to work, or at least not work long. [Why_is_Elm_More_Popular_Than_PureScript]
- Haskellers who already knew of better abstractions did not have trouble migrating to PS and experience the benefit quickly. [Why_is_Elm_More_Popular_Than_PureScript]
- Elm was needlessly bombarded by Haskellers who wanted a more powerful Elm, which conflicted with Elm's design goals/philosophy. PS, which did have those goals, met these needs/desires well. [Why_is_Elm_More_Popular_Than_PureScript]
- Haskellers should not use Elm because they will find it too limiting. Rather, they should use PS. [Why_is_Elm_More_Popular_Than_PureScript]

#### Compared to Haskell

##### Easier setup process

- Using PureScript was more fun than the hassle when compared to the commentator's experience with Haskell. [Learn_PureScript_or_Haskell_First]
- In short, in this person's experience, PureScript is easy to set up and start coding unlike Haskell in various ways [Learn_PureScript_or_Haskell_First]
- PureScript doesn't require adding language extensions like "OverloadedStrings" or running it with `-Wall` [Learn_PureScript_or_Haskell_First]
- While this person argues that it's generally easier to install and maintain PS than Haskell on a machine, that comment did not account for the major breaking changes that occurred in the `0.12.0` release. Other comments in this post also argue against this point. [Learn_PureScript_or_Haskell_First]

##### Less fragmented ecosystem

- Haskell user prefers and welcomed non-fragmented dependency managers. [PureScript_First_Impressions]
- Haskell user prefers and welcomed a centralized documentation site [PureScript_First_Impressions]

##### Removes some of Haskell's baggage

- PS' type system is more granular, powerful, and polished than Haskell, avoiding some of its baggage. [Learn_PureScript_or_Haskell_First]
- PS seems to be trying to remove the baggage that Haskell continues to carry, but it is not explicitly trying to replace/improve it. [Why_is_Elm_More_Popular_Than_PureScript]

##### Provides better integration with JS ecosystem

- PureScript has better integration with JS build tools (e.g. webpack, parcel, etc.) than Haskell [Learn_PureScript_or_Haskell_First]
- Switching to GHCJS isn't the same idea as a "Haskell-to-JS" compiler. GHCJS includes the entire Haskell compiler in JS (probably slows down a site's load time significantly) and is designed for whole-system apps. PS has no runtime requirement and can be used like a pocket knife: a solution to a whole-system app, a simple library, a small part of some current system that integrates well, etc. [Why_is_Elm_More_Popular_Than_PureScript]

##### Miscellaneous

- To one person, Haskell's community seems less friendly / welcoming than other languages' communities in general and the Purescript community specifically. [Learn_PureScript_or_Haskell_First]
- The PureScript core contributor believes that "the Haskell tradition" is having the purpose to explore FP languages, their implementations, and their practices. [Wallowing_in_Despair]

### Comments specifically in favor of PS

#### Good for Front-End Applications

- A PureScript user believes that PureScript is good for solid development of frontend applications. [Hitchhikers_Guide_to_Elm]
- FP programmer wanted a better solution for web dev and implemented such a solution. [Why_is_Elm_More_Popular_Than_PureScript]

#### High Long-Term Potential

- PS' long-term value is that the language can compile to multiple backends quite easily. Still, the exact performance considerations are not as clear as one library maintainer realized when writing [Learn_PureScript_or_Haskell_First]
- PS has companies behind it to some degree that guarantees it will be worth knowing for next few years, but who can see beyond that, especially when the web changes faster than many other contexts.

#### Easy Setup Process / Good Build Tools

- "the install and setup of the environment is straight forward." [My_Experience_With_PureScript_So_Far]
- build tools supporting fast feedback loops make developers more productive [My_Experience_With_PureScript_So_Far]
- `pulp` was simple to set up things [PureScript_First_Impressions]
- PS has great out-of-box support for Atom IDE [My_Experience_With_PureScript_So_Far]
- Atom support was easy to set up [PureScript_First_Impressions]

#### Miscellaneous

- PS has excellent documentation browsing [My_Experience_With_PureScript_So_Far]
- PS + Halogen can be 'dropped in' as replacements for Angular apps, making migration easier [PureScript_vs_ReasonML_Bucklescript_in_2018]
- Even if one does not understand FP, they can get help on a regular basis from really smart people (core contributors) [PureScript_vs_ReasonML_Bucklescript_in_2018]
- Making implicit partial functions explicit helped one adhere to type-driven development, which also had some educational benefits [My_Experience_With_PureScript_So_Far]
 [PureScript_vs_ReasonML_Bucklescript_in_2018]
- Arguments in linked post can be argued for PS, too, except in following ways: [PureScript_vs_ReasonML_Bucklescript_in_2018]
    - JVM ecosystem entirely available to Scala.js whereas PS must build its own or use unsafe Javascript libraries
    - code works on both the server and client in Scala whereas PS does not yet have mature server frameworks and Node.js is not necessarily the best tool to use.
- Article does not mention a few issues with Scala.js that do not arise with PS [PureScript_vs_ReasonML_Bucklescript_in_2018]
    - In Jordan's opinion, Scala is not as good for FP code as PS/Haskell (expressions are not as terse; compiler must be hacked to add some features that are already present in PS/Haskell, purely FP users of Scala are not supported by language's development, who want to support OO paradigm as well: there will always be tension / things that can't be done).
    - PS can compile to other languages besides Javascript. Sometimes C/C++ (and all its ecosytem) is a better fit than the JVM (and all its ecosystem)

### Arguments Against using PS

#### Compared to Haskell

- Haskell's stronger ecosystem might make it easier for the OP to learn domain-specific concepts (e.g. parsing, cryptography, etc.) in an FP style [Learn_PureScript_or_Haskell_First]]
- Haskell's stronger ecosystem might make it easier for the OP to learn domain-specific concepts (e.g. parsing, cryptography, etc.) in an FP style [Learn_PureScript_or_Haskell_First]
- GHC has better error messages than PureScript. This was likely true. I'm not whether that gap has decreased in the last year or not and by how much. I think it's likely still the same. [Learn_PureScript_or_Haskell_First]
- `purescript-sequence`, a FingerTree implementation was slower than Array until its size got very large. In other words, collections using lazy constructs in a strict language / non-specialized runtime don't work the same as they do in Haskell.

#### Compared to Elm

##### Elm is easier to learn for JS developers due to a less-powerful / simpler type system

- A non-PureScript user prefers a simple language with a gradual/short learning curve and is willing to compromise on the quantity of manually-written code to have it. [Hitchhikers_Guide_to_Elm]
- Elm is more approachable simply because it is less powerful and requires learning less. [Elm_PureScript_In_Depth_Overview]
- Elm seems to provide a gentler introduction to FP concepts than Haskell or PureScript primarily because it has less features and potentially has better documentation than PureScript did at that time. [Learn_PureScript_or_Haskell_First]
- One person believes Elm is a great first introduction to Haskell-style Pure FP languages because Elm has the same features as Haskell but small, simple subset of Haskell's complete set of features. [Why_is_Elm_More_Popular_Than_PureScript]
- One person believes Elm is more popular than PureScript because there are more people familiar with JavaScript, which has no common culture of principles and concepts, than with Haskell, which does. [Why_is_Elm_More_Popular_Than_PureScript]
- Elm is more popular because, unlike PS, one of its main purposes is to draw JS developers towards it. It does this by showing clear and specific examples where Elm provides better solutions than JS does and by helping people migrate to the language/ecosystem. [Why_is_Elm_More_Popular_Than_PureScript]
- Person believes that JS-background people love simpler languages with smaller learner curves. I'm not sure how true that is considering how many features exist in the JS language (unless one adheres to the principles in "Javascript: The Good Parts"). [Why_is_Elm_More_Popular_Than_PureScript]
- One person's perception of PureScript is scary, possibly due to HKTs and other "Haskell-y" stuff [Elm_019_Broke_Us]
- General perception is that learning curve is steep and hidden behind a lot of jargon [Elm_019_Broke_Us]
- Elm has a faster onboarding process where one feels productive. PS, due to its powerful type system, will never be able to have a faster onboarding process. [Why_is_Elm_More_Popular_Than_PureScript]
- Elm is a good starting FP language that might be powerful enough for many use cases. For others, they might use it as a stepping stone to get to PureScript after wanting more. Each has it's place. [Why_is_Elm_More_Popular_Than_PureScript]
- 50k app and the "abstraction ceiling" has not been hit yet. App does require a lot of boilerplate-y code, but it works and solves the business problem at the end of the day. [Why_is_Elm_More_Popular_Than_PureScript]

##### Elm has an easy-to-understand Application Structure

- Elm is appealing because it's application structure is well-understood. To get the same appeal, the 'best practices' for application structure should be well documented in PS. [Elm_PureScript_In_Depth_Overview]
- Elm's architecture is simple and understandable [Why_is_Elm_More_Popular_Than_PureScript]

##### Elm has really great compiler errors

- [Jordan] Many people complain about the cryptic errors of Haskell and PureScript, likely because they do not understand the compiler / type system that well [On_ergonomics_of_FP_Compiler_Errors]
- [Jordan] Elm, which is an FP language, has great compiler errors, but only because it's type system is much simpler and less powerful [On_ergonomics_of_FP_Compiler_Errors]
- Elm has nice errors [Why_is_Elm_More_Popular_Than_PureScript]

#### Comments specifically against PS / for alternatives

##### Regarding OCaml / ReasonML / BuckleScript as an alternative

- There are other FP-like languages out there besides PureScript that might be a better 'next step' for Elm programmers. [Wallowing_in_Despair]
- Elm as a "gateway drug" to PureScript may have competition from other FP languages: ReasonML [Elm_019_Broke_Us]
- ReasonML might be an easier destination for Elm users than PureScript due to being more mature in a few important areas. [Elm_019_Broke_Us]
- Source of ReasonML's popularity is Facebook and conferences. PS might be lacking 'evangelism' in conferences [PureScript_vs_ReasonML_Bucklescript_in_2018]
- PS compile times might be longer than Ocaml [PureScript_vs_ReasonML_Bucklescript_in_2018]
- Commentator gave up on Halogen's types and perceived ReasonML's React wrappers to be better than PS. [PureScript_vs_ReasonML_Bucklescript_in_2018]
- Easier to write a backend component in Ocaml than in PS. [PureScript_vs_ReasonML_Bucklescript_in_2018]

##### Miscellaneous

- Since PureScript is still a newer language, some people that use it in production rely upon only one expert to fix problems that most others do not know how to fix. [The_State_of_Things]
- Post-`0.12.0` release, a language release does not imply ecosystem compatibility immediately after its release. [PureScript_First_Impressions]
- Post-`0.12.0` release, user expected that language's community won't be able to reach ecosystem coherence for a while. [PureScript_First_Impressions]
- Person thinks that one should only learn PS for web/JS replacement. [Learn_PureScript_or_Haskell_First]
- Author started book with presupposition that static FP languages are worth their learning curve but has now concluded that perhaps this is not true. [Wallowing_in_Despair]
- Source hopes to move to PureScript once it stabilizes more [Elm_019_Broke_Us]
- PureScript is not suited for mainstream use yet but more for forward-thinking people who may get burned by future web developments [Elm_019_Broke_Us]
- Commentator agrees that out-of-box web components are lacking and this situation is unfortunate but not enough for them to stop using PS. [PureScript_vs_ReasonML_Bucklescript_in_2018]
- It seems author's project was heavy on the UI and speed was important. PS React-based frameworks were significantly slower than solutions from other languages, making PS a deal-breaker. Had project required less UI and more complex calculations where type-safety shines brightly, author would have stuck with it. [PureScript_vs_ReasonML_Bucklescript_in_2018]
- One valid reason for not wanting to learn PS: rendering speeds of Halogen/Thermite frameworks weren't fast enough for person's use case. [Why_is_Elm_More_Popular_Than_PureScript]
- Stagnation / slow down of language/ecosystem development was a factor in author's decision [PureScript_vs_ReasonML_Bucklescript_in_2018]
- Clojurescript was fast without boilerplate-y code and useful testing libraries [PureScript_vs_ReasonML_Bucklescript_in_2018]
- Author still found Typescript + Rambda + Immutable.js to be best **overall** solution. While admitting that it's not best in each aspect, the combination of it had the best environment for author. [PureScript_vs_ReasonML_Bucklescript_in_2018]
- Some perceive the core contributors' focus on developing the language over writing good documentation as a sort of "We're really smart. We won't come down to you; you'll have to come to us" mindset. [Why_is_Elm_More_Popular_Than_PureScript]
- One person believes the PureScript core maintainers will reject any attempt to compromise their favored abstractions to move towards "simplified" ideas. These "simplified" ideas are likely intended to improve the language's ease–of-use and approachability. [Why_is_Elm_More_Popular_Than_PureScript]
- PS "tries to be a better Haskell than Haskell" but comes at the cost of needing to learn many more concepts. Not everyone needs that power, nor wants to gain those benefits when other competing interests call (i.e. learning another imperative programming language might have better overall gain). [Why_is_Elm_More_Popular_Than_PureScript]
- One person believes that abstraction doesn't mitigate the complexities of an application which has a large feature set. [Why_is_Elm_More_Popular_Than_PureScript]
- A PureScript core maintainer believes that deeper concepts and idioms are best learned by consuming Haskell learning resources. [Why_use_Purescript]

### Arguments against using OCaml / ReasonML / BuckleScript?

- Seems OCaml / ReasonML / BuckleScript has a minor documentation problem of its own? [PureScript_vs_ReasonML_Bucklescript_in_2018]
- Seems OCaml / ReasonML / BuckleScript also is lacking a mature server solution? [PureScript_vs_ReasonML_Bucklescript_in_2018]
- OCaml / ReasonML / BuckleScript - new learners are also advised to check out their forum/chatroom for getting help from people already familiar with it. [PureScript_vs_ReasonML_Bucklescript_in_2018]
- Summary of a new learner's experience with OCaml / ReasonML / BuckleScript seems similar to other experiences of new learners of PS: [PureScript_vs_ReasonML_Bucklescript_in_2018]
    - sparse tutorials that are not part of some larger whole forces new learner to piece together the parts with difficulty
    - no clear linear learning path led to wasted time, something which would not occur in other ecosystems
    - while upsides of this ecosystem are good, they were not worth it for the author.

## Various "Learning Paths" to reach PureScript

- [Alex] A PureScript user sees that major language releases bring higher-than-normal newcomers to the language. [How_Do_We_Avoid_Ecosystem_Incoherence]
- Some people who give up on a language are simply waiting for its documentation to improve, so that they can have an easier learning process in the future. [PureScript_vs_ReasonML_Bucklescript_in_2018]
- Learner wrote working programs based on a few libraries and patterns/examples by the looks of it before learner really understood things. [Why_is_Elm_More_Popular_Than_PureScript]

### From Nothing

- Potential learning audience: those who have no experience in web development whatsoever [Why_is_Elm_More_Popular_Than_PureScript]

### From JavaScript

- One person believes that more people would try PureScript if it had more documentation targeting the JS/web audience. [Why_is_Elm_More_Popular_Than_PureScript]
- This resource (i.e. [A Mostly-Adequate Guide to FP (in JavaScript)](https://github.com/MostlyAdequate/mostly-adequate-guide)) might provide a better learning path for JS-background people before they see it written using a better syntax via PS. [Why_use_Purescript]

### From Elm

- A PureScript user entered PureScript after going through Elm. [Hitchhikers_Guide_to_Elm]
- Elm could be a useful 'gateway drug' into PureScript [Elm_PureScript_In_Depth_Overview]
- Pux could be a "gateway drug" library from Elm into PS [Elm_PureScript_In_Depth_Overview]
- It seemed the FP community responded with something like, "Why the hell would one start with Elm and then transition into PureScript? Why not just start with PureScript?" [Wallowing_in_Despair]
- A core contributor doesn't think the "Elm -> PS" path is a stupid idea. In some ways, it might be better than the "JS -> PS" path some others take. [Wallowing_in_Despair]
- It seems if one wants to do web development using an FP paradigm, Elm has better learning resources to help one get familiar with the concepts before switching to Purescript. Again, Elm as a "gateway drug" into PureScript seems like a good possibility. [Learn_PureScript_or_Haskell_First]
- Probably addressing the last thought in the previous comment, the author shows that Elm has more in common with PureScript than the commentor thought. [Wallowing_in_Despair]
- There is no clear path (learning path perhaps?) from Elm, which has a gentle learner curve, to a more powerful general-purpose FP language. [Wallowing_in_Despair]
- PureScript core contributor says that Elm users don't think in terms of Functor/Monad (because those terms aren't in their language/libraries?). While these patterns have naturally emerged in Elm, their community doesn't think/design in terms of it. [Wallowing_in_Despair]
- Highlights that there is a large philosophical difference between the two languages: Elm and PureScript. [Wallowing_in_Despair]
- Community member did a good job of using scaffolding to lessen the fear of PureScript: if you already get Elm's X ("comparable", "Cmd"), then PureScript's Y (type classes, effect system) is X + 1. [Elm_019_Broke_Us]
- Another Elm-inspired framework recommended is `purescript-hedwig` [Elm_019_Broke_Us]
- Source advised against `Pux` due to lack of documentation [Elm_019_Broke_Us]
- There is a library that feels similar to Elm to help Elm programmers transition to PureScript [Elm_019_Broke_Us]
- A person intended to write documentation which helps one transition from Elm into PureScript [Elm_019_Broke_Us]
- Elm is stil quite different from Javascript [Why_is_Elm_More_Popular_Than_PureScript]
- Once people love Elm, it's lack of features can make others want something better with PS as the proposed "obvious solution." [Why_is_Elm_More_Popular_Than_PureScript]
- Another learner stating that the JS -> Elm learning path worked well for learning FP concepts. It's not clear whether the learner also learned PS. [Why_is_Elm_More_Popular_Than_PureScript]

### From Haskell

- If one's goal is to learn an FP language, learning Haskell and then PureScript isn't necessarily a bad idea since Haskell and PureScript are very similar and Haskell is arguably more powerful than PureScript. However, if one's goal is to learn PureScript or do website development, it would be unfortunate to learn Haskell before learning PureScript. [Learn_PureScript_or_Haskell_First]
- Haskell has more documentation (but better?) than PureScript, so Haskell is recommended for newcomers. It's not entirely clear whether the Haskell documentation is "better" than PureScript, but it is implied. [Learn_PureScript_or_Haskell_First]
- Seems like Haskell had more material than PureScript: if one did not satisfy you or help you, you could look at another tutorial/guide. If you encounter the same situation in PureScript, tough luck as there isn't another tutorial/guide. [Learn_PureScript_or_Haskell_First]

### No Category

- Good insight here: one can look at material from all three languages (PS, Haskell, Elm) to get a better understanding for how the code works. In other words, the concepts can translate from one language to another. [Learn_PureScript_or_Haskell_First]
- A newcomer believes documentation of the background of PureScript is necessary qualification of a production-quality language [Elm_019_Broke_Us]
- A newcomer believes the PureScript community's level of satisfaction of its documentation and infrastructure is less than that of other programming languages. [Elm_019_Broke_Us]

## Ideas for how to improve PS Docs

### Things that need to be fixed

- There are lots of easy documentation problems to resolve in the core documentation. [Features_You_Want_Future_PureScript_to_Not_Have]
- PureScript by Example uses `unsafePartial` in such a way that it might wrongly imply that one uses it more frequently than one actually does. [Elm_PureScript_In_Depth_Overview]
- The reasons for using `unsafePartial` might not be well-documented/explained [Elm_PureScript_In_Depth_Overview]
- Help/Documentation on using Pursuit's search could be better highlighted to draw more attention to it. [PureScript_First_Impressions]
- Any conversations made on Slack that are worth keeping long-term (e.g. answers to stupid questions) do not persist long-term. This seems to contribute to new users asking the same questions again and again, taking time away from advanced users in the language from spending time on other more useful things. [The_State_of_Things]
- Many questions asked in the FP Slack channel could be better asked on SO with the one asking the question notifying people on the FP Slack channel. This would make such 'documentation' persist longer than the Slack logs. [Discussion_about_WNTYAD]

### Things that can be improved or better communicated

- The documentation repo's error pages are not up-to-date or completely filled out [The_State_of_Things]
- Regular compiler error messages do not also output the information one would see via a type-directed search to help the user determine what they are probably trying to write but failing to write. Elixir's compiler does this. [My_Experience_With_PureScript_So_Far]
- The FFI documentation should explain the disadvantages of giving first-class syntax for Javascript FFI due to PS' "compile to multiple backends" nature. [PureScript_First_Impressions]
- The FFI documentation should explain the advantages of writing an implementation for some function outside of the PureScript langauge (i.e. in Javascript source file): "allows you to fake out all non-pure state and effects and get as close to pure as possible." [PureScript_First_Impressions]
- A better version of Bower would be a huge improvement for PS community's build tooling. [PureScript_First_Impressions]
- Public acknowledgement that some people (not defined here) do not know how to update Try Purescript and Pursuit. (Secondary source) - Phil and Harry might be the only ones who know how to update it. [The_State_of_Things]
- Encouraging new users to open issues for documentation issues would help track down what already-written documentation is not immediately understandable to new users and what entities have yet to be documented. [The_State_of_Things]
- Perhaps providing a single centralized location for all cross-repo documentation issues that are easy enough for new beginners to do would help. To aid in recognition, they could all use the same label name: `new contributor`. [The_State_of_Things]
- The documentation repo is presented as a loose collection of potentially unrelated articles, not as a systematic presentation of articles that all fit within a larger vision. [The_State_of_Things]
- Author believes it's best for people with high status in a community to find ways to make low-status (unattractive?) jobs more attractive. [Wallowing_in_Despair]
- Documentation and tooling should not choose the latest language and library versions by default. Instead, it should be explicit about the language version being used and be conservative with upgrades. [How_Do_We_Avoid_Ecosystem_Incoherence]
- A PureScript outsider believes documentation should explain why the language doesn't have data types or concepts that they are familiar with. [Why_use_Purescript]
- It's not clear to new learner why one shouldn't just use GCHJS or some similar Haskell solution. [Why_is_Elm_More_Popular_Than_PureScript]
- Person might not have known about PS' other backends that make it more viable in the long-term. PS' "compile-to-anything" nature may not be well publicized. [Learn_PureScript_or_Haskell_First]
- Seems that PureScript by Example was not well-known by those outside the PS community? [Why_is_Elm_More_Popular_Than_PureScript]
- A PureScript users believes that language documentation should include a description of how easy it is to contribute to the language and affect its direction. [Why_use_Purescript]
- This PureScript user implies the library/architecture they used should document the situations it was designed for and the situations in which it is likely a poor fit. [Exploring_the_MVI_Architecture_with_PureScript_Puzzler]
- Author wanted more user-friendly libraries that handled more lower-level things, so that author could focus on learning and not fixing plumbing issues. [Exploring_the_MVI_Architecture_with_PureScript_Puzzler]
- Author suggests a new library for higher-level bindings to VDom to gain convenience, at cost of abiding by design choices of library. [Exploring_the_MVI_Architecture_with_PureScript_Puzzler]
- Concept's intended purpose and author's intended purpose differ. Thus, author used a hacky solution. This might have arisen due to the author not knowing how to use the library properly or because the library did not provide a basic building block that does what he needs it to. [Exploring_the_MVI_Architecture_with_PureScript_Puzzler]
- One PureScript user experienced the run-time behavior of the `signal` library to be difficult to understand and/or control when writing a program using the library. [Exploring_the_MVI_Architecture_with_PureScript_Puzzler]

### Providing Code Examples in Other Languages

- A PureScript user believes a good learning path is to teach a person from a language they are already familiar with. [Why_use_Purescript]
- A PureScript outsider believes the documentation should show how to use PureScript in a pre-existing project written in a different language. [Why_use_Purescript]

## Problems New Learners Face when Learning PS

### Baggage Learners Bring with Them

- People who hear that Purescript "compiles to Javascript" incorrectly assume/expect it to use a syntax similar to Javascript or other compile-to-JS languages. [Elm_PureScript_In_Depth_Overview]
- Author expects such explanations to be made in the module/function/type's documentation as found in Pursuit rather than some external resource like `Purescript By Example`, which does a good job explaing what that is. Linking to such explanations might address such pain points. [My_Experience_With_PureScript_So_Far]
    - Library (`purescript-assert`?) likely did not yet provide `assertX` with custom warning errors attached to it like `quickCheck (\a -> a <?> "custom warning error when it fails")` [My_Experience_With_PureScript_So_Far]
    - Author possibly assumes that unit testing is the default testing used for FP languages rather than property testing [My_Experience_With_PureScript_So_Far]
    - Author possible does not know about `purescript-spec` as a testing library [My_Experience_With_PureScript_So_Far]
- FP language's roots and similarities do not seem to be well-understood by outsiders and may contribute to outsiders' lack of understanding or initial expectations about FP languages that get broken. [Wallowing_in_Despair]
- PS and other FP solutions that are more powerful than Elm are not on most JS developer's radar of possible alternatives. [Why_is_Elm_More_Popular_Than_PureScript]
- PS was perceived as "unmaintained" because the docs hadn't been improved [Why_is_Elm_More_Popular_Than_PureScript]
- OO programmers likely need a bottom-up approach to teaching FP rather than the top-down approach many use [Why_is_Elm_More_Popular_Than_PureScript]
- One person believes that static FP concepts and their documentation should not require knowing other concepts as prerequisite to understanding and useage. [Why_is_Elm_More_Popular_Than_PureScript]
- One person believes that hiearchical classes are not a great idea because it assumes people know everything in the hierachy. Java's class hierarchy is "evidence" that this is true. [Why_is_Elm_More_Popular_Than_PureScript]
- One PureScript user made a game to practice PureScript and to learn the `signal` library. [Exploring_the_MVI_Architecture_with_PureScript_Puzzler]
    - One user of the `signal` library didn't know the best way to structure his app using the library. This highlights the aspect of 'best practices' documentation. [Exploring_the_MVI_Architecture_with_PureScript_Puzzler]
    - The author believes the signal library should offer a means of defining a branch in a signal graph which is conditionally active. [Exploring_the_MVI_Architecture_with_PureScript_Puzzler]
    - This PureScript user believes writing a GUI in a declarative/descriptive, non-imperative way is an easy way to develop a GUI app. [Exploring_the_MVI_Architecture_with_PureScript_Puzzler]
    - This PureScript user believes the best practices encoded in the "stateless GUI" design prescribed by the practice they are following in this app doesn't have a clear relation to traditional software design best practices they know. Since author stated above that 'stateless GUI is really cool,' author might not yet be familiar with 'best practices' for how to design such a program using this concept. We can't tell whether author used modular code to break big components down into smaller ones and whether these distinctions were done well. [Exploring_the_MVI_Architecture_with_PureScript_Puzzler]
    - This PureScript user believes the library/architecture they used was missing concepts, which would make it unsuitable for more complex applications. [Exploring_the_MVI_Architecture_with_PureScript_Puzzler]

### Difficulty in understanding PureScript's Syntax

- Author's first major issue and turn off was not being able to read the syntax of a Haskell-like language. This issue alone made him choose to look at Elm rather than PureScript, which is arguably more powerful than Elm. Unlike most people, the author did not give up and looked at Haskell/PureScript again, eventually reaching an understanding via each language's "standard" for learning them. [Elm_PureScript_In_Depth_Overview]
- The `do` syntax was not immediately understood by the author. [Elm_PureScript_In_Depth_Overview]

### Difficulty in understanding how to do X in PureScript

- A PureScript user has trouble figuring out how to solve application problems in PureScript, which is a reason for why PureScript is hard to learn. [Hitchhikers_Guide_to_Elm]
- A PureScript user feels rewarded when using PureScript because the primary sticking points are figuring out how to do things *in* the language, rather than figuring out *non-language* problems. [Hitchhikers_Guide_to_Elm]
- Not being able to mutate variables is a hard thing to initally grasp by new learners who are used to doing so freely. [Elm_PureScript_In_Depth_Overview]
- I don't know whether this concept (local and controlled side effects are still considered 'pure' if functions are referentially transparent) is well-documented in PureScript learning resources (even in my own, Jordan's PureScript Reference) [Elm_PureScript_In_Depth_Overview]
- This PureScript user believes it's difficult to integrate with a JavaScript library function which uses property-existence to define its behavior because PureScript's type system isn't flexible enough to define the type of that function in a simple way. (I think it's possible to modify the type signature of the JS library wrapper to use a typeclass to assert the argument has a subset of the fields expected by the function.) `{ attributes: { disable: "" } }` vs `{ attributes: {} }` [Exploring_the_MVI_Architecture_with_PureScript_Puzzler]

### Miscellaneous

- The Haskell book has exercises in addition to its explanations. [Learn_PureScript_or_Haskell_First]
- Migrating to psc-package requires a manual process. Not sure how much time that takes. [PureScript_First_Impressions]
- User did not understand the compiler errors user got as a result of not importing Prelude. [My_Experience_With_PureScript_So_Far]
- New learner experienced minor issue with build tool (need to restart it to sync with current state of build) [My_Experience_With_PureScript_So_Far]
- Newcomers to the language feel antagonized by the unfamiliar concepts and language operators. Perhaps documentation can mitigate the confusion and anguish experienced by newcomers. [My_Experience_With_PureScript_So_Far]
- new learners are scared by Halogen's types initially, likely because it's unfamiliar, uses jargon they don't yet know, and they fear that this understanding is needed to make things work. It's not clear whether the fear is due to not knowing how to resolve common Halogen errors or where to put types in type signatures or what. [PureScript_vs_ReasonML_Bucklescript_in_2018]
- People seem to think, at least initially, that type signatures are not 'good enough' for documentation. While one can understand a lot from them, new learners aren't used to do this, perhaps, or get close but not quite over a threshold of understanding for how to use that value/type/function/module. [PureScript_vs_ReasonML_Bucklescript_in_2018]
- A PureScript user believes language documentation should explain the depth of the language and its patterns/libraries to ensure users don't try to learn hard things before they understand more foundational things. [Why_use_Purescript]

## Ways to Improve New Learner Experience

### Clarify whether learning materials are up-to-date or not

- The PS language site was the first thing new learner went to. The oudated Eff-based example created a horrible new-user experience [PureScript_First_Impressions]
- There is a public awareness within the PS community that the documentation repo is not fully up-to-date with the PureScript language [The_State_of_Things]
- Outdated materials/websites are currently included in the main PureScript language's website. These should be removed to prevent new learners from thinking that these resources are in-sync with the latest PureScript language. [The_State_of_Things]
- The PureScript by Example book is not fully up-to-date with the PureScript language. [The_State_of_Things]
- [Alex] A PureScript user believes the PureScript HTML website should reflect active resources, and inactive resources should direct people to active resources. [How_Do_We_Avoid_Ecosystem_Incoherence]
- Assuming we keep the 'Try Purescript' website, it would help new learners to know which version of PureScript is running on that site. This can notify them whether the version is outdated/old or is the latest version. [How_Do_We_Avoid_Ecosystem_Incoherence]

### Better explain how to use/write FFI

- The FFI maybe needs better documentation, especially for a newcomer to statically-typed language. [PureScript_First_Impressions]
- user questions the lack of better FFI support via libraries that handle/write it for developers [PureScript_First_Impressions]
- Writing FFI is very boilerplate-y and wastes developer time. There should be a faster way to do the same thing, potentially via a library or through code generation. [PureScript_First_Impressions]
- new learner found it annoying that PS FFI requires a lot of boilerplate to be written. [PureScript_First_Impressions]
    - There might be code generation solutions to the above problem that he did not know about.

### Use Library Badges to indicate compiler compatibility

- An idea that might only be relevant if one is using Bower as a dependency manager: a library badge in the Git repo indicating which version of the language the library is compatible. [How_Do_We_Avoid_Ecosystem_Incoherence]
- Purescript-language-version-library-compatibility badges are easy to make via shields.io
- One needs to know which version of a dependency to install, so that it does not result in problems. However, this seems specific to Bower, not psc-package, and only when a breaking change has occurred recently. If the community moves away from using Bower, this solution is irrelevant. [How_Do_We_Avoid_Ecosystem_Incoherence]

### Make Pursuit more 'beginner-friendly'

- New users like to use Pursuit to learn how to solve problems when writing the language / understand what some concept/function/type is. [PureScript_First_Impressions]
- Having a 'beginner-friendly' version of Pursuit search that highlights / prioritizes / highly ranks the common things new learners would search for would be helpful. [My_Experience_With_PureScript_So_Far]
- Adding a filter to Pursuit Search that shows only libraries that are compatible with a specific PureScript language version would help. Unfortunately, this requires library maintainers to somehow indicate what that version is. [How_Do_We_Avoid_Ecosystem_Incoherence]
- Even a heavily-invested user of PS must navigate through readmes and docs to understand something. How much more a new learner? [How_Do_We_Avoid_Ecosystem_Incoherence]

### Provide Examples of Code Solving Some Problem

- General idea / approach to doing SQL was explained, but there isn't a complete and working example. Person was referred to Haskell database libraries, but it seems that referrer wasn't sure whether they would help. [Why_use_Purescript]
- A PureScript learner believes PureScript doesn't have a singular documented answer for UI programming tasks, such as click/drag, animations, and cursor effects. [Why_use_Purescript]

### Improve Compiler Error Messages

- [Jordan] Many people complain about the cryptic errors of Haskell and PureScript, likely because they do not understand the compiler / type system that well [On_ergonomics_of_FP_Compiler_Errors]
- [Jordan] Elm, which is an FP language, has great compiler errors, but only because it's type system is much simpler and less powerful [On_ergonomics_of_FP_Compiler_Errors]
- [Jordan] Compiler errors shouldn't tell you that something wrong occured (that's obvious, otherwise an error would not have been emitted). Rather, they should tell you what went wrong using non-jargon-y language and tell you what to do to fix them [On_ergonomics_of_FP_Compiler_Errors]
- [Alex] A PureScript user believes error messages should highlight the problem in the code in a way that makes resolution actionable, not explain why it bothers the compiler using technical jargon. [On_ergonomics_of_FP_Compiler_Errors]
- [Alex] A PureScript user believes that a compiler is a logic-checker, which means it can not be wrong. So, rather than explain it's full reasoning, it should just provide actionable description of the resolution. If details are desired, provide them in a separate document linked from the error message. [On_ergonomics_of_FP_Compiler_Errors]
- Person believes that Elm is more popular because its errors are better than PS' errors. It's easier to sell to your average no-expertise-in-FP developer [Why_is_Elm_More_Popular_Than_PureScript]
- The PS' language's errors have gotten better and there's only so much an error can say before it's actually teaching a concept rather than giving an error message. [Why_is_Elm_More_Popular_Than_PureScript]
- It might be impossible to have PS' powerful type system and all its features with error messages that are as helpful/clear as Elm's error messages. [Why_is_Elm_More_Popular_Than_PureScript]

### Explain how PS integrates with other web build tools

- New useres want to know how PureScript integrates with Webpack / CSS Modules / Code Splitting. [Why_use_Purescript]
- A PureScript outsider believes documentation should teach how to integrate the output of the PureScript compiler with other tools in the target language ecosystem. [Why_use_Purescript]

### Miscellaneous

- Providing good migration stories would help people who want to use it but can't because their 'system/program/app' would stop working for some period of time. A migration needs to be seamless and address the issues/concerns one might have. [Why_use_Purescript]
- Two options here: [Why_use_Purescript]
   - Show reasons for why Node is a "rock solid" solution to server-side things
   - Show reasons for why other backends (C/C++ ?) can provide a better server environment than Node...?
- Being required to import each import is tedious and annoying. [My_Experience_With_PureScript_So_Far]
    - However, the person might not know that the `atom-ide` / `purescript-lang` atom packages enable one to type in the Type, hit tab for the autocomplete, and the IDE will insert both the autocompletion and import the module if it's not imported already. This issue and its possible solution could be better documented.
    - The person might also not know that people often define their own Prelude to account for the above annoyance
- A suggestion for reducing the number of communication groups within PS down to 3 and defining general "policies" for what should go where [The_State_of_Things]
- Some users perceive that PS has a frequent breaking-changes language release cycle. This perception was true at various parts in the release, but hasn't been recently. [The_State_of_Things]
    - The number of weeks until next breaking change, starting at `v0.5.0` and going to `v0.12.0`: `10 28 34 31 17 18 25 60`
    - The average of the above number series: `27.875 weeks`
- [Alex] A core contributor believes the only reason to not adopt psc-package as the recommended dependency manager is missing features which make it a "general purpose" package manager and UX conveniences. [How_Do_We_Avoid_Ecosystem_Incoherence]
- Nix is really nice for FP libraries but difficult to set up [PureScript_First_Impressions]
- PureScript is not yet 'stable' to such a degree that migration guides and troubleshooting their issues is always well documented. This should be new learners expectations from the start. [How_Do_We_Avoid_Ecosystem_Incoherence]
- `pulp init` or a new `pulp` command could be configured to set up a learning environment for new learners that "just works." [How_Do_We_Avoid_Ecosystem_Incoherence]
- New learner looked at Haskell's docs rather than PS' docs to understand something. [Why_is_Elm_More_Popular_Than_PureScript]
- First I've heard of Neon [(an alternative "purescript-prelude" library that does not use any FP jargon and is pretty straightforward)]. It's also only updated for `0.11.7`, so this comment is somewhat out of date, too. Still, the ideas explained in Neon would make learning FP code easier. I just wonder what the tradeoffs would be. [Why_is_Elm_More_Popular_Than_PureScript]
- A PureScript outsider believes the documentation should describe the quality of the runtime. [Why_use_Purescript]

## PureScript's Mediums of Communication

### GitHub Issue Tracker

- GitHub issues should not be used for "help me" questions. [The_State_of_Things]

### Slack

- Slack is **sometimes** good for getting immediate response and transient things [The_State_of_Things]
- Slack is the "go to" for stupid questions [The_State_of_Things]
- Slack is useful for short conversations that work across timezones and internet connectivity issues. [The_State_of_Things]
- Slack acts as a newsfeed of sorts for PureScript [The_State_of_Things]
- The Slack channel provided the most up-to-date "I need help now" info. [How_Do_We_Avoid_Ecosystem_Incoherence]
- FP Slack filled-in any gaps in documentation. [PureScript_vs_ReasonML_Bucklescript_in_2018]

### Discourse Forum

- Discourse is **preferred** for seemingly longer discussions that aren't quite worthy of a GitHub issue [The_State_of_Things]

### Things relating to Slack and Discourse mediums

- [Jordan] The Slack channel and Discourse site are not easily findable. [How_Do_We_Avoid_Ecosystem_Incoherence]
- [Alex] A PureScript user believes the Slack channel and Discourse site are the best resources for PureScript users. [How_Do_We_Avoid_Ecosystem_Incoherence]
- [Alex] A PureScript user believes that all PureScript users should visit the Slack and Discourse instances as their primary resource for help. [How_Do_We_Avoid_Ecosystem_Incoherence]
- [Alex] A PureScript user believes the PureScript language HTML website should direct its visitors to PureScript's Slack/Discourse instances. (The PureScript website is currently a primary resource visited by a subset of the PureScript community and it should direct people to the best resource for PureScript help known by this PureScript user.) [How_Do_We_Avoid_Ecosystem_Incoherence]

### Inactive Mediums

- [Alex] A PureScript user believes the Gitter chatroom is not very active. [How_Do_We_Avoid_Ecosystem_Incoherence]

## Why Previous Documentation Efforts Failed

- PS documentation has always been bad. This problem has been the same throughout its history in that it hasn't gotten worse over time [The_State_of_Things]
- Not many PS learning resources have been available in times past [Why_is_Elm_More_Popular_Than_PureScript]

### FP "Best Practices" are not well-defined, are assumed, or are unconscious habits

- The commentor might be implying that all statically-typed FP languages don't share a common set of idioms. [Wallowing_in_Despair]
- It seemed the FP community thought that studying and documenting idioms/"design patterns"/habits of good FP programmers wasn't worth it. [Wallowing_in_Despair]
- It seems hard for the author (who is not as well-versed in FP idioms) to document them when those who know them don't care enough to share them. [Wallowing_in_Despair]
- Some FP idioms exist across FP languages (e.g. type classes) whereas others are specific to the language. As an example, the commentor believes that Elm doesn't have the same idioms as languages like PureScript. [Wallowing_in_Despair]
- The goal of documenting FP idioms is a great goal, but it's not clear how this could be done easily. [Wallowing_in_Despair]
- Many FP programmers don't consciously know the habits they have developed over time. Some habits, they may take for granted and assume others do likewise, being surprised to find that others don't. [Wallowing_in_Despair]
- The author believes that all fields of study need to document their idioms (best-practices?) and discuss them. The author says that programming communities (and FP communities specifically) do not tend to do this. [Wallowing_in_Despair]
- The author believes the FP community is blind to/ignores the idioms and practices of the wider programming language community because the FP community values aesthetics (over pragmatism?). [Wallowing_in_Despair]
- Saying that Elm is not a part of the Haskell tradition seems like a stupid thing to say because of how obvious its truth seems to be. [Wallowing_in_Despair]
- The PureScript core contributor may be implying that the difference between a programming language community which uses terms referring to academic theory and one which simply applies the benefits of the theories is that members of the former community thinks in terms of theory while members of the latter are blind to the theory when developing their programs and think only in terms of their program's domain. [Wallowing_in_Despair]
- The author, in contrast, believes that "the Haskell tradition" is having the language features of Haskell and the idioms used by the Haskell community. [Wallowing_in_Despair]
- It seems the author and the commentor were using the same word to mean different things. [Wallowing_in_Despair]

### FP's Culture Creates "Knowledge Silos"

- PureScript tends to draw intellectually curious people. [Wallowing_in_Despair]
- Biggest concern author has: the kind of culture that FP languages tend to develop never grow large enough that they make an impact/difference in the mainstream. Author clarifies what that 'subculture' is while being in a very negative emotional mood: [Author_Venting_About_Book]
    - it attracts/creates people who use a particular language
    - these kinds of people aren't the best ones to share it with others / show convincingly that FP languages are better than the status quo.
    - This situation continuously loops and the problem never gets fixed.
- Basic ideas of [Type Classes vs the World](https://www.youtube.com/watch?v=hIZxTQP1ifo) video: [Author_Venting_About_Book]
    - Type classes were 'discovered' because one guy misunderstood what another guy meant
    - **Type classes allow a programmer to use "dumb reusable types" (e.g. `Either`, `Maybe`, `Tuple`, `List`) whose contained types (e.g. the `Int` type in `Maybe Int`) are later 'constrained' with the required properties need to do some computation (i.e. a number-like type that can be added via `Monoid`)**
    - There are two styles of 'type classes:' real type classes and 'implicits' (Scala's type classes, Rust's "traits", etc.)
    - Implicit-styled type classes are more "powerful" in one degree but end up leading to possibilties that make programming harder. Haskell type classes do not add this 'benefit,' so using type classes are more reliable and easier to reason about. The key issue is commutativity: if some type has an instance for a sub type class (e.g. given there is an `Ord a`...), then logically there are ways to determine its intance for a super type class (e.g. ... then there is also a `Eq (List a)`)
    - Addressing "but why can't we just do X" reasons (including his thoughts for why Coq/Agda/Iris or, `a`, etc. other dependently-typed languages won't provide the 'refactor and it still works' guarantees of Haskell)
- Referring to the `Type Classes vs The World (video)`, this is the kind of knowledge that struggles to make its way out of the FP community. [Author_Venting_About_Book]
- `kmett` might be a good person to follow for extracting FP knowledge that remains otherwise stuck in 'knowledge silos.' [Author_Venting_About_Book]
- Source may have had disagreements with PureScript leaders that was fueled more by emotions than logical arguments and understanding one another's viewpoints. [Elm_019_Broke_Us]
- Source may have also just wanted really good documentation but did not receive the desired support from core contributors [Elm_019_Broke_Us]

### No well-defined criteria for which libraries count as 'core' libraries and ensuring their documentation is good/up-to-date

- Documentation for core PS libraries are great but it quickly falters. Perhaps documenting only "core" libraries is not 'good enough' or doesn't cover enough libraries? [PureScript_vs_ReasonML_Bucklescript_in_2018]

### Reviewing Documentation PRs can be just as difficult as code PRs

- Core contributor believes that accepting documentation means it needs to be reviewed. [Wallowing_in_Despair]
- Core contributor believes that some people are better or faster at reviewing documentation than others. [Wallowing_in_Despair]
- Core contributor believes that reviewing documentation can be just as difficult, if not more so, than reviewing code. [Wallowing_in_Despair]

### Limited Manpower / Not Enough Automation

- The workload is too great for one person to do alone without burning out. [The_State_of_Things]
- There is public acknowledgement that there are not enough workers to keep the documentation resources in-sync with latest language releases. As a result, much time is spent putting out fires rather than moving the language/ecosystem forward. [The_State_of_Things]
- Volunteer-based languages and their development do not have the same luxuries/resources as other languages. The desire to get somewhere exists, but not the time, especially when language changes/improvements break current documentation. [Wallowing_in_Despair]
- A core contributor is already stretched thin with maintaining code, so asking for better documentation is too much to ask. [Wallowing_in_Despair]
- [Jordan] Only volunteers who must pay their bills through other means are working on this language. There is no financial incentive for them to complete work, nor can they give the language their full time. [How_Do_We_Avoid_Ecosystem_Incoherence]
- [Alex] A PureScript user sees that there is no "full-time" developers, but notes the opposite, that he sees there are a few people whose contributions are nearly that of full-time developers. [How_Do_We_Avoid_Ecosystem_Incoherence]
- [Alex] A PureScript user believes that none of PureScript's contributors have a financial incentive to start or complete work. [How_Do_We_Avoid_Ecosystem_Incoherence]
- [Alex] PureScript does not have enough manpower (or automation) to reliably update everything in the ecosystem before making a release. [How_Do_We_Avoid_Ecosystem_Incoherence]

### Slow submitted-reviewed-merged timeline of documentation PRs kills documentation momentum

- The author believes that enthusiasm in contributing to docs lowers when it takes a long time to make a contribution (without getting a reward, like a merged PR?). [Wallowing_in_Despair]
- The author cites evidence that even a trivial change to a core library goes unmaintained for weeks. [Wallowing_in_Despair]

### Knowing whom to trust with write access, defining best workflow procedures, and providing necessary support

- One cannot use the "nobody gets paid to do it" reason as an excuse for poor documentation. Others have the same restraint and yet still succeed. [Wallowing_in_Despair]
- Responding to core contributor's post about being stretched thin, the author suggests sharing the load with others. [Wallowing_in_Despair]
- Core contributor thinks idea sounds good [Wallowing_in_Despair]
    - (This reminds me of the point that the Elm creator mentioned in his talk about "The Hard Parts of Open Source" Someone might say, "Why not delegate some activity to someone else?" Elm creator responds sarcastically, "Gee... I never thought of that!" before explaining the various concerns he has that has stopped him from doing that previously.) [Wallowing_in_Despair]
- The author believes that it's OK to allow a slightly-incorrect piece of documentation to exist if it's clear the documentation author is different from the code author, and the documentation author promises to maintain the documentation. [Wallowing_in_Despair]
- The author believes that being trusted with commit-rights to a library will encourage him to be more productive. [Wallowing_in_Despair]
- One has offered to maintain Pursuit, but might need some (but likely not a lot) help getting oriented to the project [The_State_of_Things]
- It's difficult to improve the core library experience without help from the creators or maintainers of it. [How_Do_We_Avoid_Ecosystem_Incoherence]

### Core contributors have not provided, nor known about, the desired support that 'unofficial' documentation efforts wanted/expected

- Getting support from core contributors would greatly impact the author's work. [Wallowing_in_Despair]
- Core contributor does not know what extra support the author expects while the author is contributing to PureScript. [Wallowing_in_Despair]
- Core contributor was prioritizing an important breaking-change release in the compiler and updating libraries to work with it over improving current documentation. [Wallowing_in_Despair]
- The core contributor's incentive is to improve the language to help him make better programs, not necessarily explaining the language to others. [Wallowing_in_Despair]
- Author reflects that there is a missing point of contact between two communities, so that his book does not succeed in either one of them. The implied communities are the non-FP / mainstream community and FP community. [Author_Venting_About_Book]
- Seems like the commentor is saying, "Wait. Is the book for the FP community, too? I thought it was only for Elm programmers... [Wallowing_in_Despair]

### Breaking Changes Renders Documentation Outdated

- Keeping documentation up-to-date via the medium of a book costs a lot of time. Breaking changes quickly destroys much of this work. [The_State_of_Things]
- Using Try Purescript as 'learning environment with PureScript already installed' became an unreliable environment due to a breaking change. [The_State_of_Things]
- A breaking change in the language sometimes greatly impacts the ecosystem and other times only minorly impacts it. [The_State_of_Things]
- Core contributor is expressing belief that breaking changes in core libraries are not likely to happen in the future as frequently and that language is finally stablizing. [The_State_of_Things]
- There is a lack of communication between the language developers/contributors and those who document the language about what changes will be included/excluded in the next release. This makes it harder for the documenter to know what to write, what to correct/change/fix, and what to continue ignoring. [The_State_of_Things]
- There is a lack of communication about the release schedule of the language and 'saving' all breaking changes for a single major release. [The_State_of_Things]
- [Alex] A PureScript user believes that new language releases which include breaking changes often lead to miscommunication. [How_Do_We_Avoid_Ecosystem_Incoherence]
- [Alex] A PureScript user believes that miscommunication of language releases/changes is largely accepted as normal by the community. [How_Do_We_Avoid_Ecosystem_Incoherence]
- [Alex] A PureScript user believes that there was no release-related documentation marketed/announced a reasonable time before the release. [How_Do_We_Avoid_Ecosystem_Incoherence]

### Lack of a clearly-defined community-wide mutually-held vision/goal

- One person is willing to write documentation and contribute. Unfortunately, there is not a larger vision as to what should be done and how this person should direct their documentation efforts. [How_Do_We_Avoid_Ecosystem_Incoherence]
- I'm not sure what coordination this would entail. Perhaps a unified vision of what the community is trying to accomplish? [How_Do_We_Avoid_Ecosystem_Incoherence]
- A user expressing confidence that the community is able to solve its problems; it just currently lacks coordination of some sort. [How_Do_We_Avoid_Ecosystem_Incoherence]
- It would be best to hold off on documentation until a stable language specification is defined. Otherwise, the same problems encountered above (quickly outdated learning resources that cost a lot of time to make) will occur again. [The_State_of_Things]
- There does not seem to be a well-defined mutually-held 'vision' for the future of the language's development. As a result, it's hard to start writing documentation material that will coincide with the `v1.0` release of the language. [The_State_of_Things]

### Miscellaneous

- There is "issue spam" in the language repo's issue tracker, making it harder to see what really needs to be done / should be done to get a `v1.0` release. [The_State_of_Things]

## Why a "v1.0" PureScript release has not been made

### Lack of a clearly-defined core-contributor-wide mutually-held language specification

- A proposal for how to make a `v1.0` release (mentioned before but encountered resistance from other core contributors) [The_State_of_Things]
    - fix any bugs that can't be documented
    - engineer things to make anticipated future additions easy / non-breaking
    - write a spec for the language
    - commit to stable release window
- Two potential breaking changes (one would require polykinds and the other would require quantified constraints) may come at a later unknown time. [The_State_of_Things]
- The 'resistance' mentioned before was based in not wanting to produce breaking changes in later releases. The 'resistance' stil exists in a small manner in that `garyb` does not want a complete "feature freeze." However, it's no longer about stopping a `v1.0` as much as it is a "how do we make `v1.0` that does not require us to introduce breaking changes soon after its release?" [The_State_of_Things]

### Keeping the motto of `Avoid "success at all costs"` and understanding its meaning

- The phrase "avoid success at all costs" could be interpreted in two different ways. [Why_is_Elm_More_Popular_Than_PureScript]
    - First way, "(avoid success) at all costs," is attempting to avoid any sort of success no matter what. It would imply trying to stop people from using the language at all. This is not how the above phrase is meant.
    - Second way, "avoid (success at all costs)," does not prioritize "success" (that comes at the cost of poor decisions with negative long-term consequences) over decisions based on solid foundations. Success is desired, but people will not take shortcuts to get there.
    - PS has the mentality of the second one, which sometimes is at odds with others' desires to see it "succeed" even if that means the language would suffer over the long-term.
- Those that follow Haskell tend to follow its motto, "avoid success at all costs," which the author seems to interpret (via implication) as "avoid mainstream usage at all costs." [Wallowing_in_Despair]
    - The "avoid success at all costs" phrase should be understood as "avoid (success at all costs)," meaning avoid short-term gain or other niceities that cause problems later and prioritize/pursue long-term goals that provide great foundations and are overall better.
- The PureScript core contributor believes that PureScript follows Haskell for now, but might not in the future. [Wallowing_in_Despair]
- Core contributor is perfectly fine with saying, "PureScript shouldn't be used if one can accomplish their goals using Elm." [Wallowing_in_Despair]
- PS is not meant for everyone, nor does it try to be. Rather, it tries to be great at specific things, so that those who value the same things the core contributors value are drawn to it and use it. [Why_is_Elm_More_Popular_Than_PureScript]

### Fear that people will misinterpret a "v1.0" compiler release for a "v1.0" ecosystem release

- Whether "PureScript is production-ready yet" depends on one's use-case, which is different for everyone. [Wallowing_in_Despair]
- [Alex] A core contributor believes that the PureScript language/compiler and the "PureScript product" can be difficult for most people to differentiate. [How_Do_We_Avoid_Ecosystem_Incoherence]
- [Alex] A core contributor believes that a `v1.0` release should include improving the "PureScript product" (the ecosystem). [How_Do_We_Avoid_Ecosystem_Incoherence]
- [Alex] Most people who hear that there is a `v1.0` PureScript release will think it means a "complete solution" when it might only mean the language/compiler. This might result in a net-negative press for the language. [How_Do_We_Avoid_Ecosystem_Incoherence]
- [Alex] A core contributor believes that the compiler's ecosystem should not block releases of the compiler, because the time required to update the ecosystem is nearly as long as the time between major compiler releases. [How_Do_We_Avoid_Ecosystem_Incoherence]
- core contributors to PS prioritize improving the language over improving the documentation / onboarding process [Why_is_Elm_More_Popular_Than_PureScript]

## Things that have changed since 'The State of Things'

- Thomas Honeyman implemented the [Real World App] for PureScript
- Core contributors released two new releases of PureScript (`0.12.1`, `0.12.2`) after a period where language development had slowed
- Jordan Martinez wrote his PureScript Reference learning repo
- Jusin Woo and Fabrizio Ferrai have made `spago` more mature and a viable `Bower` alternative once it fully integrates with rest of PS infrastructure (e.g. Pursuit)

## Unanswered Questions

- An unanswered question: how can the community communicate/enforce compiler-library versioning. I believe that concept means "this version of the library works on this version of the compiler." [How_Do_We_Avoid_Ecosystem_Incoherence]
- If much of person's code uses FFI, then is the overall advantages that PS bring better than just writing vanilla JS? [Why_is_Elm_More_Popular_Than_PureScript]
    - Counter argument: the above issue might be due to useful libraries not existing in PS that then leads the person to need to use FFI to get the same thing. [Why_is_Elm_More_Popular_Than_PureScript]
- These two questions here were not really answered: [Why_use_Purescript]
   - how should click/drag/transitions/animiations (stateful things) be done in general?
   - how should same things be done using a UI library like Pux?
- What became of these people's work?
    - We should follow up with these people ([see this thread](https://twitter.com/ThibaudDauce/status/895534464071331840)) to see what they ultimately came up with (if anything). If the project did not get anywhere, there's still likely some historical value here (what worked, what problems they encountered, etc.) [Why_use_Purescript]

## Things relating to breaking changes

### Compiler-Library-Ecosystem Things

- [Alex] A PureScript user believes that compiler related projects, such as build tools, should be updated along with compiler releases. (One cannot benefit from a new compiler version if the tooling used by their previously-written project doesn't support it.) [How_Do_We_Avoid_Ecosystem_Incoherence]
- [Alex] A PureScript user believes that major libraries in the ecosystem should work with the latest available version of the compiler. (One can not benefit from the new release if the shared libraries used in the previously-written project don't work with the latest available compiler version. [How_Do_We_Avoid_Ecosystem_Incoherence]
- [Jordan] An official "ecosystem is `<release version>`-ready" announcement might help prevent this. Likewise, Including a "this release is made but not ecosystem-ready yet" note in the languages' release notes that includes a link as to what "ecosystem-ready releases" mean might help prevent this negative press. [How_Do_We_Avoid_Ecosystem_Incoherence]
- [Alex] A core contributor believes that compiler-related projects (the ecosystem) are an important aspect of a compiler release. [How_Do_We_Avoid_Ecosystem_Incoherence]
- [Alex] A core contributor believes communication of a major compiler release has significant impact on language's followers. [How_Do_We_Avoid_Ecosystem_Incoherence]
- [Alex] An official "ecosystem is `<release version>`-ready" announcement might help prevent this. Likewise, including a "this release is made but not ecosystem-ready yet" note in the languages' release notes that includes a link as to what "ecosystem-ready releases" mean might help prevent this negative press. [How_Do_We_Avoid_Ecosystem_Incoherence]
- [Alex] There used to be a process/checklist of things to do for making a language release. [How_Do_We_Avoid_Ecosystem_Incoherence]
- [Alex] There is not a clear place to store a checklist like this. [How_Do_We_Avoid_Ecosystem_Incoherence]
- [Alex] The compiler repo is the first idea of a place to store this list, but it is inappropriate because it is related to non-compiler things like docs, libs, and tooling. [How_Do_We_Avoid_Ecosystem_Incoherence]
- [Alex] A PureScript user believes that all contributors want to make the PureScript language and its ecosystem of projects a happy place to work. [How_Do_We_Avoid_Ecosystem_Incoherence]

### Dependency Managers

- [Alex] A core contributor believes ecosystem compatability is difficult or unreliable while PureScript community recommends using Bower as a dependency manager. [How_Do_We_Avoid_Ecosystem_Incoherence]
- [Alex] A core contributor believes that psc-package is the best option for dependency manager for introductory resources to use and recommend, as it would resolve the library-compatibility issues of Bower. [How_Do_We_Avoid_Ecosystem_Incoherence]
- [Jordan] However, psc-package does not provide a complete solution to the problems which Bower does. While psc-package might be good for introductory learning materials, it is not as good for production code as Bower. Thus, many major libraries (e.g. Aff, Halogen) use Bower. New learners likely look at these libraries written or supported by "successful companies using PS in production" and see that they use Bower, not psc-package. Thus, they think they should do likewise. [How_Do_We_Avoid_Ecosystem_Incoherence]
- [Jordan] Once a `psc-package`-based approach becomes more mature, one major company will switch to it and do so eagerly. [How_Do_We_Avoid_Ecosystem_Incoherence]
- [Alex] An company using PureScript is eager to adopt `psc-package` when it becomes more mature. [How_Do_We_Avoid_Ecosystem_Incoherence]
- Bower should be seen as a "semver layer on top of Git" and less of a JS package manager. [Why_is_Elm_More_Popular_Than_PureScript]

### Communicating Changes in the Ecosystem

- A newsfeed of some sort that summarizes the changes in the ecosystem would help one know what has gone on recently. [How_Do_We_Avoid_Ecosystem_Incoherence]
- Library changes were not announced in a very public manner, including what is being deprecated and what their new library names are. Bower + Pursuit did more to worsen the situation than help. [How_Do_We_Avoid_Ecosystem_Incoherence]
- It would help if language releases coincided with core library releases and included some form of public announcement about the changes. [How_Do_We_Avoid_Ecosystem_Incoherence]
- Although the idea of a "core library" is mentioned, criteria for what that is a core library and a complete list of them is not included here. (While the 'web' libraries make sense to be called 'core', it would help to clarify why, so that similar ones are included, too.) [How_Do_We_Avoid_Ecosystem_Incoherence]
- An `upcoming-ps-release` branch in some libraries helped ensure they were compatible with the next language version almost as soon as it was released. This approach seems to have been a successful approach. [How_Do_We_Avoid_Ecosystem_Incoherence]
- While this approach of using an upcoming-compiler-release-branch in libraries was successful, others did not follow it, perhaps because they were not aware of that approach or the release candidate window was too short. [How_Do_We_Avoid_Ecosystem_Incoherence]
- If a person starts and maintains a new library, they need to be notified of breaking changes in an upcoming language release. Ideally, this would be done via them subscribing to some notificaton system, or learning of it via a public announcement or someone opening up an issue for it in their repo. Of these approaches, the last one is best if it can be automated. [How_Do_We_Avoid_Ecosystem_Incoherence]
- A solution to notifying library users of upcoming language changes will likely require an automated tool that integrates with Pursuit and GitHub, and a team of volunteers that handle any of the un-automated work. [How_Do_We_Avoid_Ecosystem_Incoherence]
- There can be better communication between maintainers of the language and maintainers of heavily-used libraries around major releases. [How_Do_We_Avoid_Ecosystem_Incoherence]
- Release changes can be summarized and explained in a blog post, and include a migration guide. [How_Do_We_Avoid_Ecosystem_Incoherence]
- A documentation team consisting of volunteers can help communicate release changes to language users and library maintainers. A documentation team's responsibilities could include: [How_Do_We_Avoid_Ecosystem_Incoherence]
    - writing documentatin for core libraries
    - summarizing major changes in a blog post, why the changes were made, where new libraries (if any) can be found, and a "migration" guide
    - potentially pushing library documentation to Pursuit
- The entire process the ecosystem must go through from language release to ecosystem compatibility is not the most efficient it can be, nor is it widely understood by non-core-contributors. [How_Do_We_Avoid_Ecosystem_Incoherence]
- A potential 'success' indicator for determining whether a language release went smoothly/efficiently is a 30-day guarantee that the ecosystem is compatible with the latest language release (potentially excluding larger documentation efforts like the PureScript by Example book). [How_Do_We_Avoid_Ecosystem_Incoherence]
- The question of how releases integrate with the process of making a release to NPM needs to be further explored. There might be additional things that could be optimized here. [How_Do_We_Avoid_Ecosystem_Incoherence]

## Unused Interpretations

- Each non-Elm language, general-purpose pure FP language, seems to have pros which are outweighed by the "warts" of the language. [Wallowing_in_Despair]
- The author's definition of being welcomed into a language community is when an "insider" tells others to listen to him, even if he's probably wrong. [Wallowing_in_Despair]
