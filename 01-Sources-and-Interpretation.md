# Sources and Interpretation

## Defining Our Terms

**Definition**:
A "source" is any source of data that makes a truth claim (it claims that something is true. Whether that statement is actually true needs to be explored).

The goal of this step is to do the necessary work to make it easier to do the next step: defining the context/narrative.

Sources can be broken into two types: primary sources and secondary sources. Primary sources are stand-alone sources whereas secondary sources are interpretations, summaries, analyzations of primary sources.

**Examples of Primary Sources:**
- An original paper that introduces some idea for the first time
- A blog post
- A tweet
- A talk
- A conversation in a forum, chatroom, etc. where one person speaks their own opinion, makes their own logical argument, etc. These statements are not interpretations of some external data.

**Examples of Seconary Sources:**
- A blog post that summarizes another blog post
- A conversation where one person uses phrases like "I remember X being true," "I think X is true," and/or "I heard someone say X is true." and these phrases are used to mean "I interpreted information in such a way that I reached some conclusion and I am stating that conclusion, not necessarily the process by which I reached that conclusion, so that you can 'check my work of logical deduction.'"

**Gathering Sources**:
One first gathers sources without bias as to who said what or where it comes from and categorizes them according to primary/secondary source distinctions. At this stage, no assessment of the sources or interpreting what they say is done.

**Interpretation**:
After gathering as many sources as is reasonable in the allotted time period, one begins to assess a source and give it weight. Some sources bear more "weight" than others (primary bear more weight than secondary). Some are more subjective (biased, unbalanced in assessment, misinformed, etc.) while others are more objective (real evidence/arguments that must be addressed with real answers). Once assessed, one interprets the main themes/ideas that one hears the source communicating.

<hr>

The rest of this document should be a list of sources where each source has
- a link to the original post/comment
- a quote of the relevant parts of that post/comment and an interpretation that highlights the main ideas of the relevant parts

Since maintaining the primary/secondary source distinctions can be hard to do when analyzing/interpreting blog posts, forum comments, etc., they will not be categorized as such here.

## Source: 'The State of Things'

https://discourse.purescript.org/t/the-state-of-things/282

### Opening Comment

