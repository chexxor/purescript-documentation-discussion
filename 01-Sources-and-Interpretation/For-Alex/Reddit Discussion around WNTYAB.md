
## Source: Reddit discussion around 'what nobody tells you about documentation'

https://www.reddit.com/r/programming/comments/9i0jgh/what_nobody_tells_you_about_documentation/

### Openint Thread

[just links to the original post]

### Thread

> The really hard part is keeping the end user in mind.
> You have:
> - Documentation for new core developers
> - Documentation for plug-in developers
> - Documentation for distributors
> - Documentation for end users
>
> Some of those four parts are going to aim at 1, 2, 3 or even all 4 of those groups. You might need several copies. Or just abbreviated versions. Or links to external versions.

- In reality, there are more than 4 different types of documentation. Let's think fo the many dimensions:
    - The 4 normal types (intended audience based on goal): get started, how to do one thing, reference, explanation
    - The X audiences based on background / purpose (new core developers, plug-in developers, distributors, end-users).
- Putting the above idea into terms of PS
    - audience based on background: Javascript, Haskell, Elm, TypeScript, other language entirely
    - audience based on purpose: front-end or back-end, each with these concerns (performance, complex logic, hitting quick deadline, migrating to better system, refactor-heavy due to prototypal nature)

### Comment

> Documentation is hard to get right and it only gets harder when documentation exists in multiple places.
> Not that I've seen it implemented, but shouldn't it be possible to encode all your documentation in a single place with a formatting scheme (e.g. CSS classes, conditional display by URI) to show/hide content based upon the use case?
> I won't claim to have a handle on the latest and greatest solutions but, if anyone has any suggestions which meet the criteria of encoding all relevant information in a single place and conditionally presenting it to users, that'd be much appreciated.

- Knowledge can at best be encoded into views that we call 'documentation.' Documentation is 'good' when one's view happens to correlate with what they need to 'see' at a given time. However, due to how 'views' work, they must explain the same concepts in different orders, show some content rather than other content based on what the reader needs, etc.

### Comment

> That's typically not a good practice. It is true that avoiding duplication is strongly encouraged in code and configuration. But different types of docs present information in different order, using different words, assuming different reader background, putting different emphasis. Good documentation will have references in all the right places to have the reader navigate it properly, where "properly" varies between types of documentation.

- Having documentation in a centralized place is not what's important. Rather, the ease with which one navigates throughout an ecosystem's documentation is important. If the documentation can answer questions like "Does the user know where to find X knowledge given that they now/already now Y, and can they easily get there?"

> Essentially, yes there's duplication, with all the same problems (e.g. copies going out of sync, same mistakes having to be fixed in multiple places) but I haven't seen a better way of doing it. Trying to refactor like software frequently makes it an unreadable mess.

- Documentation, by nature, goes out of sync quickly because the code it documents changes.

### Comment

> Easy to picture applying a taxonomy to the information set and using templates w/transclusion to generate docs if all the documentation were in a CMS, just wondering if a native application specific to technical documentation exists.

> It may just be wishful thinking, but I've got to believe that the problem space of information architecture for documentation must have evolved beyond maintaining auto-documentation for code libraries + an API reference guide w/HOWTO's + an end user guide w/HOWTO's + sales documentation, etc.

- Documentation might be a problem space worth monetizing if someone can think of a good solution for that problem.

### Comment

> I'd be very happy to see such a system evolve but like I said, I haven't seen one yet. It's possible that one is right around the corner, and you are more than welcome to take a stab at it. But understand that it is not just the technical part of organizing and labeling information: it also has a cultural component. You will have to build up a community of people who understands how to best author the information presented in a new medium. And those who can pass the knowledge on. That part takes far longer than the technical implementation. You'll need experience writing documentation that others find useful, and you'll need to ask yourself which part of it was the most tedious part. Finally, you'll need to automate away the parts you found tedious. As for me, I'll admit I do not even have a problem statement formalized enough, let alone a solution.
> So no, I wouldn't say these problems "have evolved" to that point yet, just that they can evolve :)

- Part of the issue of documentation is the cultural aspects of it: if others do not have the culture of writing it, then it won't get done.
- The next part is finding people who can write good documentation.
- The last part is finding good ways to automate tedious tasks.


### Comment

