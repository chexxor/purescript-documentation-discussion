
## Source: "Lessons learned porting a game from Purescript to Elm"

https://alpacaaa.net/blog/post/elm-purescript-in-depth-overview/

### How I got here

> A few months ago, I decided I was going to learn Haskell. The first thing I noticed was that I couldn’t read Haskell code. It was so different to anything I had experienced so far. All those strange symbols gave me a very hard time trying to understand what was going on. Maybe I should have started from something simpler.
> I heard that a language called Purescript existed, that it was purely functional and that it compiled to JS. Sounded like a good deal to me, after all I wanted to experience what it was like to program in a purely functional language, I didn’t want to settle on Haskell if that wasn’t my thing. Plus, a language that compiles to JS has to be approachable, right? Wrong. Purescript was as much confusing and frustrating as Haskell (in fact, they’re very similar languages). So I eventually considered Elm, which turned out to be the perfect language to learn FP.

- People who hear that Purescript "compiles to Javascript" incorrectly assume/expect it to use a syntax similar to Javascript or other compile-to-JS languages.
- Author's first major issue and turn off was not being able to read the syntax of a Haskell-like language. This issue alone made him choose to look at Elm rather than PureScript, which is arguably more powerful than Elm.

> I didn’t want to give up on Haskell nor Purescript though. Over the coming weeks, I came back multiple times to these seemingly obscure languages. The resources that definitely helped me the most in grokking the concepts behind them are the excellent `Purescript By Example` and the glorious `Haskell Book`.

- Unlike most people, the author did not give up and looked at Haskell/PureScript again, eventually reaching an understanding via each language's "standard" for learning them.

> I remember looking for short and easy to follow examples while still learning, and the simplest I could find was this little game: `star-dodge-clone` (link to playable demo). Despite being simple, it wasn’t at all easy, at least for an uninitiated wanderer like me. I remember going through the ~250 total lines of Purescript code but couldn’t figure out pretty much anything.

- The above simple demo still assumes too much advanced background info for a new learner to understand it.
- People think 'simple' demos (like that above) don't require that much understanding. The "simple" demo above uses the following language features:
    - the `Eff` monad
    - a Graphics library
    - symbolic functions (e.g. `<$>` instead of `map`)
    - implicit monadic functions via the `<-` bind syntax
    - Type Classes
    - Type Aliases
    - algebraic data types
    - records and their accessor syntax
    - value assignments via `let`
    - FFI
    - pattern matching
    - pattern guards

### Language Simplicity

> I find Elm code much easier to reason about .... That’s not to say that Purescript code is unintelligible (far from it) but there’s a lot more to learn and you must develop an intuition for certain things. The type system in Purescript is more advanced and, as a consequence, you’ll often see involved type signatures.

- Elm is more approachable simply because it is less powerful and requires learning less.
- Elm could be a useful 'gateway drug' into PureScript

> ... this can’t be expressed in Elm, as it lacks type classes.

- PS has type classes whereas Elm does not: one reason why one might want to use PS instead of Elm.

> I find The Elm Architecture (TEA for short) a very very nice and simple pattern to follow when working on UI code. Being Purescript [is] a much more general purpose language, it doesn’t put such constraints on the developer.

- Elm is appealing because it's application structure is well-understood. To get the same appeal, the 'best practices' for application structure should be well documented in PS.

> Of course, there’s no shortage of excellent libraries to structure your frontend code – I played a little with Pux which somewhat resembles TEA.

- Pux could be a "gateway drug" library from Elm into PS

> First of all, there’s do notation. Why are things defined with a `<-` instead of a =? This is one of the first questions that beginner haskellers face and you’re going to have the same WTF moments in Purescript as well (if you’re unexperienced like I was). Turns out do notation has a very specific purpose and it makes total sense once you figure out how bind works and how annoying it is to nest sequenced computations. (I’ll say it again, if you don’t know what the hell you just read, stick with Elm for a while, you won’t regret it)

- The `do` syntax was not immediately understood by the author.

> Another thing that I thought was not available in purely functional programming languages is mutability. With references you get exactly that (newRef creates a new reference, a variable if you will, which you can update with modifyRef). Of course mutation is controlled and it’s much different than using a mutable variable in an imperative language, but as a beginner it’s hard to tell what’s happening.

- Not being able to mutate variables is a hard thing to initally grasp by new learners who are used to doing so freely.

> In general, Purescript is much more low level than Elm which means you can do pretty crazy stuff while being very precise and explicit about what you want to do (without losing purity).

- PS is more precise and powerful at a lower level than Elm.

> In Elm, you are forced to do that (handle every input possibility in a function and thereby make it total), while Purescript offers escape hatches (via the `unsafe`-prefixed functions), meaning that you can effectively have partial functions. This might seem counter intuitive, why would you deliberately lose the guarantees given by the compiler and the type system? The answer is convenience. Honestly, at first I was surprised to see `unsafePartial` used that much throughout the `Purescript By Example` book, because I thought a sane person wouldn’t want to give up totality, but of course that’s not the case.

- PureScript by Example uses `unsafePartial` in such a way that it might wrongly imply that one uses it more frequently than one actually does.
- The reasons for using `unsafeParital` might not be well-documented/explained

> ... Elm strive to be total and prevent you from shooting yourself in the foot in any way, while Purescript gives you more freedom, but you have to understand the consequences of what you’re doing.

- Good summary of the differences between Elm and PS' handling of partial functions

> One of the most important things I learnt about functional programming is that local and controlled side effects are super useful and don’t undermine purity in any way, as long as functions are referentially transparent. In this case, unsafeLevel clearly is not, so this is certainly not the best example to convey my point, so let’s make another. (I’m sure unsafeLevel was written out of convenience in the game, just to keep it short and sweet).

- I don't know whether this concept (local and controlled side effects are still considered 'pure' if functions are referentially transparent) is well-documented in PureScript learning resources (even my own)
