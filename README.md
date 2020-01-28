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
$ nano a.txt
```

Let us create some content in our file `a.txt`:

```
Mr. Utterson the lawyer was
a man of a rugged countenance
that was never lighted by a smile;
cold, scanty and embarrassed in discourse;
backward in sentiment;
lean, long, dusty, dreary
and yet somehow lovable.
```

Now, let us create a file `b.txt` which contains some errors on line five:

```
Mr. Utterson the lawyer was
a man of a rugged countenance
that was never lighted by a smile;
cold, scanty and embarrassed in discourse;
bckwrd n sntmnt;
lean, long, dusty, dreary
and yet somehow lovable.
```

If we run `diff a.txt b.txt` in the terminal, we will get the following output
(this is important)

```patch
5c5
< backward in sentiment;
---
> bckwrd n sntmnt;
```

There are four lines in this output, and each line is important.
1. `5c5` consists of two line numbers `5` and `5`, separated by a `c` (for _change_)
1. The `<` character means content in the _first_ file (`a.txt`)
1. The `---` separator means that we are done with the _first file_ of this _hunk_
1. The `>` character means content in the _second_ file (`b.txt`)

If we _delete_ the fifth line in `b.txt` (the one reading `bckwrd n sntmnt;`), and
run `diff`, the output will be:

```patch
5d4
< backward in sentiment;
```

You might have guessed it: the `d` in `5d4` means that a line was _deleted_.
Were we to _add_ a line to the second file, the output would likely be `5a6`.

Notice how a diff (a _patch_) between two files can tell us how to go from _one
file_ (`a.txt`) to another file (`b.txt`), and back again.  And indeed, there is
a tool, called `patch`, that takes a diff and _applies_ it to a file, producing
the second file:

```bash
$ diff a.txt b.txt > fix.patch
$ patch a.txt fix.patch
patching file a
```

It is also possible to go back (we are asked in this case)

```bash
$ patch b.txt fix.patch
patching file b
Reversed (or previously applied) patch detected!  Assume -R? [n]
```

(press `y` for reverse patching).

Once you understand this back-and-forth you will be able to understand
everything version control is about!

**Hunks**

As we saw above, the diff output consisted of one line with something like
`5c5`, one (or more) line(s) starting with `<`, a separator `---`, followed by
one (or more) line(s) starting with `>`.  This is one _section_ of a diff,
called a _hunk_.  If you have several changes in different places in the file,
you will likely have _several hunks_.  You should be able to decode their
meaning now, i.e. what is the difference between `a.txt` and `b.txt`.

```patch
2c2
< a man of a rugged countenance
---
> a man of rugged countenance
6c6
< lean, long, dusty, dreary
---
> lean, long dusty, dreary
```

## Exercises

1. Create (`touch`) a new text file.
1. Write some lines.
1. Copy that file to a different file and make a couple of changes.
1. Run `diff` on the two files and save the output to a new file.
1. Experiment with several changes and inspect the output of `diff`.
1. Apply `patch` on the file and the output.

## References

* [Text files](https://en.wikipedia.org/wiki/Text_file)
* [`diff`](https://en.wikipedia.org/wiki/Diff)
* [`man diff`](http://man7.org/linux/man-pages/man1/diff.1.html)
* [`man patch`](http://man7.org/linux/man-pages/man1/patch.1.html)
* [Hunks](http://www.gnu.org/software/diffutils/manual/html_node/Hunks.html)

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
