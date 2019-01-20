
## Source: Wallowing in Dispair

https://gist.github.com/marick/e8b01375309fafaefb879c4840b6da75

### Opening Gist

> Many of you have reacted to my wallowing-in-despair tweet by complimenting my book. Thank you! I think it's a good introduction to Elm, teaching it in an interestingly different way.

- Book teaches Elm in a different manner than usual.

> What it is _not_ is the book I hoped to write, which had three goals I really believed in:
> 1. "The book teachs the ideas and idioms of statically-typed functional programming...."
> 2. ... And so I imagine those two women as FP insiders, seeing this book as unrigorous clownish capering, what with the idioms and messy systems and all.... So she gives me hope this book will find favor with both outsiders and insiders."
> 3. ... I find Elm a bit too opinionated (and I worry about the sustainability of a language that depends so much on one person). So I had this dream that PureScript would be a great next step for people like me: Elm, but more (typeclasses, effects, etc.) So the book was conceived as a progression from Elm to PureScript.

- Books goals were:
    1. teach FP idioms
    2. be well-perceived by both those already familiar with FP and those who are not
    3. progress the reader from Elm to PureScript

> Although PureScript was (and is) less of a "whole product" than Elm, I thought it would inevitably become one. It seems to me that various of the modern languages (like Elixir, Rust, and Elm) have raised the bar for what is required for a mass-audience programming language. Surely all ambitious languages will adapt to the new reality.

- Author's belief was that PureScript would 'raise to the bar' that other languages had set

> After some months of succumbing to the sunk cost fallacy, I've concluded that I should stop kidding myself that I'll achieve those goals.

- Author believed goals would be achieved but later realized and accepted after much denial that they would not be achieved

> The insurmountable-by-me problems are [each of the 3 reasons are covered separately]:
> 1. My book has not wooed the static FP opinion leaders. For example, it's been surprising how definite people have been that a progression from Elm to PureScript/Haskell is stupid.

- It seemed the FP community responded with something like, "Why the hell would one start with Elm and then transition into PureScript? Why not just start with PureScript?"
- The author's first goal was not realized and it seems there is nothing he can do to fix/change that.

> 2. As another example, I can't interest people in the idea that fuzzy things like idioms, patterns, and habits are worthy of study and writing down.... It's not realistic for me to harvest these things without the enthusiasm of fluent practitioners (of the sort that collaborated in the early patterns and agile movements).

- It seemed the FP community thought that studying and documenting idioms/"design patterns"/habits of good FP programmers wasn't worth it.
- It seems hard for the author (who is not as well-versed in FP idioms) to document them when those who know them don't care enough to share them.

> 3. I no longer think PureScript is a good next step after Elm. It's a language for enthusiasts-to-visionaries and true believers and people motivated by intellectual curiosity (that would be me), and I think it will continue to require too much work for it to be adoptable by my target audience. That leaves me without a good next step in the book, _and_ without one for my own projects.

- There are other FP-like languages out there besides PureScript that might be a better 'next step' for Elm programmers.
- PureScript tends to draw intellectually curious people.
- The author probably thought, "Well, crap! How do I end my book now since I no longer assume one of its main presuppositions? Moreover, which language do I use for my own software projects now?"

> My core conclusion is that, when it comes to learning what the Haskell tradition has to teach, the "outsider" I write for has Elm and then... no good option. There's value in the rest of that tradition, but I just can't honestly tell **my particular audience** it's worth the effort to search for it among the dated practices, clashing final vocabulary (personal axioms), and low standards in important areas.

- There is no clear path (learning path perhaps?) from Elm, which has a gentle learner curve, to a more powerful general-purpose FP language.
- Each non-Elm language, general-purpose pure FP language, seems to have pros which are outweighed by the "warts" of the language.
- The author's point-of-view is as an Elm programmer looking for a "post-Elm" language.

>>   My goal is to make the most compelling case I can that static FP will give you new abilities, especially new abilities for modeling a messy domain riddled with exceptions to the rules. [...]
>> For early readers, I should note that I am not yet myself convinced the case is compelling...
>
> I'm now thinking I've convinced myself it's not.

- Author started book with presupposition that static FP languages are worth their learning curve but has now concluded that perhaps this is not true.

> Elm is good. Outside the Haskell tradition, F# seems good and ReasonML seems promising. But, when it comes to the more purely Haskellish languages, the motto ["avoid success at all costs"](https://www.reddit.com/r/haskell/comments/39qx15/is_this_the_right_way_to_understand_haskells/) has been achieved.

- Those that follow Haskell tend to follow its motto, "avoid success at all costs," which the author seems to interpret (via implication) as "avoid mainstream usage at all costs."

