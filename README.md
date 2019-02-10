# PureScript Documentation Discussion & Planning

Discussing PureScript 2019 documentation improvement, as initiated here:

https://discourse.purescript.org/t/purescript-documentation-efforts-in-2019

## Project Goal

This project is about documenting **what PureScript currently is**. It's about how to do that in an efficient way and how organize and convey the information in a ready-friendly way. It isn't, then, deciding **what PureScript should be**.

Doing this involves learning newcomers', long-time users', and project maintainers' opinions of its documentation and discovering the actual state of PureScript's current documentation. Having this information, we can calculate what is missing from the current documentation, produce ideas for improving the documentation and its process, and develop and refine strategies for successfully accomplishing this.

## Explaining Our Methodology

To get an understanding of the methodology used here, see these files in order:
1. `01 sources and interpretations/ReadMe.md`
2. `02 context or narrative.md`
3. `03 purepose and principles.md`
4. `04 outcome brainwrite next actions/outcome1.md`

Here is our current status:
- Done
    - <del>Phase 1: Gathering and interpreting various sources</del>
- Current
    - **Phase 2: defining the context/narrative**
- Next
    - Phase 3: defining the purpose, principles, and outcome
    - Phase 4: completing those outcomes

## Project Management

### Create a Work Item

Open an issue to indicate some task that needs to be done. If it's a new source of data, include it as a link.

### Start on a Work Item

If an issue is not assigned, assume anyone can work on it.

1. When you're ready to start working on an issue, assign the corresponding issue to yourself. When you do this, you are committing to completing the work.
2. If a file for that source does nto already exist, create one.

### Working on a Work Item

1. Do all work related to that source in that file. This is to prevent merge conflicts from slowing our analysis down.
2. Push any changes directly to `master`.

### Completing a Work Item

Once you have finished your initial work...
1. Move the file to the corresponding "For [other person]" folder to indicate that this person can review your work.
2. Push this final change to `master`
3. Mark the corresponding issue as closed with a comment that includes the specific commit hash that has the final commit in your work.

## License

See the [CONTRIBUTORS.md](CONTRIBUTORS.md) file for license.
