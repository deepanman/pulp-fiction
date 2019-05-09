# Git History

> It all started with the Big Bang..


> For git it all starts with Linus for Linux…

For a decade, the community was contributing to linux via tar balls and patches, which Linus thinks is much superior than CVS.

He always wanted to use the best tools to get the job done.

From 2002, Bitkeeper, a commercial SCM tool was used for kernel development,
which was free to use for open source development.

Three years down the line, one of the contributors, Andrew Tridgell, reverse engineered the bitkeeper protocols and tried to create a tool with a feature, which was something offered by bitkeeper for commercial licensing.

- Ref: [Linux weekly news](https://lwn.net/Articles/686986/)
- Ref: [Wiki](https://en.wikipedia.org/wiki/BitKeeper)

BitMover, the company that makes BitKeeper, on license violation, they revoked access for all Linux users.

> Linus wanted to find an alternate SCM, which will support these parameters:

- Should be distributed
- Should be performant
- Guarantees what’s put in, comes out
- Do the exact opposite of CVS, the tool which he hated so much with passion!

## **On 6 April 2005**

- Linus writes to the kernel mailing list that he’s taking time off to figure out the alternative and recommends his team to look into monotone (SCM)
  - [mail archive](https://lwn.net/Articles/130681/)

## **On 7 April 2005**

- He replies to Chris Wedgwood that monotone wasn't performant and he created the tool, GIT and asks for support.
  - [Mail Archive](https://lwn.net/Articles/131312/)

> The first one to send me the changelog tree of sparse-git (and a tool to commit and push/pull further changes) gets a gold star, and an honorable
mention. I've put a hell of a lot of clues in there (*).
I've worked on it (and little else) over the last two days. Time for somebody else to tell me I'm crazy.

## **On 8 April 2005**

> The git could commit itself using git.

- [First git commit](https://github.com/git/git/tree/e83c5163316f89bfbde7d9ab23ca2e25604af290)

## GIT meaning

From the GIT man page

```
What is GIT

- The stupid content tracker |  

- Can mean anything, depending on your mood!

- Random three-letter combination that is pronounceable, and not actually used by any common UNIX command! The fact that it is a mispronunciation of "get" may or may not be relevant.

- Stupid. Contemptible, and despicable. Simple! Take your pick from the slang dictionary!

- "Global Information Tracker" - You're in a good mood, and it actually works for you. Angels sing, and a light suddenly fills the room!

- "Goddamn Idiotic Truckload of sh*t" - When it breaks

This is a stupid (but extremely fast) directory content manager. It doesn't do a whole lot, but what it—does—do well is track directory contents efficiently.

```

## New Git Maintainer

Junio C Hamano now works at Google. He’s the maintainer of Git since 26 July 2005. Git 1.0 released in the same year’s December(2005).

Ref: [New Git Maintainer](https://lwn.net/Articles/145123/)

Linus Torvalds said in 2012 that one of his biggest successes was recognizing how good a developer Hamano was on Git, and trusting him to maintain it.
