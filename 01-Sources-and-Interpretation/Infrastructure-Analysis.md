# Infrastructure Analsysi

## Who are the core contributors to the PS language and infrastructure as a whole?

This helps us know who has write access to the repos

Core repos that have significant impact on PureScript community's documentation or build process as a whole

- PureScript language repo
- Pursuit repo
- PureScript website repo
- Documentation repo
- Prelude repo
- pulp repo
- psc-package repo
- package set repo
- spago repo

### PureScript Organization Members

- garyb
- joneshf
- kRITZCREEK
- LiamGoodacre
- paf31 (no longer contributing to the PureScript language but still the only person AFAIK who has access to some key infrastructure. For example, [the Pursuit deployment](https://github.com/purescript/pursuit/issues/385#issuecomment-456228798))

### PureScript Language Repository: main contributors by commits

- garyb
- joneshf
- kRITZCREEK
- LiamGoodacre
- nwolverson (recent contributions made)
- natefaubion (recent contributions made)

### Other Key Members

- hdgarrood
- justinwoo

... and a few others that do not immediately come to mind.

## The Purs Docs command

### How does it work?

Seems to do a subset of the work of the compiler (purs) because going the full way of the compiler would lead to hard-to-understand docs. As a result, there are a few issues that arise that are still being worked out, such as [desugaring type classes](https://github.com/purescript/purescript/issues/3264).

There are a number of output formats, but usually Markdown or HTML is the result. The Markdown output does not produce GitHub-Flavored Markdown because they use the [CheapSkate](https://github.com/jgm/cheapskate) Haskell library. It seems that [HTML will become the default](https://github.com/purescript/purescript/issues/3489) in next breaking-change release).

### How could improvements here greatly benefit the entire ecosystem?

There's not a lot here. Even the sole issue below would only benefit the community slightly in that it would be more readable. There are workarounds for this issue.
- [purescript/purescript#3507 - Doc comments for type class functions are included in docs](https://github.com/purescript/purescript/issues/3507)

## Pursuit

### What does PS' main documentation website, Pursuit, currently do well?

- one can use a number of different types of search, such as
    - package name (e.g. `purescript-prelude`)
    - module name with unfinished module path will act as a wildcard (e.g. `Data.List.` )
    - function name (e.g. `map`)
    - function's type signature including polymorphic ones (e.g. `(a -> b) -> f a -> f b`)
    - symbolic aliases to functions (e.g. `(<$>)`)
- one can navigate throughout the website fairly well
    - `s` keyboard shortcut focuses the search bar
    - Links to various entities work
        - source code repository (GitHub)
        - source code of a given entity (function, type, etc.)
        - Modules & submodules in package
        - dependencies of package
        - specific versions of a package
        - anchors provided for many entities for pasting URLs elsewhere
- Help page is rather useful, but is not highlighted as well as it could be

### What does PS' main documentation website, Pursuit, currently not do at all but should do?

#### Things mentioned in the Pursuit Issue Tracker on GitHub

The following are listed by category/topic and I've included my own flag for indicating, in my opinion, how important such a feature is.

##### Gains in making search more useful

- Search for all instances of a given type class: [311]](https://github.com/purescript/pursuit/issues/311) / [349](https://github.com/purescript/pursuit/issues/349)
    - Super Important: New learners will greatly benefit from this because the abstract notion of a type class can be made more concrete by looking at the various ways data types implement it.
- [Tool that shows difference between two versions](https://github.com/purescript/pursuit/issues/139)
    - Nice to have feature, but might be outside scope of Pursuit: isn't this what the package's release notes are for?
- [Search only within a specific package](https://github.com/purescript/pursuit/issues/179)
    - Very important: can be very useful for exploring a package or finding the right entity (function / type) that one needs
- [Search Filter: only allow functions, packages, modules, types](https://github.com/purescript/pursuit/issues/290)
    - Nice to have feature: most of this can already be done if one inputs the search in the correct way (e.g. type signature for function, "purescript-" for package, "Module.Path." for modules)
- [Make modules clickable URLs](https://github.com/purescript/pursuit/issues/268)
    - Nice to have feature: one can click on other entities to navigate around the documentation

#### Gains in making it easier to understand the ecosystem

- [Package tags and descriptions for finding related packages](https://github.com/purescript/pursuit/issues/147)
    - Super Important: tags and descriptions can quickly narrow down a person's search for a library by quite a bit. This is especially true for new learners who are not familiar with the language. It's also true for people who are already familiar with the ecosystem because new libraries can be published that they are not aware of.
- [Include a page that only lists 'core libraries/packages'](https://github.com/purescript/pursuit/issues/326)
    - Somewhat important: The importance of this depends on which other features in this list get implemented and when. If none of the other features are implemented, this is a very useful feature to have now. However, if the 'package tag and descriptions' feature is implemented, it would likely cover meet the need this feature would satisfy.
- [Sitemap for Pursuit and a sitemap for each package](https://github.com/purescript/pursuit/issues/106)
    - Somewhat important: The importance of this depends on which other features in this list get implemented and when. If none of the other features are implemented, this is a very useful feature to have now. However, if the 'package tag and descriptions' feature is implemented, it would likely cover meet the need this feature would satisfy.
- [Given a package, show all other packages that depend on it](https://github.com/purescript/pursuit/issues/292)
    - Important: This is useful again for exploring the ecosystem and/or finding packages: "If I use X, then what else works with X?"
- [Clicking on declaration uses it to search for its usage throughout ecosystem](https://github.com/purescript/pursuit/issues/168)
    - Important: This is similar to the point immediately above ('show dependents' idea) but with a bit more fine-grained control. Honestly, these two concepts should be merged together into one idea: show what depends on some entity (function, module, type, package, etc.)

#### Gains that help indicate old libraries

- [Feature: mark libraries as deprecated](https://github.com/purescript/pursuit/issues/287)
    - Important: This would be useful for everyone because it immediately shows which libraries to ignore.
- [Badge that indicates whether docs on Pursuit are not the same as latest on Bower](https://github.com/purescript/pursuit/issues/111)
    - Important: this would raise awareness that the docs are outdated. One can then view the docs on Pursuit to get a general idea before looking at the latest release to see what fully changed.

#### Gains in code readability

- [PureScript code syntax highlighter](https://github.com/purescript/pursuit/issues/115)
    - Nice to have: some examples would be easier to read or easier to copy their pattern if this was done.
- [Source code in-lined with docs for better context](https://github.com/purescript/pursuit/issues/137)
    - (This might already be implemented) Important: in situations where docs have not been written, one can immediately see the source code, which might clarify any misunderstandings they have.
- [Support Latex for Math via KaTeX](https://github.com/purescript/pursuit/issues/155)
    - Nice to have: some ideas are better explained using well-rendered mathematical notions.

#### Gains in other aspects

- [Provide an API for Pursuit to make it usable by 3rd-party tools](https://github.com/purescript/pursuit/issues/180)
    - Very Important: this capability would make Pursuit easier to work with other 3rd-party tools.
- [Add a 'search' button so one can use mouse to run search](https://github.com/purescript/pursuit/issues/347)
    - Nice to have: since this is a (likely) trivial fix, it's a wonder that no one has fixed it yet.

### Things not highlighted in Pursuit Issue Tracker on GitHub

- a visualized dependency graph (including transitive ones) for one package
    - because visualizations help us see things in a better format than other mediums
- a visualization of how one type can be created, transformed into another type, or consumed
    - because sometimes our goal is to determine how to create a given type, or how to convert it into something else, etc.
- an RSS feed or something to notify others that a new package has been uploaded to Pursuit
    - because when new libraries are uploaded, there's no way to know about them unless the author makes an announcement on Discourse/Slack/Reddit
- an option to only show packages that exist in a `psc-package` package set
    - this would help one know where `spago` needs to be used to configure the package set
- an option to only show packages that were compiled using or are compatible with a specific version of PureScript
    - this would help address the havoc that arises when a 'breaking change' language release occurs and one is trying to determine which libraries have been updated for that release.
- Will Pursuit's scope include documentation for backends other than Javascript? Will it be possible to search for FFI-only code based on which backends currently support that?

## Buld Tool Integration with Pursuit

The build tools `purp` and `spago` do not currently integrate at all with Pursuit. It's also somewhat difficult to determine how they would ever integrate with Pursuit...

`pulp`, when used with `Bower` as a dependency manager, is the only build tool that currently integrates with Pursuit. However, `pulp` allows anyone to impersonate anyone else and upload documentation for a package, even when that person should not have access to that.

The long-term use of `Bower` as a dependency manager seems up-in-the-air as its authors no longer recommend using it and the `psc-package`/`package-set`/`spago` build tools are becoming more mature overall.

## Pre-existing PureScript Learning Resources

This section overviews the other learning materials that already exist in the PS ecosystem?

- Who wrote them?
- How active are the author(s)?
- What are their incentives?
- Would they want to be part of a potential documentation team?
- Who is their intended audience?
- What type of documentation is it? (i.e. tutorial, how-to, reference, explanation)

| Resource Name | Author | Activity? | Incentives? | Potential Doc Team member? | intended audience? | type of documentation? |
| - | - | - | - | - | - | - | - |
| PureScript By Example | Phil Freeman | not active, but is a user of PS | help a new person get familiar with the language enough to actually build something useful | not likely due to burning out and still recovering from it among other reasons | PS learners | tutorial / explanation
| [PureScript Resources](https://purescript-resources.readthedocs.io/en/latest/) | Justin Woo | Justin is quite active in the community, but AFAIK does not contribute to his resource that frequently | probably just a way to summarize a few things for new people | not sure | new learners | mixture of how-tos, quick-starts, and some explanations
| [PureScript - Jordan's Reference](https://github.com/JordanMartinez/purescript-jordans-reference) | Jordan Martinez | frequently active on the learning resource but does not do much else for the larger community | to learn PureScript by teaching it to others via the Feynmann technique | possibly | new learners and people needing a centralized "do it all" kind of learning resource | a mixture of getting-started, how-tos, explanation, and reference; mostly explanation and reference; code-as-an-example
| [Lens for the Mere Mortal: PureScript Edition](https://leanpub.com/lenses) | Brian Merick | Not very active AFAIK; author has moved on to other languages...? | to explain how to use lenses immediately without first explaining how and why they work | people who want to understand Lenses but are afraid of them because of how complicated the types get; people who have tried learning Lenses using other tutorials and still do not understand them. | Quick Start, explanation, how to
| [A Guide to PureScript Numeric Hierarchy](https://a-guide-to-the-purescript-numeric-hierarchy.readthedocs.io/en/latest/introduction.html) | hdgarrood | very active and a core contributor to the PS language and a number of libraries | to explain PureScript's numeric type class hierarchy | likely? | those who do not have a strong math background | tutorial / explanation
| [Real World App](https://github.com/thomashoneyman/purescript-halogen-realworld) | thomashoneyman | active and contributes to a number of Halogen-related projects | show that PS is a viable/better alternative to other solutions; show a fully functional, well-commented program written in FP style/concepts | not sure | people already familiar with basic FP concepts; people who want to see what "good FP code" looks like (or at least one way of writing 'good FP code') | code-as-an-example
| [MultiPac](https://github.com/hdgarrood/multipac) | hdgarrood | create a good learning resource that's also a fun experimental project | learners looking for real examples | code-as-an-example

## Learning Resources targeting different backgrounds

| Resource Name | Author | Activity? | Incentives? | Potential Doc Team member? | intended audience? | type of documentation? |
| - | - | - | - | - | - | - | - |
| [Egghead.io Learn PS course](https://egghead.io/courses/professor-frisby-introduces-composable-functional-javascript) | Brian Lonsdorf | Not sure | Not sure | Not sure | Javascript developers who want to learn FP in Javascript | explanation and how-to ?
| [Outersider's Guide to Statically Typed Functional Programming](https://leanpub.com/outsidefp) | Brian Merick | Not very active AFAIK; author has moved on to other languages...? | to explain the benefits of FP programming to "outsiders," people who do not know it, without using FP jargon or the usual approach that FP people use to explain FP | Not sure, but seems unlikely | Javascript developers who want to learn Elm? Elm developers who are ready for something more powerful? | Getting Started, How-to, Explanation

### PS' Differences from Haskell

https://github.com/JordanMartinez/purescript-jordans-reference/blob/latestRelease/00-Getting-Started/03-Other-Important-Info.md#differences-from-haskell

- Two resources that explain PS' differences from Haskell

### PS' Differences from Elm

https://gist.github.com/justinwoo/0118be3e4a0d7394a99debbde2515f9b

- Out-of-date but still includes a few things

## Other FP Learning Resources

### What I Wish I knew When Learning Haskell

http://dev.stephendiehl.com/hask/

- What type of documentation is it? (i.e. tutorial, how-to, reference, explanation)
    - incomplete topic guide to various things

### Haskell Programming: From First Principles

http://haskellbook.com/

- What type of documentation is it? (i.e. tutorial, how-to, reference, explanation)
    - well-written book on Haskell and learning how to write programs in FP style

### Specific Topics in Haskell

https://github.com/bitemyapp/learnhaskell/blob/master/specific_topics.md

- What type of documentation is it? (i.e. tutorial, how-to, reference, explanation)
    - Link-farm to various other sources
