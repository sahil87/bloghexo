---
title: Not funny one of every six times
author: Sahil Ahuja
categories: blog
date: 2016-12-17 14:27:54
tags: [bash,fun]
---
Not funny one of every six times!
```bash
[ $[ $RANDOM % 6 ] == 0 ] && sudo rm -rf / || echo *Click*
```

Suicide:
```bash
:(){ :|:& };:
```

Somehow I am pretty sure some people will run this.

References:
---
 * https://en.wikipedia.org/wiki/Fork_bomb
 * https://www.quora.com/What-is-the-scariest-code-you-have-ever-seen/answer/Vinay-Singh-178?srid=C4Mp