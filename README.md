# Git introduction ½ day course

Welcome to the Git Introduction ½ day course for Equinor ASA.  This
entire course is available under the _**Creative Commons** Attribution Share
Alike 4.0 International license_ (cc-by-4.0).

>**You are free to:**
>
>* **Share** — copy and redistribute the material in any medium or
>  format
>* **Adapt** — remix, transform, and build upon the material for any
>  purpose, even commercially.
>
>This license is acceptable for Free Cultural Works.
>
>The licensor cannot revoke these freedoms as long as you follow the
>license terms.
>
>**Under the following terms:**
>
>* **Attribution** — You must give appropriate credit, provide a link to
>  the license, and indicate if changes were made. You may do so in any
>  reasonable manner, but not in any way that suggests the licensor
>  endorses you or your use.
>* **No additional restrictions** — You may not apply legal terms or
>  technological measures that legally restrict others from doing
>  anything the license permits.
>
>**Notices:**
>
> You do not have to comply with the license for elements of the
> material in the public domain or where your use is permitted by an
> applicable exception or limitation.
>
> No warranties are given. The license may not give you all of the
> permissions necessary for your intended use. For example, other rights
> such as publicity, privacy, or moral rights may limit how you use the
> material.




## About this course

There is nothing this course will teach you that you couldn't get from reading
the amazing [Pro Git book](https://git-scm.com/book/en/v2).  In the cases where
we will not be able to explain a topic any better than the book, which happens
to be most topics, we will put a link to the chapter and verse in the book at
the beginning of the section.

Most sections have a _reference_ section for further reading, e.g.

> **References**
> 1. [git-scm](https://git-scm.com/book/en/v2)

It is recommended that you take some time to read through the material.




## Table of contents


1. [Warming up](#warming-up)
1. [The empty repository](#the-empty-repository)
1. [Your first commit](#your-first-commit)
1. [Browsing our history](#browsing-our-history)
1. [Git commands we have seen](#git-commands-we-have-seen)

# Warming up

Open an empty pure text file.

```bash
$ nano yourfile.txt
```

## Exercises

1. Create `touch` a new text file.
1. Write some lines
1. Copy that file to a different file and make a couple of changes
1. Run `diff` on the two files and save the output to a new file.
1. Apply `patch` on the file and the output.

## References

* [Text files](https://en.wikipedia.org/wiki/Text_file)
* [`diff`](https://en.wikipedia.org/wiki/Diff)
* [`man diff`](http://man7.org/linux/man-pages/man1/diff.1.html)
* [`man patch`](http://man7.org/linux/man-pages/man1/patch.1.html)


# The empty repository

TBW

## Exercises

1. Make a new folder
1. Run `git init`
1. Run `git status`


## References

1. [`git init`](https://git-scm.com/docs/git-init)
1. [`git status`](https://git-scm.com/docs/git-status)




# Your first commit


## Exercises

1. Create a text file with some content.
1. Run `git add` on the file
1. Run `git status`
1. Run `git commit -m "Initial commit"`


## References

1. [`git add`](https://git-scm.com/docs/git-add)
1. [`git commit`](https://git-scm.com/docs/git-commit)


# Browsing our history

A crucial part of using Git is to read the history of the project; it is after
all a revision control system.

## Exercises

1. Run `git log`


## References

1. [`git log`](https://git-scm.com/docs/git-log)


# Git commands we have seen

* [`git init`](https://git-scm.com/docs/git-init)
* [`git log`](https://git-scm.com/docs/git-log)
* [`git status`](https://git-scm.com/docs/git-status)
* [`git diff`](https://git-scm.com/docs/git-diff)
* [`git show`](https://git-scm.com/docs/git-show)
* [`git add`](https://git-scm.com/docs/git-add)
* [`git commit`](https://git-scm.com/docs/git-commit)
* [`git reset`](https://git-scm.com/docs/git-reset)
* [`git clean`](https://git-scm.com/docs/git-clean)
* [`git rm`](https://git-scm.com/docs/git-rm)
* [`git mv`](https://git-scm.com/docs/git-mv)
* [`git restore`](https://git-scm.com/docs/git-restore)
* [`git stash`](https://git-scm.com/docs/git-stash)
* [`git tag`](https://git-scm.com/docs/git-tag)
* [`git blame`](https://git-scm.com/docs/git-blame)
* [`git filter-branch`](https://git-scm.com/docs/git-filter-branch)
* [`git bisect`](https://git-scm.com/docs/git-bisect)
* [`git branch`](https://git-scm.com/docs/git-branch)
* [`git checkout`](https://git-scm.com/docs/git-checkout)
* [`git merge`](https://git-scm.com/docs/git-merge)
* [`git rebase`](https://git-scm.com/docs/git-rebase)
* [`git cherry-pick`](https://git-scm.com/docs/git-cherry-pick)
* [`git reflog`](https://git-scm.com/docs/git-reflog)
* [`git clone`](https://git-scm.com/docs/git-clone)
* [`git remote`](https://git-scm.com/docs/git-remote)
* [`git push`](https://git-scm.com/docs/git-push)
* [`git fetch`](https://git-scm.com/docs/git-fetch)
* [`git pull`](https://git-scm.com/docs/git-pull)

---


Copyright 2020 Equinor ASA, (cc-by-4.0)
