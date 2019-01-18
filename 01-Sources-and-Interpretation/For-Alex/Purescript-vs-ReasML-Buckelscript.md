
## Source: Purescript vs ReasonML / Buckescript in 2018

https://www.reddit.com/r/functionalprogramming/comments/7vveeu/purescript_vs_reasonmlbucklescript_in_2018/

### Opening Thread

> Which language would you pick for a new project in 2018, that has an imporant browser component?
>
> Last year I looked into both, found the OCAML documentation and error messages extremly lacking, and enjoyed purescript much more.
>
> However, it seems that purescript stagnated since and reasonml is building up steam.
>
> What's your guys impression as of early 2018 regarding advantages, documentation, ecosystem (JS interop, well documented libraries) and future-proofedness (is this a word?) of these platforms and which one would you pick?

- main focus of author is: which language is best choice in 2018 for a new project that requires important browser components? This author is not looking to write libraries and stick with anything long-term. Author seems to want productivity _now_ once language is learned.

### Comment

https://www.reddit.com/r/functionalprogramming/comments/7vveeu/purescript_vs_reasonmlbucklescript_in_2018/dtw5qm7/

> My company uses PureScript (with Halogen) for the frontend of our web app with Python on the backend.
> PureScript is mature enough for our entire frontend to be built in the language; we’re halfway through transitioning from an Angular app.

- Commentator's background: transitioning an Angular app into a Halogen app; also mixing a typed-FP language with Python (an odd mix..., but might show that they might later transition from Python to Haskell)

> Halogen has scary types when you get started, but once you’ve been working with the framework for a week or two they start to become second nature. We’ve enjoyed working in the language and have already seen a marked improvement in the reliability of the app where Angular has been replaced by Halogen.

- new learners are scared by Halogen's types initially, likely because it's unfamiliar, uses jargon they don't yet know, and they fear that this understanding is needed to make things work. It's not clear whether the fear is due to not knowing how to resolve common Halogen errors or where to put types in type signatures or what.

> The greatest weakness we have experienced so far is a lack of great components like typeaheads, day pickers, and so on ready to go for Halogen. We’ve needed to implement several of these ourselves where we might ordinarily have reached for an out-of-the-box solution like react-autocomplete. Yet this is an annoyance, not a dealbreaker.

- Commentator agrees that out-of-box web components are lacking and this situation is unfortunate but not enough for them to stop using PS.

> As far as your points, I can’t speak to ReasonML...

- Commentator has no familiarity with ReasonML

