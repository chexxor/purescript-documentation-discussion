
## Source: Why Use Purescript (Tweet)

### Opening Tweet

https://twitter.com/paf31/status/895350468360028160

> I wrote a few notes about why you should use PureScript

### Thread: Tech's Cons

https://twitter.com/Profpatsch/status/895402654842671104

Key comments are listed below:

> From what I see there’s common complaints with rebuttals, no actual cons. Cons are stuff like unsuitable use cases, implementation bugs.

> I think quite a lot of the rebuttals were more like "yes, it's not ideal, but...", for example where I recommend GHCJS if you need laziness.

> I mean, I might not write the performance critical code in PureScript, for say, a game, but that's what the FFI is for.

- One person thought there really weren't any cons, just some situations where it's not "ideal". For example, if you want lazy evaluation by default, PureScript is not ideal for you.

### Thread: Good First Impressions but Lacking Deeper Concept Explanations

https://twitter.com/raimeyuu/status/895379846938992640

Key comments are listed below:

> I tried PureScript, first impression was really good, but I was lacking some guidance for e.g. free monads etc. So deeper concepts :-) tips?

> I think most of the Haskell resources should translate over well, but you shouldn't need such advanced concepts so early on, really.

> So you suggest to focus on foundations while these advanced concepts would become attractive later on?

> I think so, yes.

> I'm not saying don't read about them now, of course. Just that they shouldn't stop you from making stuff now :)

- Lack of explanation on 'deep concepts' issue was not addressed. Rather, the implied idea was "new learners just don't need to know them immediately and should focus on fundamentals first."
- A PureScript core maintainer believes that deeper concepts and idioms are best learned by consuming Haskell learning resources.

### Thread: Example of SQL in PS

https://twitter.com/sseraphini/status/895578222057934848

Key comments are listed below:

> Do u have an example of SQL in purescript, how does it handle sql injection?

> The simplest way is to just have a separate type for SQL query strings and user values, and only have safe functions for converting between.

> Any code example of this idea? I don't know much about purescript

> Have a look at any of the Haskell database libraries perhaps.

- General idea / approach to doing SQL was explained, but there isn't a complete and working example. Person was referred to Haskell database libraries, but it seems that referrer wasn't sure whether they would help.

### Thread: Questions regarding how to do X for general and specific things

https://twitter.com/dlants/status/895361210274652160

Key comments are listed below:

> Another concern is access to low-level UX polish. It's not clear how click/drag, transitions/animations, cursor effects should be done.

> Doesn't NPM provide solutions for these already?

> You mean using FFI or in PS packages? Hardest part is fitting into the UI lib design. Qs like "how do I build click/drag against Pux?"

> I think you'd have to ask someone who knows more about Pux :)

> I love using PS for my side project, and I think this rough spot will get better for me as I continue learning FP.

- A PureScript learner believes PureScript doesn't have a singular documented answer for UI programming tasks, such as click/drag, animations, and cursor effects.
- The two questions here were not really answered:
    - how should click/drag/transitions/animiations (stateful things) be done in general?
    - how should same things be done using a UI library like Pux?

### Thread: Address 'Category Theory Required' Myth

https://twitter.com/_gilmi/status/895360612347371521

> "Too much category theory" - maybe add a link to [the haskell pyramid]( https://patrickmn.com/software/the-haskell-pyramid/)?

- A PureScript user believes language documentation should explain the depth of the language and its patterns/libraries to ensure users don't try to learn hard things before they understand more foundational things.

> Also maybe add that the compiler, tools (and devs) are pretty approachable so it's easy to contribute and affect the direction of the lang

- A PureScript users believes that language documentation should include a description of how easy it is to contribute to the language and affect its direction.
- There are other factors that draw people to an ecosystem and these are some of the strengths of the language.

### Comment: Useful JS -> FP Learning Resource

https://twitter.com/_KtorZ_/status/895936657572192256

> I'll also highly recommend the https://github.com/MostlyAdequate/mostly-adequate-guide by `@drboolean` as a training material and perfect bridge between JS and FP :)

- A PureScript user believes a good learning path is to teach a person from a language they are already familiar with.
- This resource might provide a better learning path for JS-background people before they see it written using a better syntax via PS.

### Comment: Migration Guide

https://twitter.com/james_a_forbes/status/895652189988765699

Key ideas below:

> I'd really like to see how to migrate to purescript in a larger JS project without abandoning the existing build process.
> For example, write 1 component in a React codebase in purescript, within an incremental compilation toolchain e.g. browserify/webpack.
> It seems that to get a justifiable benefit for the time investment you need distinct/clear system boundaries. Which means I can't adopt it.
> But if you look at things like flowtype, typescript, sanctuary-def, there's a good migration story. So I'd love to see solutions to that.

- Providing good migration stories would help people who want to use it but can't because their 'system/program/app' would stop working for some period of time. A migration needs to be seamless and address the issues/concerns one might have.
- A PureScript outsider believes the documentation should show how to use PureScript in a pre-existing project written in a different language.

### Comment: 

https://twitter.com/antiselfdual/status/895480705156751361

> Lack of tuples and orphans.

- A PureScript outsider believes documentation should explain why the language doesn't have data types or concepts that they are familiar with.

### Comment: Confidence in Node for Server-Side Solutions

https://twitter.com/d6y/status/895355035927891969

> Thank you! Alternative to “I don’t want to use node”: I lack node experience,need confidence that node is rock solid (monitoring, profiling)

- Two options here:
    - Show reasons for why Node is a "rock solid" solution to server-side things
    - Show reasons for why other backends (C/C++ ?) can provide a better server environment than Node...?
- A PureScript outsider believes the documentation should describe the quality of the runtime.

### Thread: Missing a Full Webapp Step-by-Step Tutorial

https://twitter.com/ThibaudDauce/status/895534464071331840

> I think PureScript is missing a full webapp step-by-step tutorial (front, back, database, mails, authentication, forms, validation…)

> exactly, it would be just invaluable. I would be more than happy to pay for such course/tutorial.

> This might be something I could work towards

> I'm available to help if needed :-)

> I'll reach out if I get something going!

- We should follow up with these people to see what they ultimately came up with (if anything). If the project did not get anywhere, there's still likely some historical value here (what worked, what problems they encountered, etc.)
- The Real World App that `thomashoneyman` finished recently is a step in this direction as well.

### Comment: Integration with advanced web dev features

https://twitter.com/iwinux/status/895470276057587712

> Lang features are cool, but how do I integrate it with Webpack / CSS Modules / Code Splitting then?

- This wasn't answered but does provide a good question.
- A PureScript outsider believes documentation should teach how to integrate the output of the PureScript compiler with other tools in the target language ecosystem.
