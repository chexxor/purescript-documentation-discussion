# Our Outcome Ideas

## Goal: The top 30 dependencies used in PS' ecosystem have examples and counterexamples in all of their Pursuit docs.

### How: A community-curated "ACME" Spago project

We make a version of Justin Woo's "ACME" Spago project ([project](https://github.com/justinwoo/acme-spago) & [resulting docs](https://jusrin.dev/acme-spago/)). For packages that are lacking docs or are maintained by core contributors who won't respond quickly, we could use Spago to override those packages with a version supplied by a community member that includes more documentation.

All changes should be accepted with little questioning. However, the project should heavily warn against people using the resulting package set in production as one could easily introduce malware here.

## Goal: Collect the best and clearest explanations for FP concepts into a central location

In general, these are the kinds of things I had in mind:
- What are some of the clearest explanations of FP concepts?
- How hard is it to port their code examples to PureScript?
- Have people written an explanation that "walks one through" an FP paper's ideas in a clear way?

I don't want another 'link farm.' That leads to information overload and decision paralysis.

Rather, I want the top 1 or 2 explanations on something.

### How: Add it to Jordan's learning repository

These links could be added to [Jordan's learning repo](http://www.github.com/jordanmartinez/purescript-jordans-reference) as it exists partly for this purpose.

While lacking expertise in some areas, he can still sift through them and help determine which are great, good, duplicates, or just downright bad.

## Goal: Convert all answered Slack-based questions into StackOverflow Questions and Answers

Slack is still an ideal place to ask a question. However, it doesn't persist.

### How: Reask and reanswer it on StackOverflow

When a question on the `#purescript` or `#purescript-beginner` Slack channel gets answered, request the person who asked it to post the question on StackOverflow and link to the question in the chatroom.

Then, let someone (whether the answerer or someone who saw it) "answer" that question and give credit it to the answerer.

We should prioritize persistent docs over crediting who answered the question.

## Goal: Collect the best solutions to common build-related problems into a central location

- Integrating PureScript to work with JS build tools?
- Integrating PureScript with CI (Travis, AppVeyor, etc.)?
- Possible "tree-shaking" approaches to PureScript and their tradeoffs?

### How: Add it to a special "build" repository

I would suggest adding it to Jordan's learning repo, but this idea only works well if there are lots of small sample projects to build. Thus, it'd be better kept as its own repository.

## Goal: Add Syntax Examples for Core Libraries

Sometimes, Pursuit docs don't help you know how to use something. However, a lot can be gleaned/imitated by looking at an example. For example:
- [Halogen's "basic button component" example](https://github.com/slamdata/purescript-halogen/blob/master/examples/basic/src/Button.purs)
- [Jordan's example for how to create a tree via `purescript-tree`](https://github.com/JordanMartinez/purescript-jordans-reference/blob/latestRelease/22-Projects/src/11-Table-of-Contents/04-Tree/01-Syntax.purs#L31-L64)
- [Jordan's example of the "hello world" program via the ReaderT design pattern](https://github.com/JordanMartinez/purescript-jordans-reference/blob/latestRelease/21-Hello-World/08-Application-Structure/src/11-Hello-World/02-ReaderT.purs)

### How: Document a syntax example in Jordan's Learning Repo

I've begun to do this myself [here](https://github.com/JordanMartinez/purescript-jordans-reference/tree/latestRelease/22-Projects/src/01-Libraries) with a few libraries that I've used when building some projects. Perhaps I will later turn this into a separate top-level folder and call it "cookbook"

## Unsorted Ideas

Rather, we (non-core-contributors / users of PS) can focus on answering questions like these:
- What are "best practices" for various topics/areas? For example:
    - Guidelines for writing a good bindings library
        - How should a library author analyze the library to which they want to write bindings?
        - What are common problems such people face and their possible solutions?
