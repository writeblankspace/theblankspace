+++
title = 'Why Python is better than JavaScript'
date = 2021-08-12
tags = ['dev']
draft = false
+++

<!-- meta:
- title: Why Python is better than JavaScript
- template: archive
- date: 12. August 2021
- tags: features, public, python, javascript, development
- img-header: https://i.imgur.com/tw4aQcf.jpg
- img-alt: Photo by Chris Ried on Unsplash
-->

Something a lot of beginners ask. When you begin exposure to the world of programming languages, you'll probably hear JavaScript a lot. Until you hear about another language: Python.

Python is an amazing language. When I was starting out, I tried JavaScript - but Python eventually became more ideal for me, especially since I'm not much into webdev.

{{< toc >}}

## The difference between PY and JS

Python and JavaScript are really similar in many ways. Both languages have been updating and evolving to support what the other has. For example, JavaScript became an object-oriented programming language to par Python.

The biggest flaw about Python was that it didn't really support web development like JavaScript. I've researched a bit on that, and found no easy solution.

If JavaScript and Python are so similar, and Python doesn't support web development, why not just go straight to JavaScript?

JavaScript may be really popular, but so is Python. Many beginners tend to switch from JS to PY for one main reason: Python is simple and easy, and achieves the same things as JavaScript (aside from webdev).

## Assignment

The first thing you'll learn about Python after coming from JavaScript is that it's *dead simple*. In JavaScript, you'll have to know the differences between `let`, `const`, and `var` variables. They have rules as to how they're used and such.

```js
let varOne = foo; // this can be reassigned
const varTwo = bar; // this can only be declared once

function funcOne(x) {
  /* a normal function */
  console.log(x);
}
funcTwo = (x) => {
  /* an arrow function */
  console.log(x);
}

// here's a loop:
const list = ["a", "b", "c"]

for (i = 0; i < list.length; i++) {
  console.log(`${i}: ${list[i]}`)
  /*
  0: a
  1: b
  3: c
  */
}
```

Above are examples of declaring variables and functions in JavaScript, as well as making a loop. Now let's see how that looks in Python:

```py
varOne = foo # can be reassigned
varTwo = bar # and so can this

def funcOne(x):
  """ only one way to make functions """
  print(x)

def funcTwo(x):
  """ it's dead simple """
  print(x)

# here's a loop:
list = ["a", "b", "c"]
increment = 0

for item in list:
  print(f"{increment}: {item}")
  increment += 1
  """
  0: a
  1: b
  2: c
  """
```

In Python, we don't deal with three variable types and long function declarations. Nor do we deal with brackets for our blocks. Nor do we have to put a `;` at the end of *every single line*. And there's the loop - in JavaScript we need to analyse all that `i = 0; i < list.length; i++`, while in Python we just think about looping through each `item` in `list`.

Very simple. Very straightforward.

The best thing about Python is that an ordinary human can read everything without needing a knowledge of code. You won't have to bother about `const` and `let`, and you know that `def funcOne():` would be a function, and the indented block after it will be the function's code. The loop is also *way* easier to understand. Need I say more?

## Blocks

Here's another difference: in JavaScript, we deal with `{}`s for blocks. In Python... we just use `:` and an indent.

```js
func = () => {
  // indented block
}
```

Meanwhile, let's see the Python equivalent:

```py
def func():
  # indented block
  pass
```

In JavaScript, we use brackets to enclose blocks. In Python, we seemingly use nothing except a colon to signify a block.

But something you need to take note is how Python needs indentations for blocks. Not indenting your blocks properly can lead to an error. And if you see that `pass` over there, it means that you aren't allowed to leave blocks empty, like in JavaScript.

By the way, a `pass` statement does literally nothing except get rid of errors from empty blocks.

Looking at the two examples, Python looks a lot neater, without anything unnecessary. We got rid of annoying semicolons as well as brackets!

## Wait, did I blow your mind?

Okay, it seems like I gave you a full, sub-standard lesson on how to go from JavaScript to Python. But long story short, Python is *so* simple. I made the move and ended up writing my bots in Python (rip JavaScript). I hope you do too!

**NOTE 23 Jul 2024: I was an angry teen back when this was written. JavaScript and Python serve different purposes and really, don't yuck anyone's yum. Still, I'm Team Python all the way... although I'll need to learn JavaScript at some point since it would still be very useful.**
