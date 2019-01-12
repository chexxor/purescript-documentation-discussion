# Sources and Interpretation

## Defining Our Terms

**Definition**:
A "source" is any source of data that makes a truth claim (it claims that something is true. Whether that statement is actually true needs to be explored).

The goal of this step is to do the necessary work to make it easier to do the next step: defining the context/narrative.

Sources can be broken into two types: primary sources and secondary sources. Primary sources are stand-alone sources whereas secondary sources are interpretations, summaries, analyzations of primary sources.

**Examples of Primary Sources:**
- An original paper that introduces some idea for the first time
- A blog post
- A tweet
- A talk
- A conversation in a forum, chatroom, etc. where one person speaks their own opinion, makes their own logical argument, etc. These statements are not interpretations of some external data.

**Examples of Seconary Sources:**
- A blog post that summarizes another blog post
- A conversation where one person uses phrases like "I remember X being true," "I think X is true," and/or "I heard someone say X is true." and these phrases are used to mean "I interpreted information in such a way that I reached some conclusion and I am stating that conclusion, not necessarily the process by which I reached that conclusion, so that you can 'check my work of logical deduction.'"

**Gathering Sources**:
One first gathers sources without bias as to who said what or where it comes from and categorizes them according to primary/secondary source distinctions. At this stage, no assessment of the sources or interpreting what they say is done.

**Interpretation**:
After gathering as many sources as is reasonable in the allotted time period, one begins to assess a source and give it weight. Some sources bear more "weight" than others (primary bear more weight than secondary). Some are more subjective (biased, unbalanced in assessment, misinformed, etc.) while others are more objective (real evidence/arguments that must be addressed with real answers). Once assessed, one interprets the main themes/ideas that one hears the source communicating.

<hr>

The rest of this document should be a list of sources where each source has
- a link to the original post/comment
- a quote of the relevant parts of that post/comment and an interpretation that highlights the main ideas of the relevant parts

Since maintaining the primary/secondary source distinctions can be hard to do when analyzing/interpreting blog posts, forum comments, etc., they will not be categorized as such here.

## Source: 'The State of Things'

https://discourse.purescript.org/t/the-state-of-things/282

### Opening Comment

