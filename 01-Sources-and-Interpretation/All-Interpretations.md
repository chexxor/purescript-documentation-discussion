# All Interpretations

The following interpretations have been copied over from various sources. In some situations, they have been further edited or clarified when their meaning was not clear when read in isolation from other things. The bracketed content `[example_slug_name]` refers to the unqiue slug name of a source, so that one could see the full context of that interpretation.

<hr>

## Code as Examples Referenced in Discussions

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

## Comparing Elm, PureScript, and Haskell: which language do I use?

### General Statements

- The target / purpose for learning FP language should be the controlling factor. [Learn_PureScript_or_Haskell_First]
- Good summary of the learning curves of these languages: Elm is lowest, PS is next, Haskell is highest. [Learn_PureScript_or_Haskell_First]
- Learning one language or another does not matter since the type classes and general foundations apply equally to all of them. [Learn_PureScript_or_Haskell_First]

### Specific statements about the langauges

- If one wants to do FP web development and get the full power of FP languages and is willing to pay the cost of a steeper learning curve, then they should start with PureScript. Still, this learning curve could be made less steep if there was more beginner-friendly documentation. [Learn_PureScript_or_Haskell_First]
- "PureScript focuses on Web, Haskell is more general, but in case you're only interested in playing with a functional language, I'd pick PureScript for that." [Learn_PureScript_or_Haskell_First]
- Good summary of the differences between Elm and PS' handling of partial functions: "Elm strive to be total and prevent you from shooting yourself in the foot in any way, while Purescript gives you more freedom, but you have to understand the consequences of what you’re doing." [Elm_PureScript_In_Depth_Overview]askell and Purescript, which one is easier to learn since both use the same concepts that translate easily between both languages (e.g. type classes, Functor, etc.)?" [Learn_PureScript_or_Haskell_First]
- One will be more productive overall in languages that have more mature ecosystem and active communities. However, if one wants to specifically do web programming and not use Haskell's solutions to that problem and needs something more powerful than Elm, then one seems limited to Purescript, Elixir, or Closure. [Learn_PureScript_or_Haskell_First]
- A number of usability issues (REPL slows to a crawl with 10+ packages; bower as package management with psc-package still a WIP) stopped one commentator from continuing choosing PS over Haskell as a language to learn FP. [Learn_PureScript_or_Haskell_First]
    - Addressing this comment, some have been resolved whereas some others have not. AFAIK, the REPL no longer responds that slowly. `psc-package` is that stack-like alternative mentioned above that is become more established. Moreover, `spago` addresses some of its shortcomings due to the tedious nature of modifying packaget sets. However, `spago` does not yet have as much support in various things as `psc-package`.

### Arguments For PS

#### Compared to Elm

- A PureScript user prefers PureScript over Elm because they don't like a language which dogmatically enforces a certain way of programming. [Hitchhikers_Guide_to_Elm]
- A PureScript user believes PureScript's FFI is simpler than Elm. [Hitchhikers_Guide_to_Elm]
- A JavaScript/React/PureScript user believes PureScript's FFI is fairly easy and is better than ReasonML's and Elm's FFI. [Hitchhikers_Guide_to_Elm]
- A PureScript user believes PureScript compiles to smaller amounts of JS than Elm for the same thing, making pages load faster than Elm-written ones. [Hitchhikers_Guide_to_Elm]
- A PureScript user believes that using it is dead-simple because it compiles to JavaScript (because it is readable?). [Hitchhikers_Guide_to_Elm]
- A PureScript user believes that a language can limit what you can do and learn, and is reason for leaving the language. [Hitchhikers_Guide_to_Elm]
- A PureScript user feels limited by Elm's type system. [Hitchhikers_Guide_to_Elm]
- PS has type classes whereas Elm does not: one reason why one might want to use PS instead of Elm. [Elm_PureScript_In_Depth_Overview]
- PS is more precise and powerful at a lower level than Elm. [Elm_PureScript_In_Depth_Overview]

#### Compared to Haskell

