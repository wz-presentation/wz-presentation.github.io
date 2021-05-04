# Speech draft

Time limit is 3 minutes. Base on some research on public speech, 100~150 wpm is
a good pace for presentations.

## 1

Hi, everyone, thank you for coming to the talk. My name is Wenhan and I go by
Cosmos. Today, I'll talk about the project with my supervisor Mike on

> Mea culpa, how developers fix their own simple bugs differently from other
> developers.

<!-- 44-->

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

So to investigate this problem, we look at the SStuBs dataset which is
a collection of single statement bugs. Single statement bugs here means bugs
that are fixed by modifying a single statement in code.

We start with the dataset which only contains the bug fix location and the last
commit where the bug is still present. Then, we use the information to trace
when the bug is introduced.

<!-- 69-->

## 4

We achieved this by adapting the original SZZ algorithm to work with *Git*.
When developing using *Git*, bug fix commits sometimes are only introduced to
the master or now preferred main branch when they are merge from another
branch. 

When this happens, there are two key events, first is the commit where the bug
fix change happen and the other is the commit where the bug fix change is
integrated to the main branch.

In our work, we use the bug fix commit to determine the author of the
bug fix.

<!-- 91-->

## 5

More specifically, we investigate the difference between same author and
different author bug fixes by fix time and size.

For bug fixing time, since we are interested from the project's perspective, so
we measure the time difference between the bug is introduced to the project and
bug fix change is made in to the project.

Due to the natural of single statement bugs, the intuitive way of calculating
the churn by the net change will often result in zero. So we use the sum of
number of added and removed lines to measure code churn.

<!-- 95-->

## 6

So first, let's look at how often are single statement bugs fixed by the same
author.

From the SStuBs dataset, about half of the bug fixes are done by the same
author. In other words, it is also quite common for a single statement bug to
be fixed by a different author.

<!-- 52-->

## 7

Now, let's look at bug fixing time. 

Single statement bug fixes by a different author spans a wide range. So it
seems like, these bugs fixed as they are discovered.

On the other hand, most single statement bug fixes by the same author happen
within the day the bug is introduced!

<!-- 51-->

## 8

So, what about the fix size then.

There's also a large difference! As you can see here, single statement bug
fixes are very small and most of them are in a small range, between 2 and 13
lines to be exact.

At the same time, bug fixing changes by the same author can be very large with
over a quarter of the bug fixes containing changes of larger than 700 lines.

<!-- 71-->

## 9

Our study suggests that these bug changes might be results from the underlying
development patters.

Where same author bug fixes are done quickly after the bug is introduced and
often embedded in a larger commit.

Meanwhile, bug fixes by a different author occurs later in the project life
time and often only contain the bug fix itself.

<!-- 57-->

## 10

And that wraps up the presentation. Thank you for coming.

<!-- 10-->
