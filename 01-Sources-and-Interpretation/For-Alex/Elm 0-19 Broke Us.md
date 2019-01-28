
## Source: Elm 0.19 Broke Us

### Comment

https://dev.to/wires/comment/52l3

> Where Elm takes you by the hand and steers you on a rather strict track PureScript gives you a powerful tool and maybe a bit too much freedom ;)

- PureScript is a more powerful language than Elm but provides less guidances as to how to write code

> It's not where Elm is yet (things get's brocken on new versions and it takes longer for the packages to get updated) but I'm really hoping that we will use PureScript over Elm in production once it stabilized a bit more.

- Source hopes to move to PureScript once it stabilizes more

### Comment

https://dev.to/kspeakman/comment/5224

> Thanks for the suggestion! I haven't looked deeply at PureScript. Although it sounds like a scary place right now. :) I also don't get as much into the Haskell-y stuff like HKTs and so forth. But I will check it out!

- One person's perception of PureScript is scary, possibly due to HKTs and other "Haskell-y" stuff

### Comment

https://dev.to/carstenk_dev/comment/5255

> It's really not that bad/complicated to learn (HKT's and PureScript) - but you gain some incredible cool powers ;)
> To give you a small glimpse: if you understand what `comparable` is about in Elm you basically understood type-classes. But instead of have a fixed set of them that only works with a predefined subset you can add you own types to them (it's called making your type an instance of it) and you can even define your own type-classes if you want, but that is rarely needed.
> If you understood what `Cmd` is about you are ready to talk about effect system - but again you can do it on a level where you are in more control of the runtime and where you are allowed to use effects (still everything is pure).

- Community member did a good job of using scaffolding to lessen the fear of PureScript: if you already get X ("comparable", "Cmd"), then Y (type classes, effect system) is X + 1.

> If you want to try it out this might be a good start: github.com/utkarshkukreti/purescri...
> this framework is very Elm-inspired and you should get a good idea (normally I would advise PUX but right now the documentation was not updated for purescript-0.12 and so this might confuse you too much)

- Another Elm-inspired framework recommended is `purescript-hedwig`
- Source advised against Pux due to lack of documentation

### Comment

https://dev.to/marick/comment/52da

> My original plan for An Outsider's Guide to Statically Typed Functional Programming was to transition from Elm to PureScript.

- A person intended to write documentation which helps one transition from Elm into PureScript

> Spork seemed to me the best PureScript implementation of The Elm Architecture.

- There is a library that feels similar to Elm to help Elm programmers transition to PureScript

> However, I'd only put PureScript into production if I had people with Haskell experience and a good amount of time to become contributors. The community is friendly to beginners, but there's a vast amount of background that isn't explained in a systematic way, and the community standards for documentation and infrastructure just aren't up to the level we've come to expect from systems like Elm or Elixir or even Clojure.

- No examples given of this 'documentation gap,' but I think everyone agrees it exists
- A newcomer believes documentation of the background of PureScript is necessary qualification of a production-quality language
- A newcomer believes the PureScript community's level of satisfaction of its documentation and infrastructure is less than that of other programming languages.
- A newcomer believes the PureScript community is friendly to beginners and contributors.

> This (lack of documentation/standards/infrastructure of PS compared to Elixir/Clojure) is not seen by the opinion leaders as a problem - I hope it eventually will...

- Source believes that PureScript leaders do not care about documentation/standards/infrastructure of PS
- The "leaders" are never defined here, but it probably refers to the core contributors.
- If that was the opinion of the leaders, why was that the case? Is it still the case now and if so why?

> ...but it makes PureScript something best suited for technology enthusiasts or visionaries.

- PureScript is not suited for mainstream use yet but more for forward-thinking people who may get burned by future web developments

> But my original hope - learning it well by describing it well, then using it for real work - isn't going to come to pass.

- Someone else has tried the Feynman technique, similar to Jordan's purescript reference work

> I'm thinking of trying ReasonML from the F#/OCaml line of hybrid FP tools. I think it would be an easier transition from Elm than PureScript would be.

- Elm as a "gateway drug" to PureScript may have competition from other FP languages: ReasonML

> Disclaimer: I was too strident in claiming that PureScript needs documentation and infrastructure up to the modern standard. Many PureScript people think I'm a jerk and also biased. I don't think so (at least about the bias), but they could be right.

- Source may have had disagreements with PureScript leaders that was fueled more by emotions than logical arguments and understanding one another's viewpoints.
- Source may have also just wanted really good documentation but did not receive the desired support from core contributors

### Comment

https://dev.to/wires/comment/52l3

> Agreed with the Purescript documentation, I takes a long time to become at home in that. Lot's of stuff is folklore and/or Haskell derived knowledge.
> Still less frustrating than Elm.

- General perception is that learning curve is steep and hidden behind a lot of jargon
- PureScript is less frustrating than Elm?

> Regarding ReasonML: it is like the saner brother of Elm, with a normal type system and mature tooling behaviour; in this way it's easier and better than Purescript, IMHO.

- ReasonML might be an easier destination for Elm users than PureScript due to being more mature in a few important areas.

> Both are highly recommended. FWIW, we are moving our code away from Elm to Purescript, Haskell, Idris and ReasonML.

- Source is moving towards langauges with stronger FP concepts than Elm.

### Comment

https://dev.to/mgajda/comment/52j6

> Switch to PureScript!
> It has type classes, elastic developer community, support for Node, and many other non-browser platforms!

- PS users might be watching Elm channels of communication as a way to encourage people to switch to it...?
