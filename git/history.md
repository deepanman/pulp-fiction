# History

It all starts with Linus for Linux… For a decade, the community was contributing via tar balls and patches, which he thinks is much superior than CVS. 

Linus always wanted to use the best tools to get the job done.

From 2002, Bitkeeper, a commercial SCM tool was used for kernel development, which was free to use for open source development and had few other rules.

Three years down the line, one of the contributors, Andrew Tridgell, reverse engineered the bitkeeper protocols and tried to create a tool, which was something offered by bitkeeper for commercial licensing. 

Larry McVoy is the CEO of BitMover, the company that makes BitKeeper. On license violation, they revoked access for all Linux users.

Linus wanted to find an alternate SCM, which will support these parameters:

    Should be distributed
    Should be performant
    Guarantee's what’s put in comes out
    D0 the exact opposite of CVS, the tool which he hated so much with passion!

On 6 April 2005, he wrote to the kernel mailing list that he’s taking time off to figure out the alternative and recommends his team to look into monotone (SCM) mail archive: https://lwn.net/Articles/130681/ 

On 7 April 2005, he wrote that monotone wasn't performant and he created the tool, GIT, all by himself and this to the kernal mailing list.

> The first one to send me the changelog tree of sparse-git (and a tool to commit and push/pull further changes) gets a gold star, and an honorable
mention. I've put a hell of a lot of clues in there (*).
I've worked on it (and little else) over the last two days. Time for somebody else to tell me I'm crazy.
Mail Archive: https://lwn.net/Articles/131312/

On 8 April 2005,
> The git could commit itself using git. Initial commit 

> First commit - https://github.com/git/git/tree/e83c5163316f89bfbde7d9ab23ca2e25604af290

## Git Man page

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

## Junio Hamano

Junio C Hamano now works at Google. He’s the maintainer of Git since 26 July 2005. Git 1.0 released in the same year’s December.


Linus Torvalds said in 2012 that one of his biggest successes was recognizing how good a developer Hamano was on Git, and trusting him to maintain it. [6]
 
## Timeline

https://www.atlassian.com/git/articles/10-years-of-git