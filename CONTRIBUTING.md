Contributing to openvela
==========================

\[ English | [简体中文](CONTRIBUTING_zh-cn.md) \]

openvela has been developed by an active team of software engineers and researchers. Any contributions from the open-source community to improve this project are welcome!

openvela is licensed under Apache License 2.0.

Sign the CLA
-----------------------

You must sign the Contributor License Agreement in order to contribute.

[ [Personal](https://open-vela.cnbj1.mi-fds.com/open-vela/cla/Xiaomi_Documentation_Open_Source_Individual_CLA.pdf) | [Enterprise](https://open-vela.cnbj1.mi-fds.com/open-vela/cla/Xiaomi_Documentation_Open_Source_Corporate_CLA.pdf) ]


Bug reports
-----------

If you think you have found a bug in openvela, first make sure that you are testing against the latest version of openvela (your issue may already have been fixed). 
If not, search our issues list on GitHub in case a similar issue has already been opened.


Feature requests
----------------

If you find yourself wishing for a feature that doesn't exist in openvela, you are probably not alone. There are bound to be others out there with similar needs. Many of the features that openvela has today have been added because our users saw the need. 
Open an issue on our issues list on GitHub which describes the feature you would like to see, why you need it, and how it should work.


Contributing code and documentation changes
-------------------------------------------

If you would like to contribute a new feature or a bug fix to openvela, please discuss your idea first on the GitHub issue. If there is no GitHub issue for your idea, please open one. It may be that somebody is already working on it, or that there are particular complexities that you should know about before starting the implementation. There are often a number of ways to fix a problem and it is important to find the right approach before spending time on a PR that cannot be merged.

### Fork and clone the repository

You will need to fork the main openvela code or documentation repository and clone it to your local machine. See [GitHub help page](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo) for help.

### Tips for code changes

* Following these tips prior to raising a pull request will speed up the review cycle.
* Add integration tests, if applicable
* Make sure the code you add follows the formatting guidelines
* Lines that are not part of your change should not be edited (e.g. don't format unchanged lines, don't reorder existing imports)
* Add the appropriate license headers to any new files

### Submitting your changes

* Test your changes
   
> Run the test suite to make sure that nothing is broken.

* Sign the Contributor License Agreement
   
> Please make sure you have signed our Contributor License Agreement. We are not asking you to assign copyright to us, but to give us the right to distribute your code without restriction. We ask this of all contributors in order to assure our users of the origin and continuing existence of the code. You only need to sign the CLA once.

* Rebase your changes
   
> Update your local repository with the most recent code from the main openvela repository, and rebase your branch on top of the latest main branch. We prefer your initial changes to be squashed into a single commit. Later, if we ask you to make changes, add them as separate commits. This makes them easier to review. As a final step before merging we will either ask you to squash all commits yourself or we'll do it for you.

* Submit a pull request
   
> Push your local changes to your forked copy of the repository and submit a pull request. In the pull request, choose a title which sums up the changes that you have made, and in the body provide more details about what your changes do. Also mention the number of the issue where discussion has taken place, eg "Closes #123".


### How to deal with conflicts

You generally do NOT need to rebase your pull requests unless there are merge conflicts with the main. When GitHub complaining that "Can’t automatically merge" on your pull request, you'll be asked to rebase your pull request on top of the latest main branch, using the following commands:

* First rebasing to the most recent main:

```
git remote add upstream https://github.com/open-vela/[repository].git
git fetch upstream
git rebase upstream/[branch]
```

* Then git may show you some conflicts when it cannot merge, say `conflict.cpp`, you need
  - Manually modify the file to resolve the conflicts
  - After resolved, mark it as resolved by

```
git add conflict.cpp
```

* Then you can continue rebasing by

```
git rebase --continue
```

* Finally push to your fork, then the pull request will be got updated:

```
git push --force
```
