# Infrastructure Analsysi

## Who are the core contributors to the PS language and infrastructure as a whole?

This helps us know who has write access to the repos

Official core repos that have significant impact on PureScript community's documentation or build process as a whole

- PureScript language repo
- Pursuit repo
- PureScript website repo
- Documentation repo
- Prelude repo
- pulp repo
- psc-package repo
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

## The Purs Docs command

### How does it work?

Seems to do a subset of the work of the compiler (purs) because going the full way of the compiler would lead to hard-to-understand docs. As a result, there are a few issues that arise that are still being worked out, such as [desugaring type classes](https://github.com/purescript/purescript/issues/3264).

There are a number of output formats, but usually Markdown or HTML is the result. It seems that [HTML will become the default](https://github.com/purescript/purescript/issues/3489) in next breaking-change release).

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

##### Gains in making search more useful

- [Tool that shows difference between two versions](https://github.com/purescript/pursuit/issues/139)
- [Search only within a specific package](https://github.com/purescript/pursuit/issues/179)
- Search for all instances of a given type class: [311]](https://github.com/purescript/pursuit/issues/311) / [349](https://github.com/purescript/pursuit/issues/349)
- [Search Filter: only allow functions, packages, modules, types](https://github.com/purescript/pursuit/issues/290)
- [Make modules clickable URLs](https://github.com/purescript/pursuit/issues/268)

#### Gains in making it easier to understand the ecosystem

- [Package tags and descriptions for finding related packages](https://github.com/purescript/pursuit/issues/147)
- [Include a page that only lists 'core libraries/packages'](https://github.com/purescript/pursuit/issues/326)
- [Sitemap for Pursuit and a sitemap for each package](https://github.com/purescript/pursuit/issues/106)
- [Given a package, show all other packages that depend on it](https://github.com/purescript/pursuit/issues/292)
- [Clicking on declaration uses it to search for its usage throughout ecosystem](https://github.com/purescript/pursuit/issues/168)

#### Gains that help indicate old libraries

- [Feature: mark libraries as deprecated](https://github.com/purescript/pursuit/issues/287)
- [Badge that indicates whether docs on Pursuit are not the same as latest on Bower](https://github.com/purescript/pursuit/issues/111)

#### Gains in code readability

- [PureScript code syntax highlighter](https://github.com/purescript/pursuit/issues/115)
- [Source code in-lined with docs for better context](https://github.com/purescript/pursuit/issues/137)
- [Support Latex for Math via KaTeX](https://github.com/purescript/pursuit/issues/155)

#### Gains in other aspects

- [Provide an API for Pursuit to make it usable by 3rd-party tools](https://github.com/purescript/pursuit/issues/180)
- [Add a 'search' button so one can use mouse to run search](https://github.com/purescript/pursuit/issues/347)

### Things not highlighted in Pursuit Issue Tracker on GitHub

- a visualized dependency graph (including transitive ones) for one package
- a visualization of how one type can be created, transformed into another type, or consumed
- an RSS feed or something to notify others that a new package has been uploaded to Pursuit
- an option to only show packages that exist in a `psc-package` package set
- an option to only show packages that were compiled using or are compatible with a specific version of PureScript

## Buld Tool Integration with Pursuit

When reviewing build tools integration with Pursuit...
- what integrates with it
- how well/poorly does it integrate with it?
- what are these integrations' main benefits/limitations and why?

### Build Tool

## Pre-existing Learning Resources

- What other learning materials already exist in the PS ecosystem?'
- Who wrote them and how active are those people?
- What are their incentives?
- Would they want to be part of a potential documentation team?
- Who is their intended audience?
- What type of documentation is it? (i.e. tutorial, how-to, reference, explanation)

### Source
