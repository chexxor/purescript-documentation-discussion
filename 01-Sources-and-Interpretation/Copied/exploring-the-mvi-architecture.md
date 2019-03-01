
## Source: Exploring the MVI Architecture with Purescript Puzzler

http://fluffynukeit.com/exploring-the-mvi-architecture-with-purescript-puzzler/

> Below is a collection of my impressions of the experience in making this game. My goal here is not to argue for or against any of these libraries or techniques but simply to write my ideas down while they are still fresh in my head and invite discussion.

- What follows are a rough draft of the author's thoughts/impressions and have not been given considerable thought as to how to best word/communicate things. These might also be based more on feelings/perception than clear examples.

### Signal Library

> The signal library has some quirks, but overall it’s really nice. It’s essentially a clone of Elm, which has been exploring the concept of FRP related GUIs for a long time, so a lot of the kinks have been worked out.

- Author is likely already familiar with Elm.

#### Signals Defined for All Time

> This formulation ([that signals are defined for all points in time, including time zero]) occasionally presented me with pain points when using signals. For instance, in order to get notifications of DOM events, I needed to put a Channel in my event handlers. In most cases, this isn’t a problem, but consider events that fire rapidly like drag events (drag and drop was my first approach for Purescript Puzzler, which I abandoned after great difficulty). Usually I won’t want to update the model on every drag event, so I can use `sampleOn (every 40)` at the subscription site so that drag events are limited firing at a 40 ms rate. But wait…what if dragging stops? No new events are put on the channel, but I’m still sampling the most recent event at 40 ms! Gah! A similar situation as this caused a nasty bug in which a “toggle” event kept firing, causing a div border to flash at 80 ms period. I worked around this by combining my sampling with `distinct'` to eliminate samples that didn’t change, but it does show that constant-time signals can be tricky to think about.

- This "pain point" is more about the design used in the `signal` library and how the author used that library than the library itself.
- One PureScript user experienced the run-time behavior of the `signal` library to be difficult to understand and/or control when writing a program using the library.

> Another nit is that a `Channel` must be initialized with some value for time zero, but if a channel is being used to send events, how do I initialize when no events have happened yet? I had to create a dummy event called `Init`, that did absolutely nothing and had no significance, just to give the channel some kind of value.

- Concept's intended purpose and Author's intended purpose differ. Thus, author used a hacky solution. This might have arisen due to the author not knowing how to use the library properly or because the library did not provide a basic building block that does what he needs it to.

> It’s possible that with some smarter designing, I could order the MVI components in such a way that the initial value to start the chain is the initial `GameState`, eliminating the need for `Init`, but it is not obvious to me whether that would work out.

- This question relates to how to structure things, highlighting another aspect of documentation for 'best practices.'

#### Trickness with Effectful Signals

> I had a lot of problems trying to figure out a way to process signals in an effectful way that also incorporated state.... However, I couldn’t figure out a way to use the signal combinators to achieve this. Instead, I had to provide an initial, dummy `VTree`, render it, then use the rendered node and the previous `VTree` as internal state that I folded over with new `VTree`s.

- Another example of author using a hacky solutoin to achieve something. I'm not sure whether author is unfamiliar with FRP or this arose for lack of good documentation or author is doing something outside of the norm.

#### Signal Distinction

- Author seemed to be suggesting one way the library could improve here to account for a problem author encountered.

#### Interactions "Set in Stone"

> Once a signal line is established, I don’t think there is any way to “unsubscribe” from signal line updates.

- The author believes the `signal` library should offer a means of defining a branch in a signal graph which is conditionally active.

> It’s also not clear to me how I would listen to multiple signals on the fly, adding new signals as needed. I expect it to be possible; I just don’t have any experience with it and feel like it could be a pain point.

- Author has question that author was not able to answer on own. Not sure whether author contacted others for help on Slack or not.

### Virtual Dom

> Overall, virtual-dom is really cool to use. Writing a declarative GUI without having to worry about update-this or change-color-that was a straightforward, easy experience.

- This PureScript user believes writing a GUI in a declarative/descriptive, non-imperative way is an easy way to develop a GUI app.

