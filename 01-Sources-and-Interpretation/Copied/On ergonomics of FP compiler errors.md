
## Source: On Ergonomics of FP Compiler Errors

http://metaleap.net/blog.ergonomic-purescript-error-messages.html#My%20take:

Jordan
- Many people complain about the cryptic errors of Haskell and PureScript, likely because they do not understand the compiler / type system that well
- Elm, which is an FP language, has great compiler errors, but only because it's type system is much simpler and less powerful
- PureScript's error messages have improved
- Compiler errors shouldn't tell you that something wrong occured (that's obvious, otherwise an error would not have been emitted). Rather, they should tell you what went wrong using non-jargon-y language and tell you what to do to fix them

Alex
- A PureScript user believes error messages should highlight the problem in the code in a way that makes resolution actionable, not explain why it bothers the compiler using technical jargon.
- A PureScript user believes that a compiler is a logic-checker, which means it can not be wrong. So, rather than explain it's full reasoning, it should just provide actionable description of the resolution. If details are desired, provide them in a separate document linked from the error message.
