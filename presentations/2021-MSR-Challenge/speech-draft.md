# Speech draft

Time limit is 3 minutes. Base on some research on public speech, 100~150 wpm is
a good pace for presentations.

TODO:

* Make sure no "popping"

## 1

Hi, everyone, thank you for coming to the talk. My name is Wenhan. Today, I'll
talk about the project with my supervisor Mike on

> Mea culpa: how developers fix their own simple bugs differently from those of
> other developers.

<!-- MAY-uh CUL-pah-->

## 2

Bugs are inevitable during the development process. In open source development,
many users submit changes to improve a project.

When these changes are related to fixing bugs, depend on the author of the
fixing change, there are two scenarios. One where the bug is fixed by the same
developer who introduced the bug, and the other by a different developer.

These two different scenarios introduce an interesting problem, do developers
fix their own bugs differently?

<!-- 75-->

## 3

So to investigate this problem, we use the SStuBs dataset which is a collection
of single statement bugs that are fixed by modifying a single statement in the
code base.

The dataset itself only contains the bug fix location its last appearance. We
use this information to extract the bug induce commit using an adapted SZZ
algorithm to work with *Git*.

<!-- 69-->

## 4

In *Git*, bug fix commits sometimes are only introduced to the master or now
preferred main branch when they are merge from another branch. 

When this happens, there are two key events, first, when the bug fix change is
made in a commit, and the other is when the bug fix commit is merge into the
code base.

In our work, we use the bug fix commit to determine the author of the bug fix.
Since often, the merge is done by another developer.

<!-- 91-->

## 5

We focus on two metrics when investigating whether developers fix their own
simple bugs differently. How long did it take to fix the bug and how large is
the bug fix. 

We consider the bug fixing time from the project's perspective. So the time is
determined by when the bug is introduced to the project and when the bug fix is
merged in to the project. 

We had to diverge a little bit from the common way of calculating commit size
since the majority of simple bug fixes only modify the lines and results in
a net change of zero lines. So instead, we use the total number of added and
removed lines as the size of the bug fix.

<!-- 95-->

## 6

First, let's look at how often are single statement bugs fixed by the same
author.

In the SStuBs dataset, about half of the bug fixes are done by the same author.

<!-- 52-->

## 7

Now, let's look at the bug fixing time. 

Single statement bug fixes by a different author spans a wide range. These bugs
are probably fixed as they are discovered down in the line.

On the other hand, most single statement bug fixes by the same author happen
within the day the bug is introduced!

<!-- 51-->

## 8

So, what about the fix size then.

There's also a large difference! As you can see here, single statement bug
fixes by different developers are small with most of the bug fixes between
2 and 13 lines.

At the same time, commits containing simple bug fixes by the same developer can
be very large.

<!-- 71-->

## 9

Our observations suggests these effects might come from the different
underlying development patterns.

While some simple bug fixes occur in the development process where it happens
immediately and is embedded in a larger commit. 

Other simple bugs are discovered later in the project life time and are fixed
by another developer.

<!-- 57-->

## 10

And that wraps up the presentation. Thank you for coming.

<!-- 10-->