[Actual comment](https://discourse.purescript.org/t/the-state-of-things/282)

- This was written by the language creator, so it bears significant weight
- The language creator admits to stopping his language contributions and oversight due to burning out, so these statements should be interpreted in light of that. He might be more negative in his assessment than an other contributor because of that burnout.

> We seem to have developed something of a documentation problem. Even now, the documentation repository is only partially updated for the 0.12 release, and generally it is quite unstructured and lacks a single vision for what good documentation should look like.

- There is a public awareness that the documentation repo is not fully up-to-date with the PureScript language
- The documentation repo is presented as a loose collection of potentially unrelated articles, not as a systematic presentation of articles that all fit within a larger vision.

> Also regarding documentation, I still need to update the book.

- The PureScript by Example book is not fully up-to-date with the PureScript language.

> It seems to take longer with each major compiler update, and honestly, I’m not motivated to update it again without some sort of guarantee that I won’t have to redo everything again in a few months.... I would like to write a lot more documentation for PureScript, but I hate the idea that it will become out of date quickly, and that I will have yet more projects to update in future.

- Keeping documentation up-to-date via the medium of a book costs a lot of time. Breaking changes quickly destroys much of this work.
- The workload is too great for one person to do alone without burning out.

> So without some sort of plan for the future of the language, and some idea of what changes are coming (and just as importantly, which aren’t), I’m not likely to write anything, and I wouldn’t be surprised if others avoided writing for the same reason.

- There is a lack of communication between the language developers/contributors and those who document the language about what changes will be included/excluded in the next release. This makes it harder for the documenter to know what to write, what to correct/change/fix, and what to continue ignoring.

> I think we (i.e. 'we' will mean "the community generally" hereafter) need to come to the difficult realization that everyone is already stretched thin, and that we need to try to do less in order to do things well.
> - If Try PureScript takes too much time to update, then we should not advertise it on the website.
> - If the documentation cannot be updated in sync with the compiler, then it should also be unlinked from the website, and marked as stale.

- There is public acknowledgement that there are not enough workers to keep the documentation resources in-sync with latest language releases. As a result, much time is spent putting out fires rather than moving the language/ecosystem forward.
- Outdated materials/websites are currently included in the main PureScript language's website. These should be removed to prevent new learners from thinking that these resources are in-sync with the latest PureScript language.

> I have said before that I think we should avoid new features and concentrate on bug fixes and documentation. Now that 0.12 is out, I think it is a great time to prune any inessential feature requests from the issue tracker and make a plan to concentrate on these things instead.

- There is "issue spam" in the language repo's issue tracker, making it harder to see what really needs to be done / should be done to get a `v1.0` release.

> There needs to be a plan for the future, and that plan needs to be documented. I would like to start working on a specification for the language, something which I consider essential for documentation purposes, but it doesn’t make sense to start documenting a language when there is no plan in place for the next milestone.

- There does not seem to be a well-defined mutually-held 'vision' for the future of the language's development. As a result, it's hard to start writing documentation material that will coincide with the `v1.0` release of the language.

> For me, the ideal situation would be this: we agree that the compiler is not perfect as it exists now, but that its flaws are relatively minor and easily documented; we make a plan to release 1.0 (or 13.0?) by fixing any bugs we cannot document, and engineering things as best as possible in order to facilitate feature additions we anticipate; then we write a specification for this language, and commit to a stable release window, ideally as long as possible. When I’ve brought this idea up in the past, it’s met some opposition, but I think this would be massively beneficial and enable the creation of lots of stable documentation.

- A proposal for how to make a `v1.0` release resistant to future breaking changes
- This idea has been mentioned before but has been met with resistance. We don't know what that 'resistance' is as there are there are no external links or other evidence as to what that is.

### Comment (language user)

https://discourse.purescript.org/t/the-state-of-things/282/2

> I prefer Discourse for things that don’t warrant a GitHub issue. I find that Slack can sometimes be good for getting an immediate response and for transient things.

- GitHub issues should not be used for "help me" questions.
- Slack is **sometimes** good for getting immediate response and transient things
- Discourse is **preferred** for seemingly longer discussions that aren't quite worthy of a GitHub issue

### Comment (language user)

https://discourse.purescript.org/t/the-state-of-things/282/3

- This was written by a user of the language and suggests ideas for improving documentation.

Relevant parts and their interpretation appear below:

> Maybe a solution to getting better documentation would be to have some live on the main compiler repo as issues with the `new contributor` label and if others find they need more docs in popular libraries to open an issue with similar label on library repo and have a section on here with all of these accumulated. They wouldn’t strictly have to be just docs anything beginner friendly. But writing Docs is a good way to get into a language.

- Perhaps providing a single centralized location for all cross-repo documentation issues that are easy enough for new beginners to do would help. To aid in recognition, they could all use the same label name: `new contributor`.
- Encouraging new users to open issues for documentation issues would help track down what already-written documentation is not immediately understandable to new users and what entities have yet to be documented.
- Writing new docs or improving old ones is a good way to get started with a language.

### Comment (language user)

https://discourse.purescript.org/t/the-state-of-things/282/4

Source admits to being a 'pure user' of language.

> As a pure user of the language I’m also quite frustrated with rapid backwards incompatible changes to the language and standard “library”. It hinders my ability to introduce it more widely into production because once the compiler changes it’s me who is solely responsible to “make it work again, forchristsakes!”. I think the time has come to have a definition of “version 1.0” and work towards it.

- There is a lack of communication about the release schedule of the language and 'saving' all breaking changes for a single major release.
- Since PureScript is still a newer language, some people that use it in production rely upon only one expert to fix problems that most others do not know how to fix.

> If you take volunteers I can maintain Pursuit. I’m infrastructure engineer/manager by day. It will take me some time to figure my way around “server side Haskell” but I’ve seen harder things in my life. Let me know if I can help.

- One has offered to maintain Pursuit, but might need some (but likely not a lot) help getting oriented to the project

> As for the communication channels, the Slack is great for asking a stupid question if you got stuck in the middle of something simple. The lack of logging sucks big time and I remember myself reading IRC logs for hours with great results.

- Slack is the "go to" for stupid questions
- Any conversations made on Slack that are worth keeping long-term (e.g. answers to stupid questions) do not persist long-term. This seems to contribute to new users asking the same questions again and again, taking time away from advanced users in the language from spending time on other more useful things.

### Comment (core contributor)

https://discourse.purescript.org/t/the-state-of-things/282/5

From garyb, a core contributor of the language.

> I guess regarding Try Purescript / Pursuit there need to be more of us who are aware of how to update it / how they work, as I think it’s just you and Harry at the moment.

- Public acknowledgement that some people (not defined here) do not know how to update Try Purescript and Pursuit
- (Secondary source) - Phil and Harry might be the only ones who know how to update it.

> I think that [(i.e. we have a documentation problem)] started with the initial release and has been true ever since. I can’t think of a time in PS’s history where we had docs resources that were good and up to date (book aside). I agree it’s a problem, I just don’t think characterising it as something new or that has gotten worse is true - perhaps it’s just become more apparent now you’re primarily a user?

- PS documentation has always been bad
- This problem has been the same throughout its history in that it hasn't gotten worse over time

> I looked back at the releases as to how long the gap between them was and how breaking they were, for as long as I’ve been involved with the project.... So I’m not sure the perception that we’re breaking things constantly is entirely true, especially with the last release since it was by far the longest period of non-breaking.

The number of weeks until next breaking change, starting at `v0.5.0` and going to `v0.12.0`:
`10 28 34 31 17 18 25 60`
The average of the above number series:
`27.875 weeks`

- Some users perceive that PS has a frequent breaking-changes language release cycle. This perception was true at various parts in the release, but hasn't been recently.

> Also, the breaking changes that weren’t library related in 0.12 were relatively minor compared with changing => in 0.11, etc.

- A breaking change in the language sometimes greatly impacts the ecosystem and other times only minorly impacts it.

> Just pointing out PS is definitely slowing down into a more stable state anyway. Especially after 0.12, the Effect changes and some of the other library changes that went out, there’s very little that I can think of that I’d like to do differently in the core libraries now. In fact there are only two changes I can think of, one would require polykinds and the other would require quantified constraints, so they’re probably not going to be any time soon.

- Core contributor is expressing belief that breaking changes in core libraries are not likely to happen in the future as frequently and that language is finally stablizing.
- Two potential breaking changes may come at a later unknown time.

> I think having the Discourse is valuable for sure, as hopefully we can encourage non-transient discussions that aren’t issue specific to move here instead.
> There’s also the Google Group, but I can’t remember the last time I looked at that.
> I use Slack as even though there’s no persistent logging it has enough of a backlog that I can actually catch up with the last day or so, which is about all I ever did with IRCBrowse too. That and you can reply to people who are offline.
> I don’t use Gitter at all or the IRC channel anymore.

- This list seems to include all of the PureScript groups out there and how frequently people use them and why.
- Slack is useful for short conversations that work across timezones and internet connectivity issues.
- Slack acts as a newsfeed of sorts for PureScript

> Perhaps we should cull the list to just point people to Discourse and GH issues for “real” discussions, Slack (and maybe IRC) for quick questions / transient discussions, and leave it at that.

- A suggestion for reducing the number of communication groups down to 3 and defining general "policies" for what should go where

> I’m less hostile to this idea (i.e. creating a specification for the language, focusing on bug fixing and stopping new features) than I once was, but mainly because I think the “missing” features that I feel are the greatest causes of friction for me can be added without breaking old code. I guess it depends by what we mean by committing to a long term stable release, if we’re talking about not grossly breaking things, I’d say we’re at a point where that’d be no impediment at all, but if we’re talking about an entire feature freeze then I’m still reluctant.

- The 'resistance' mentioned before was based in not wanting to produce breaking changes in later releases.
- The 'resistance' stil exists in a small manner in that `garyb` does not want a complete "feature freeze." However, it's no longer about stopping a `v1.0` as much as it is a "how do we make `v1.0` that does not require us to introduce breaking changes soon after its release?"

### Reply (core contributor)

https://discourse.purescript.org/t/the-state-of-things/282/6

> I think the language is at a good point where we could focus a lot more on documentation if we decided to commit to a stable language specification.

- It would be best to hold off on documentation until a stable language specification is defined. Otherwise, the same problems encountered above (quickly outdated learning resources that cost a lot of time to make) will occur again.

### Comment (language user)

https://discourse.purescript.org/t/the-state-of-things/282/7

> Errors: a number of these are undocumented in the docs repo. Unfortunately, I can’t figure these out unless I get really lucky and write code that fails to compile. If one of the core contributors worked on the errors part, the documentation would be largely up-to-date.

- The documentation repo's error pages are not up-to-date or completely filled out

### Comment (language user)

> I had the misfortune of making a free PS course that uses TryPureScript a couple of months before 0.12 was due and some of it’s changes, I think, broke a couple of my lessons due to the way I taught them. Need to check it out properly just not had the motivation! I like it as a tool but can totally understand the hassle of keeping it and attached material up to date.

- Using Try Purescript as 'learning environment with PureScript already installed' became an unreliable environment due to a breaking change.

### Comment (language user)

https://discourse.purescript.org/t/features-you-want-future-purescript-to-not-have/115/5

> Soul mate! There’s a ton of low-hanging fruit in even core documentation. I hope after 0.12 that pull requests like this one 53 for Data.Map get approved.

- There are lots of easy documentation problems to resolve in the core documentation.

### Comment (language contributor)

https://discourse.purescript.org/t/how-do-we-avoid-ecosystem-incoherence-in-the-future/209/9

> I would love to help (update core libraries) – I’m not shy about writing documentation or putting time into these updates – but without being a core contributor I have no idea what these plans even are. As a consumer I largely find myself digging around readmes and docs that may or may not have been updated trying to guess at what ecosystem shifts have just happened. This is a little disconcerting as a heavily-invested commercial user of PureScript.

- It's not clear what the "big picture" of the PureScript project is.
- It's difficult to improve the core library experience without help from the creators or maintainers of it.

https://discourse.purescript.org/t/how-do-we-avoid-ecosystem-incoherence-in-the-future/209/14?u=chexxor

> However, perhaps we could do something more. We could at least make a good faith effort to notify people who maintain repositories available on Pursuit if their code is going to break in the new release.

- There can be better communication between maintainers of the language and maintainers of heavily-used libraries around major releases.

> Finally, there could be a “documentation team” which I also volunteer for

- A documentation team consisting of volunteers can help communicate release changes to language users and library maintainers.
- Release changes can be summarized and explained in a blog post, and include a migration guide.

### Comment (language user)

https://discourse.purescript.org/t/how-do-we-avoid-ecosystem-incoherence-in-the-future/209/15?u=chexxor

> Definitely a lot of good stuff to work on listed already (and it’s a little late for 0.12) but I just wanted to point out that releasing a new compiler version doesn’t need to mean it’s becomes the default.

- Documentation and tooling should not choose the latest language and library versions by default
- Documentation and tooling should be explicit about the language version being used and be conservative with upgrades.

### Comment (new language user)

https://www.reddit.com/r/purescript/comments/8qaiwl/purescript_first_impressions/

> pursuit is also great once you figure out how it works (some more top-level "what is this thing?" documentation would be good).

- New users like to use Pursuit to learn how to solve problems when writing the language.

> Probably the worst part of my PureScript experience was the FFI. This is an area where the language needs to be more generous with special syntax and compiler features -- it's crazy how much boilerplate I need to produce to write types for extremely common JavaScript patterns compared to other languages

- The FFI maybe needs better documentation, especially for a newcomer to statically-typed language.

> Take calling a method on a class for example: you need to make a Javascript file which wraps your existing method by doing exports.myMethodImpl = function(...), that function probably needs to return another function if it's an Effect, then you need to foreign import the function and wrap the arguments in a Fn3, and then you need to make another function that calls the first function and invokes runFn3 on it.

- The FFI documentation should explain the advantages of writing an out-of-PureScript implementation.

### Blog post (new language user)

https://sadraskol.com/posts/my-experience-with-purescript-so-far

> Purescript leaves you alone in the jungle of its methods and functional gibberish. If you don’t know what a Monoid, a Foldable or a <$> is, you better learn the language with tutorial first! It feels like the language wasn’t build for programmers first, but for Haskell programmers with strong theorical background. Could you easily guess what’s the difference between a Semi-groupoid and a Monoid?

- Newcomers to the language feel antagonized by the unfamiliar concepts and language operators.
- Perhaps documentation can mitigate the confusion and anguish experienced by newcomers.

### Comment (language user)

https://www.reddit.com/r/haskell/comments/5quf5y/learn_purescript_or_haskell_first/dd2i8pq/

> Haskell will have a lot more material (than PureScript) and a much stronger ecosystem so I'd go with that for now.

- Haskell has more documentation (but better?) than PureScript, so Haskell is recommended for newcomers.

### Blog post (new language user)

https://alpacaaa.net/blog/post/elm-purescript-in-depth-overview/

> Plus, a language that compiles to JS has to be approachable, right? Wrong. Purescript was as much confusing and frustrating as Haskell (in fact, they’re very similar languages).

- Users of compiler-to-JavaScript languages expect an approachable language.
- PureScript's new user experience can be a confusing and frustrating experience.

## List of Yet-To-Be-Analyzed Sources

The following quotes were found by searching the PureScript Discourse, Twitter, and Google for PureScript documentation, impressions, and experience reports.

> Core PureScript has great documentation (see the PureScript book, the Halogen guide and example repos). However, most of the rest of PureScript learns from Haskell by having mediocre documentation. You’ll need to become familiar reading types and briefly checking source code to see what’s going on. That said, we’ve rarely had trouble with documentation; most functions are self-explanatory and the functional programming Slack is great for filling in the gaps.
> https://www.reddit.com/r/functionalprogramming/comments/7vveeu/purescript_vs_reasonmlbucklescript_in_2018/dtw5qm7/

> I think PureScript is missing a full webapp step-by-step tutorial (front, back, database, mails, authentication, forms, validation…)
> https://twitter.com/ThibaudDauce/status/895534464071331840

> I tried PureScript, first impression was really good, but I was lacking some guidance for e.g. free monads etc. So deeper concepts :-) tips?
> https://twitter.com/raimeyuu/status/895379846938992640

