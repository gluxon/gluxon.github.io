---
layout: default
title: "Why does GitHub let me commit as other people?"
published: true
---

## Why does GitHub let me commit as other people?

I was investigating an issue on one of my team's repositories today. While I
had never entered my password to complete a Git push, my GitHub account was
appearing along commits I knew others had made.

Looking at the [GitHub documentation](https://help.github.com/articles/setting-your-username-in-githttps://help.github.com/articles/setting-your-username-in-git)
sheds some light on the situation. GitHub uses the `user.email` git config value
to resolve a username. Sure enough, I recalled that one of the public computers
at the team's workplace still had my email set. But wait, does GitHub really
skip verification when pushing?

![](http://i.imgur.com/7XH2TJc.png)

Yes. Yes it does.

To be fair, this does not appear to be a GitHub only issue. I am unsure of how
Git works internally, but I can imagine how verification in this field would
become difficult with pull requests as they show the original author. (And
properly should.) Regardless of how much refactoring might have to be done,
this is an issue that should be fixed for obvious reasons.

And yes, since this is a security opportunity that would be fun to take
advantage of, I present to you a harmless debate among GitHub staff. (Be sure to
look at the commit log!)

[![](http://i.imgur.com/S0h6MsM.png)](https://github.com/gluxon/CommitsFromAnyone/commits/master)