### Comment

https://gist.github.com/marick/e8b01375309fafaefb879c4840b6da75#gistcomment-2568976

> I think a problem with goal 1 ("the ideas and idioms of statically-typed functional programming") is that often these are somewhat language specific. Haskell, PureScript, and people who use Scalaz/Cats use the same sorts of abstractions (predominantly based around the Functor/Applicative/Monad hierarchy, Monoid, etc), but Elm doesn't really have that at all, so there's a huge step there. I'm not as familiar with the non-Haskell MLs, but I get the impression they're not used as foundations there for the average program.

- Some FP idioms exist across FP languages (e.g. type classes) whereas others are specific to the language. As an example, the commentor believes that Elm doesn't have the same idioms as languages like PureScript.
- The commentor might be implying that all statically-typed FP languages don't share a common set of idioms.

> Regarding insurmountable-problem 1, that is strange and unfortunate. I don't see why people would think that going from Elm to PS/Haskell is stupid. I've seen evidence of people making that transition. It seems like somewhat less of a step from JS (and that's doable too).

- A core contributor doesn't think the "Elm -> PS" path is a stupid idea. In some ways, it might be better than the "JS -> PS" path some others take.

> I'm not too sure how "My book has not wooed the static FP opinion leaders" is relevant, the book isn't for them? > I also don't know who these people you refer to are :smile:

- Seems like the commentor is saying, "Wait. Is the book for the FP community, too? I thought it was only for Elm programmers...

> I think the attempt to do what you describe in problem 2 is interesting, I'd also have no idea how to do it. These things (that aren't concretely based on things like particular abstractions - I assume that's what you're getting at) are difficult to spot due to their very nature, since they become unconscious habits. The only things I can think of right now though is the idea of making illegal states unrepresentable, choosing the smallest possible type that can accurately describe something, avoiding booleans, things like that... is that the kind of thing you had in mind?

- The goal of documenting FP idioms is a great goal, but it's not clear how this could be done easily.
- Many FP programmers don't consciously know the habits they have developed over time. Some habits, they may take for granted and assume others do likewise, being surprised to find that others don't.

> I can't argue with 3, since it's a (perfectly valid) opinion. It also goes to that question that people ask periodically and we hate... "is it production ready?" :wink:. The answer depends a great deal on the person who is asking and the situation they're in. I've been employed writing PS for a user facing product for 3 years, so to me the answer is most definitely yes, but I can totally understand why that is not true for everyone.

- Whether "PureScript is production-ready yet" depends on one's use-case, which is different for everyone.

> There is a reason we've not made a 1.0 release yet. Progress is slow on documentation and things because nobody gets paid to directly work on PureScript, so it has to fit in whatever free time contributors have, along with actual fixes and improvements to the languages and core libraries.

- Volunteer-based languages and their development do not have the same luxuries/resources as other languages. The desire to get somewhere exists, but not the time, especially when language changes/improvements break current documentation.

> I noticed a point you have in the conclusion here that you consider Elm to be part of the Haskell tradition, and personally I'm not even sure that's true. They have similar syntax and both are pure, but that's about all they have in common. Maybe that's where a lot of the struggle comes from? It would perhaps explain some of the "incommensurability" issues.

- FP language's roots and similarities do not seem to be well-understood by outsiders and may contribute to outsiders' lack of understanding or initial expectations about FP languages that get broken.

### Comment

https://gist.github.com/marick/e8b01375309fafaefb879c4840b6da75#gistcomment-2569097

> I think you might be surprised by how such ideas (like type classes) are embedded in Elm without the mechanisms Haskell and PureScript provide. Types that are functors have a map. It's not polymorphic in the editor/compiler, but it is in the programmer's head. andThen is the same as bind, but pipelining is favored over do notation.

- Probably addressing the last thought in the previous comment, the author shows that Elm has more in common with PureScript than the commentor thought.

> In my experience of being an outsider, I succeed when I gain the respect of an insider who is willing to say to other insiders "This guy is probably wrong, but worth taking seriously".

- The author's definition of being welcomed into a language community is when an "insider" tells others to listen to him, even if he's probably wrong.

> You are an opinion leader. False modesty is common, and admirable, but support of the "worth taking seriously" type from you, or Freeman, or Hegemann would have a huge impact.

- Getting support from core contributors would greatly impact the author's work.

