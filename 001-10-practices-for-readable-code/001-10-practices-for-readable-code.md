Written by [**Jason McCreary**](https://jasonmccreary.me/) - [original version](https://jasonmccreary.me/articles/practices-write-readable-code-less-complex/)

Translated and adapted by [**Bruno Bandeira**](https://brunobandeira.me/)

# 10 practices for readable code

I've been writing code for 20 years. During that time I've worked with 17 teams coding different languages to build hundreds of projects. These include everything from a simple blog site, to **[APIs](https://jasonmccreary.me/articles/why-i-leave-a-job/)** supporting 3,000 requests/second, to **[top selling apps](https://jasonmccreary.me/articles/successful-app-fail/)**.

From these experiences, combined with **[the books I've read](https://jasonmccreary.me/articles/the-reading-list/)**, it's become apparent to me what matters most in code: **readability**.

On the surface, readability may seem subjective. Something which may vary between languages, codebases, and teams. But when you look underneath, there are core elements within all code which make it readable.

Many programmers are too close to the computer. If the code runs, nothing else matters. Although a common defense it removes all of the human elements from what we do.

Over the last several months I've worked to distill these elements into 10 practices for writing code with a focus on improving readability and decreasing complexity. I've written about these in detail and applied them to real-world code snippets in **[BaseCode](https://basecodefieldguide.com/)**.

Many will unfortunately dismiss these as too trivial. Too fundamental. But I assure you, every bit of bad code I've encountered has failed to apply these practices. And every bit of good code you find one, if not many, of these practices.

## Formatting
So much energy is wasted on formatting. Tabs versus spaces. Allman versus K&R. You'll reach a point where you realize formatting is **not what matters** in programming. Adopt a standard format, apply it to the codebase, and automate it. Then you can refocus that energy on actually writing code.

## Dead code
All those commented blocks, unused variables, and unreachable code are rot. They effectively say to the reader, "I don't care about this code". So a cycle of decay begins. Over time this dead code will kill your codebase. It's classic **[Broken Windows Theory](https://en.wikipedia.org/wiki/Broken_windows_theory)**. You must seek and destroy dead code. While it doesn't need to be your primary focus, always be a **[Boy Scout](https://jasonmccreary.me/articles/are-you-a-boy-scout/)**.

## Nested code
The foundation of nearly all code is logic. We write code to make decisions, iterations, and calculations. This often results in branches or loops which create deeply nested blocks of code. While this may be easy to track for a computer, it can be a lot of mental overhead for a human. As such, the code appears complex and unreadable. Unravel nested code by using guard clauses, early returns, or aspects of functional programming.

## Using objects
Despite the current era of Object Oriented Programming, we still have **[Primitive Obsession](https://blog.codinghorror.com/code-smells/)**. We find this in long parameter lists, data clumps, and custom array/dictionary structures. These can be refactored into objects. Doing so not only formalizes the structure of the data, but provides a home of all that repeat logic which accompanies the primitive data.

## Big Blocks
While I don't adhere to hard numbers, code blocks can reach a critical length. When you determine you have a big block of code, there's an opportunity to recognize, regroup, and refactor the code. This simple process allows you to determine the context and abstraction level of the code block so you can properly identify the responsibilities and refactor the code into a more readable and less complex block.

## Naming
Sure, naming things is hard. But only because we make it hard. There's a little trick which works well with many things in programming, including naming - deferral. Don't ever get stuck naming something. Just keep coding. Name a variable a sentence if you must. Just keep coding. I guarantee by the time you complete the feature or work a better name will have presented itself.

## Removing Comments
This single practice was the original game changer for me. It's what put me on the path of focusing on readability. Despite **[my efforts to explain](https://jasonmccreary.me/articles/removing-comments/)**, there's always at least one person who hates me for it. They have that one example where a comment was absolutely necessary. Sure, when the Hubble telescope telemetry system has to interface with a legacy adapter by return `687` for unknown readings then that may need to be communicated with a comment. But for pretty much everything else, you should challenge yourself to rewrite the code so it doesn't need a comment.

## Reasonable Returns
We return the oddest values for things. Especially for boundaries cases. Values like `-1`, or `687`, or `null`. In turn, a lot of code is written to handle these values. In fact, the creator of `null` calls it **[The Billion Dollar Mistake](https://www.infoq.com/presentations/Null-References-The-Billion-Dollar-Mistake-Tony-Hoare)**. You should aim to return a more reasonable value. Ideally something that allows the calling code to carry on even in the event of a negative path. If there are truly exceptional cases, there are better ways to communicate them than `null`.

## Rule of Three
Think of a mathematical series of numbers. I provide you with the number `2` and ask, "What's next?" Maybe it's `3` or `4`, but maybe it's `1` or `2.1`. In reality you have no idea. So, I provide another number in the series `2, 4` and ask, "What's next?" Maybe it's `6` or `8` or `16`. Again, despite our increased confidence we don't really know. Now I provide another number in the series `2, 4, 16` and ask, "What's next?" Now with three data points our programmer brains see the squared series and determine the next number to be `256`. That's the *Rule of Three*.

The example demonstrates without distracting us with code that we shouldn't predetermine an abstraction or design right away. The Rule of Three counteracts our need to fight duplication by deferring until we have more data to make an informed decision. In the **[words of Sandi Metz](https://www.sandimetz.com/blog/2016/1/20/the-wrong-abstraction)**, *"duplication is far cheaper than the wrong abstraction."*

## Symmetry
Now for the final practice and one which gives any bit of code that lasting touch of near poetic readability - symmetry. This is pulled straight from Kent Beck's **[Implementation Patterns](https://www.amazon.com/Implementation-Patterns-Kent-Beck/dp/0321413091)** which simply states:

> Symmetry in code is where the same idea is expressed the same way everywhere it appears.

This is easier said than done. Symmetry embodies the creative side of writing. It's underlies many of the other practice: naming, structure, objects, patterns. It may vary language to language, codebase to codebase, and team to team. As such, you could spend the term of your natural life pursuing it. Yet, once you start applying symmetry to your code, a **[purer form appears](https://twitter.com/gonedark/status/1041716025862119425)** and the code takes shape quickly

Thank you **JMac** for allowing me to do this.
