
## Source: "Learn Purescript or Haskell first?"

https://www.reddit.com/r/haskell/comments/5quf5y/learn_purescript_or_haskell_first/

Thread was created on Jan 19, 2017. These answers are likely not entirely true anymore due to the amount of change that has occurred since then.

> Hey, which language should someone learn first? There are good materials for learning Purescript.
> I'm just wondering if one language would be better than the other for beginners based on the design of the language / tooling.

The main goal is not "Should I learn Purescript?" But "I want to learn an FP language. Between Haskell and Purescript, which one is easier to learn since both use the same concepts that translate easily between both languages (e.g. type classes, Functor, etc.)?"

### Comment

https://www.reddit.com/r/haskell/comments/5quf5y/learn_purescript_or_haskell_first/dd2b1my

> I would pick haskell over purescript.
> Purescript is great but as a new language, there are a lot of usability aspects that are in the process of (rapidly) being smoothed out. For example, as of ~ 6 months ago the repl would slow to a crawl if I loaded more than 10 or so packages. Also, last I checked ps was piggybacking on bower for package management with a WIP stack-like alternative. Eventually I'm sure the latter will be superior, but afaik it's not finished yet.
> These are all being resolved very quickly, but expect "we're laying down tracks right in front of the train" kind of challenges in the ecosystem, tools, and the language itself.

- A number of these issues have been resolved whereas some others have not. AFAIK, pulp no longer responds that slowly. `psc-package` is that stack-like alternative mentioned above that is become more established. Moreover, `spago` addresses some of its shortcomings due to the tedious nature of modifying packaget sets. However, `spago` does not yet have as much support in various things as `psc-package`.

> Haskell can be rough in spots as well in the language/ecosystem/tooling, but overall it's had more time to mature.
> In learning Haskell, absolutely start with haskellbook.com and avoid learn you a haskell.
> Once you're comfortable, transitioning to purescript will be relatively straightforward.

- If one's goal is to learn an FP language, this isn't necessarily a bad idea since Haskell and PureScript are very similar and Haskell is arguably more powerful than PureScript. However, if one's goal is to learn PureScript or do website development, it would be unfortunate to learn Haskell before learning PureScript.

### Comment

https://www.reddit.com/r/haskell/comments/5quf5y/learn_purescript_or_haskell_first/dd2gz4d

> As a purescript contributor.... Another aspect to consider is quality of compiler errors: psc's type errors have improved hugely over the last year or so, but I think it's still going to be a little while before they measure up to GHC's.

- GHC has better error messages than PureScript. This was likely true. I'm not whether that gap has decreased in the last year or not and by how much. I think it's likely still the same.

> I know that starting with PureScript is possible because I've spoken to people who have done so, but I do tend to recommend Haskell for people who are completely new to FP.

- a core contributor did not recommend PS to people new to FP seemingly because the learning resources for PS were not as good as Haskell's.

### Comment

https://www.reddit.com/r/haskell/comments/5quf5y/learn_purescript_or_haskell_first/dd2wkc8

> I much prefer the newer Haskell from first Principles. It comes with exercises, and a bit more formality.

- The Haskell book has exercises in addition to its explanations.

### Comment (language user)

https://www.reddit.com/r/haskell/comments/5quf5y/learn_purescript_or_haskell_first/dd2i8pq

> Haskell will have a lot more material (than PureScript) and a much stronger ecosystem so I'd go with that for now.

- Haskell has more documentation (but better?) than PureScript, so Haskell is recommended for newcomers. It's not entirely clear whether the Haskell documentation is "better" than PureScript, but it is implied.
- Seems like Haskell had more material than PureScript: if one did not satisfy you or help you, you could look at another tutorial/guide. If you encounter the same situation in PureScript, tough luck as there isn't another tutorial/guide.
- Haskell's stronger ecosystem might make it easier for the OP to learn domain-specific concepts (e.g. parsing, cryptography, etc.) in an FP style

### Comment

https://www.reddit.com/r/haskell/comments/5quf5y/learn_purescript_or_haskell_first/dd270gt

