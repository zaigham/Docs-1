---
title: "Becoming a Contributor"
_old_id: "1127"
_old_uri: "contribute/becoming-a-contributor"
---

<div>- [<span style="color: #000000">**The Contributor License Agreement**</span>](#BecomingaContributor-)
- [I've submitted my CLA, now what? I want to commit!](#BecomingaContributor-I%27vesubmittedmyCLA%2Cnowwhat%3FIwanttocommit%5C%21)
  - [In a Nutshell](#BecomingaContributor-InaNutshell)
- [Using Git and GitHub and the MODX Branching Strategy](#BecomingaContributor-UsingGitandGitHubandtheMODXBranchingStrategy)
- [My code contribution was rejected! What?!](#BecomingaContributor-Mycodecontributionwasrejected%5C%21What%3F%5C%21)
- [See Also](#BecomingaContributor-SeeAlso)

</div>So, you're itching to get in on the development or documentation of MODX Revolution or MODX Evolution. But, to your dismay, you're confused on how to start that process. This article will help you get to your level of commitment in development - be it an active coder or a tester who submits patches.

**The Contributor License Agreement**
-------------------------------------

If you want to work on bugs or features and actually commit some code to MODX, or contribute to the documentation, the first step is to fill out and send in a **[Contributor License Agreement (CLA)](http://develop.modx.com/contribute/cla/)** after creating your MODX account. A CLA protects your contributions, but also gives MODX and its user base clear permission to use those contributions any way that is compliant with the MODX license (GPL), and it's based on--<del>more like copied directly from</del>--the same one used by Apache and the Dojo Foundation.

I've submitted my CLA, now what? I want to commit!
--------------------------------------------------

Now that you have access to the issue tracker, go ahead and fix some bugs or work on a feature.

Collaborating on MODX's code is easy. MODX uses Git for source control, and our repositories are hosted on [GitHub](http://github.com/modxcms/).

### In a Nutshell

**We prefer that you submit source code changes by using GitHub's Pull Requests.** Simply fork the project and clone the repository. Create a bugfix or feature branch locally, and start working on your change. Then, once you've finished and tested it thoroughly, push your branch to your fork and send a Pull Request to the official modxcms repository. An Integration Manager will then integrate or reject your request. That's it! No getting access from the core team needed - just push and pull in Git! (Please, no political jokes hidden in the comments. Really.)

Those with publicly accessible git repositories not on GitHub can attach details on accessing the repository to the relevant issue(s) in the issue tracker. Also explain which branch is relevant and, if relevant, reference the commits themselves.

Alternatively, though Pull Requests are preferred first and other external git repositories second, we will also accept patch files attached to a ticket in the issue tracker. If you do this, please ensure that your patches are generated against the most recent files (either from a release branch or the develop branch).

Using Git and GitHub and the MODX Branching Strategy
----------------------------------------------------

If you can code, but source/version control and collaborating is new to you, don't panic! The section on [Using Git and GitHub](/community/contribute/using-git-and-github/ "Using Git and GitHub") will fill you in on how to get started and also explains the branching strategy used by MODX and what that means for contributors.

My code contribution was rejected! What?!
-----------------------------------------

Every once in a while, a contribution submitted doesn't make it into the core. It's not because we don't like you. In all honesty, Jason loves darts, and at random intervals he staples contributions to the wall and we choose the one he hits while blindfolded. (Okay, so that's not true. He's not blindfolded.)

Sometimes a contribution you submit won't make it in. That may be for a myriad of reasons:

- A contribution doesn't follow [Code Standards](/revolution/2.x/developing-in-modx/code-standards "Code Standards")
- The contribution will be moved to a component rather than the core
- The contribution will be deferred to a later release
- We used a different contribution to fix the issue
- The contribution caused too many other issues to arise
- The patch was submitted in [lolcode](http://lolcode.com/), which although we had a hoot reading, was pretty useless in the end

So don't take offense. We really appreciate _any and all_ contributions to MODX, and we seriously consider everything that this wonderful community gives to it. MODX has thrived because of this community. However, some things just won't match with the MODX vision and design philosophy; so be patient with us, and know we really like people who submit pull requests and patches. A ton. Did we mention we really like people who have forked us?

See Also
--------

1. [Development Environments](/community/contribute/becoming-a-contributor/development-environments)
2. [MODX PHP Coding Standards](/community/contribute/becoming-a-contributor/modx-php-coding-standards)