> The OO world has a ton of experience harvesting idioms and such. It shouldn't be ignored. Also, other academic fields have experience in such things. My wife's a professor of veterinary medicine, and they do it. I've been at retreats where veterinarians (because of their rules for continuing education, a mix of academics and practitioners) talk about practices. Dinnertime conversation is boring to the outsider, fascinating to the insider, because they're a community of practice that is explicit about what they are. Most programming communities are, too, but don't acknowledge it, which makes their teaching broken - or, rather, focused on a minority that can get through the hazing of broken teaching.

- The author believes that all fields of study need to document their idioms (best-practices?) and discuss them. The author says that programming communities (and FP communities specifically) do not tend to do this.

> A canny move in the development of PureScript would be to elevate the status of people who write documentation. "Nobody gets paid to directly work on X" is true of many technologies. Some have more success at documentation. Why?

- One cannot use the "nobody gets paid to do it" reason as an excuse for poor documentation. Others have the same restraint and yet still succeed.

> Not being sure Elm is part of the Haskell tradition: to me, that's an astounding statement. If not, what tradition is it a part of? Consider that your reaction might be an example of the narcissism of small differences (In this special case, ignoring all the commonalities in favor of the differences most important to people of your affinity group.)

- Saying that Elm is not a part of the Haskell tradition seems like a stupid thing to say because of how obvious its truth seems to be.

> There is so much knowledge out there that the static FP community pushes away for aesthetic reasons.

- The author believes the FP community is blind to/ignores the idioms and practices of the wider programming language community because the FP community values aesthetics (over pragmatism?).

### Comment

https://gist.github.com/marick/e8b01375309fafaefb879c4840b6da75#gistcomment-2569233

> Maybe you're right, it is a long time since I used Elm. I just wonder what would motivate the average Elm user to think of things in those terms (Functor, Monad) when there's no reason to do so - the abstractions that make use of those things generically are not really easy to leverage in the same way. I can see that recognising map and andThen as patterns that many types can implement would occur commonly, just not the more theoretical way of looking at those things.

- PureScript core contributor says that Elm users don't think in terms of Functor/Monad (because those terms aren't in their language/libraries?). While these patterns have naturally emerged in Elm, their community doesn't think/design in terms of it.
- The PureScript core contributor may be implying that the difference between a programming language community which uses terms referring to academic theory and one which simply applies the benefits of the theories is that members of the former community thinks in terms of theory while members of the latter are blind to the theory when developing their programs and think only in terms of their program's domain.

> Haskell is explicitly a language designed as a common base for exploring the implementation of pure non-strict functional programming languages and practices. It's not even one language really, given the many and varied extensions and what they can do to change it. A very real-world-usable programming language falls out of this, but it was not the original motivation.
> Elm is not a general purpose programming language, it's designed with a clear goal in mind, primarily guided by one individual, with a focus on simplicity and ease of use. Doing things outside of its intended focus is somewhat discouraged (the whole native thing being locked down recently).

- The PureScript core contributor believes that "the Haskell tradition" is having the purpose to explore FP languages, their implementations, and their practices.
- The author, in contrast, believes that "the Haskell tradition" is having the language features of Haskell and the idioms used by the Haskell community.
- It seems the author and the commentor were using the same word to mean different things.

> Maybe we have different views of what it means to be in the Haskell tradition? For what it's worth, I'd say PureScript isn't intended to follow it indefinitely either, although we're not out of that phase yet (since language features are still being introduced occasionally).

- The PureScript core contributor believes that PureScript follows Haskell for now, but might not in the future.

> I really don't think the differences are that small - there are fundamental differences in philosophy. I would have made attempts to start contributing to Elm rather than PureScript back when I did, if I thought Elm was following a path I was interested in. It was certainly a lot further ahead in actually being usable than PS was at the time.

- Highlights that there is a large philosophical difference between the two languages.

> Also, for what it's worth, I think Elm is a perfectly usable language and totally understand why people would choose it, the advantages its approach has when it comes to learning, and so on. I don't feel some tribal affiliation to PS that means I must disregard its successes or strong points; if I intend to criticise aspects of it I'll be explicit about it (for example, when I mentioned "doing things outside of its intended focus is somewhat discouraged", I can see how that would read as taking a shot at Elm, but it's meant as purely a factual statement).

- Core contributor is perfectly fine with saying, "PureScript shouldn't be used if one can accomplish their goals using Elm."

> I'm also not too sure what that support would look like! I try to engage with your questions/problems with PS on Twitter, I'm very much in favour of your work on adding documentation to -profunctor-lenses. Regarding the book specifically, I admit I've not been very useful there perhaps, but I don't know what I can offer there - I don't read programming books (I have to pound information into my head by doing... books, talks, papers, etc. only become useful when I've already achieved half an understanding on my own terms).