- PS' type system is more granular, powerful, and polished than Haskell, avoiding some of its baggage. [Learn_PureScript_or_Haskell_First]
- Using PureScript was more fun than the hassle when compared to the commentator's experience with Haskell. [Learn_PureScript_or_Haskell_First]
- While this person argues that it's generally easier to install and maintain PS than Haskell on a machine, that comment did not account for the major breaking changes that occurred in the `0.12.0` release. Other comments in this post also argue against this point. [Learn_PureScript_or_Haskell_First]
- In short, in this person's experience, PureScript is easy to set up and start coding unlike Haskell in various ways [Learn_PureScript_or_Haskell_First]
- PureScript doesn't require adding language extensions like "OverloadedStrings" or running it with `-Wall` [Learn_PureScript_or_Haskell_First]
- To one person, Haskell's community seems less friendly / welcoming than other languages' communities in general and the Purescript community specifically. [Learn_PureScript_or_Haskell_First]
- Haskell user prefers and welcomed non-fragmented dependency managers. [PureScript_First_Impressions]
- Haskell user prefers and welcomed a centralized documentation site [PureScript_First_Impressions]
- PureScript has better integration with JS build tools (e.g. webpack, parcel, etc.) than Haskell [Learn_PureScript_or_Haskell_First]
- The PureScript core contributor believes that "the Haskell tradition" is having the purpose to explore FP languages, their implementations, and their practices. [Wallowing_in_Despair]

#### No Category

- A PureScript user believes that PureScript is good for solid development of frontend applications. [Hitchhikers_Guide_to_Elm]
- PS' long-term value is that the language can compile to multiple backends quite easily. Still, the exact performance considerations are not as clear as one library maintainer realized when writing [Learn_PureScript_or_Haskell_First] `purescript-sequence`, a FingerTree implementation that was slower than Array until its size got very large.
- "the install and setup of the environment is straight forward." [My_Experience_With_PureScript_So_Far]
- build tools supporting fast feedback loops make developers more productive [My_Experience_With_PureScript_So_Far]
- `pulp` was simple to set up things [PureScript_First_Impressions]
- PS has excellent documentation browsing [My_Experience_With_PureScript_So_Far]
- PS has great out-of-box support for Atom IDE [My_Experience_With_PureScript_So_Far]
- Atom support was easy to set up [PureScript_First_Impressions]
- Making implicit partial functions explicit helped one adhere to type-driven development, which also had some educational benefits [My_Experience_With_PureScript_So_Far]

### Arguments Against using PS

#### Compared to Haskell

- Haskell's stronger ecosystem might make it easier for the OP to learn domain-specific concepts (e.g. parsing, cryptography, etc.) in an FP style [Learn_PureScript_or_Haskell_First]- Haskell's stronger ecosystem might make it easier for the OP to learn domain-specific concepts (e.g. parsing, cryptography, etc.) in an FP style [Learn_PureScript_or_Haskell_First]
- GHC has better error messages than PureScript. This was likely true. I'm not whether that gap has decreased in the last year or not and by how much. I think it's likely still the same. [Learn_PureScript_or_Haskell_First]

#### Compared to Elm

- A non-PureScript user prefers a simple language with a gradual/short learning curve and is willing to compromise on the quantity of manually-written code to have it. [Hitchhikers_Guide_to_Elm]
- Elm is more approachable simply because it is less powerful and requires learning less. [Elm_PureScript_In_Depth_Overview]
- Elm is appealing because it's application structure is well-understood. To get the same appeal, the 'best practices' for application structure should be well documented in PS. [Elm_PureScript_In_Depth_Overview]
- Elm seems to provide a gentler introduction to FP concepts than Haskell or PureScript primarily because it has less features and potentially has better documentation than PureScript did at that time. [Learn_PureScript_or_Haskell_First]

#### No Category

- There are other FP-like languages out there besides PureScript that might be a better 'next step' for Elm programmers. [Wallowing_in_Despair]
- Post-`0.12.0` release, user expected that language's community won't be able to reach ecosystem coherence for a while. [PureScript_First_Impressions]
- Person thinks that one should only learn PS for web/JS replacement. [Learn_PureScript_or_Haskell_First]
- Author started book with presupposition that static FP languages are worth their learning curve but has now concluded that perhaps this is not true. [Wallowing_in_Despair]

## Various "Learning Paths" to reach PureScript

### From Elm

