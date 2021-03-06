
## Source: 'How do we avoid incoherence in the Ecosystem?'

https://discourse.purescript.org/t/how-do-we-avoid-ecosystem-incoherence-in-the-future/209/

### Opening Thread

> Despite the hard work of many contributors and maintainers, there has been a lot of confusion surrounding the release of 0.12. My understanding is that this has happened in the past and is a phenomenon by and large accepted by the existing PureScript community.

Jordan
- New language releases that include breaking changes often lead to confusion. The "confusion" is not defined in this section, so that we can know what causes it and how to fix it.
- This "confusion" is largely accepted as "normal" by the community. In other words, "it just comes with the language."

Alex
- A PureScript user believes that new language releases which include breaking changes often lead to miscommunication.
- A PureScript user believes that miscommunication of language releases/changes is largely accepted as normal by the community.

> As a current user who follows changes in the ecosystem closely it didn’t cause me many problems, but anyone new to PS right now is feeling a lot of pain and (I believe) more likely than not to decide PureScript isn’t an investment worth making. The pain is diminishing daily as tools and libraries are updated which is great! The good news is that a major update like this creates greater than normal buzz. The bad news is that buzz draws newcomers at potentially the worst possible time.

Jordan
- New language releases are news-worthy and often draw in a lot of traffic. Perhaps people who want to use the language but have been turned off before now think, "Great! Maybe I can actually understand how to use it this time!" Others who have never heard of it might think, "What is this? It seems worth checking out." However, when either audience checks the site, they are immediately turned off. The overall effect is a net-negative for PureScript as a whole.

Alex
- A PureScript user sees that major language releases bring higher-than-normal newcomers to the language.

> I understand that several factors contributed to the situation, among them:
> - No central coordination

- I'm not sure what coordination this would entail. Perhaps a unified vision of what the community is trying to accomplish?

> - No full-time effort (though `garyb` and `kritzcreek` came closer than could be expected). Nobody’s getting paid to do this work.

Jordan
- Only volunteers who must pay their bills through other means are working on this language. There is no financial incentive for them to complete work, nor can they give the language their full time.

Alex
- A PureScript user sees that there is no "full-time" developers, but notes the opposite, that he sees there are a few people whose contributions are nearly that of full-time developers.
- A PureScript user believes that none of PureScript's contributors have a financial incentive to start or complete work.

> - Documentation was not updated to warn users about the problems they would encounter during this time of flux.

Alex
- A PureScript user believes that there was no release-related documentation marketed/announced a reasonable time before the release.

> - Tooling (specifically Pulp) was not updated in conjunction with the release of 0.12.0.

Jordan
- Self-explanatory: one cannot benefit from a new release if the tooling support doesn't make it work well.
- A language should provide a "complete solution" to business problems, including build tools that 'just work.'