> Building Purescript Puzzler was a great learning experience, especially since I’m not the most experienced web dev. I sunk my teeth into a few cool libraries and got my first real taste of FRP outside of toy examples. However, I still feel like thar be dragons lurking in the shadows with this approach, and the apparent lack of complex examples is not reassuring. I think part of the problem with this is the absence of wrapper libraries that make common tasks easier, which inhibits exploration.
> http://fluffynukeit.com/exploring-the-mvi-architecture-with-purescript-puzzler/

> I felt the same way. Learning PureScript wasn't difficult for me but I already knew Haskell. I can't imagine what it's like for someone who doesn't know Haskell to learn PureScript, because there are very few tutorials designed for that audience. Most of the docs on PureScript are very much "reference" style so you have to already know what you're looking for to even find them.
> https://www.reddit.com/r/haskell/comments/79i7h9/why_is_elm_more_popular_than_purescript/dp2ztyi/

> It also feels like PureScript is unmaintained. I tried PS out twice over a year or two and the docs were more or less the same (very sparse).
> ...
> A big issue for me, too, was that I felt like I was looking at Haskell docs to figure out how to do things more than I was using PS documentation. At that point, why not just use a Haskell compiler that targets JavaScript instead? And, if I end up using the FFI to include the majority of my JS code, can’t I just write functional JavaScript code in the first place and cut out the middle man?
> https://www.reddit.com/r/haskell/comments/79i7h9/why_is_elm_more_popular_than_purescript/dp2ngoe/

> Also, Purescript has this interesting property of being hard to learn (because it is powerful), but dead simple to use (because it compiles to JS). So you only really get stuck on figuring out how to do things in PS, as opposed to how to get PS working, and therefore every time you get unstuck, you have leveled up. So it's hard, but rewarding.
> https://vue-hn.now.sh/item/17125882

> However, I'd only put PureScript into production if I had people with Haskell experience and a good amount of time to become contributors. The community is friendly to beginners, but there's a vast amount of background that isn't explained in a systematic way, and the community standards for documentation and infrastructure just aren't up to the level we've come to expect from systems like Elm or Elixir or even Clojure.
> https://dev.to/marick/comment/52da