> I'd recommend Elm for a beginner. It's a much simpler type system than Haskell or Purescript, so you can learn the basics of static typing and immutable programming before dealing with typeclasses, monads, GADTs, etc.
> The community is very beginner friendly, and it's pretty easy to go from nothing to a fully functional web app quickly.
> Not saying you shouldn't learn Haskell or Purescript, but if you're specifically looking for a gradual introduction, Elm is the way to go.

- It seems if one wants to do web development using an FP paradigm, Elm has better learning resources to help one get familiar with the concepts before switching to Purescript. Again, Elm as a "gateway drug" into PureScript seems like a good possibility.

### Comment

https://www.reddit.com/r/haskell/comments/5quf5y/learn_purescript_or_haskell_first/dd2khmb

> [whether Elm is good for beginners] really depends on what that beginner [wants] to get out of learning a new language...
> - Know a general purpose functional programming language -> not Elm
> - Get experience with typed FP -> Any of 'm (Elm, PureScript, Haskell)
> - Learn the "hard parts" -> PureScript and Haskell
> - Not get stuck too much in the beginning and/or have a soft learning curve -> Elm
> - etc.

- Elm seems to provide a gentler introduction to FP concepts than Haskell or PureScript primarily because it has less features and potentially has better documentation than PureScript did at that time.
- If one wants to do FP web development and get the full power of FP languages and is willing to pay the cost of a steeper learning curve, then they should start with PureScript. Still, this learning curve could be made less steep if there was more beginner-friendly documentation.

### Comment

https://www.reddit.com/r/haskell/comments/5quf5y/learn_purescript_or_haskell_first/dd35zno

> PureScript because:
> - Easier setup and ecosystem maintenance on your machine.
> - Type system is as powerful as Haskell's (compared to something more simple like Elm), while not inheriting its historical marks. You get something more polished upfront.
> - Good reference book, PureScript by Example.

- PureScript by Example is now outdated, so the "good reference book" isn't as strong of an argument
- PS' type system is more granular, powerful, and polished than Haskell, avoiding some of its baggage.
- While this person argues that it's generally easier to install and maintain PS than Haskell on a machine, that comment did not account for the major breaking changes that occurred in the `0.12.0` release. Other comments in this post also argue against this point.

> PureScript focus on Web, Haskell is more general, but in case you're only interested in playing with a functional language, I'd pick PureScript for that.

- This is a good summary.

> I've read LYAH and other haskell materials and courses (CIS 194), as well as PureScript by Example. Played with both (Elm too just a bit before learning of PureScript), and that's my conclusion taking a beginners POV.

- Good insight here: one can look at material from all three languages (PS, Haskell, Elm) to get a better understanding for how the code works.

### Comment

