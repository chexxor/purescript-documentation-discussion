
## Source: "My experience with Purescript so far"

https://sadraskol.com/posts/my-experience-with-purescript-so-far

This is a blog post that has multiple sections

The person who wrote it learned PS for a non-serious side project and to write scripts for querying their MongoDB.

### Environment Tools

> the install and setup of the environment is straight forward.

- self-explanatory

> The incremental build is super fast on my machine so you can have a quick feedback on your test while you code with a simple pulp --watch test.

- build tools supporting fast feedback loops make developers more productive

> purescript excels at is documentation browsing

- self-explanatory

> It’s a shame that the results (for `map`) are weidly ordered. I would have preferred to have the `Data.Functor (map)` at the top, since it’s the most common. But this is only a detail, I’m sure maintainers are aware of these sort of things and are working towards a better browsing experience.

- Having a 'beginner-friendly' version of Pursuit search that highlights / prioritizes / highly ranks the common things new learners would search for would be helpful.

> Another nice surprise is the Atom Ide. If you use Atom, it offers a nice ide that take care of autocomplete or source browsing.

- Great out-of-box support for Atom IDE

> I need to restart the plugin from time to time to synchronise it with the current state of the build.

- Minor issue that might be resolvable or might not be depending on what causes the problem and how much manpower it takes to fix.

### Language Features

> Purescript is so pure that it won’t allow you to use partial functions without special treatments. This pushes you to a type driven development, which allowed me to learn a lot about the problems I was trying to solve.

- Making implicit partial functions explicit helped one adhere to type-driven development, which also had some educational benefits

> Purescript does not come “batteries included”, you need to import every dependencies, even the + operator! I don’t know why, since the static typing system allows to prune useless code easily, and tree shaking is done by default when packaging the javascript. Anyways it’s a surprising feature, that isn’t clearly indicated.

- Being required to import each import is tedious and annoying. However, the person might not know that the `atom-ide` / `purescript-lang` atom packages enable one to type in the Type, hit tab for the autocomplete, and the IDE will insert both the autocompletion and import the module if it's not imported already. This issue and its possible solution could be better documented.

> You will have weird error messages when not importing Prelude.

- This could be documented as "common errors" with an easy fix.

### Purescript User Experience

> Let’s say you mistype the function `traverse` to `traversee`. In Elixir, the compiler will warn you that there’s a more natural option: it will suggest methods in the context that look like your mistyping using the `jaro distance`. It’s a shame that the Purescript compiler does not do such things, even more because the type system would allow to suggest some very smart and elegant choices. No such explanation is given by purescript compiler.

- The issue here seems to be that error messages do not do a sort of type-directed search to help infer what the user is probably trying to write but failing to write.
- Type-directed search could fix this issue in some cases, but it wouldn't work exactly as the author describes.

> Purescript leaves you alone in the jungle of its methods and functional gibberish. If you don’t know what a Monoid, a Foldable or a <$> is, you better learn the language with tutorial first! It feels like the language wasn’t build for programmers first, but for Haskell programmers with strong theorical background. Could you easily guess what’s the difference between a Semi-groupoid and a Monoid?

- Newcomers to the language feel antagonized by the unfamiliar concepts and language operators.
- Perhaps documentation can mitigate the confusion and anguish experienced by newcomers.
- Author expects such explanations to be made in the module/function/type's documentation as found in Pursuit rather than some external resource like `Purescript By Example`, which does a good job explaing what that is. Linking to such explanations might address such pain points.

> The most representative to me is the purescript-assert library, when the assertion work, everything is fine. But once you get an error, here’s the result:
> As you can see, there’s no comprehensible error message, not even the line of the error in the .purs test file. If you have more than one assertion in your tests, which is quite the norm, you can’t know which assertion fails.

- Library likely did not yet provide `assertX` with custom warning errors attached to it like `quickCheck (\a -> a <?> "custom warning error when it fails")`
- Author possibly assumes that unit testing is the default testing used for FP languages rather than property testing
- Author possible does not know about `purescript-spec` as a testing library

> Fortunately, other libraries allow to perform testing with better output.

- Unfortunately, the author does not help the reader by indicating what other testing libraries they could use. Thus, this statement is somewhat biased.

> I deeply regret that basic libraries don’t go in a spirit of helping the programmers.

- There is truth to this statement in some points that author has raised.

> As this tweet says:
>
>>  Programming languages should help programmers becoming better
>
> Purescript only provides half the tools for the statement to be true.

- This is a rather subjective summary statement because it does not define what its criteria is. For all we know, PureScript could provide 1/3, 1/8, or even 4/5 of the tools. It depends on the criteria used to judge it.

> Purescript is not in its stable stage yet, and most of the work is still to be provided. I have great hopes in Purescript. It offers a super nice way of doing Javascript in a safe and productive way.

- Despite the critiques raised in this post, author will likely use the language in the future when things get better
- 
