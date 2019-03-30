# Why docs are lacking

This file includes more details for the summary in the section 'why docs are lacking.'

### PureScript is not _currently_ trying to be the next "mainstream language"

A few have wrongly assumed that PureScript is trying to replace [insert your favorite web language here]. That is not the case.

PureScript has the following philosophy:
> Making a language "popular" (e.g. industry-standard, taught in universities' curriculums, etc.) is not a justification for decreasing its "power," such as limiting the language's expressiveness, making it less safe, less secure, etc.
>
> Making the language easier to use and learn by improving it is good and supported.
> Achieving the same goals by crippling, downgrading, or dumbing down the language is rejected. Users will either learn it properly or use something else.
>
> Plenty of languages chose to sacrifice safety, security, efficiency, etc. to gain the benefits of "popularity."
>
> PureScript will not be another such language. Rather, it will try to progress in "the right way," even when it's inconvenient, makes it harder to learn, etc.
>
> ~ Summary of [A Response that Explains the Motto: 'Avoid (Success at All Costs)'](https://news.ycombinator.com/item?id=12056169) (edits made: replaced 'Haskell' with 'PureScript'; removed "research-related concepts")

While typically stated differently, one could summarize this philosophy as "value power and expressivity over popularity."

The current focus (see later point) is not on making documentation great. Rather, it's on implementing the language features that haven't yet been implemented.

However, even if great documentation was the focus, one will still have to learn difficult concepts before they can be productive. This fact will never change.

Thus, PureScript might not be the language for you:
- If you value 'popularity' over 'power,' use a different language.
- If you value 'power' over 'popularity' and are determined to learn hard things, use this language.

(Related interpretation sections: [Keeping the motto of `Avoid "success at all costs"` and understanding its meaning](https://github.com/chexxor/purescript-documentation-discussion/blob/master/01-Sources-and-Interpretation/All-Interpretations.md#knowing-whom-to-trust-with-write-access-defining-best-workflow-procedures-and-providing-necessary-support))

### Only core contributors have write / deployment privileges to PureScript websites

The following PureScript websites either are outdated or could be modified to improve the documentation situation.

Who can merge PRs into the websites' repositories and redeploy them once these PRs are merged?

| Site | Write Privilege | Deploy Privelege | Source
| -- | -- | -- | -- |
| PureScript language website | Core Contributors | None. GitHub Pages | -
| Pursuit | Core Contributors | Phil Freeman | [The State of Things, point 2](https://discourse.purescript.org/t/the-state-of-things/282)
| Try PureScript | Core Contributors | Phil Freeman | [The State of Things, point 2](https://discourse.purescript.org/t/the-state-of-things/282)

### Core contributors are spread thin

> It’s been 7 months since I announced that I would be taking a long break from PureScript development....
>
> In retrospect, I think it’s fair to say that I was quite thoroughly burned out from trying to balance open source work and real life.
>
> I still love to _use_ PureScript, and I’ve been working to increase PureScript adoption at work....
>
> ~ Phil Freeman, the creator of the PureScript language [(1st & 2nd paragraph)](https://discourse.purescript.org/t/the-state-of-things/282)

The following quote is a response to another's "wallowing:"

> Just to wallow for a second, I...
> - contribute to/review stuff on the compiler
> - attempt to keep on top of the issues, discussions, PRs on roughly 75 libraries (some of which are tiny and almost never change, some of which are purescript-dom :grimacing:)
> - engage with people on Twitter, StackOverflow, Reddit, Slack
> - and very occasionally investigate some idea of my own.
>
> So unless I stop doing some of that, there's no chance I can make any meaningful steps to improving the documentation situation.
>
> ~ Gary Burgess, a core contributor ([2nd paragraph](https://gist.github.com/marick/e8b01375309fafaefb879c4840b6da75#gistcomment-2569261), edits made: content was turned into a list; "..." changed to "," for readability)

After reading such statements, we can only step back and ask,
- Are the core contributors doing ok?
- Are you getting enough rest?
- Are you still investing in meaningful relationships?
- Is contributing to PureScript still enjoyable to you or has it become burdensome?

Thank you for the language you have created, the libraries you wrote and maintain, and all the other things you have done for the benefit of this language and its ecosystem.

Thank you for putting up with frustrating people, enduring negative and impatient attitudes, and trolls.

#### Implications

Reviewing documentation can be just as difficult as reviewing code. Some people are faster at reviewing things than others.

Thus, maintaining momentum when documenting code is difficult:
- Some documentation PRs are missed/forgotten.
- Many do not get a timely response from core contributors (one may wait for weeks)
- Some do not get merged in a timely manner either.

Lastly, I (Jordan) don't know whether some tasks could be automated and whether that would help.

(Related interpretation sections: [Limited Manpower / Not Enough Automation](https://github.com/chexxor/purescript-documentation-discussion/blob/master/01-Sources-and-Interpretation/All-Interpretations.md#limited-manpower--not-enough-automation), [Slow submitted-reviewed-merged timeline of documentation kills momentum](https://github.com/chexxor/purescript-documentation-discussion/blob/master/01-Sources-and-Interpretation/All-Interpretations.md#slow-submitted-reviewed-merged-timeline-of-documentation-prs-kills-documentation-momentum), [Reviewing documentation PRS can be just as difficult as code PRs](https://github.com/chexxor/purescript-documentation-discussion/blob/master/01-Sources-and-Interpretation/All-Interpretations.md#reviewing-documentation-prs-can-be-just-as-difficult-as-code-prs))

#### Why Not Just Delegate?

> A hypothetical developer says, "If it's so much work, why not just **delegate** the work? This 'somebody' can also be a proxy who's gathering feedback, so that you don't have to be in these discussions."
>
> The contributor responds sarcastically, "Oh! Delegation, of course! I hadn't thought about that...."
>
> There's actually an assumption going on here: "If 'free' rice means you can take as much as you want, then 'free' labor implies you can take as much as you want." But that isn't how labor works. If you don't pay for labor, you get less.
>
> Even if everyone could help, there's still limitations due to coordinating efforts: who does what, when, and where, and all without affecting someone else's work.
>
> ~ summary of the 'Why Not Just... Pattern' in [The Hard Parts of Open Source](https://youtu.be/o_4EX4dPppA?t=257)

One shouldn't trust everyone on the internet. (I know, big surprise.)

For example, consider the `event-stream incident`. The maintainer unknowingly gave write-access to a malicious actor. Practically everyone depends on this code. The actor injected code that could be used to steal bitcoins:
- [initial issue](https://github.com/dominictarr/event-stream/issues/116)
- [injected code explanation](https://github.com/dominictarr/event-stream/issues/116#issuecomment-441759047)
- [original maintainer's response](https://github.com/dominictarr/event-stream/issues/116)
- [a sarcastic blog post summarizing this class of attack](https://hackernoon.com/im-harvesting-credit-card-numbers-and-passwords-from-your-site-here-s-how-9a8cb347c5b5)

New maintainers, once found and properly screened, have to be supported (which takes time and thought), so that they can actually fulfill their role. If they decide to leave soon after starting, then one has wasted time and effort.

(Related interpretation sections: [Knowing whom to trust with write access, defining best workflow procedures, and providing necessary support](https://github.com/chexxor/purescript-documentation-discussion/blob/master/01-Sources-and-Interpretation/All-Interpretations.md#knowing-whom-to-trust-with-write-access-defining-best-workflow-procedures-and-providing-necessary-support))

#### Why Not Just Fund the Language Developers?

Been there, done that. Someone took it down. ([PureScript Open Collective]((https://opencollective.com/purescript))

Our viewpoint of this situation:
- Fans of PureScript wanted to throw money at the project. Why? Perhaps because
    - they want to help the project and its goals
    - they dont have the time or mental capacity to contribute
- Several people used OpenCollective to indicate they'd like to pledge money to the "github.com/purescript/purescript" project.
- Several weeks later, someone claimed that project's corresponding OpenCollective page and turned off the public page.
- We believe this was because there was no clear vision as to how the funds would be spent.

Perhaps this idea could be revisited in the future. For now, we cannot say.

### Breaking Changes Outdate Documentation and Kill Documenters' Motivation

The main 'go-to' documentation resource for PureScript was/is [PureScript By Example](https://leanpub.com/purescript/) by Phil Freeman. This resource documents the `0.11.7` PureScript release. The current PureScript release is `0.12.3` (as of this writing).

The `0.12.0` was a significant achievement but one that came with a lot of breaking changes. Phil responded to it in this way:

> [The PureScript by Example book] seems to take longer [to update] with each major compiler update, and honestly, I’m not motivated to update it again without some sort of guarantee that I won’t have to redo everything again in a few months....
> I would like to write a lot more documentation for PureScript, but I hate the idea that it will become out of date quickly....
> So without some sort of plan for the future of the language, and some idea of what changes are coming (and just as importantly, which aren’t), I’m not likely to write anything, and I wouldn’t be surprised if others avoided writing for the same reason.
>
> ~ Phil Freeman [The State of Things, point 4](https://discourse.purescript.org/t/the-state-of-things/282)

Gary later pointed out that releases with "breaking changes" were occuring less frequently ([source](https://docs.google.com/spreadsheets/d/1MO8siLLSOpkKHJ_eBNRJbipBquFgqlaSS-QSnALDSo8/edit#gid=0)). Still, keep in mind that Phil was likely updating the book each time such a release was made.

(Related interpretation sections: [Breaking Changes Render Documentation Outdated](https://github.com/chexxor/purescript-documentation-discussion/blob/master/01-Sources-and-Interpretation/All-Interpretations.md#breaking-changes-renders-documentation-outdated))

### There Is No Roadmap That Coordinates Efforts

Defining a roadmap is hard. It's easy to...
- ...disagree on which goals should be pursued and which to ignore
- ...disagree on how to word such goals
- ...do nothing and let someone else contribute

Creating a "good" roadmap takes significant time and energy.

PureScript does not currently have such a roadmap. Rather, core contributors seem to have a general direction they are pursuing (see next point).

Therefore:
- Those who could help do not know where help is needed
- Those who would help do not know how they can help

#### Avoiding a `v1.0` PureScript language release

When people announce "Language X is now `1.0`!", it tends to draw a lot of focus and a lot of traffic. People probably think, "Wow! It's now stable enough to be used to write all my programs."

In short, one core contributor believes that many would perceive a `v1.0` release as a `v1.0` ecosystem release. The language could be considered 'good enough' for a `v1.0`. However, the ecosystem is definitely not.

What good is a `v1.0` language, if
- common libraries haven't stabilized yet or are non-existant?
- the ecosystem is incoherent in a number of ways?
- the dependency managers are still unfriendly to users?
- the IDE support is still lacking?

Thus, core contributors might avoid defining a roadmap to prevent people from having a `v1.0` ecosystem connotation.

#### Defining a Language Specification

When should future breaking changes be done: before a `v1.0` or afterwards?

`garyb`, a core contributor, has resisted efforts to define a language specification. Why? Because he wants to add two features that will require breaking changes: "poly-kinds and something that requires qualified constraints." ([The State of Things, 6th paragraph in his comment](https://discourse.purescript.org/t/the-state-of-things/282/5))

If done before a `v1.0`, then the language will likely be stable, documentation will not go out of date, and the ecosystem can flourish.

If done after a `v1.0`, then many libraries and docs will need to be updated, the language's reputation might suffer, and people might be forever turned off to it.

(Related interpretation sections: [Lack of a clearly-defined communit-wide mutually-held vision/goal](https://github.com/chexxor/purescript-documentation-discussion/blob/master/01-Sources-and-Interpretation/All-Interpretations.md#lack-of-a-clearly-defined-community-wide-mutually-held-visiongoal), [Lack of a clearly-defined core-contributor-wide mutually-held language specification](https://github.com/chexxor/purescript-documentation-discussion/blob/master/01-Sources-and-Interpretation/All-Interpretations.md#lack-of-a-clearly-defined-core-contributor-wide-mutually-held-language-specification), [Fear that people will misinterpret at "v1.0" compiler release for a "v1.0" ecosystem release](https://github.com/chexxor/purescript-documentation-discussion/blob/master/01-Sources-and-Interpretation/All-Interpretations.md#fear-that-people-will-misinterpret-a-v10-compiler-release-for-a-v10-ecosystem-release))

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

### What Exactly are FP's "Best Practices"

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