Alex
- A PureScript user believes that compiler related projects, such as build tools, should be updated along with compiler releases. (One cannot benefit from a new compiler version if the tooling used by their previously-written project doesn't support it.)

> - Although core and contrib libs were updated during this time, some key pieces were missing, most notably Aff and Halogen (despite the best efforts of natefaubion).

Jordan
- Major libraries in the ecosystem were not updated at the same time as the language release. So, one could not immediately benefit from the new release.

Alex
- A PureScript user believes that major libraries in the ecosystem should work with the latest available version of the compiler. (One can not benefit from the new release if the shared libraries used in the previously-written project don't work with the latest available compiler version.

> - The Slack channels and this Discourse instance are great resources, but I could only find one reference to Slack (at https://github.com/purescript/purescript#help

Jordan
- The Slack channel and Discourse site are not easily findable.

Alex
- A PureScript user believes the Slack channel and Discourse site are the best resources for PureScript users.
- A PureScript user believes that all PureScript users should visit the Slack and Discourse instances as their primary resource for help.

> - It would be helpful to have this information duplicated at purescript.org

Jordan
- The Slack/Discourse links should be included in the PureScript language website.

Alex
- A PureScript user believes the PureScript language HTML website should direct its visitors to PureScript's Slack/Discourse instances. (The PureScript website is currently a primary resource visited by a subset of the PureScript community and it should direct people to the best resource for PureScript help known by this PureScript user.)

> - I think the link to Gitter should also be removed as it’s not very active and that can be discouraging.

Jordan
- The Gitter chatroom is not very active. If it gets removed completely, one should announce that in the channel and include links to the new chatrooms to use and why.

Alex
- A PureScript user believes the Gitter chatroom is not very active.
- A PureScript user believes the PureScript HTML website should reflect active resources, and inactive resources should direct people to active resources.

> I want to reiterate that no blame is being assigned and there’s no need for recrimination. I think we all want make this ecosystem a joy to work in for experienced users and newcomers alike.

Jordan
- An indicator of a healthy community that is focusing on problem-solving, not the blame-game.

Alex
- A PureScript user believes that all contributors want to make the PureScript language and its ecosystem of projects a happy place to work.

### Comment (core contributor)

https://discourse.purescript.org/t/how-do-we-avoid-ecosystem-incoherence-in-the-future/209/2

> I think another point to consider is how we can better communicate (or somehow enforce) compiler<->library versioning.

- An unanswered question: how can the community communicate/enforce compiler-library versioning. I believe that concept means "this version of the library works on this version of the compiler."

> Absolutely, it (i.e. not announcing the next language release without first updating the ecosystem) is why I haven’t mentioned or retweeted anything about 0.12 on my twitter yet!

Jordan
- Some people get this idea whereas others do not. This should be communicated as something to expect for new learners
- An official "ecosystem is `<release version>`-ready" announcement might help prevent this. Likewise, Including a "this release is made but not ecosystem-ready yet" note in the languages' release notes that includes a link as to what "ecosystem-ready releases" mean might help prevent this negative press.

Alex
- A core contributor believes that compiler-related projects (the ecosystem) are an important of a compiler release.
- A core contributor believes communication of a major compiler release has significant impact on language's followers.
- An official "ecosystem is `<release version>`-ready" announcement might help prevent this. Likewise, including a "this release is made but not ecosystem-ready yet" note in the languages' release notes that includes a link as to what "ecosystem-ready releases" mean might help prevent this negative press.

### Comment (core contributor)

https://discourse.purescript.org/t/how-do-we-avoid-ecosystem-incoherence-in-the-future/209/3

> The kind of issues we’re encountering here are also why I’m reluctant to make a 1.0 release in the near future, because we still do have a lot of ecosystem stuff to solve - I don’t believe for a second most people (esp. newcomers) will see a distinction between the PureScript language/compiler 1.0 and the “PureScript product” as a whole. But that’s probably another discussion.

Jordan
- garyb's resitance to making a `v1.0` release are better explained: a `v1.0` PureScript langauge is not the same as a `v1.0` Purescript Ecosystem / Complete Solution to most business problems. Most people who hear that there is a `v1.0` PureScript release will think it also includes the latter when it only includes the former. This might result in a net-negative press for the language.

Alex
- A core contributor believes that the PureScript language/compiler and the "PureScript product" can be difficult for most people to differentiate.
- A core contributor believes that a `v1.0` release should include improving the "PureScript product" (the ecosystem).
- Most people who hear that there is a `v1.0` PureScript release will think it means a "complete solution" when it might only mean the language/compiler. This might result in a net-negative press for the language.

### Comment

https://discourse.purescript.org/t/how-do-we-avoid-ecosystem-incoherence-in-the-future/209/4

>> From `paf31` on the Slack Channel: "For the other major release, we used to have a checklist of all of the stuff that came with the compiler"
>
> Where would be a good place to keep a more comprehensive checklist? The compiler repo doesn’t seem appropriate as we want to cover docs, libs, and third-party tooling as well.

Jordan
- There is not a place that stores an up-to-date process/checklist of things to do for making a language release.
- The documentation repo is likely a bad place to store that checklist/process.

Alex
- There used to be a process/checklist of things to do for making a language release.
- There is not a clear place to store a checklist like this.
- The compiler repo is the first idea of a place to store this list, but it is inappropriate because it is related to non-compiler things like docs, libs, and tooling.

### Comment (core contributor)

https://discourse.purescript.org/t/how-do-we-avoid-ecosystem-incoherence-in-the-future/209/5

> It is unrealistic to expect that we wait for everything to update before we release a compiler version. If we did that we’d probably never get a release. For example, many newcomers are using the PureScript book, but we obviously can’t wait for Phil to update everything in the book before a release.... We absolutely need to be able to do a release, and let the ecosystem gradually catch up, because we just don’t have the community resources do it all at once.

Jordan
- Purescript, being developed purely by volunteers, does not currently have an efficient toolchain and/or enough manpower to reliably update everything in the ecosystem before making a release.

Alex
- A core contributor believes that the compiler's ecosystem should not block releases of the compiler, because the time required to update the ecosystem is nearly as long as the time between major compiler releases.
- PureScript does not have enough manpower (or automation) to reliably update everything in the ecosystem before making a release.

> The book is currently problematic in how it recommends users get started and start installing libraries, which results in incompatibilities.
> The number one issue is that there is not any easy or reliable way to deal with compiler compatibility as long as we are recommending Bower in our introductory materials....

Jordan
- Part of the up-to-date documentation issue is due to using Bower as a dependency manager because it can result in incompatibilities between dependencies.

Alex
- A core contributor believes ecosystem compatability is difficult or unreliable while PureScript community recommends using Bower as a dependency manager.

> Right now, the only viable option is psc-package. If all our introductory resources specified exact compiler versions (Just recommending npm install purescript is extremely problematic) along with an appropriate package set, we would not be having these problems.

Jordan
- Using psc-package as the dependency manager for introductory learning materials would solve the library-compatibility issues one faces with Bower.

Alex
- A core contributor believes that psc-package is the best option for dependency manager for introductory resources to use and recommend, as it would resolve the library-compatibility issues of Bower.

> The only problem with psc-package is that it is currently lacking features/tooling that make it convenient to use as a general purpose dependency manager. I know Christoph is experimenting with ways to make it more extensible via Dhall. I know for sure we will adopt it at Awake if that happens.

Jordan
- However, psc-package does not provide a complete solution to the problems which Bower does. While psc-package might be good for introductory learning materials, it is not as good for production code as Bower. Thus, many major libraries (e.g. Aff, Halogen) use Bower. New learners likely look at these libraries written or supported by "successful companies using PS in production" and see that they use Bower, not psc-package. Thus, they think they should do likewise.
- Once a `psc-package`-based approach becomes more mature, one major company will switch to it and do so eagerly.

Alex
- A core contributor believes the only reason to not adopt psc-package as the recommended dependency manager is missing features which make it a "general purpose" package manager and UX conveniences.
- An company using PureScript is eager to adopt `psc-package` when it becomes more mature.

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

- An idea that might only be relevant if one is using Bower as a dependency manager: a library badge in the Git repo indicating which version of the language the library is compatible.

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
- The Slack channel provided the most up-to-date "I need help now" info.

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

- An `upcoming-ps-release` branch in some libraries helped ensure they were compatible with the next language version almost as soon as it was released. This approach seems to have been a successful approach.

> However, unless I missed something major, there wasn’t much of a push to notify the rest of library authors about the release candidate, nor did the release candidate last very long.

- While this approach was successful, others did not follow it, perhaps because they were not aware of that approach or the release candidate window was too short.

> This seems unavoidable: we can’t force anyone to update, and if they aren’t tuned in on Slack or Discourse or Reddit then they’ll simply miss the new release, and won’t update until someone opens an issue or a pull request on their repository.
> However, perhaps we could do something more. We could at least make a good faith effort to notify people who maintain repositories available on Pursuit if their code is going to break in the new release.

- If a person starts and maintains a new library, they need to be notified of breaking changes in an upcoming language release. Ideally, this would be done via them subscribing to some notificaton system, or learning of it via a public announcement or someone opening up an issue for it in their repo. Of these approaches, the last one is best if it can be automated.

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