> This kind of experience (3 attempts at dealing with Haskell's build tools) I don't go with any language I try, which are several. With PureScript I do everything per project, but still, this is lightweight, this doesn't take insane amounts of time/disk/processor/home-bandwidth to install, compile, nuke, upgrade. Regardless using bower or not. The pacman setup for PureScript is just pulp and purescript, just that and I maintain my user setup up-to-date and can deal easily with per project maintenance.

- In short, in this person's experience, PureScript is easy to set up and start coding unlike Haskell in various ways

> Maturity doesn't necessarily equate to easy of use. I realize PureScript is evolving and unstable, I've gone through some instability with it too at time I started, PureScript by Example was on 0.8, and I just installed the compiler at the week it upgraded to 0.9. Still I could deal with that, it's understandable, the language is "new", and it was more fun than hassle actually, figuring out what had improved from compilation errors.

- Key point here "It was more fun than hassle actually."

> ... with PureScript you get something more polished in the details ... and don't confront years of evolution of a language, which you may have to toggle through compiler flags and pragmas.

- PureScript doesn't quire adding language extensions like "OverloadedStrings" or running it with `-Wall`

> On the community, sorry to say, but I found the PureScript community more friendly, and I felt the Haskell community too biased to its language too. I judge this way b/c I've used several languages and got in the mindset of several, I find bias instances in all of course, maybe this gets stronger with maturity, a side effect. In the haskell community I found some bias that were too stupid. I talked with a friend of mine another day when I mentioned something about Haskell and he got curious and asked about my haskell experience, just to confirm his own was the same, so I thought I was not really being crazy in my judgments.

- To one person, Haskell's community seems less frinedly / welcoming than other languages' communities in general and the Purescript community specifically.

### Comment

https://www.reddit.com/r/haskell/comments/5quf5y/learn_purescript_or_haskell_first/dd2hmdm

> For beginners, I would tend to go for well-supported languages with mature ecosystems and active communities. This minimizes the amount of inane work you have to do getting things working on your computer, and maximizes the number of people who can help you out when you have a question. By this metric, Haskell is the obvious winner.
> I wouldn't sweat language choice too much, however.

- This factual statement just explains that one will be more productive overall in langauges that have more mature ecosystem and active communities. However, if one wants to specifically do web programming and not use Haskell's solutions to that problem and needs something more powerful than Elm, then one seems limited to Purescript, Elixir, or Closure.

### Comment

https://www.reddit.com/r/haskell/comments/5quf5y/learn_purescript_or_haskell_first/dd4w8hp

> Haskell is immensely more powerful so I would not say they're the same. Also Haskell has language extensions.
> I'd say the only reason you should learn PureScript is if you want to learn PureScript for web/JS replacement and don't care about functional programming beyond that.

- This person seems to think that PureScript is limited to only web-related things and does not factor in the 'multiple backends' that make it more viable in the long-term.

### Comment

https://www.reddit.com/r/haskell/comments/5quf5y/learn_purescript_or_haskell_first/dd5uycd

> This is not true. Functional programming can be learned from PS quite well, and from start, as has been said, you don't have to go through many ancillary language scars. Example as said already,
> - uniformity of monoid operations,
> - row types for finer grained IO,
> - PureScript by Example covers quite beyond the introductory materials I found for Haskell at the time, ranging to monad transformers and other more advanced material while still not being verbose.

- PureScript no longer uses `Eff` and row types for finer-grained effects. Rather, it uses `Effect`. This was also something that Phil also later admitted was a good decision.

> The knowledge applied with it can be transposed to other FP contexts in general later.

- This just highlights that learning one language or another does not matter since the type classes and general foundations apply equally to all of them.

> Also technically, there's no impediment that PS move to other waters, as there exists already experimental C++ transpilers for it for example.

- PS' long-term value is that the language can compile to multiple backends quite easily. Still, the exact performance considerations are not as clear as one library maintainer realized when writing `purescript-sequence`, a FingerTree implementation that was slower than Array until its size got very large.

### Comment

https://www.reddit.com/r/haskell/comments/5quf5y/learn_purescript_or_haskell_first/dd8bb2e

> Elm, Purescript and Haskell are on a continuum. Which one to learn first depends on how steep you like your learning curves.
> Learning first Elm, then Purescript, then Haskell, has the gentlest learning curve, especially if you haven't had FP experience before.
> Elm gets you used to the syntax, immutability and purity, while being a very practical tiny language that you can learn in a week or so.
> Purescript adds typeclasses, and higher abstractions. The typeclasses hierarchy makes more sense in Purescript, because they learned from Haskell, and they could get it right from the start, without any backwards compatibility worries.
> Haskell adds laziness, which while cool, can be complex, and language extensions, which are very powerful.
>
> If you don't care about the steepness of the learning curve learn whichever you are actually going to use, eg. if you want to compile to native Haskell is better atm.

- Good summary of the learning curves of these languages: Elm is lowest, PS is next, Haskell is highest.
- The target / purpose for learning FP langauge should be the controlling factor.

### Comment

https://www.reddit.com/r/haskell/comments/5quf5y/learn_purescript_or_haskell_first/dd2hr43

> Haskell and Purescript both have "parametric polymorphism" and "type classes" and this is the most powerful thing in each language by far (besides ya know the lambda calculus). Haskell does each of these things with much more intuitive syntax in my opinion though Purescript is deployable in a more easily profitable context and has a lot of deployment resources which overlap with JavaScript which is arguably a great thing.

- PureScript can tap into the larger Javascript ecosystem via its easy FFI. However, this doesn't factor in situations where those libraries were not written in an FP style, thus making such FFI harder. Also, since it deals with Javascript, one doesn't know whether an exception will be thrown unexpectedly by a library. So, this isn't as good of an argument as the person might think.
