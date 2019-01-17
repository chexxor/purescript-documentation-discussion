
## Source: Hitchhiker's Guide to Elm

https://news.ycombinator.com/item?id=17127821

### Opening Comment

A number of comments were made, but the one that caught our attention was started by this one.

https://news.ycombinator.com/item?id=17126007

> Are the elm overlords still hell bent on "thou shalt program our way or not at all"
> Because that kind of dogmatism is a complete show stopper for languages that want to be deployed on even medium term projects.

### Comment

https://news.ycombinator.com/item?id=17127821

> This is one of the reasons why I chose Purescript for my team's projects.

- Elm's "The One Way" approach discourages others from using it in production, but the project's needs, size, etc. are not clarified here.

> Also it's got a more complete type system, a simpler FFI, and compiles to less javascript.

- PS' FFI is simpler and compiles to smaller amounts of JS for the same thing, making pages load faster than Elm-written ones.

> This is not to say that Elm is bad. O think it's great as a path into FP, and in fact _was_ my path in.

- An actual example of someone who made the leap from JS (maybe?) to Purescript through the intermediate language, Elm.

> But it does limit you in what you can do and learn.

- Elm limits what you can learn but 'what' one would learn (FP concepts, perhaps?) is not explicitly stated.

> Also, Purescript has this interesting property of being hard to learn (because it is powerful), but dead simple to use (because it compiles to JS). So you only really get stuck on figuring out how to do things in PS, as opposed to how to get PS working, and therefore every time you get unstuck, you have leveled up. So it's hard, but rewarding.

- PureScript is powerful and easy to get working, but people get stuck on how to do things in PS
- Due to it's power, learning how to do things in PS is like "leveling up" and unlocking new special abilities.

> I'm probably off topic by now, but I do think that Purescript in the frontend is a better option for solid application development.

- Elm might be good for new FP learners / simple apps whereas PureScript seems better suited for more complicated apps.

### Comment

https://news.ycombinator.com/item?id=17128442

> Purescript looks like a great language and if you want to dive into the deep end of typed FP, then it looks like an excellent choice. One reason I went with Elm for our in-house customer support app, was because of the simplicity of the language. It does result in more boilerplate but I don't think the project would have been successful if the learning curve was steeper.

- Some people prefer the benefit of simplicity and lower learning curves to a language over the cost of boilerplate.

### Comment

>> [Context](https://news.ycombinator.com/item?id=17126216) One of the reasons behind the poster saying it is that the interop between Elm and vanilla JS is quite painful especially compared to the likes of BuckleScript.

- Elm has painful interop with vanilla Javascript

https://news.ycombinator.com/item?id=17126403

> PureScript's interop is fairly easy, too. Just foreign imports, which I personally prefer over mixing languages like you might do in BuckleScript/ReasonML with their brace syntax (or might not), but it's still better than this weird message passing thing that Elm does.

- BuckleScript/ReasonML might mix languages together whereas PureScript just uses foreign imports. This difference might be trivial (based on preference) or might be significant (leads to better readability, code issues if not done this way, etc.).