- A PureScript user entered PureScript after going through Elm. [Hitchhikers_Guide_to_Elm]
- Elm could be a useful 'gateway drug' into PureScript [Elm_PureScript_In_Depth_Overview]
- Pux could be a "gateway drug" library from Elm into PS [Elm_PureScript_In_Depth_Overview]
- It seemed the FP community responded with something like, "Why the hell would one start with Elm and then transition into PureScript? Why not just start with PureScript?" [Wallowing_in_Despair]
- A core contributor doesn't think the "Elm -> PS" path is a stupid idea. In some ways, it might be better than the "JS -> PS" path some others take. [Wallowing_in_Despair]
- It seems if one wants to do web development using an FP paradigm, Elm has better learning resources to help one get familiar with the concepts before switching to Purescript. Again, Elm as a "gateway drug" into PureScript seems like a good possibility. [Learn_PureScript_or_Haskell_First]
- Probably addressing the last thought in the previous comment, the author shows that Elm has more in common with PureScript than the commentor thought. [Wallowing_in_Despair]
- There is no clear path (learning path perhaps?) from Elm, which has a gentle learner curve, to a more powerful general-purpose FP language. [Wallowing_in_Despair]
- PureScript core contributor says that Elm users don't think in terms of Functor/Monad (because those terms aren't in their language/libraries?). While these patterns have naturally emerged in Elm, their community doesn't think/design in terms of it. [Wallowing_in_Despair]
- Highlights that there is a large philosophical difference between the two languages: Elm and PureScript. [Wallowing_in_Despair]

### From Haskell

- If one's goal is to learn an FP language, learning Haskell and then PureScript isn't necessarily a bad idea since Haskell and PureScript are very similar and Haskell is arguably more powerful than PureScript. However, if one's goal is to learn PureScript or do website development, it would be unfortunate to learn Haskell before learning PureScript. [Learn_PureScript_or_Haskell_First]
- Haskell has more documentation (but better?) than PureScript, so Haskell is recommended for newcomers. It's not entirely clear whether the Haskell documentation is "better" than PureScript, but it is implied. [Learn_PureScript_or_Haskell_First]
- Seems like Haskell had more material than PureScript: if one did not satisfy you or help you, you could look at another tutorial/guide. If you encounter the same situation in PureScript, tough luck as there isn't another tutorial/guide. [Learn_PureScript_or_Haskell_First]

### No Category

- Good insight here: one can look at material from all three languages (PS, Haskell, Elm) to get a better understanding for how the code works. In other words, the concepts can translate from one language to another. [Learn_PureScript_or_Haskell_First]

## Ideas for how to improve PS Docs

### Things that need to be fixed

- There are lots of easy documentation problems to resolve in the core documentation. [Features_You_Want_Future_PureScript_to_Not_Have]
- PureScript by Example uses `unsafePartial` in such a way that it might wrongly imply that one uses it more frequently than one actually does. [Elm_PureScript_In_Depth_Overview]
- The reasons for using `unsafePartial` might not be well-documented/explained [Elm_PureScript_In_Depth_Overview]
- Help/Documentation on using Pursuit's search could be better highlighted to draw more attention to it. [PureScript_First_Impressions]
- Any conversations made on Slack that are worth keeping long-term (e.g. answers to stupid questions) do not persist long-term. This seems to contribute to new users asking the same questions again and again, taking time away from advanced users in the language from spending time on other more useful things. [The_State_of_Things]

### Things that can be improved

- The documentation repo's error pages are not up-to-date or completely filled out [The_State_of_Things]
- Regular compiler error messages do not also output the information one would see via a type-directed search to help the user determine what they are probably trying to write but failing to write. Elixir's compiler does this. [My_Experience_With_PureScript_So_Far]
- The FFI documentation should explain the disadvantages of giving first-class syntax for Javascript FFI due to PS' "compile to multiple backends" nature. [PureScript_First_Impressions]
- The FFI documentation should explain the advantages of writing an implementation for some function outside of the PureScript langauge (i.e. in Javascript source file): "allows you to fake out all non-pure state and effects and get as close to pure as possible." [PureScript_First_Impressions]
- A better version of Bower would be a huge improvement for PS community's build tooling. [PureScript_First_Impressions]
- Public acknowledgement that some people (not defined here) do not know how to update Try Purescript and Pursuit. (Secondary source) - Phil and Harry might be the only ones who know how to update it. [The_State_of_Things]
- Encouraging new users to open issues for documentation issues would help track down what already-written documentation is not immediately understandable to new users and what entities have yet to be documented. [The_State_of_Things]
- Perhaps providing a single centralized location for all cross-repo documentation issues that are easy enough for new beginners to do would help. To aid in recognition, they could all use the same label name: `new contributor`. [The_State_of_Things]
- The documentation repo is presented as a loose collection of potentially unrelated articles, not as a systematic presentation of articles that all fit within a larger vision. [The_State_of_Things]
- Author believes it's best for people with high status in a community to find ways to make low-status (unattractive?) jobs more attractive. [Wallowing_in_Despair]

