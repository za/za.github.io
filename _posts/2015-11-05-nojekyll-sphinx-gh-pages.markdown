---
layout: post
title: "Host Sphinx Documentation at GitHub Pages"
date: 2015-11-06 7:17:24
tags: "sphinx github github-pages nojekyll jekyll"
---

Today I released a documentation to which we wrote using 
[sphinx](http://sphinx-doc.org) to [GitHub (project) 
pages](https://help.github.com/articles/creating-project-pages-manually/). After 
did `git push origin gh-pages`, I saw the HTML is not pretty. Later, my friend 
found it was failed loading the CSS.

So this is the solution. Add a 
[.nojekyll](https://daler.github.io/sphinxdoc-test/includeme.html#add-a-nojekyll-file)
file. And voila!

