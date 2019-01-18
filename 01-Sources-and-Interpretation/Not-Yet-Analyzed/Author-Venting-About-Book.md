
## Source: Author Venting about Book (tweet)

https://twitter.com/marick/status/988453595220795392

### Opening Tweet

> Today I feel: my book was a stupid idea that everyone-who's-anyone hates or is at best indifferent to, and I've wasted about a year of my life, and I'm a dislikable person, and my need to be useful is an illness. Hello, depression, my old friend.

- Author is in a very negative emotional state and is likely venting as a way to express those feelings and process those feelings. Author perceives that people with influence either hate or are apathetic about his book. Since the book did not accomplish it's goals, it felt like a wasted year. Author percieves that author's desire to help is perceived by others as a problem, not a blessing. It seems like this pattern of 'not being recognized/heard' has happened before.

### Thread: FP develops a community culture that restricts them from bringing it mainstream

https://twitter.com/Kray1og/status/988457589284528129

Key comments are below:

> "I'm now thinking I've convinced myself it's not." How can that be wrong? It's a very useful data point.

> Don't understand.

> I often say that empirically we won't know if Haskellish languages have truly avoided success - or added how much net benefit - after about 40 years. In the meantime we need prophetic people who try to assess it for 'mainstream applications' as you say. Hence I think of Levin 1/
> …which is a big compliment to you. (Until after about 40 years I meant.) You've asked a key question. If you've convinced yourself there isn't a 'compelling case' (partly for ST FP culture reasons as well as 'essence') for a positive answer that's a data point in advance for me.

> Ah. What I'm most convinced of is that the track forward seems to be toward a subculture of a certain type of person (created via some combination of innate preferences and acculturation) that there won't be enough of to make all that much of a difference.

- It's hard to say whether Haskellish languages were actually successful after 40 years, so we need people who assess it now and make predictions.
- Biggest concern author has: the kind of culture that FP languages tend to develop never grow large enough that they make an impact/difference in the mainstream.

> You're making me want to read the book - ahead of others in the current backlog. The FP subculture not wanting to share in terms of evolutionary idioms/patterns, among other things, that would make it more amenable/empathetic to outsiders? Anyway, don't mind me, gotta read it.
> ... [other tweets clarifying things] .... I was trying to understand what you meant by "subculture of a certain type of person (created via some combination of innate preferences and acculturation) that there won't be enough of to make all that much of a difference". But no rush

> Well, my sentence wasn't exactly clear, either. The key thing is that the discourse/habits/shibboleths of static FP select for people who are (or are well-placed to become) of a certain type. 1/4
> (Pseudo-intellectual alert: that is, it attracts or creates - in University, mainly - people with a particular "final vocabulary" http://www.exampler.com/testing-com/writings/final-vocabulary.html …).) 2/4
> People matching that type aren't the right ones to open static FP up to other types of people (the most populous subcultures of programming). So: a tight reinforcing loop. 3/4
> This is a pessimistic assessment, born of a pessimistic moment. I could be wrong. 4/4

- Author clarifies what that 'subculture' is while being in a very negative emotional mood:
    - it attracts/creates people who use a particular language
    - these kinds of people aren't the best ones to share it with others / show convincingly that FP languages are better than the status quo.
    - This situation continuously loops and the problem never gets fixed.

### Thread: What is the 'missing link' between 'blue collar programmers' understanding 'static FP languages?'

https://twitter.com/hmemcpy/status/988453806362021889

Key comments are below:

> I think your perspective on how suitable PureScript is, as a step after Elm is probably right. I'm trying to think about how to express my thoughts here...
> There is SO MUCH amazing stuff in the FP world. Like, sorcery. Ocaml's side, Lisps and Haskell's side all hold such phenomenally beautiful, useful, and reliable things. It's just so difficult to either lead people to it, or bring it out to people.
> All the major FP contenders are now "best of breed", the others have died off. But they're "best of breed" as a result of very specific focuses and several features (accidentally or intentionally) butting together to form a value prop bigger than the sum of its parts.
> Kmett did a talk on why Haskell is good, and it's the sum of several features leaning on each other to let you write code with shockingly broad mileage.
> So I really don't know what the step is. Elm is not a bad "first" step. But it's not the general purpose programming language I think people need. PureScript, despite being smaller, is certainly not "simpler" to program in then larger languages. I think there is a missing step.

- Elm is a not a bad 'first step' but one quickly realizes its limitations when someone tries to do something outside of its intended scope.

> I'd be tempted to just go with Haskell, but PureScript seems easier. Also, I want something for the front end, for my own purposes. I link to that talk would be great.

> [Next reply was the link] - [Edward Kmett - Type Classes vs. the World](https://www.youtube.com/watch?v=hIZxTQP1ifo)

- Basic ideas of this video:
    - Type classes were 'discovered' because one guy misunderstood what another guy meant
    - **Type classes allow a programmer to use "dumb reusable types" (e.g. `Either`, `Maybe`, `Tuple`, `List`) whose contained types (e.g. the `Int` type in `Maybe Int`) are later 'constrained' with the required properties need to do some computation (i.e. a number-like type that can be added via `Monoid`)**
    - There are two styles of 'type classes:' real type classes and 'implicits' (Scala's type classes, Rust's "traits", etc.)
    - Implicit-styled type classes are more "powerful" in one degree but end up leading to possibilties that make programming harder. Haskell type classes do not add this 'benefit,' so using type classes are more reliable and easier to reason about. The key issue is commutativity: if some type has an instance for a sub type class (e.g. given there is an `Ord a`...), then logically there are ways to determine its intance for a super type class (e.g. ... then there is alos a `Eq (List a)`)
    - Addressing "but why can't we just do X" reasons (including his thoughts for why Coq/Agda/Iris or, `a`, etc. other dependently-typed languages won't provide the 'refactor and it still works' guarantees of Haskell)

> Have only watched part of this, but I note that the idea of pushing constraints down into uses ("what beginning Haskell programmers miss") is *exactly* the sort of thing I wanted to do in the book.
> It's the sort of tacit knowledge, community-of-practice knowledge that *can* be written down.

- Referring to the bolded part above, this is the kind of knowledge that struggles to make its way out of the FP community.

> Very few people have been as tireless in their quest to explain the realities of Haskell as `@kmett` has. The number of times he's politely endured comments about lens errors alone is worth a medal. He's also involved with many notable advances in common use in the last 10 years.

- `@kmett` might be a good person to follow for extracting FP knowledge that remains otherwise stuck in 'knowledge silos.'

> There must be a way to leverage this to make static FP languages more understandable to "blue collar programmers". I think my https://leanpub.com/outsidefp  is floundering because there are so few points of contact between two communities.

- Author reflects that there is a missing point of contact between two communities, so that it does not succeed in either one of them. The implied communities are the non-FP / mainstream community and FP community.