[Actual comment](https://discourse.purescript.org/t/the-state-of-things/282)

- This was written by the language creator, so it bears significant weight
- The language creator admits to stopping his language contributions and oversight due to burning out, so these statements should be interpreted in light of that. He might be more negative in his assessment than an other contributor because of that burnout.

> We seem to have developed something of a documentation problem. Even now, the documentation repository is only partially updated for the 0.12 release, and generally it is quite unstructured and lacks a single vision for what good documentation should look like.

- There is a public awareness that the documentation repo is not fully up-to-date with the PureScript language
- The documentation repo is presented as a loose collection of potentially unrelated articles, not as a systematic presentation of articles that all fit within a larger vision.

> Also regarding documentation, I still need to update the book.

- The PureScript by Example book is not fully up-to-date with the PureScript language.

> It seems to take longer with each major compiler update, and honestly, I’m not motivated to update it again without some sort of guarantee that I won’t have to redo everything again in a few months.... I would like to write a lot more documentation for PureScript, but I hate the idea that it will become out of date quickly, and that I will have yet more projects to update in future.

- Keeping documentation up-to-date via the medium of a book costs a lot of time. Breaking changes quickly destroys much of this work.
- The workload is too great for one person to do alone without burning out.

> So without some sort of plan for the future of the language, and some idea of what changes are coming (and just as importantly, which aren’t), I’m not likely to write anything, and I wouldn’t be surprised if others avoided writing for the same reason.

- There is a lack of communication between the language developers/contributors and those who document the language about what changes will be included/excluded in the next release. This makes it harder for the documenter to know what to write, what to correct/change/fix, and what to continue ignoring.

> I think we (i.e. 'we' will mean "the community generally" hereafter) need to come to the difficult realization that everyone is already stretched thin, and that we need to try to do less in order to do things well.
> - If Try PureScript takes too much time to update, then we should not advertise it on the website.
> - If the documentation cannot be updated in sync with the compiler, then it should also be unlinked from the website, and marked as stale.

- There is public acknowledgement that there are not enough workers to keep the documentation resources in-sync with latest language releases. As a result, much time is spent putting out fires rather than moving the language/ecosystem forward.
- Outdated materials/websites are currently included in the main PureScript language's website. These should be removed to prevent new learners from thinking that these resources are in-sync with the latest PureScript language.

> I have said before that I think we should avoid new features and concentrate on bug fixes and documentation. Now that 0.12 is out, I think it is a great time to prune any inessential feature requests from the issue tracker and make a plan to concentrate on these things instead.

- There is "issue spam" in the language repo's issue tracker, making it harder to see what really needs to be done / should be done to get a `v1.0` release.

> There needs to be a plan for the future, and that plan needs to be documented. I would like to start working on a specification for the language, something which I consider essential for documentation purposes, but it doesn’t make sense to start documenting a language when there is no plan in place for the next milestone.

- There does not seem to be a well-defined mutually-held 'vision' for the future of the language's development. As a result, it's hard to start writing documentation material that will coincide with the `v1.0` release of the language.

> For me, the ideal situation would be this: we agree that the compiler is not perfect as it exists now, but that its flaws are relatively minor and easily documented; we make a plan to release 1.0 (or 13.0?) by fixing any bugs we cannot document, and engineering things as best as possible in order to facilitate feature additions we anticipate; then we write a specification for this language, and commit to a stable release window, ideally as long as possible. When I’ve brought this idea up in the past, it’s met some opposition, but I think this would be massively beneficial and enable the creation of lots of stable documentation.

- A proposal for how to make a `v1.0` release resistant to future breaking changes
- This idea has been mentioned before but has been met with resistance. We don't know what that 'resistance' is as there are there are no external links or other evidence as to what that is.

### Comment (language user)

https://discourse.purescript.org/t/the-state-of-things/282/2

> I prefer Discourse for things that don’t warrant a GitHub issue. I find that Slack can sometimes be good for getting an immediate response and for transient things.

- GitHub issues should not be used for "help me" questions.
- Slack is **sometimes** good for getting immediate response and transient things
- Discourse is **preferred** for seemingly longer discussions that aren't quite worthy of a GitHub issue

### Comment (language user)

https://discourse.purescript.org/t/the-state-of-things/282/3

- This was written by a user of the language and suggests ideas for improving documentation.

Relevant parts and their interpretation appear below:

> Maybe a solution to getting better documentation would be to have some live on the main compiler repo as issues with the `new contributor` label and if others find they need more docs in popular libraries to open an issue with similar label on library repo and have a section on here with all of these accumulated. They wouldn’t strictly have to be just docs anything beginner friendly. But writing Docs is a good way to get into a language.

- Perhaps providing a single centralized location for all cross-repo documentation issues that are easy enough for new beginners to do would help. To aid in recognition, they could all use the same label name: `new contributor`.
- Encouraging new users to open issues for documentation issues would help track down what already-written documentation is not immediately understandable to new users and what entities have yet to be documented.
- Writing new docs or improving old ones is a good way to get started with a language.

### Comment (language user)

https://discourse.purescript.org/t/the-state-of-things/282/4

Source admits to being a 'pure user' of language.

> As a pure user of the language I’m also quite frustrated with rapid backwards incompatible changes to the language and standard “library”. It hinders my ability to introduce it more widely into production because once the compiler changes it’s me who is solely responsible to “make it work again, forchristsakes!”. I think the time has come to have a definition of “version 1.0” and work towards it.

- There is a lack of communication about the release schedule of the language and 'saving' all breaking changes for a single major release.
- Since PureScript is still a newer language, some people that use it in production rely upon only one expert to fix problems that most others do not know how to fix.

> If you take volunteers I can maintain Pursuit. I’m infrastructure engineer/manager by day. It will take me some time to figure my way around “server side Haskell” but I’ve seen harder things in my life. Let me know if I can help.

- One has offered to maintain Pursuit, but might need some (but likely not a lot) help getting oriented to the project

> As for the communication channels, the Slack is great for asking a stupid question if you got stuck in the middle of something simple. The lack of logging sucks big time and I remember myself reading IRC logs for hours with great results.

- Slack is the "go to" for stupid questions
- Any conversations made on Slack that are worth keeping long-term (e.g. answers to stupid questions) do not persist long-term. This seems to contribute to new users asking the same questions again and again, taking time away from advanced users in the language from spending time on other more useful things.

### Comment (core contributor)

https://discourse.purescript.org/t/the-state-of-things/282/5

From garyb, a core contributor of the language.

> I guess regarding Try Purescript / Pursuit there need to be more of us who are aware of how to update it / how they work, as I think it’s just you and Harry at the moment.

- Public acknowledgement that some people (not defined here) do not know how to update Try Purescript and Pursuit
- (Secondary source) - Phil and Harry might be the only ones who know how to update it.

> I think that [(i.e. we have a documentation problem)] started with the initial release and has been true ever since. I can’t think of a time in PS’s history where we had docs resources that were good and up to date (book aside). I agree it’s a problem, I just don’t think characterising it as something new or that has gotten worse is true - perhaps it’s just become more apparent now you’re primarily a user?

- PS documentation has always been bad
- This problem has been the same throughout its history in that it hasn't gotten worse over time

> I looked back at the releases as to how long the gap between them was and how breaking they were, for as long as I’ve been involved with the project.... So I’m not sure the perception that we’re breaking things constantly is entirely true, especially with the last release since it was by far the longest period of non-breaking.

The number of weeks until next breaking change, starting at `v0.5.0` and going to `v0.12.0`:
`10 28 34 31 17 18 25 60`
The average of the above number series:
`27.875 weeks`

- Some users perceive that PS has a frequent breaking-changes language release cycle. This perception was true at various parts in the release, but hasn't been recently.

> Also, the breaking changes that weren’t library related in 0.12 were relatively minor compared with changing => in 0.11, etc.

- A breaking change in the language sometimes greatly impacts the ecosystem and other times only minorly impacts it.

> Just pointing out PS is definitely slowing down into a more stable state anyway. Especially after 0.12, the Effect changes and some of the other library changes that went out, there’s very little that I can think of that I’d like to do differently in the core libraries now. In fact there are only two changes I can think of, one would require polykinds and the other would require quantified constraints, so they’re probably not going to be any time soon.

- Core contributor is expressing belief that breaking changes in core libraries are not likely to happen in the future as frequently and that language is finally stablizing.
- Two potential breaking changes may come at a later unknown time.

> I think having the Discourse is valuable for sure, as hopefully we can encourage non-transient discussions that aren’t issue specific to move here instead.
> There’s also the Google Group, but I can’t remember the last time I looked at that.
> I use Slack as even though there’s no persistent logging it has enough of a backlog that I can actually catch up with the last day or so, which is about all I ever did with IRCBrowse too. That and you can reply to people who are offline.
> I don’t use Gitter at all or the IRC channel anymore.

- This list seems to include all of the PureScript groups out there and how frequently people use them and why.
- Slack is useful for short conversations that work across timezones and internet connectivity issues.
- Slack acts as a newsfeed of sorts for PureScript

> Perhaps we should cull the list to just point people to Discourse and GH issues for “real” discussions, Slack (and maybe IRC) for quick questions / transient discussions, and leave it at that.

- A suggestion for reducing the number of communication groups down to 3 and defining general "policies" for what should go where

> I’m less hostile to this idea (i.e. creating a specification for the language, focusing on bug fixing and stopping new features) than I once was, but mainly because I think the “missing” features that I feel are the greatest causes of friction for me can be added without breaking old code. I guess it depends by what we mean by committing to a long term stable release, if we’re talking about not grossly breaking things, I’d say we’re at a point where that’d be no impediment at all, but if we’re talking about an entire feature freeze then I’m still reluctant.

- The 'resistance' mentioned before was based in not wanting to produce breaking changes in later releases.
- The 'resistance' stil exists in a small manner in that `garyb` does not want a complete "feature freeze." However, it's no longer about stopping a `v1.0` as much as it is a "how do we make `v1.0` that does not require us to introduce breaking changes soon after its release?"

### Reply (core contributor)

https://discourse.purescript.org/t/the-state-of-things/282/6

> I think the language is at a good point where we could focus a lot more on documentation if we decided to commit to a stable language specification.

- It would be best to hold off on documentation until a stable language specification is defined. Otherwise, the same problems encountered above (quickly outdated learning resources that cost a lot of time to make) will occur again.

### Comment (language user)

https://discourse.purescript.org/t/the-state-of-things/282/7

> Errors: a number of these are undocumented in the docs repo. Unfortunately, I can’t figure these out unless I get really lucky and write code that fails to compile. If one of the core contributors worked on the errors part, the documentation would be largely up-to-date.

- The documentation repo's error pages are not up-to-date or completely filled out

### Comment (language user)

https://discourse.purescript.org/t/the-state-of-things/282/8?u=chexxor

> I had the misfortune of making a free PS course that uses TryPureScript a couple of months before 0.12 was due and some of it’s changes, I think, broke a couple of my lessons due to the way I taught them. Need to check it out properly just not had the motivation! I like it as a tool but can totally understand the hassle of keeping it and attached material up to date.

- Using Try Purescript as 'learning environment with PureScript already installed' became an unreliable environment due to a breaking change.

## Source: 'Features you want future PureScript to *not* have?'

https://discourse.purescript.org/t/features-you-want-future-purescript-to-not-have/115

### Comment (language user)

> Soul mate! There’s a ton of low-hanging fruit in even core documentation. I hope after 0.12 that pull requests like this one 53 for Data.Map get approved.
>
> https://discourse.purescript.org/t/features-you-want-future-purescript-to-not-have/115/5

- There are lots of easy documentation problems to resolve in the core documentation.

## Source: 'How do we prevent incoherence in the Ecosystem?'

https://discourse.purescript.org/t/how-do-we-avoid-ecosystem-incoherence-in-the-future/209/

### Opening Thread

> Despite the hard work of many contributors and maintainers, there has been a lot of confusion surrounding the release of 0.12. My understanding is that this has happened in the past and is a phenomenon by and large accepted by the existing PureScript community.

- New language releases that include breaking changes often lead to confusion. The "confusion" is not defined in this section, so that we can know what causes it and how to fix it.
- This "confusion" is largely accepted as "normal" by the community. In other words, "it just comes with the language."

> As a current user who follows changes in the ecosystem closely it didn’t cause me many problems, but anyone new to PS right now is feeling a lot of pain and (I believe) more likely than not to decide PureScript isn’t an investment worth making. The pain is diminishing daily as tools and libraries are updated which is great! The good news is that a major update like this creates greater than normal buzz. The bad news is that buzz draws newcomers at potentially the worst possible time.

- New language releases are news-worthy and often draw in a lot of traffic. Perhaps people who want to use the language but have been turned off before now think, "Great! Maybe I can actually understand how to use it this time!" Others who have never heard of it might think, "What is this? It seems worth checking out." However, when either audience checks the site, they are immediately turned off. The overall effect is a net-negative for PureScript as a whole.

> I understand that several factors contributed to the situation, among them:
> - No central coordination

- I'm not sure what coordination this would entail. Perhaps a unified vision of what the community is trying to accomplish?

> - No full-time effort (though `garyb` and `kritzcreek` came closer than could be expected). Nobody’s getting paid to do this work.

- Only volunteers who must pay their bills through other means are working on this language. There is no financial incentive for them to complete work, nor can they give the language their full time.

> - Documentation was not updated to warn users about the problems they would encounter during this time of flux.

- Pre-release documentation that was marketed/announced a reasonable time before the release and easily findable after it did not occur.

> - Tooling (specifically Pulp) was not updated in conjunction with the release of 0.12.0.

- Self-explanatory: one cannot benefit from a new release if the tooling support doesn't make it work well.
- A language should provide a "complete solution" to business problems, including build tools that 'just work.'

> - Although core and contrib libs were updated during this time, some key pieces were missing, most notably Aff and Halogen (despite the best efforts of natefaubion).

- Major libraries in the ecosystem were not updated at the same time as the language release. So, one could not immediately benefit from the new release.

> - The Slack channels and this Discourse instance are great resources, but I could only find one reference to Slack (at https://github.com/purescript/purescript#help

- The Slack channel and Discourse site are not easily findable.

> - It would be helpful to have this information duplicated at purescript.org

- The Slack/Discourse links should be included in the PureScript language website.
-

> - I think the link to Gitter should also be removed as it’s not very active and that can be discouraging.

- The Gitter chatroom is not very active. If it gets removed completely, one should announce that in the channel and include links to the new chatrooms to use and why.

> I want to reiterate that no blame is being assigned and there’s no need for recrimination. I think we all want make this ecosystem a joy to work in for experienced users and newcomers alike.

- An indicator of a healthy community that is focusing on problem-solving, not the blame-game.

### Comment (core contributor)

https://discourse.purescript.org/t/how-do-we-avoid-ecosystem-incoherence-in-the-future/209/2

> I think another point to consider is how we can better communicate (or somehow enforce) compiler<->library versioning.

- An unanswered question: how can the community communicate/enforce compiler-library versioning. I believe that concept means "this version of the library works on this version of the compiler."

> Absolutely, it (i.e. not announcing the next language release without first updating the ecosystem) is why I haven’t mentioned or retweeted anything about 0.12 on my twitter yet!

- Some people get this idea whereas others do not. This should be communicated as something to expect for new learners
- An official "ecosystem is `<release version>`-ready" announcement might help prevent this. Likewise, Including a "this release is made but not ecosystem-ready yet" note in the languages' release notes that includes a link as to what "ecosystem-ready releases" mean might help prevent this negative press.

### Comment (core contributor)

https://discourse.purescript.org/t/how-do-we-avoid-ecosystem-incoherence-in-the-future/209/3

> The kind of issues we’re encountering here are also why I’m reluctant to make a 1.0 release in the near future, because we still do have a lot of ecosystem stuff to solve - I don’t believe for a second most people (esp. newcomers) will see a distinction between the PureScript language/compiler 1.0 and the “PureScript product” as a whole. But that’s probably another discussion.

- garyb's resitance to making a `v1.0` release are better explained: a `v1.0` PureScript langauge is not the same as a `v1.0` Purescript Ecosystem / Complete Solution to most business problems. Most people who hear that there is a `v1.0` PureScript release will think it also includes the latter when it only includes the former. This might result in a net-negative press for the language.

### Comment

https://discourse.purescript.org/t/how-do-we-avoid-ecosystem-incoherence-in-the-future/209/4

>> From `paf31` on the Slack Channel: "For the other major release, we used to have a checklist of all of the stuff that came with the compiler"
>
> Where would be a good place to keep a more comprehensive checklist? The compiler repo doesn’t seem appropriate as we want to cover docs, libs, and third-party tooling as well.

- There is not a place that stores an up-to-date process/checklist of things to do for making a language release.
- The documentation repo is likely a bad place to store that checklist/process.

### Comment

https://discourse.purescript.org/t/how-do-we-avoid-ecosystem-incoherence-in-the-future/209/5

> It is unrealistic to expect that we wait for everything to update before we release a compiler version. If we did that we’d probably never get a release. For example, many newcomers are using the PureScript book, but we obviously can’t wait for Phil to update everything in the book before a release.... We absolutely need to be able to do a release, and let the ecosystem gradually catch up, because we just don’t have the community resources do it all at once.

- Purescript, being developed purely by volunteers, does not currently have an efficient toolchain and/or enough manpower to reliably update everything in the ecosystem before making a release.

> The book is currently problematic in how it recommends users get started and start installing libraries, which results in incompatibilities.
> The number one issue is that there is not any easy or reliable way to deal with compiler compatibility as long as we are recommending Bower in our introductory materials....

- Part of the up-to-date documentation issue is due to using Bower as a dependency manager because it can result in incompatibilities between dependencies.

> Right now, the only viable option is psc-package. If all our introductory resources specified exact compiler versions (Just recommending npm install purescript is extremely problematic) along with an appropriate package set, we would not be having these problems.

- Using psc-package as the dependency manager for introductory learning materials would solve the library-compatibility issues one faces with Bower.

> The only problem with psc-package is that it is currently lacking features/tooling that make it convenient to use as a general purpose dependency manager. I know Christoph is experimenting with ways to make it more extensible via Dhall. I know for sure we will adopt it at Awake if that happens.

- However, psc-package does not provide a complete solution to the problems which Bower does. While psc-package might be good for introductory learning materials, it is not as good for production code as Bower. Thus, many major libraries (e.g. Aff, Halogen) use Bower. New learners likely look at these libraries written or supported by "successful companies using PS in production" and see that they use Bower, not psc-package. Thus, they think they should do likewise.
- Once a `psc-package`-based approach becomes more mature, one major company will switch to it and do so eagerly.

### Comment

https://discourse.purescript.org/t/how-do-we-avoid-ecosystem-incoherence-in-the-future/209/6

> I think we can add a line like “things are in flux, expect things not to work” to the docs repo at least.

- A temporary solution to the documentation problem, but one that likely does not do a good job of communicating 'why' that is the case and when it is likely to be fixed.

### Comment

https://discourse.purescript.org/t/how-do-we-avoid-ecosystem-incoherence-in-the-future/209/7

> Yes, we should absolutely update docs and install instructions as a minimum. Anything that recommends a blanket install without pointing out the available versions will result in problems.

- One needs to know which version of a dependency to install, so that it does not result in problems. However, this seems specific to Bower, not psc-package. If the community moves away from using Bower, this solution is irrelevant.

### Comment

https://discourse.purescript.org/t/how-do-we-avoid-ecosystem-incoherence-in-the-future/209/8

> I was wondering whether it might be possible to have a purescript release badge that we could stick in library READMEs so at least you’d know in advance with Pursuit whether the library was compatible.

- An idea that might only be relevant if one is using Bower as a dependency manager: a library badge in the Git repo indicating which version of the language with which the library is compatible.

### Comment

https://discourse.purescript.org/t/how-do-we-avoid-ecosystem-incoherence-in-the-future/209/9

> The compiler version change was not the only change in the ecosystem around that time.
> - `purescript-dom` and `purescript-dom-classy` seem to have been superceded by a collection of `purescript-web*` libraries like `web-html`, `web-dom`, `web-events`, and `web-uievents`.
> - `purescript-dom` and `purescript-dom-classy` were moved to the `purescript-deprecated/organization` with readmes noting they are deprecated, but those changes never made it to Pursuit.
> - [This originally appeared after the above list, but including it here due to context] The `purescript-foreign` library had several updates and changed namespaces. `AVar` was removed from `purescript-aff` and moved to its own package.
> So if I just update versions in Bower and install, I’ll get all sorts of version conflicts to resolve, and if I look at Pursuit, I have no indication as to why – as far as I could tell at first I just needed to wait for them to be updated. It wasn’t until I asked in Slack and `natefaubion` and `garyb` chimed in that I realized about the re-organization.
> .... I like all of these changes, but I wish there were some sort of notice summarizing the changes (to these and to the dom* libraries). For example, the Aff release notes for 5.0.0 simply say “Update for version 0.12 of the PureScript compiler.” I had to track down the new location of `AVar` on my own.
> Once I was aware of all these changes that happened at the same time as the compiler bump I could quite easily update the project, but without having access to Slack and the ability to bug y’all I would have wasted a ton of time trying to figure out what had changed and where to look for new information.

- Library changes were not announced in a very public manner, including what is being deprecated and what their new library names are. Bower + Pursuit did more to worsen the situation than help.
- The Slack channel provided the most up-to-date "I need help now" info

> I understand these are libraries, not the compiler, but if you’re building anything for the web with PureScript you’re inevitably going to reach for these fundamental libraries. It seems worth the effort to provide an official notice of core library changes that accompany a new compiler version.

- It would help if language releases coincided with core library releases and included some form of public announcement about the changes.
- Although the idea of a "core library" is mentioned, criteria for what that is a core library and a complete list of them is not included here. (While the 'web' libraries make sense to be called 'core', it would help to clarify why, so that similar ones are included, too.)

> I would love to help – I’m not shy about writing documentation or putting time into these updates – but without being a core contributor I have no idea what these plans even are.

- One person is willing to write documentation and contribute. Unfortunately, there is not a larger vision as to what should be done and how this person should direct their documentation efforts.
- It's difficult to improve the core library experience without help from the creators or maintainers of it.

> As a consumer I largely find myself digging around readmes and docs that may or may not have been updated trying to guess at what ecosystem shifts have just happened. This is a little disconcerting as a heavily-invested commercial user of PureScript.

- A newsfeed of some sort that summarizes the changes in the ecosystem would help one know what has gone on recently.
- Even a heavily-invested user of PS must navigate through readmes and docs to understand something. How much more a new learner?

### Comment

https://discourse.purescript.org/t/how-do-we-avoid-ecosystem-incoherence-in-the-future/209/10
https://discourse.purescript.org/t/how-do-we-avoid-ecosystem-incoherence-in-the-future/209/11
https://discourse.purescript.org/t/how-do-we-avoid-ecosystem-incoherence-in-the-future/209/13

> I would find it useful to be able to use Pursuit in a way that allows me to select a version of the compiler and then only see results compatible with that version. Obviously that involves other things and requires packages to declare that as well.

- Adding a filter to Pursuit Search that shows only libraries that are compatible with a specific PureScript language version would help. Unfortunately, this requires library maintainers to somehow indicate what that version is.

> I think making it more obvious which version of things are running on `try.purescript.org` might be helpful to newcomers too.

- Assuming we keep the 'Try Purescript' website, it would help new learners to know which version of PureScript is running on that site. This can notify them whether the version is outdated/old or is the latest version.

>> I was wondering whether it might be possible to have a purescript release badge that we could stick in library READMEs so at least you’d know in advance with Pursuit whether the library was compatible.
>
> Something like this is easy to create on `shields.io`

- Purescript-language-version-library-compatibility badges are easy to make via shields.io

### Comment

https://discourse.purescript.org/t/how-do-we-avoid-ecosystem-incoherence-in-the-future/209/14

> When the release candidate of the compiler came out, several core libraries opened compiler/0.12 branches, and by the time the official release occurred the majority of core libraries were already ready to go (like purescript-web*, purescript-ordered-collections, purescript-prelude, etc.).

- An `upcoming-ps-release` branch in some libraries helped insure they were compatible with the next language version almost as soon as it was released. This approach seems to have been a successful approach.

> However, unless I missed something major, there wasn’t much of a push to notify the rest of library authors about the release candidate, nor did the release candidate last very long.

- While this approach was successful, others did not follow it, perhaps because they were not aware of that approach or the release candidate window was too short.

> This seems unavoidable: we can’t force anyone to update, and if they aren’t tuned in on Slack or Discourse or Reddit then they’ll simply miss the new release, and won’t update until someone opens an issue or a pull request on their repository.
> However, perhaps we could do something more. We could at least make a good faith effort to notify people who maintain repositories available on Pursuit if their code is going to break in the new release.

- If a person starts and maintains a new library, they need to be notified of breaking changes in an upcoming language release. Ideally, this would be done via them subscribing to some notificatno system, or learning of it via a public announcement or someone opening up an issue for it in their repo. Of these approaches, the last one is best if it can be automated.

> Perhaps we could do something like this. [Due to its length, I have not included the approach's exact content here but only a summary].
> - [The basic idea was to have a tool that helps people determine which libraries will break in next release and then have people manually open issues in library repos to which core conbtributors do not have access, so that library authors are notified of the upcoming change without taking as much time away from core contributors.]

- A solution to notifying library users of upcoming language changes will likely require an automated tool that integrates with Pursuit and GitHub, and a team of volunteers that handle any of the un-automated work.
- There can be better communication between maintainers of the language and maintainers of heavily-used libraries around major releases.
- Release changes can be summarized and explained in a blog post, and include a migration guide.

> Finally, there could be a “documentation team” which I also volunteer for
> - For core libraries, we might need to update documentation when things have changed
> - If there is an accompanying ecosystem change, like the purescript-web* and purescript-avar changes, then there ought to be an accompanying official blog post that summarizes the changes, why, and where to find the new packages
> - I think the team did a great job moving libraries to purescript-deprecated and updating READMEs. It’s unfortunate these did not get pushed to Pursuit and that still ought to be fixed. It’s the right idea.
> - There should also be a ‘migration guide’ that details a) What processes are being done to upgrade everything; and b) some tips as a library author for migrating.

- A documentation team consisting of volunteers can help communicate release changes to language users and library maintainers. A documentation team's responsibilities could include:
    - writing documentatin for core libraries
    - summarizing major changes in a blog post, why the changes were made, where new libraries (if any) can be found, and a "migration" guide
    - potentially pushing library documentation to Pursuit

> I think we can learn from this compiler update and put together processes to be better next time.

- The entire process the ecosystem must go through from language release to ecosystem compatibility is not the most efficient it can be, nor is it widely understood by non-core-contributors.

> I believe it’s crucial that new users are able to come to PureScript within 30 days of a compiler release and have things working, and equally that commercial users are able to feel comfortable that new releases will resolve themselves reasonably quickly.

- A potential 'success' indicator for determining whether a language release went smoothly/efficiently is a 30-day guarantee that the ecosystem is compatible with the latest language release (potentially excluding larger documentation efforts like the PureScript by Example book).

> PureScript is a relatively new and niche language, and anyone using it should expect breaking changes and to have to figure things out from time to time.
> But these challenges don’t seem too formidable, and that gives me confidence we can resolve them and provide a better experience for new and existing users during a transition.

- A user expressing confidence that the community is able to solve its problems; it just currently lacks coordination of some sort.
- PureScript is not yet 'stable' to such a degree that migration guides and troubleshooting their issues is always well documented. This should be new learners expectations from the start.

### Comment

https://discourse.purescript.org/t/how-do-we-avoid-ecosystem-incoherence-in-the-future/209/15
https://discourse.purescript.org/t/how-do-we-avoid-ecosystem-incoherence-in-the-future/209/16

> Definitely a lot of good stuff to work on listed already (and it’s a little late for 0.12) but I just wanted to point out that releasing a new compiler version doesn’t need to mean it’s becomes the default.

- Documentation and tooling should not choose the latest language and library versions by default. Instead, it should be explicit about the language version being used and be conservative with upgrades.

> For example, most docs and beginner tutorials say to install Pulp and pulp init. If Pulp defaulted to psc-package, used purescript@latest from npm, and then found a package set for that compiler version the new user experience would be so much smoother. And we’re nearly there… just need to make sure the new npm packages published aren’t tagged as latest until a pulp init on that version just works (i.e. 0.11 and 0.12 can both exist on npm with latest still resolving to 0.11).

- `pulp init` or a new `pulp` command could be configured to set up a learning environment for new learners that "just works."

> Psc-package isn’t perfect yet, but at least it defers having to learn which libraries are compatible with which compiler until the user has an edge-case need or is writing their own libraries.

- Shortest explanation for why psc-package would likely be preferred over Bower as a dependency manager for new learners.

> It might be good to have compiler version flags as well for tutorials and books to use, like pulp init [optional compiler version].

- An idea that's useful for a quick 'getting started' approach to learning PureScript. However, this approach would only work if it is used as part of some larger vision of documentation.

> Maybe the Pulp project should even be the gatekeeper for releases to npm specifically.

- The question of how releases integrate with the process of making a release to NPM needs to be further explored. There might be additional things that could be optimized here.

## Source: "Purescript First Impressions"

https://reddit.com/r/purescript/comments/8qaiwl/purescript_first_impressions/

### Reddit post (new language user)

> pursuit is also great once you figure out how it works (some more top-level "what is this thing?" documentation would be good).

- New users like to use Pursuit to learn how to solve problems when writing the language.

> Probably the worst part of my PureScript experience was the FFI. This is an area where the language needs to be more generous with special syntax and compiler features -- it's crazy how much boilerplate I need to produce to write types for extremely common JavaScript patterns compared to other languages

- The FFI maybe needs better documentation, especially for a newcomer to statically-typed language.

> Take calling a method on a class for example: you need to make a Javascript file which wraps your existing method by doing exports.myMethodImpl = function(...), that function probably needs to return another function if it's an Effect, then you need to foreign import the function and wrap the arguments in a Fn3, and then you need to make another function that calls the first function and invokes runFn3 on it.

- The FFI documentation should explain the advantages of writing an out-of-PureScript implementation.

## Source: "My experience with Purescript so far"

https://sadraskol.com/posts/my-experience-with-purescript-so-far

### Blog post (new language user)

> Purescript leaves you alone in the jungle of its methods and functional gibberish. If you don’t know what a Monoid, a Foldable or a <$> is, you better learn the language with tutorial first! It feels like the language wasn’t build for programmers first, but for Haskell programmers with strong theorical background. Could you easily guess what’s the difference between a Semi-groupoid and a Monoid?

- Newcomers to the language feel antagonized by the unfamiliar concepts and language operators.
- Perhaps documentation can mitigate the confusion and anguish experienced by newcomers.

## Source: "Learn Purescript or Haskell first?"

https://www.reddit.com/r/haskell/comments/5quf5y/learn_purescript_or_haskell_first/

### Comment (language user)

> Haskell will have a lot more material (than PureScript) and a much stronger ecosystem so I'd go with that for now.
>
> https://www.reddit.com/r/haskell/comments/5quf5y/learn_purescript_or_haskell_first/dd2i8pq/

- Haskell has more documentation (but better?) than PureScript, so Haskell is recommended for newcomers.

## Source: "Lessons learned porting a game from Purescript to Elm"

https://alpacaaa.net/blog/post/elm-purescript-in-depth-overview/

### Blog post (new language user)

> Plus, a language that compiles to JS has to be approachable, right? Wrong. Purescript was as much confusing and frustrating as Haskell (in fact, they’re very similar languages).

- Users of compiler-to-JavaScript languages expect an approachable language.
- PureScript's new user experience can be a confusing and frustrating experience.


## List of Yet-To-Be-Analyzed Sources

The following quotes were found by searching the PureScript Discourse, Twitter, and Google for PureScript documentation, impressions, and experience reports.

> Core PureScript has great documentation (see the PureScript book, the Halogen guide and example repos). However, most of the rest of PureScript learns from Haskell by having mediocre documentation. You’ll need to become familiar reading types and briefly checking source code to see what’s going on. That said, we’ve rarely had trouble with documentation; most functions are self-explanatory and the functional programming Slack is great for filling in the gaps.
> https://www.reddit.com/r/functionalprogramming/comments/7vveeu/purescript_vs_reasonmlbucklescript_in_2018/dtw5qm7/

> I think PureScript is missing a full webapp step-by-step tutorial (front, back, database, mails, authentication, forms, validation…)
> https://twitter.com/ThibaudDauce/status/895534464071331840

> I tried PureScript, first impression was really good, but I was lacking some guidance for e.g. free monads etc. So deeper concepts :-) tips?
> https://twitter.com/raimeyuu/status/895379846938992640

