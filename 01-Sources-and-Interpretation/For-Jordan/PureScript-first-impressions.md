
## Source: "Purescript First Impressions"

https://reddit.com/r/purescript/comments/8qaiwl/purescript_first_impressions/

### Opening Thread

> Hi folks, I downloaded PureScript for the first time on Saturday. I have fairly minimal prior Haskell experience, but I remember how the basics work.

- Source already has familiarity with Haskell / FP languages and will likely be comparing it to Haskell

> Thought it would be interesting to write down my first impressions:
> - First, the compiler and tooling around pulp really blew me away with how well it worked and how simple it was to set up, so bravo for that!

- pulp was simple to set up things

> - I decided to install purescript-ide for Atom, and had another 'oh wow' moment, because it works really well! Very impressive

- Atom support was easy to set up

> - I'm really glad that package management is centralized in bower -- I hate navigating package manager fragmentation

- Haskell user prefers and welcomed non-fragmented dependency managers.

> - Figuring out that Eff has been replaced with Effect took me a hell of a long time (literally the front page example on purescript.org is wrong). You don't get to do this kind of thing too many times!

- The PS language site was the first thing he went to
- The oudated Eff-based example created a horrible new-user experience

> - pursuit is also great once you figure out how it works (some more top-level "what is this thing?" documentation would be good). Lack of fragmentation continues to be a big draw for me.

- New users like to use Pursuit to learn how to solve problems when writing the language / understand what some concept/function/type is.
- Haskell user prefers and welcomed a centralized documentation site
- Help/Documentation on using Pursuit's search could be better highlighted to draw more attention to it.

> - Probably the worst part of my PureScript experience was the FFI. This is an area where the language needs to be more generous with special syntax and compiler features -- it's crazy how much boilerplate I need to produce to write types for extremely common JavaScript patterns compared to other languages

- Not really a documentatino issue but more of a user-friendiness/productivity issue
- There might be code generation solutions to the above problem that he did not know about.
- The FFI maybe needs better documentation, especially for a newcomer to statically-typed language.

### Comment

https://www.reddit.com/r/purescript/comments/8qaiwl/purescript_first_impressions/e0hoebs

> Honestly it's one of the best FFI experiences I had out there but there are certain tricks (for example FN2 & co. to help out with uncurried functions or all the stuff in the utils) that might not be very well documented and maybe we can improve when we hear what your main troubles where

- FFI tricks might not be well documented for new users/learners

### Comment

https://www.reddit.com/r/purescript/comments/8qaiwl/purescript_first_impressions/e0j5bzw

> Yeah - I played around with 0.12 recently and it's too immature imo - to be the default at least. Most packages aren't updated, and since there are a bunch of breaking changes I don't see this happening soon.

- Note: this comment occurred 22 days after the `0.12.0` release
- Indication that a language release does not imply ecosystem compatibility immediately after its release.
- Expectation that language's community won't be able to reach that coherence for a while.

> Also, although bower has some nice parts, I'd like to see more movement towards psc-package. The problem atm is that while lots of packages could go on it with little-to-no changes it's a manual process where the default is packages don't get onboarded. I've heard Nix is really nice for functional libraries (heard about it in this regard through Haskell) but it's hard to get set up.

- Nix is really nice for FP libraries but difficult to set up
- Migrating to psc-package requires a manual process. Not sure how much time that takes.

> Something like bower that has better dependency management (both recording hashes, and making sure you don't end up with lots of the "choose a package" messages) would be a vast improvement, imo.

- A better version of Bower would be a huge improvement for PS community's build tooling.

### Reddit post (new language user)

https://www.reddit.com/r/purescript/comments/8qaiwl/purescript_first_impressions/e0ip6h2

> Take calling a method on a class for example: you need to make a Javascript file which wraps your existing method by doing exports.myMethodImpl = function(...), that function probably needs to return another function if it's an Effect, then you need to foreign import the function and wrap the arguments in a Fn3, and then you need to make another function that calls the first function and invokes runFn3 on it.
> There's purescript-ffi-utils to help with some of this (which isn't updated to 0.12 yet), but most other compile-to-javascript languages have first class syntax for this. I see no reason why I can't write one line of purescript (and zero lines of javascript!) to say "hey, I have this method with these types, please generate the stuff to let me call it."

- Writing FFI is very boilerplate-y and wastes developer time. There should be a faster way to do the same thing, potentially via a library or through code generation.

### Comment

https://www.reddit.com/r/purescript/comments/8qaiwl/purescript_first_impressions/e0iqgya

> If we can write libraries to help, why do we need first-class syntax? JavaScript isn't the only language that PureScript compiles to, so I think it would be a mistake to bake anything specific to JS into the language syntax.

- The FFI documentation should explain the disadvantages of giving first-class syntax for Javascript FFI due to PS' "compile to multiple backends" nature.

### Comment

https://www.reddit.com/r/purescript/comments/8qaiwl/purescript_first_impressions/e0owwym

> I haven't done a deep dive into purescript FFI but a lot of your issues are common with FFI from a non-pure, non-functional languages to functional languages. Converting arety into currying while in your guest language and then providing a method for the host language to call this function will knowing the types of each step. And that's just for functions we'd consider to be pure.
> I agree it would be nice for a one liner (and we probably should have one) but a big benefit to this longer process is it allows you to fake out all the non-pure state and effects to get as close to pure as possible.

- The FFI documentation should explain the advantages of writing an out-of-PureScript implementation.
