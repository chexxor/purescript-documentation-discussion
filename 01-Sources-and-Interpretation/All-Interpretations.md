# All Interpretations

The following interpretations have been copied over from various sources. The bracketed content `[example_slug_name]` refers to the unqiue slug name of a source, so that one could see the full context of that interpretation.

<hr>

- There are lots of easy documentation problems to resolve in the core documentation. [Features_You_Want_Future_PureScript_to_Not_Have]
- A PureScript user prefers PureScript over Elm because they don't like a language which dogmatically enforces a certain way of programming. [Hitchhikers_Guide_to_Elm]
- A PureScript user believes PureScript's FFI is simpler than Elm. [Hitchhikers_Guide_to_Elm]
- A PureScript user believes PureScript compiles to smaller amounts of JS than Elm for the same thing, making pages load faster than Elm-written ones. [Hitchhikers_Guide_to_Elm]
- A PureScript user entered PureScript after going through Elm. [Hitchhikers_Guide_to_Elm]
- A PureScript user feels limited by Elm's type system. [Hitchhikers_Guide_to_Elm]
- A PureScript user believes that a language can limit what you can do and learn, and is reason for leaving the language. [Hitchhikers_Guide_to_Elm]
- A PureScript user believes that learning PureScript is hard to learn, and the reason is it is powerful. [Hitchhikers_Guide_to_Elm]
- A PureScript user believes that using it is dead-simple because it compiles to JavaScript (because it is readable?). [Hitchhikers_Guide_to_Elm]
- A PureScript user has trouble figuring out how to solve application problems in PureScript, which is a reason for why PureScript is hard to learn. [Hitchhikers_Guide_to_Elm]
- A PureScript user feels rewarded when using PureScript because the primary sticking points are figuring out how to do things *in* the language, rather than figuring out *non-language* problems. [Hitchhikers_Guide_to_Elm]
- A PureScript user believes that PureScript is good for solid development of frontend applications. [Hitchhikers_Guide_to_Elm]
- A non-PureScript user prefers a simple language with a gradual/short learning curve and is willing to compromise on the quantity of manually-written code to have it. [Hitchhikers_Guide_to_Elm]
- A JavaScript/React/PureScript user believes PureScript's FFI is fairly easy and is better than ReasonML's and Elm's FFI. [Hitchhikers_Guide_to_Elm]
- People who hear that Purescript "compiles to Javascript" incorrectly assume/expect it to use a syntax similar to Javascript or other compile-to-JS languages. [Elm_PureScript_In_Depth_Overview]
- Author's first major issue and turn off was not being able to read the syntax of a Haskell-like language. This issue alone made him choose to look at Elm rather than PureScript, which is arguably more powerful than Elm. Unlike most people, the author did not give up and looked at Haskell/PureScript again, eventually reaching an understanding via each language's "standard" for learning them. [Elm_PureScript_In_Depth_Overview]
- The simple demo, `star-dodge-clone`, still assumes too much advanced background info for a new learner to understand it. People think 'simple' demos (like that above) don't require that much understanding. The "simple" demo above uses the following language features: [Elm_PureScript_In_Depth_Overview]
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
- Elm is more approachable simply because it is less powerful and requires learning less. [Elm_PureScript_In_Depth_Overview]
- Elm could be a useful 'gateway drug' into PureScript [Elm_PureScript_In_Depth_Overview]
- PS has type classes whereas Elm does not: one reason why one might want to use PS instead of Elm. [Elm_PureScript_In_Depth_Overview]
- Elm is appealing because it's application structure is well-understood. To get the same appeal, the 'best practices' for application structure should be well documented in PS. [Elm_PureScript_In_Depth_Overview]
- Pux could be a "gateway drug" library from Elm into PS [Elm_PureScript_In_Depth_Overview]
- The `do` syntax was not immediately understood by the author. [Elm_PureScript_In_Depth_Overview]
- Not being able to mutate variables is a hard thing to initally grasp by new learners who are used to doing so freely. [Elm_PureScript_In_Depth_Overview]
- PS is more precise and powerful at a lower level than Elm. [Elm_PureScript_In_Depth_Overview]
- PureScript by Example uses `unsafePartial` in such a way that it might wrongly imply that one uses it more frequently than one actually does. [Elm_PureScript_In_Depth_Overview]
- The reasons for using `unsafePartial` might not be well-documented/explained [Elm_PureScript_In_Depth_Overview]
- Good summary of the differences between Elm and PS' handling of partial functions: "Elm strive to be total and prevent you from shooting yourself in the foot in any way, while Purescript gives you more freedom, but you have to understand the consequences of what you’re doing." [Elm_PureScript_In_Depth_Overview]
- I don't know whether this concept (local and controlled side effects are still considered 'pure' if functions are referentially transparent) is well-documented in PureScript learning resources (even in my own, Jordan's PureScript Reference) [Elm_PureScript_In_Depth_Overview]
