+++
title = 'Rant on html5 and h1 in articles'
date = 2024-07-30T19:59:42+03:00
tags = ['dev', 'rant']
draft = false
+++

I was using Firefox's reading mode on my site one day and thought some stuff looked off. Then I remembered: semantic elements. Maybe that's why my site sometimes looks weird in reading mode!

One of the things I did was change some `<div>`s into `<article>`s. I suppose it helped. It made my html look so much better and nicer. That was maybe half a week ago.

{{< toc >}}

## The problem

Today, I edited my [about page](../about) and condensed and freshened it up a bit. I also added table of contents to every page where relevant. Then I noticed something strange: my `<h2>`s were the *exact* same size as the title of the article, which was an `<h1>`.

Perplexed, I went to DuckDuckGo and searched up my problem.

## Some research

I found that someone had [the same question](https://stackoverflow.com/questions/39547412/same-font-size-for-h1-and-h2-in-article) as me on StackOverflow, plus more insight. Turns out, the `<h1>` gets smaller when inside elements like `<article>`, `<aside>`, `<nav>` and `<section>`.

Apparently, someone decided that the `<h1>` should get smaller in visual size as you went down nests of such elements. For each nest, you'd have an `<h1>`. However, having tons of them, all the same size, would be hard to look through. So the `<h1>` would just get smaller.

## Why I hate this

I have no problem with my `<h1>`s getting smaller down each nest. But my question is: *why make it look like the `<h2>`?*

Someone told me that it was better practice to use an `<h1>` for an article title rather than the site title (i.e. don't use an `<h1>` for the title) because the article is considered more important than the site title. Using the same `<h1>` on *every* page diminishes the importance of the most important header.

So I did that. My site title is some random `<p>` tag (as of the time of writing) and my article titles are `<h1>`s. *Except I have `<h2>`s in my articles too and it looks bad*.

Why can't they make the `<h1>` smaller *and* make every other heading look smaller too? Seriously, if you go down the heirarchy enough you could have an `<h1>` that looks like a pathetic `<h6>`.

## What I did

I wanted this site to use as little CSS as possible but without compromising visual design. And right now, visual design took precedence. I needed to make my `<h1>`s look like the most important heading there, as they are. Assert dominance and all that.

So here's what I put:

```css
article h1 {
	font-size: 2em;
	margin: 0.67em 0;
}
```

And yeah, if I didn't change the `margin` too, the `<h1>` would have an awful amount of space that looks pretty ridiculous. Ugh. Gotta add it in too, I guess.

## Just a rant

So yeah. I wish the other headers would, *at the very least*, get smaller too, so people like me who want to reduce on CSS get to reduce on CSS. Who on earth would want an `<h1>` to look like an `<h2>` anyway?
