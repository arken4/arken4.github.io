---
layout: post
title: Building Front-matter Parser
---

A few days ago, I tried to build a static site generator from scratch using JS and Deno. While there is [already one available for use](https://deno.land/x/pagic), I want to understand how static site generator works. I believe by building a simple static site generator myself, I will understand it better.

The project started well until I need a markdown parser. One of the requirements of the engine is a markdown parser, which I happily announce that Deno has a [third-party module](https://deno.land/x/markdown) available. There's a catch, though: it doesn't support front-matter parsing, which I need for parsing metadata from a markdown document.

Yesterday, I tried to find a way out for parse front-matter out of the document. I have an idea to find some font-matter parser packages. But the idea itself turned down quickly as those packages have dependencies, and the dependencies itself have dependencies, and the dependencies' dependencies have dependencies, and so forth. I'm not saying it's impossible to make this package running on Deno. It's just not worth it for my project.

Another idea came in. It suggests that I need to build the parser on my own on top of Deno's module. Not a bad idea, but I'll see what I can do.