> ... but can share about PureScript:
> - Advantages The standard mix from functional programming: stability, no runtime errors, easy refactoring, easy concurrency, high ceiling for abstraction, great data modeling, etc. PureScript also has a tremendously helpful community in the functional programming Slack channel (https://fpchat-invite.herokuapp.com) and we receive help from core contributors at least weekly.

- PS is an FP language with all of those benefits
- Even if one does not understand FP, they can get help on a regular basis from really smart people (core contributors)

> - Documentation > Core PureScript has great documentation (see the PureScript book, the Halogen guide and example repos). However, most of the rest of PureScript learns from Haskell by having mediocre documentation. You’ll need to become familiar reading types and briefly checking source code to see what’s going on. That said, we’ve rarely had trouble with documentation; most functions are self-explanatory and the functional programming Slack is great for filling in the gaps.

- Documentation for core PS libraries are great but it quickly falters. Perhaps documenting only "core" libraries is not 'good enough' or doesn't cover enough libraries?
- People seem to think, at least initially, that type signatures are not 'good enough' for documentation. While one can understand a lot from them, new learners aren't used to do this, perhaps, or get close but not quite over a threshold of understanding for how to use that value/type/function/module.
- FP Slack filled-in any gaps in documentation.

> - Ecosystem This is hard to answer without knowing specifically what you’re building. We’re building a complex web application involving lots of forms, data management, some visualization, etc. and haven’t had trouble. JS interop is a strong point of PureScript; right now we’re just dropping Halogen components as full replacements to most of our Angular app. Some PS libraries (like Data.Array) are wrappers for core Javascript functionality. It’s quite easy to do.

- Commentator's needs were different than author's in that former had much more complexity where performance was perhaps not as big of an issue as realibility.
- PS + Halogen can be 'dropped in' as replacements for Angular apps, making migration easier

> - Future-proofed-ness Hard to say. There are companies invested in PureScript (SlamData is an obvious one; I work at Conde Nast), and it’s got an active community. You’re safe for at least the next 5 years, but after that, who knows? The web moves fast.

- PS has companies behind it to some degree that guarantees it will be worth knowing for next few years, but who can see beyond that, especially when the web changes faster than many other contexts.

### Comment

https://www.reddit.com/r/functionalprogramming/comments/7vveeu/purescript_vs_reasonmlbucklescript_in_2018/dtw35pb/

> I had to rule out both PureScript and ReasonML due to the server-side. I ended up picking Scala.js, partly because of [this blog post](http://www.lihaoyi.com/post/FromfirstprinciplesWhyIbetonScalajs.html) [summary: Scala.js was iniitally poor, buggy, slow, and lacked libraries before it became more mature over the years. Author is this post chose it because some things never changed: perfect IDE support (type inference, auto-complete, docs-on-hover), Scala-Scala code interops seamlessly with Scala-Javascript code, perfect scala compatibility (no additional learning needed to make same code now run on browser), cross-platform ecosystem (same code runs flawlessly on server or client, on JVM or browser; all JVM ecosystem immediately available), static optimizability (dead code elimination? optimizations not possible in dynamically-typed languages). Author chose Scala.js because it solved all the chronic problems of web development]...

- Arguments in linked post can be argued for PS, too, except in following ways:
    - JVM ecosystem entirely available to Scala.js whereas PS must build its own or use unsafe Javascript libraries
    - code works on both the server and client in Scala whereas PS does not yet have mature server frameworks and Node.js is not necessarily the best tool to use.
- Article does not mention a few issues with Scala.js that do not arise with PS
    - In my opinion, Scala is not as good for FP code as PS/Haskell (expressions are not as terse; compiler must be hacked to add some features that are already present in PS/Haskell, purely FP users of Scala are not supported by language's development, who want to support OO paradigm as well: there will always be tension / things that can't be done).
    - PS can compile to other languages besides Javascript. Sometimes C/C++ (and all its ecosytem) is a better fit than the JVM (and all its ecosystem)

> and I'm satisfied with my choice. I wrote a small library to handle my client-side rendering, which has proved surprisingly resilient.
> Scala has a vibrant community, with many useful libraries that are cross-compiled to both JVM and JS, and the language is very powerful - my state serialization is powered by the uPickle library which makes serializing a custom class as easy as auto-deriving a type class instance.

- Commentator largely just re-hahes what linked article already states.

### Comment

https://www.reddit.com/r/functionalprogramming/comments/7vveeu/purescript_vs_reasonmlbucklescript_in_2018/dtw0xdu/

> warning: I'll use ReasonML, Bucklescript and Ocaml interchangeably because we're talking about web stuff anyway I guess?

- I've edited the below responses to include those so his statements can be taken in isolation without the meaning changing.
-
> I've got the same impression - that Purescript is not getting more popular and ReasonML [ReasonML, Bucklescript and Ocaml] is popping up on conferences etc becaue of Facebook.

- Source of ReasonML's popularity is Facebook and conferences. PS might be lacking 'evangelism' in conferences

> Purescript has Higher Kinded Types and Ocaml [ReasonML, Bucklescript and Ocaml] has its first-class modules and "functor"-thingys. This difference has also other implications but Purescript's compile times are probably bigger.

- PS compile times might be longer than Ocaml

> I tried using Purescript's Halogen but I couldn't comprehend its types so I gave up. There are Purescript wrappers around React but I didn't try any of them. I feel like ReasonML [ReasonML, Bucklescript and Ocaml] should have pretty solid React wrappers.

- Commentator gave up on Halogen's types and perceived ReasonML's React wrappers to be better than PS.

> If you wanted to write a back-end component in one of these languages, I feel like it'd be easier with Ocaml [ReasonML, Bucklescript and Ocaml].
> TLDR: I'd probably choose Bucklescript.

- Easier to write a backend component in Ocaml than in PS.

### Opening Thread - Edit 1 month later

> Edit one month later: Greetings to the visitors from the future! After playing around further, I gave up on Ocaml. For me
> - Error messages were completley useless. Everything would yield a "syntax error" with a seeming random line-number. In many cases the error message wasn't described, but encoured me to send pull requests with an updated message. These were obviously beginner mistakes, so nothing too fancy, and it forced me to scan every line manually to make sure all the ; and ) were in place.
> - I never got warm with the reason syntax. The javascripty look of reason made it more difficult to write than original ocaml/bucklescript, especially when to put ; {} () or not.
> - Tutorials/docs are rare and confusing. I never knew if I was learning Reason, Bucklescript or Ocaml
> - The toolchain only works if Reason, Bucklescript, Merlin and Ocaml are in very specific versions. Obviously the error messages you get are shit, so I spent far too much time on getting it running and I had to compile from source. Also, ReasonReact is it's own framework, so it's one more layer detached from react and data needs to be handed around between the components. All in all, updates are unpredictable and I don't trust the upgrade path.
> - Server side ecosystem is practically non-existent for modern use cases.
> - Apparently the majority of users are French students who learn Ocaml at university and there is very little adoption outside.
>
> Final verdict for me personally: Unless there's a french guy in your team who already knows it, troubleshooting and boarding is hell and a time vapire. Also given the low maturity of the framework (error messages, old ocaml version, tutorials), I don't trust its upgrade path.
> Maybe you get better results, but for me it's not worth it.

- OCaml had too many problems for him as a new learner; productivity only seemed possible if someone else on a team already knew it

> Purescript: Stagnated, but still nice. The React frameworks are terribly slow in benchmarks up to 8x slower than most of the field. For complex client side calculations and limited UI with a team that already knows haskell, I'd probably pick this.

- Stagnation / slow down of language/ecosystem development was a factor in author's decision
- It seems author's project was heavy on the UI and speed was important. PS React-based frameworks were significantly slower than solutions from other languages, making PS a deal-breaker
- Had project requried less UI and more complex calculations where type-safety shines brightly, author would have suck with it

> Clojurescript: I stumbled upon it because its react frameworks perform amongst the fastest with less code, it's functional and immutable (with escape hatches). It's not typed, but it has Spec, which allows for quickcheck type autogenerated test cases, spec reuse for runtime validation and even regex and code-defined validation for what values are allowed into a type. The compiler is quick and clojure on the server integrated with the java ecosystem, it also has frameworks for react native.

- Clojurescript was fast without boilerplate-y code and useful testing libraries

> All in all, this may sound blasphemous, but for me the most useful functional, typed frontend language is still Typescript with Ramda and Immutable.js. That gives me ADT, function composition, immutability, lenses, etc, with a rich ecosystem and easy boarding. Only thing I miss is type inference which makes me retype interfaces and types all over the place. For UI oriented applications Clojure(script) with Spec seems a nice fit. (I didn't check elm due to mounting negative feedback about breaking changes between versions). To use even more typed features purescript still the best, but be concious of the performance penalty.

- Author still found Typescript + Rambda + Immutable.js to be best **overall** solution. While admitting that it's not best in each aspect, the combination of it had the best environment for author.

### Comment

https://www.reddit.com/r/functionalprogramming/comments/7vveeu/purescript_vs_reasonmlbucklescript_in_2018/dvqqq38/

[Commentator largely responds to most of the above 'edit 1 month later' response. Not much was deemed worthwhile in including here.]

> Docs could probably use some consolidation but I think it’s pretty simple to tell which you’re learning: if you’re on the Reason doc site, you’re learning Reason, and if you’re on the BuckleScript doc site, you’re learning BuckleScript, and in either case you’re learning OCaml 😉

- Seems OCaml / ReasonML / BuckleScript has a minor documentation problem of its own?

> Server side is a work in progress, but there are several options on the OCaml side.

- Seems OCaml / ReasonML / BuckleScript also is lacking a mature server solution?

> Adoption and French guys is a bit of a red herring 😉 if you’re interested, drop in to the Reason Discord and pick it up naturally like people all over the world are doing. It’s just a language like any other. Companies like Facebook, Jane Street, Docker, Citrix, Uber, Microsoft, are using OCaml. Check out the industrial users consortium.

- OCaml / ReasonML / BuckleScript - new learners are also advised to check out their forum/chatroom for getting help from people already familiar with it.

### Comment

https://www.reddit.com/r/functionalprogramming/comments/7vveeu/purescript_vs_reasonmlbucklescript_in_2018/dvqxsbr/

>> [Based on which website for OCaml / ReasonML / BuckleScript you're on], I think it’s pretty simple to tell which you’re learning ([Context: 2nd paragraph](https://www.reddit.com/r/functionalprogramming/comments/7vveeu/purescript_vs_reasonmlbucklescript_in_2018/dvqqq38/))
> From a newcomers perspective, it's not simple at all. For exampe: reason-cli doens't work and I get some unclear error message. Is this an ocaml problem? A bucklescript problem? A reason problem? I ended up solving it with the ocaml docs and a bucklescript walkthrough.
> Same goes with learning other concepts. There are only sparse tutorials and examples online, so sometimes I end up with a blog post on bucklescript and sometimes on reasonml. For a lot of concepts, I find recommendations to read a chapter in Real World Ocaml or something similar.
> The entire experience was just very bumpy and painfull, chasing unclear errors and wasting tons of time on things that are non-issues in other ecosystems. For me, it's definitley not worth the potential upsides.

- Summary of a new learner's experience with OCaml / ReasonML / BuckleScript seems similar to other experiences of new learners of PS:
    - sparse tutorials that are not part of some larger whole forces new learner to piece together the parts with difficulty
    - no clear linear learning path led to wasted time, something which would not occur in other ecosystems
    - while upsides of this ecosystem are good, they were not worth it for the author.

### Comment

https://www.reddit.com/r/functionalprogramming/comments/7vveeu/purescript_vs_reasonmlbucklescript_in_2018/dvr0euz/

> Gotcha, and thanks again for such a detailed response. I believe the community and core team are all working quite hard on documentation and onboarding, so maybe in the near future it will make sense for you

- Commentator states that both community and language's core team are unified in working together to improve documentation and new-learner onboarding process.

### Comment

https://www.reddit.com/r/functionalprogramming/comments/7vveeu/purescript_vs_reasonmlbucklescript_in_2018/dvr1g5i/

> Yes, I think Ocaml/BS is a solid basis, and it's an interesting development, I'm sure I'll have another look in a year or two.

- Some people who give up on a language are simply waiting for its documentation to improve, so that they can have an easier learning process in the future.