## Problems New Learners Face when Learning PS

### Baggage Learners Bring with Them

- People who hear that Purescript "compiles to Javascript" incorrectly assume/expect it to use a syntax similar to Javascript or other compile-to-JS languages. [Elm_PureScript_In_Depth_Overview]
- Author expects such explanations to be made in the module/function/type's documentation as found in Pursuit rather than some external resource like `Purescript By Example`, which does a good job explaing what that is. Linking to such explanations might address such pain points. [My_Experience_With_PureScript_So_Far]
    - Library (`purescript-assert`?) likely did not yet provide `assertX` with custom warning errors attached to it like `quickCheck (\a -> a <?> "custom warning error when it fails")` [My_Experience_With_PureScript_So_Far]
    - Author possibly assumes that unit testing is the default testing used for FP languages rather than property testing [My_Experience_With_PureScript_So_Far]
    - Author possible does not know about `purescript-spec` as a testing library [My_Experience_With_PureScript_So_Far]
- FP language's roots and similarities do not seem to be well-understood by outsiders and may contribute to outsiders' lack of understanding or initial expectations about FP languages that get broken. [Wallowing_in_Despair]

### No Category

- Author's first major issue and turn off was not being able to read the syntax of a Haskell-like language. This issue alone made him choose to look at Elm rather than PureScript, which is arguably more powerful than Elm. Unlike most people, the author did not give up and looked at Haskell/PureScript again, eventually reaching an understanding via each language's "standard" for learning them. [Elm_PureScript_In_Depth_Overview]
- A PureScript user has trouble figuring out how to solve application problems in PureScript, which is a reason for why PureScript is hard to learn. [Hitchhikers_Guide_to_Elm]
- A PureScript user feels rewarded when using PureScript because the primary sticking points are figuring out how to do things *in* the language, rather than figuring out *non-language* problems. [Hitchhikers_Guide_to_Elm]
- The `do` syntax was not immediately understood by the author. [Elm_PureScript_In_Depth_Overview]
- A PureScript user believes that learning PureScript is hard to learn, and the reason is it is powerful. [Hitchhikers_Guide_to_Elm]
- Not being able to mutate variables is a hard thing to initally grasp by new learners who are used to doing so freely. [Elm_PureScript_In_Depth_Overview]
- I don't know whether this concept (local and controlled side effects are still considered 'pure' if functions are referentially transparent) is well-documented in PureScript learning resources (even in my own, Jordan's PureScript Reference) [Elm_PureScript_In_Depth_Overview]
- The Haskell book has exercises in addition to its explanations. [Learn_PureScript_or_Haskell_First]
- a core contributor for PS did not recommend PS to people new to FP seemingly because the learning resources for PS were not as good as Haskell's. [Learn_PureScript_or_Haskell_First]
- Person might not have known about PS' other backends that make it more viable in the long-term. PS' "compile-to-anything" nature may not be well publicized. [Learn_PureScript_or_Haskell_First]
- Migrating to psc-package requires a manual process. Not sure how much time that takes. [PureScript_First_Impressions]
- User did not understand the compiler errors user got as a result of not importing Prelude. [My_Experience_With_PureScript_So_Far]
- New learner experienced minor issue with build tool (need to researt it to sync with current state of build) [My_Experience_With_PureScript_So_Far]
- Newcomers to the language feel antagonized by the unfamiliar concepts and language operators. Perhaps documentation can mitigate the confusion and anguish experienced by newcomers. [My_Experience_With_PureScript_So_Far]

## Ways to Improve New Learner Experience

- Having a 'beginner-friendly' version of Pursuit search that highlights / prioritizes / highly ranks the common things new learners would search for would be helpful. [My_Experience_With_PureScript_So_Far]
- Being required to import each import is tedious and annoying.  [My_Experience_With_PureScript_So_Far]
    - However, the person might not know that the `atom-ide` / `purescript-lang` atom packages enable one to type in the Type, hit tab for the autocomplete, and the IDE will insert both the autocompletion and import the module if it's not imported already. This issue and its possible solution could be better documented.
    - The person might also not know that people often define their own Prelude to account for the above annoyance
