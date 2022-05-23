---
title: "Hugo with GitFx"
date: 2021-12-23T12:26:51Z
author: "B1nj0y"
draft: false
summary: "This blog shows hugo-gitfx shortcode usage by a `hello world` example."
tags: ["git", "gitfx", "actionserverless", "serverless"]
---

Link: [https://gitx.io/post/hugo-with-gitfx/](https://gitx.io/post/hugo-with-gitfx/)

I posted [a message](https://news.ycombinator.com/item?id=26381561) in HackerNews when I'd released [ActionServerless(GitFx)](https://github.com/gitx-io/ActionServerless) early this year. And most of replies criticized that I'm abusing GitHub actions service. Then I emailed GitHub for their attitude, they replied that they don't think that's an abuse as so far.

GitFx can create a service for your developing, testing and learning with the convenience that GitHub actions provides. But I know there's no enough usage of it until now.

I ever thought to create a tool that can be embedded into tech blogs, to show code, run code and display output of code, just as [golang playground](https://go.dev/play/) does. It seems there're a lot of such services at present. I ever created one with docker. But it's a little bit heavy to run so many docker containers.

Now I have GitFx, I realize it's really a nice solution:

1. Use GitFx to run code, and store output to a route.
2. Take Hugo as your blog framework for example, we provide a shortcode to show code and its output in your blogs.

You can create a vivid tutorial blog now! And of course I can't wait to give you one for how to use GitFx with Hugo.

## Hello world

### Set up GitFx in action

We put our code in a folder under root directory, 'app' folder in our example. We create a source file named `hello.py`. We just code a `print("Hello world!")` into it with a GitFx route(a route is a line of comment to define a file path to store output of the code).

We need to set up a GitHub action workflow, the main part of configuration related with GitFx is:

```yml
...
- uses: gitx-io/ActionServerless@master
  with:
    filepath: './app'
...
```

### Show code in your Hugo blog

 We use Hugo shortcode [hugo-gitfx](https://github.com/gitx-io/hugo-gitfx) to show the content of `hello.py` and its output. What you need is just to write one line in your blog:
> \{\{< gitfx "app/hello.py" >\}\}

The code and output showed below is the magic of it:

{{< gitfx "app/hello.py" >}}

You're welcome to have a try if you're a Hugo user!
