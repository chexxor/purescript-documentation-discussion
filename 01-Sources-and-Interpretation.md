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

The rest of this document should be a list of sources, followed by an interpretation of that source that highlights the main ideas it makes.

## List of Sources

Such an opinion is held by long-time maintainers of the project as well as newbies to the language.

The following quotes were found by searching the PureScript Discourse, Twitter, and Google for PureScript documentation, impressions, and experience reports.

> We seem to have developed something of a documentation problem. Even now, the documentation repository is only partially updated for the 0.12 release, and generally it is quite unstructured and lacks a single vision for what good documentation should look like.
> ...
> There needs to be a plan for the future, and that plan needs to be documented. I would like to start working on a specification for the language, something which I consider essential for documentation purposes, but it doesn’t make sense to start documenting a language when there is no plan in place for the next milestone.
> - https://discourse.purescript.org/t/the-state-of-things/282

> I think that started with the initial release and has been true ever since. I can’t think of a time in PS’s history where we had docs resources that were good and up to date (book aside).
> https://discourse.purescript.org/t/the-state-of-things/282/5

> I would love to help – I’m not shy about writing documentation or putting time into these updates – but without being a core contributor I have no idea what these plans even are. As a consumer I largely find myself digging around readmes and docs that may or may not have been updated trying to guess at what ecosystem shifts have just happened. This is a little disconcerting as a heavily-invested commercial user of PureScript.
> https://discourse.purescript.org/t/how-do-we-avoid-ecosystem-incoherence-in-the-future/209/9

> Soul mate! There’s a ton of low-hanging fruit in even core documentation. I hope after 0.12 that pull requests like this one 53 for Data.Map get approved.
> https://discourse.purescript.org/t/features-you-want-future-purescript-to-not-have/115/5?u=chexxor

> pursuit is also great once you figure out how it works (some more top-level "what is this thing?" documentation would be good).
> https://www.reddit.com/r/purescript/comments/8qaiwl/purescript_first_impressions/

> Purescript leaves you alone in the jungle of its methods and functional gibberish. If you don’t know what a Monoid, a Foldable or a <$> is, you better learn the language with tutorial first! It feels like the language wasn’t build for programmers first, but for Haskell programmers with strong theorical background. Could you easily guess what’s the difference between a Semi-groupoid and a Monoid?
> https://sadraskol.com/posts/my-experience-with-purescript-so-far

> Haskell will have a lot more material (than PureScript) and a much stronger ecosystem so I'd go with that for now.
> https://www.reddit.com/r/haskell/comments/5quf5y/learn_purescript_or_haskell_first/dd2i8pq/

> Plus, a language that compiles to JS has to be approachable, right? Wrong. Purescript was as much confusing and frustrating as Haskell (in fact, they’re very similar languages).
> https://alpacaaa.net/blog/post/elm-purescript-in-depth-overview/

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