- The PS language site was the first thing new learner went to. The oudated Eff-based example created a horrible new-user experience [PureScript_First_Impressions]
- New users like to use Pursuit to learn how to solve problems when writing the language / understand what some concept/function/type is. [PureScript_First_Impressions]
- new learner found it annoying that PS FFI requires a lot of boilerplate to be written. [PureScript_First_Impressions]
    - There might be code generation solutions to the above problem that he did not know about.
- The FFI maybe needs better documentation, especially for a newcomer to statically-typed language. [PureScript_First_Impressions]
- A suggestion for reducing the number of communication groups within PS down to 3 and defining general "policies" for what should go where [The_State_of_Things]
- Some users perceive that PS has a frequent breaking-changes language release cycle. This perception was true at various parts in the release, but hasn't been recently. [The_State_of_Things]
    - The number of weeks until next breaking change, starting at `v0.5.0` and going to `v0.12.0`: `10 28 34 31 17 18 25 60`
    - The average of the above number series: `27.875 weeks`
- There is a public awareness within the PS community that the documentation repo is not fully up-to-date with the PureScript language [The_State_of_Things]
- user questions the lack of better FFI support via libraries that handle/write it for developers [PureScript_First_Impressions]
- Outdated materials/websites are currently included in the main PureScript language's website. These should be removed to prevent new learners from thinking that these resources are in-sync with the latest PureScript language. [The_State_of_Things]
- Writing FFI is very boilerplate-y and wastes developer time. There should be a faster way to do the same thing, potentially via a library or through code generation. [PureScript_First_Impressions]
- Nix is really nice for FP libraries but difficult to set up [PureScript_First_Impressions]
- The PureScript by Example book is not fully up-to-date with the PureScript language. [The_State_of_Things]

## PureScript's Mediums of Communication

- GitHub issues should not be used for "help me" questions. [The_State_of_Things]
- Slack is **sometimes** good for getting immediate response and transient things [The_State_of_Things]
- Slack is the "go to" for stupid questions [The_State_of_Things]
- Slack is useful for short conversations that work across timezones and internet connectivity issues. [The_State_of_Things]
- Slack acts as a newsfeed of sorts for PureScript [The_State_of_Things]
- Discourse is **preferred** for seemingly longer discussions that aren't quite worthy of a GitHub issue [The_State_of_Things]

## Why Previous Documentation Efforts Failed

- PS documentation has always been bad. This problem has been the same throughout its history in that it hasn't gotten worse over time [The_State_of_Things]

### Limited Manpower

- The workload is too great for one person to do alone without burning out. [The_State_of_Things]
- There is public acknowledgement that there are not enough workers to keep the documentation resources in-sync with latest language releases. As a result, much time is spent putting out fires rather than moving the language/ecosystem forward. [The_State_of_Things]
- Volunteer-based languages and their development do not have the same luxuries/resources as other languages. The desire to get somewhere exists, but not the time, especially when language changes/improvements break current documentation. [Wallowing_in_Despair]
- A core contributor is already stretched thin with maintaining code, so asking for better documentation is too much to ask. [Wallowing_in_Despair]

### Trusting People with Write Access to Repos and Supporting Them

- One cannot use the "nobody gets paid to do it" reason as an excuse for poor documentation. Others have the same restraint and yet still succeed. [Wallowing_in_Despair]
- Responding to core contributor's post about being stretched thin, the author suggests sharing the load with others. [Wallowing_in_Despair]
- Core contributor thinks idea sounds good [Wallowing_in_Despair]
    - (This reminds me of the point that the Elm creator mentioned in his talk about "The Hard Parts of Open Source") [Wallowing_in_Despair]
