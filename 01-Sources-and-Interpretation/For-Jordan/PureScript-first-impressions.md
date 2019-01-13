
## Source: "Purescript First Impressions"

https://reddit.com/r/purescript/comments/8qaiwl/purescript_first_impressions/

### Reddit post (new language user)

> pursuit is also great once you figure out how it works (some more top-level "what is this thing?" documentation would be good).

- New users like to use Pursuit to learn how to solve problems when writing the language.

> Probably the worst part of my PureScript experience was the FFI. This is an area where the language needs to be more generous with special syntax and compiler features -- it's crazy how much boilerplate I need to produce to write types for extremely common JavaScript patterns compared to other languages

- The FFI maybe needs better documentation, especially for a newcomer to statically-typed language.

> Take calling a method on a class for example: you need to make a Javascript file which wraps your existing method by doing exports.myMethodImpl = function(...), that function probably needs to return another function if it's an Effect, then you need to foreign import the function and wrap the arguments in a Fn3, and then you need to make another function that calls the first function and invokes runFn3 on it.

- The FFI documentation should explain the advantages of writing an out-of-PureScript implementation.
