
## Source: On Ergonomics of FP Compiler Errors

http://metaleap.net/blog.ergonomic-purescript-error-messages.html#My%20take:

Main ideas:
- Many people comlain about the cryptic errors of Haskell and PureScript, likely because they do not understand the compiler / type system that well.
- Elm, which is an FP language, has great compiler errors, but only because it's type system is much simpler and less powerful
- PS' error messages have improved
- Compiler errors shouldn't tell you that something wrong occured (that's obvious, otherwise an error would not have been emitted). Rather, they should tell you what went wrong using non-jargon-y language and tell you what to do to fix them