- Getting support from core contributors would greatly impact the author's work. [Wallowing_in_Despair]
- Core contributor does not know what extra support the author expects while the author is contributing to PureScript. [Wallowing_in_Despair]
- Core contributor believes that accepting documentation means it needs to be reviewed. [Wallowing_in_Despair]
- Core contributor believes that some people are better or faster at reviewing documentation than others. [Wallowing_in_Despair]
- Core contributor believes that reviewing documentation can be just as difficult, if not more so, than reviewing code. [Wallowing_in_Despair]
- The author believes that enthusiasm in contributing to docs lowers when it takes a long time to make a contribution (without getting a reward, like a merged PR?). [Wallowing_in_Despair]
- The author believes that it's OK to allow a slightly-incorrect piece of documentation to exist if it's clear the documentation author is different from the code author, and the documentation author promises to maintain the documentation. [Wallowing_in_Despair]
- The author cites evidence that even a trivial change to a core library goes unmaintained for weeks. [Wallowing_in_Despair]
- The author believes that being trusted with commit-rights to a library will encourage him to be more productive. [Wallowing_in_Despair]
- One has offered to maintain Pursuit, but might need some (but likely not a lot) help getting oriented to the project [The_State_of_Things]

### Breaking Changes Renders Documentation Outdated

- Keeping documentation up-to-date via the medium of a book costs a lot of time. Breaking changes quickly destroys much of this work. [The_State_of_Things]
- Using Try Purescript as 'learning environment with PureScript already installed' became an unreliable environment due to a breaking change. [The_State_of_Things]
- It would be best to hold off on documentation until a stable language specification is defined. Otherwise, the same problems encountered above (quickly outdated learning resources that cost a lot of time to make) will occur again. [The_State_of_Things]
- A breaking change in the language sometimes greatly impacts the ecosystem and other times only minorly impacts it. [The_State_of_Things]
- Core contributor is expressing belief that breaking changes in core libraries are not likely to happen in the future as frequently and that language is finally stablizing. [The_State_of_Things]
- There is a lack of communication between the language developers/contributors and those who document the language about what changes will be included/excluded in the next release. This makes it harder for the documenter to know what to write, what to correct/change/fix, and what to continue ignoring. [The_State_of_Things]
- There is a lack of communication about the release schedule of the language and 'saving' all breaking changes for a single major release. [The_State_of_Things]

### FP "Best Practices" are not well-defined, are assumed, or are unconscious habits

- The commentor might be implying that all statically-typed FP languages don't share a common set of idioms. [Wallowing_in_Despair]
- It seemed the FP community thought that studying and documenting idioms/"design patterns"/habits of good FP programmers wasn't worth it. [Wallowing_in_Despair]
- It seems hard for the author (who is not as well-versed in FP idioms) to document them when those who know them don't care enough to share them. [Wallowing_in_Despair]
- Some FP idioms exist across FP languages (e.g. type classes) whereas others are specific to the language. As an example, the commentor believes that Elm doesn't have the same idioms as languages like PureScript. [Wallowing_in_Despair]
- The goal of documenting FP idioms is a great goal, but it's not clear how this could be done easily. [Wallowing_in_Despair]
- Many FP programmers don't consciously know the habits they have developed over time. Some habits, they may take for granted and assume others do likewise, being surprised to find that others don't. [Wallowing_in_Despair]
- The author believes that all fields of study need to document their idioms (best-practices?) and discuss them. The author says that programming communities (and FP communities specifically) do not tend to do this. [Wallowing_in_Despair]
- The author believes the FP community is blind to/ignores the idioms and practices of the wider programming language community because the FP community values aesthetics (over pragmatism?). [Wallowing_in_Despair]
- Saying that Elm is not a part of the Haskell tradition seems like a stupid thing to say because of how obvious its truth seems to be. [Wallowing_in_Despair]
- The PureScript core contributor may be implying that the difference between a programming language community which uses terms referring to academic theory and one which simply applies the benefits of the theories is that members of the former community thinks in terms of theory while members of the latter are blind to the theory when developing their programs and think only in terms of their program's domain. [Wallowing_in_Despair]
- The author, in contrast, believes that "the Haskell tradition" is having the language features of Haskell and the idioms used by the Haskell community. [Wallowing_in_Despair]
- It seems the author and the commentor were using the same word to mean different things. [Wallowing_in_Despair]

### No Category

- There is "issue spam" in the language repo's issue tracker, making it harder to see what really needs to be done / should be done to get a `v1.0` release. [The_State_of_Things]
- PureScript tends to draw intellectually curious people. [Wallowing_in_Despair]
- Each non-Elm language, general-purpose pure FP language, seems to have pros which are outweighed by the "warts" of the language. [Wallowing_in_Despair]
- Seems like the commentor is saying, "Wait. Is the book for the FP community, too? I thought it was only for Elm programmers... [Wallowing_in_Despair]
- Core contributor was prioritizing an important breaking-change release in the compiler and updating libraries to work with it over improving current documentation. [Wallowing_in_Despair]
- The author's incentive is to improve the language to help him make better programs, not necessarily explaining the language to others. [Wallowing_in_Despair]
- The author's definition of being welcomed into a language community is when an "insider" tells others to listen to him, even if he's probably wrong. [Wallowing_in_Despair]
- Writing new docs or improving old ones is a good way to get started with a language. [The_State_of_Things]