> Overall, virtual-dom is really cool to use.... I never have to worry about keeping the GUI and game state in sync because I’m building the GUI from scratch at each update.
>
> For small projects, I wouldn’t hesitate to use virtual-dom again. However, for more complex ones, I have some concerns.

#### Room for VDom Wrapper Libraries

> The virtual-dom bindings for purescript are pretty low level, and that’s the way I think they should be. In JS land, the virtual-hyperscript DSL can be use to easily set up VTrees and includes a lot of convenient features out of the box, but it is opinionated. I’d love to see a similar purescript library and will probably make one sometime in the future.

- Author suggests a new library for higher-level bindings to VDom to gain convenience at cost of abiding by design choices of library.

#### Stateless GUI is a double-edged sword

> Not worrying about GUI state is a huge relief on the GUI side, but that means that every single stateful component in the application is now included in the Model – open dialogs, mouse location clicks, you name it. Purescript Puzzler is pretty simple in both the model and the GUI, so this is manageable. However, I can’t help but feel that in the general case, this actually couples the Model to the GUI more instead of less. Now the Model needs to know about all the little components on the GUI side in order to capture their state. This kind of formulation does not lend itself well to composition or separation of concerns.

- Since author stated above that 'stateless GUI is really cool,' author might not yet be familiar with 'best practices' for how to design such a program using this concept. We can't tell whether author used modular code to break big components down into smaller ones and whether these distinctions were done well.

- This PureScript user believes the best practices encoded in the "stateless GUI" design prescribed by the practice they are following in this app doesn't have a clear relation to traditional software design best pracices they know.

[Other issues raised by author were more about the MVI architecture author was using. Thus, they have not been included here.]

#### Animations are Inherently Stateful

[Author shares one issue and one way to deal with that but states that author did not every try it. Thus, author confesses "I can't comment on them extensively." Skipping this.]

#### Full VTree Diff Each Update

[Author ponders some issues with the VDom concept that's not related to PS]

#### Virtual-Dom Uses Javascript Conventions

> Virtual-dom uses a number of JS style conventions that present some impedance when trying to use them from Purescript. The biggest is probably the use of arbitrary records that define id, attributes, style, etc. These are pretty verbose and annoying. In fact, most of the work done by the virtual-hyperscript DSL is simply building these records for the user in an easier way. However, in Purscript, each record is technically a different type, which doesn’t always jive well with the type system.

- I'm not sure what `virtual-hyperscript` is or what issues with the type system author is talking about.

> Another JS convention is the use of `undefined` to remove properties from nodes. This only affected me in one case in which I needed to disable/enable the Hint button. To disable/enable, I use the following attributes.
```purescript
{ attributes: { disable: "" } }
-- presence of disable attribute disables button, regardless of value
{ attributes: {} }
-- absence of disable attribute enables button
```

> The problem is that the above two records have different types, so I cannot return one or the other from an if clause.

- Unfortunately, I don't know enough about this topic to know what the issue here is. I'm also not sure how much of this is due to the author using a bad solution to a real problem.
- This PureScript user believes it's difficult to integrate with a JavaScript library function which uses property-existence to define its behavior because PureScript's type system isn't flexible enough to define the type of that function in a simple way. (I think it's possible to modify the type signature of the JS library wrapper to use a typeclass to assert the argument has a subset of the fields expected by the function.)

#### Overall

> Building Purescript Puzzler was a great learning experience, especially since I’m not the most experienced web dev.

- Two possible ideas here:
    - Author made a better web app than expected despite not having much web experience.
    - Author's above problems might be due to author's lack of experience (and lack of documentation or other support) than due to the language itself or library designs.

> I sunk my teeth into a few cool libraries and got my first real taste of FRP outside of toy examples. However, I still feel like _thar be dragons_ lurking in the shadows with this approach, and the apparent lack of complex examples is not reassuring. I think part of the problem with this is the absence of wrapper libraries that make common tasks easier, which inhibits exploration.

- Author could not find complex examples that helped author troubleshoot issues.
- Author wanted more user-friendly libraries that handled more lower-level things, so that author could focus on learning and not fixing plumbing issues.
- This PureScript user believes the library/architecture they used was missing concepts, which would make it unsuitable for more complex applications.
- This PureScript user implies the library/architecture they used should document the situations it was designed for and the situations in which it is likely a poor fit.