> Building Purescript Puzzler was a great learning experience, especially since I’m not the most experienced web dev. I sunk my teeth into a few cool libraries and got my first real taste of FRP outside of toy examples. However, I still feel like thar be dragons lurking in the shadows with this approach, and the apparent lack of complex examples is not reassuring. I think part of the problem with this is the absence of wrapper libraries that make common tasks easier, which inhibits exploration.
> http://fluffynukeit.com/exploring-the-mvi-architecture-with-purescript-puzzler/

> I felt the same way. Learning PureScript wasn't difficult for me but I already knew Haskell. I can't imagine what it's like for someone who doesn't know Haskell to learn PureScript, because there are very few tutorials designed for that audience. Most of the docs on PureScript are very much "reference" style so you have to already know what you're looking for to even find them.
> https://www.reddit.com/r/haskell/comments/79i7h9/why_is_elm_more_popular_than_purescript/dp2ztyi/

> It also feels like PureScript is unmaintained. I tried PS out twice over a year or two and the docs were more or less the same (very sparse).
> ...
> A big issue for me, too, was that I felt like I was looking at Haskell docs to figure out how to do things more than I was using PS documentation. At that point, why not just use a Haskell compiler that targets JavaScript instead? And, if I end up using the FFI to include the majority of my JS code, can’t I just write functional JavaScript code in the first place and cut out the middle man?
> https://www.reddit.com/r/haskell/comments/79i7h9/why_is_elm_more_popular_than_purescript/dp2ngoe/

> Also, Purescript has this interesting property of being hard to learn (because it is powerful), but dead simple to use (because it compiles to JS). So you only really get stuck on figuring out how to do things in PS, as opposed to how to get PS working, and therefore every time you get unstuck, you have leveled up. So it's hard, but rewarding.
> https://vue-hn.now.sh/item/17125882

> However, I'd only put PureScript into production if I had people with Haskell experience and a good amount of time to become contributors. The community is friendly to beginners, but there's a vast amount of background that isn't explained in a systematic way, and the community standards for documentation and infrastructure just aren't up to the level we've come to expect from systems like Elm or Elixir or even Clojure.
> https://dev.to/marick/comment/52da