## Why a "v1.0" release has not been made

- There does not seem to be a well-defined mutually-held 'vision' for the future of the language's development. As a result, it's hard to start writing documentation material that will coincide with the `v1.0` release of the language. [The_State_of_Things]
- A proposal for how to make a `v1.0` release (mentioned before but encountered resistance from other core contributors) [The_State_of_Things]
    - fix any bugs that can't be documented
    - engineer things to make anticipated future additions easy / non-breaking
    - write a spec for the language
    - commit to stable release window
- Two potential breaking changes (one would require polykinds and the other would require quantified constraints) may come at a later unknown time. [The_State_of_Things]
- The 'resistance' mentioned before was based in not wanting to produce breaking changes in later releases. The 'resistance' stil exists in a small manner in that `garyb` does not want a complete "feature freeze." However, it's no longer about stopping a `v1.0` as much as it is a "how do we make `v1.0` that does not require us to introduce breaking changes soon after its release?" [The_State_of_Things]
- Post-`0.12.0` release, a language release does not imply ecosystem compatibility immediately after its release. [PureScript_First_Impressions]
- Those that follow Haskell tend to follow its motto, "avoid success at all costs," which the author seems to interpret (via implication) as "avoid mainstream usage at all costs." [Wallowing_in_Despair]
    - The "avoid success at all costs" phrase should be understood as "avoid (success at all costs)," meaning avoid short-term gain or other niceities that cause problems later and prioritize/pursue long-term goals that provide great foundations and are overall better.
- The PureScript core contributor believes that PureScript follows Haskell for now, but might not in the future. [Wallowing_in_Despair]
- Whether "PureScript is production-ready yet" depends on one's use-case, which is different for everyone. [Wallowing_in_Despair]
- Core contributor is perfectly fine with saying, "PureScript shouldn't be used if one can accomplish their goals using Elm." [Wallowing_in_Despair]
- Since PureScript is still a newer language, some people that use it in production rely upon only one expert to fix problems that most others do not know how to fix. [The_State_of_Things]

## Things that have changed since 'The State of Things'

- Thomas Honeyman implemented the [Real World App] for PureScript
- Core contributors released two new releases of PureScript (`0.12.1`, `0.12.2`) after a period where language development had slowed
- Jordan Martinez wrote his PureScript Reference learning repo
- Jusin Woo and Fabrizio Ferrai have made `spago` more mature and a viable `Bower` alternative once it fully integrates with rest of PS infrastructure (e.g. Pursuit)

<hr>

[Author_Venting_About_Book]

- Author is in a very negative emotional state and is likely venting as a way to express those feelings and process those feelings. Author perceives that people with influence either hate or are apathetic about his book. Since the book did not accomplish it's goals, it felt like a wasted year. Author percieves that author's desire to help is perceived by others as a problem, not a blessing. It seems like this pattern of 'not being recognized/heard' has happened before. [Author_Venting_About_Book]
- It's hard to say whether Haskellish languages were actually successful after 40 years, so we need people who assess it now and make predictions.[Author_Venting_About_Book]
- Biggest concern author has: the kind of culture that FP languages tend to develop never grow large enough that they make an impact/difference in the mainstream. [Author_Venting_About_Book]
- Author clarifies what that 'subculture' is while being in a very negative emotional mood: [Author_Venting_About_Book]
    - it attracts/creates people who use a particular language
    - these kinds of people aren't the best ones to share it with others / show convincingly that FP languages are better than the status quo.
    - This situation continuously loops and the problem never gets fixed.