> I'm sure you can make some fancy flow chart scheme to acheive this, but at the end of the day the documents are separate enough in use case and wording to where each "fork" is different enough to justify some duplication.Remember, DRY's goal is to reduce redundancy, but redundancy isn't an objectively negative thing (just ask network engineers).
> The most optimal way on top of this would be to just make sure you can properly filter to exactly all the documents a change will effect. Which is non-trivial in and of itself.

- Visual flow charts that adhere to the code might replace documentation...? One thought that comes to mind is [Teaching New Tricks to Old Programs](https://www.youtube.com/watch?v=vzLK_xE9Zy8&index=3&list=LL0RItGq_oLk-fvqppBpwtew&t=0s) which could literally visualize a program (see 34:00 and onward)

### Comment

> There's only two forms of documentation that seem to remain useful after a year or so.
> First, straight documentation of all the supported functionality. Even when it is out of date, it provides useful insight to what you can do, or at the very least what it tried to do.
> Second, getting started tutorials. With any new piece of software it's sometimes hard to grok the basic syntax/use case/interface. Having a guide that lets you know how to use the very core functionality can make a huge difference. We've all opened a new tool/framework/application and thought "okay, I know this thing was built to do X, the documentation says I need to just runX, but how and where?" I often get over that first hump much faster with a few pages of setup documentation and toy examples.
> All forms of documentation are useful, but in my experience the other kinds they wilt so fast that all attempts to maintain them fail.

- good documentation might just cover the 'basic idea' well and how to get started
- Of the 4 types, 2 quickly go stale after 1 year and need updating

### Thread

(Context)

> Is this considered common knowledge?
> I ask because I've been in the field for a while but never had it click until reading this article. This makes so much sense and I feel it will be extremely valuable when I write documentation in the future.

### Comment

> I have not found it refer to four distinct parts yet.
> I also am not sure if separating the four does good.
> Why should documentation not include all of it? Short code examples, and usage examples. And more explanation to it, too, including an API documentation.

- Examples speak clearer than documentation

### Comment

> The author doesn't seem to be suggesting the four be separated as in four distinct different documentation. Just that when you do document, you make sure your documentation covers the 4 parts where possible.

### Comment

> And that it covers the parts somewhat separately. Don't put tutorials inside your reference docs, put them as a separate page. However, do link between the two regularly so that users can connect the dots.

- 4 types are boundaries that are kept within the content of each type. One can still store them in the same overall project as long as there is a clear boundary between them.

### Comment

> That depends on what you understand and think by separation.
> When I'm a new user to the software I don't want technical details, or concept elaborations, or specific how-tos for very specific issues. I want an introduction, something to get an idea of the software and how it works.
> If the other parts are too close to that, too integrated, it will convolute the documentation for me as a reader with clutter, for now uninteresting stuff stealing focus.

- Getting Started guides that do not distract with other important but not relevant-at-the-time matters are what new learners want
- People who write such guides might struggle to know what to include and exclude because they know what the trade-offs are.

> For the documenter too closely integrated documentation is harder to maintain, harder to spot what needs changes. If it is well structured and separated, that should be a lot easier.
> Of course that does not mean it has to be completely separate, separately hosted documentation instances. And of course they should link to related other documentation. As long as there is distinct separation on an article/page level that's separated enough.

- closely integrated documentation is harder to maintain; loosely integrated documentation is easier to maintain

> The page you linked, to fpm, doesn't seem to have a lot of documentation. The intro page spans all areas of course. There is Packages which clearly is technical reference documentation - so it is separate from the other documentation. Use Cases is more of a tutorial and how-to.

### Thread

> I will say writing the difference between context and reference is hard. Mainly because context relies on others problems. You can't just write a perfect paragraph describing how to use the code, unless you have people with questions. Otherwise you are shooting in the dark.

- It's hard to write some documentation without a good problem to solve. Thinking of such problems is hard but very easy when someone else comes to you with one.

> I will say I love godoc. https://blog.golang.org/godoc-documenting-go-code
> Converts your code to https://godoc.org automatically.
> Which is just a pleasure on top of go just being a pleasure to read.

- I think this concept already exists in PS via Pursuit and the `purs docs` / `pulp publish` commands

### Thread

> Not directly a response to the article but, why do so many developers care so little about documentation? The stuff is ground zero of your user experience.
> Sometimes I feel like having terrible documentation feels like the developer equivalent of hazing: I had to suffer through this, so you will have to too.

- Why don't developers care more about docs?
- Lack of documentation feels like a form of hazing

### Comment

> Off the top of my head:
> - Because programming is much more interesting than writing docs
> - Because docs don't add any feature nor fix any bugs, it can be seen as useless work
> - Because programming skills don't have to tranfer to writing skills
>
> Am guilty of this as well. I guess writing docs should really be thought of as being part of writing code ideally.

- If the concept "your code is documented or it fails to compile" could be enforced, this would address this issue
- Writing documentation isn't "fun", doesn't add new features / fix bugs, and doesn't use skills that a programming job requires

### Comment

> Yeah. It is much more fun to write code than write documentation. The problem for me is just how to convey and how much to convey. The 4 audiences are a good start.

- Sometimes the intent to write is there but not knowing what to say is the bottleneck / wall people hit before stopping.

> Given how long I have been writing inline documentation. I feel confident in writing what I feel is good information. I am wrong. I am always wrong. Seeing someone come in and modify the shit I wrote is impressive and makes me sad.

- What you think is 'good' documentation is never 'good enough' in someone else's eyes.

> Also there is the, "don't write comments that are obvious" rule. If I have a function or method that increments then how much should I write? The method is "self-documenting" but it isn't. What other information is needed to ensure the reason the method or function is incrementing?

- Some writers get stopped at, "When is 'self-documenting' code via type signatures and the entity's name good enough and when should it be documented?"

### Comment

> More specifically, everything except reference is useless to the person writing it, because by definition, documentation is written by someone who already knows the stuff they're writing.

- Writing documentation (for 3 of 4 types) is useless to the writer as long as the writer already knows it.

### Comment

> Absolutely. Which reminds me of the recent post about typing skills not being a hinderance to being a good programmer. Clearly both typing and language skills are very important when fleshing out succinct docs without (many) errors.

- a good programmer does not need to be great at typing or other skills required for writing good docs.

### Comment

> In addition to Kametrixom's comment, early on you might not want to write documentation because things are still in flux.
> (Then before you know it ... you've already pushed v1.0 and writing documentation from the ground up now feels like too much of a chore!)

- What's the point in writing documentation if you know that an upcoming breaking change will make it outdated?

### Comment

> The other comments answering that question are great. I think also there's often elitism and perspective problems. Some programmers are like, "well, my code is readable and who needs comments when there's readable code?". They ignore the fact that reading code is still very time consuming (especially if you haven't spent months writing it), high level time documentation is a must to tie things together, and that simply there's usually too much code to read that could be succinctly summed up. They forget that not everyone has their experience and familiarity with the codebase on a whole. They don't realize knowledge they take for granted about the code and the patterns they use and the naming scheme they follow.
> So in short, they're never really considering what it's like to be exposed to their code from the perspective of an outsider. Thus, they skip "obvious" documentation and make bad assumptions about what you know.

- Some developers might think "It's obvious what this code does. Why does it need documentation?" simply because they aren't looing at this with 'never seen it before' eyes.

### Comment

> Assuming you're referring to user documentation, the reason why developers often care little about it usually comes down to a few things:
> - often, nobody else in the company cares much about user documentation either.
> - the developers often work at a different granularity / along different structural lines than that of the user documentation. For example, four different developer tasks might, when all are completed, amount to a change in a single paragraph in the user documentation and so none of the four developers involved feel ownership for the documentation change. Similarly, a single developer task might mirror having to make changes in several different places in the user documentation, sometimes in places that are not obviously linked to the part of the code that was changed.
> - the developers often do not receive any feedback on user documentation. Either because none is given (good documentation is invisible, bad documentation is ignored) or because the feedback goes to other parts of the organisation and doesn't flow back to the developers.
> - incentive structures and project pressures tend to narrow the developers' focus to a) functional requirements and b) successful (technical) software deployments. User documentation falls outside of this narrowed focus.

- Users don't read user documentation. More often, they will just ask the support team and/or pay a consulting agency to tell them the answer instead.
- Some code might require consulting 4 different developers to make an accurate chaneg
- Businesses do not give programmers an incentive to write documentation

### Comment

> Because ultimately you're asking me to write a bunch of code which takes hours to get right... and then do it all again in English with no compiler. Fuck that.

- There's no "compiler error" (or other forms of compiler support that push the programmer towards doing things the 'right way') for writing documentation

> ... Ultimately I care so little because my company cares so little. If they actually cared they'd put real resources towards solving the problem.

- (Duplicate) Businesses do not give programmers an incentive to write documentation

### Comment

> I work for a big company (1200+ people) writing internal tools, this is my perspective:
> - Most end users don't read the documentation, no matter how often it's pointed out. It's a nightmare. We're trying various methods of getting people to read the info they need to read.
> - I have a mountain of work (my team is very understaffed atm), so I usually don't bother with superfluous documentation.
> - I do write internal documentation for other people on my team, mostly HOWTO's on how to get setup, or the broad strokes of how a system works
> - I tend to stay away from dev documentation that is too in depth, better to keep it brief and "vague" then go too in depth. Code is always moving, meaning any documentation is out of date the moment it was put online. Like previous point, broad strokes and reasoning/intent then pointing out exactly how it fits together. I've got some legacy systems we inherited from people that have left, that have odd quirks and no one knows why it is the way it is. Always difficult to say at that point if it was intentional, a mistake or a quick workaround/hack.

- Documentation that explains things broadly and is less tied down to a specific version of some code tends to remain up-to-date longest.

> Depending on the audience, actual code samples in a common place can be more useful then some blurbs on an (internal) website. Seeing as they will have to be fixed if the code drastically changes.

- Examples of code are easier to maintain and are often better than some blog posts on the same matter.

> ... tl;dr: It's weighed for usefulness on my part. No point writing documentation only a small set of people will read, better to guide them through it in that case.

### Comment

> And the missing, and most important docs: examples / samples (kind of under howtos, but not quite)

- (duplicate) working code examples are sometime better than actual written content.

> And the problem with tutorials/howtos is that you have to pick the right starting points.
> Noobs? Really hardProgrammer but doesn't have deep knowledge in your product? Hard and the typical caseSomeone with familiarity with a competing/similar product? Easier but often lots of products.

- The number of possible audiences complicates up-to-date documentation significantly.

### Comment

> I cannot stress how important code/API examples are. I hate having to read though someone else's code in order to figure out how to use it.

- Providing working examples of code that show how to properly use some subset of an API is better than making someone read through that API and figure out how to piece them together. (In some cases, this is not necessarliy true for PS because the type signatures are designed so that two functions together)

### Comment

> Or the aimless guessing. Sometimes I have to actually write the code first because I can't figure out from the docs what the output or side effects really look like. Sometimes I see examples that show how to use the thing, but don't at all make it clear what the result looks like.

- True learning sometimes requires the person to actually figure things out for themselves.

### Comment

> Code examples are required no matter which kind of documentation you're writing. They given context to the words being spoken. You can't make a "working" tutorial without them. A how-to guide that doesn't give you some solution in code is going to be useless. An explanation without a code sample to ponder over would be too abstract to think clearly about. Reference material that doesn't have examples is often too obtuse to actually understand.

- While one can have code examples without written documentation, one cannot have written documentation without code examples.

### Comment

> Documentation is utterly broken. It is so broken, it is not funny any more and is costing society billions. A few of the problems:
> - A change in a UI element breaks the doc
> - A change in functionality breaks the doc
> - A change in named symbols (classes, functions, etc) breaks the doc
> - A change in the code structure breaks the doc (e.g. removing a base class)
> - A change in the theme may break many UI elements
> - A change in text resources breaks the doc
> - A change in spec breaks the doc

> Honestly, I could go on for a very long time making a list with a ton of small stuff that breaks documentation. It's time to get a documentation IDE bound to the codebase which breaks the fucking build when a doc item breaks.

- (duplicate) Making the build fail unless documentation is added could help documentation purposes
- There is a huge list of things that can make documentation go out of date. Perhaps this is the real issue behind why no one wants to write documentation. Thus, it's worth asking which medium of documentation is easier to 'update' once these changes or which is less vulnerable to such changes.

### Comment

> The best documentation is when you type your question into google and receive the exact answer with a code sample (on stackoverflow). This is all I ever wanted, and it can't get any better. If the first google result is not a SO link it always makes me unhappy.

- SO is its own form of documentation
- Many questions asked in the FP Slack channel could be better asked on SO with the one asking the question notifying people on the FP Slack channel. This would make such 'documentation' persist longer than the Slack logs.

> If you don't have a specific question in mind then reading some documentation/tutorials is probably what you want (which doesn't happen often).

- Being able to ask a good question presupposes an understanding of the domain / library / language.

### Comment

> This is all good and well but the one most important thing about documentation from my experience that is never mentioned and concerns you directly as a coder: writing documentation forces you to write better code because when you write documentation you find inconsistencies in your design and code.`This applies both to end-user docs and developer docs.

- Documentation is really a way of thinking about design, but often done after the code has already been written according to some other design.
