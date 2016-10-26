---
layout: post
title: "Fail Running Test Code"
date: 2016-10-26 16:56:24
tags: "django test-code python"
---

I was recalling, how did I run the test code. Until I found that I had written
the snippet. I copy-paste it... and the test code was fail. Something wrong. No
changes in the test code since my last commit.

I tried the other test code. Looks OK. I tried to rename the fail test code
filename, still no good. So, what's the problem?

Until I found this [stackoverflow
question](http://stackoverflow.com/questions/25575073/attributeerror-module-object-has-no-attribute-tests).

So, I tried to import the modules written in the test code via shell. Finally
now I know which part of the code that fails to import the library.