- Elm is a not a bad 'first step' but one quickly realizes its limitations when someone tries to do something outside of its intended scope. [Author_Venting_About_Book]
- Basic ideas of this video: [Author_Venting_About_Book]
    - Type classes were 'discovered' because one guy misunderstood what another guy meant
    - **Type classes allow a programmer to use "dumb reusable types" (e.g. `Either`, `Maybe`, `Tuple`, `List`) whose contained types (e.g. the `Int` type in `Maybe Int`) are later 'constrained' with the required properties need to do some computation (i.e. a number-like type that can be added via `Monoid`)**
    - There are two styles of 'type classes:' real type classes and 'implicits' (Scala's type classes, Rust's "traits", etc.)
    - Implicit-styled type classes are more "powerful" in one degree but end up leading to possibilties that make programming harder. Haskell type classes do not add this 'benefit,' so using type classes are more reliable and easier to reason about. The key issue is commutativity: if some type has an instance for a sub type class (e.g. given there is an `Ord a`...), then logically there are ways to determine its intance for a super type class (e.g. ... then there is also a `Eq (List a)`)
    - Addressing "but why can't we just do X" reasons (including his thoughts for why Coq/Agda/Iris or, `a`, etc. other dependently-typed languages won't provide the 'refactor and it still works' guarantees of Haskell)
- Referring to the bolded part above, this is the kind of knowledge that struggles to make its way out of the FP community. [Author_Venting_About_Book]
- `kmett` might be a good person to follow for extracting FP knowledge that remains otherwise stuck in 'knowledge silos.' [Author_Venting_About_Book]
- Author reflects that there is a missing point of contact between two communities, so that it does not succeed in either one of them. The implied communities are the non-FP / mainstream community and FP community. [Author_Venting_About_Book]

- PureScript is a more powerful language than Elm but provides less guidances as to how to write code [Elm_019_Broke_Us]
- Source hopes to move to PureScript once it stabilizes more [Elm_019_Broke_Us]
- One person's perception of PureScript is scary, possibly due to HKTs and other "Haskell-y" stuff [Elm_019_Broke_Us]
- Community member did a good job of using scaffolding to lessen the fear of PureScript: if you already get X ("comparable", "Cmd"), then Y (type classes, effect system) is X + 1. [Elm_019_Broke_Us]
- Another Elm-inspired framework recommended is `purescript-hedwig` [Elm_019_Broke_Us]
- Source advised against Pux due to lack of documentation [Elm_019_Broke_Us]
- A person intended to write documentation which helps one transition from Elm into PureScript [Elm_019_Broke_Us]
- There is a library that feels similar to Elm to help Elm programmers transition to PureScript [Elm_019_Broke_Us]
- No examples given of this 'documentation gap,' but I think everyone agrees it exists [Elm_019_Broke_Us]
- A newcomer believes documentation of the background of PureScript is necessary qualification of a production-quality language [Elm_019_Broke_Us]
- A newcomer believes the PureScript community's level of satisfaction of its documentation and infrastructure is less than that of other programming languages. [Elm_019_Broke_Us]
- A newcomer believes the PureScript community is friendly to beginners and contributors. [Elm_019_Broke_Us]
- Source believes that PureScript leaders do not care about documentation/standards/infrastructure of PS [Elm_019_Broke_Us]
- The "leaders" are never defined here, but it probably refers to the core contributors. [Elm_019_Broke_Us]
- If that was the opinion of the leaders, why was that the case? Is it still the case now and if so why? [Elm_019_Broke_Us]
- PureScript is not suited for mainstream use yet but more for forward-thinking people who may get burned by future web developments [Elm_019_Broke_Us]
- Someone else has tried the Feynman technique, similar to Jordan's purescript reference work [Elm_019_Broke_Us]
- Elm as a "gateway drug" to PureScript may have competition from other FP languages: ReasonML [Elm_019_Broke_Us]
- Source may have had disagreements with PureScript leaders that was fueled more by emotions than logical arguments and understanding one another's viewpoints. [Elm_019_Broke_Us]
- Source may have also just wanted really good documentation but did not receive the desired support from core contributors [Elm_019_Broke_Us]
- General perception is that learning curve is steep and hidden behind a lot of jargon [Elm_019_Broke_Us]
- PureScript is less frustrating than Elm? [Elm_019_Broke_Us]
- ReasonML might be an easier destination for Elm users than PureScript due to being more mature in a few important areas. [Elm_019_Broke_Us]
- Source is moving towards langauges with stronger FP concepts than Elm. [Elm_019_Broke_Us]
- PS users might be watching Elm channels of communication as a way to encourage people to switch to it...? [Elm_019_Broke_Us]