- Core contributor does not know what extra support the author expects while the author is contributing to PureScript.

### Comment

https://gist.github.com/marick/e8b01375309fafaefb879c4840b6da75#gistcomment-2569261

> A fair point (regarding not using 'nobody gets paid' as an excuse for poor docs). There is the issue that accepting documentation does mean it has some need of being reviewed too though, and I find that significantly harder than reviewing code a lot of the time. Writing/editing/explaining is a very slow process for me.

- Core contributor believes that accepting documentation means it needs to be reviewed.
- Core contributor believes that some people are better or faster at reviewing documentation than others.
- Core contributor believes that reviewing documentation can be just as difficult, if not more so, than reviewing code.

> Just to wallow for a second... I contribute to/review stuff on the compiler, attempt to keep on top of the issues, discussions, PRs on roughly 75 libraries (some of which are tiny and almost never change, some of which are purescript-dom grimacing), engage with people on Twitter, StackOverflow, Reddit, Slack, and very occasionally investigate some idea of my own. So unless I stop doing some of that, there's no chance I can make any meaningful steps to improving the documentation situation.

- A core contributor is already stretched thin with maintaining code, so asking for better documentation is too much to ask.

> But yes, I suppose it's true - I could choose to stop doing some of that perhaps. But after thinking about this for a while, doing those things is more valuable to me than dealing with the documentation situation, right now at least. It's not that I don't care about it, it's just that I care more about being able to make stuff than I do about explaining it to everyone. A somewhat selfish position to be sure, but I'm trying to be honest.

- The author's incentive is to improve the language to help him make better programs, not necessarily explaining the language to others.

### Comment

https://gist.github.com/marick/e8b01375309fafaefb879c4840b6da75#gistcomment-2570153

> PureScript - and you - don't have to go it alone!
> There are people with experience harvesting and writing down idioms/habits/etc. I happen to be one of them. But leave that aside, because it's too big a leap, I think.

- Responding to core contributor's post about being stretched thin, the author suggests sharing the load with others.

> When it comes to documentation, the trick is not to add more work to the existing community, it's to broaden the community. There are people who've done that, whether intuitively or with a plan. (I am not one of them.) (There are even people who study such things, like Nadia Eghbal.) They could be learned from. Though not an expert, I have observed the primates-we-call-human for a long time, and I know part of it involves high-status people making low-status jobs higher status. It's a fairly low effort force multiplier.

- Author believes it's best for people with high status in a community to find ways to make low-status (unattractive?) jobs more attractive.
- (This reminds me of the point that the Elm creator mentioned in his talk about "The Hard Parts of Open Source")

### Commment

https://gist.github.com/marick/e8b01375309fafaefb879c4840b6da75#gistcomment-2570172

> My efforts to help with PureScript API documentation are going too slowly to maintain my enthusiasm. But you don't have time/devotion to make things go faster.

- The author believes that enthusiasm in contributing to docs lowers when it takes a long time to make a contribution (without getting a reward, like a merged PR?).

> So let's change the process for the lens repo.
> 1. We (mostly you) collect people who are willing to watch the repo and review my changes.
> 2. You give me commit rights, but I pinky-promise only to change documentation.
> 3. If I get a thumbs-up from someone on the technical good-enough-ness of a doc pull request, I merge it.
> 4. If you're worried that technical incorrectness will slip through, I'll (a.) be perfectly happy to put a disclaimer that any such screwups are my fault, not the package author(s), and (b.) I promise to address them within a week.
> If I go crazy and change the code or sneak really bad documentation past everyone, you revert and then destroy my reputation. (If you want, I'll find volunteers with reach in the communities whose opinions I care about, and get them to agree to help destroy me.)

- The author believes that being trusted with commit-rights to a library will encourage him to be more productive.
- The author believes that it's OK to allow a slightly-incorrect piece of documentation to exist if it's clear the documentation author is different from the code author, and the documentation author promises to maintain the documentation.

> (Could work for more than lenses. It's twelve days and counting for the first comment on - much less an acceptance of - a trivial change to Data.Map: putting the functions people are more likely to be looking for at the top of the list.)

- The author cites evidence that even a trivial change to a core library goes unmaintained for weeks.

### Comment

https://gist.github.com/marick/e8b01375309fafaefb879c4840b6da75#gistcomment-2570222

> Ok, sounds good. And I am sorry about how slowly things are going, it's particularly bad at the moment because we're trying to make a 0.12 compiler release (w/corresponding library updates).

- Core contributor thinks idea sounds good
- Core contributor was prioritizing an important breaking-change release in the compiler and updating libraries to work with it over improving current documentation.
