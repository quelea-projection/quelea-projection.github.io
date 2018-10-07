Are you a developer that fancies contributing to the Quelea project?
Great\! This guide is not extensive, nor thorough, but should act as a
good starting point. If you have any further questions then please head
over to the [Quelea discussion
group](https://groups.google.com/forum/#!forum/quelea-discuss).

## Brief summary

Quelea is written in Java (the GUI in JavaFX) and hosted on Github. It
requires (at least) Java 8 to run at the time of writing, but that is
likely to increase in the near future to Java 10 or 11. You can check
out the code [here](https://github.com/quelea-projection/Quelea), which
is a Gradle project.

You are of course welcome to fork the project as well (the beauty of
open source\!) and make any chances you wish, however bear in mind that
we probably won't accept them back into the main Quelea codebase unless
you've asked us first on the discussion group (and we've said
yes\!)

## Code quality requirements

`- All new classes and methods must have appropriate Javadoc comments.`
`- New GUIs should be written in code rather than FXML (I'm aware this goes against the wishes of many, but it helps consistency as we've done things this way thus far.)`
`- Existing infrastructure must be used where possible and sensible - on importers for example, you should tie into the existing ImportDialog and Parser inheritance hierarchy.`
`- Proper indentation please - that's 4 spaces per level, no tabs.`
`- Please keep individual commits reasonably atomic, it makes code reviews much easier.`

## FAQ

### I really don't understand how to get started

Feel free to ping us over on the discussion group with problems you're
having, and we'll do our best to help. That said, if you want to work on
most aspects of Quelea you will need a reasonable grasp of Java.

### Can I have commit access?

Not right away, but if you build up a good reputation with us for
submitting good, bug free (as far as is reasonable) code, then we may
consider it. You'd definitely have to provide us with a few good merge
requests first.

## This all sounds a bit draconian

Please don't take all the above as our attempt to discourage
contributions. As much as we'd love to accept anyone's patches from
anywhere, this just isn't practical. In fact, some years ago we accepted
a couple of patches with minimal checking, but it caused all sorts of
issues and took us months to properly rectify. We feel it's much better
to lay down the rules / expectations first, so that people aren't
disappointed later if their patches aren't accepted (or we request
further work before they are.)---

---
