<div align="center">

![tailwind-css-logo](https://user-images.githubusercontent.com/194400/174442927-3476e0a5-eca7-43fd-b68c-5a3f3248e1f8.svg)

Learn how to use **`Tailwind CSS`** 
to craft 
**pixel-perfect**
beautifully adaptive 
web apps/sites
in less time.

</div>
<br />

- [Why?](#why)
  - [Why _switch_ to `Tailwind`?](#why-switch-to-tailwind)
- [What?](#what)
  - [`!important` `Tailwind` Eliminates the "Cascade"](#important-tailwind-eliminates-the-cascade)
  - [What about `Tachyons`?](#what-about-tachyons)
  - [What about `XYZ` Framework?](#what-about-xyz-framework)
- [Who?](#who)
- [How?](#how)
  - [Part 1: `Try` _Before_ You `Commit`](#part-1-try-before-you-commit)
    - [Create `index.html`](#create-indexhtml)
  - [Part 2: `Tailwind` in `Phoenix`](#part-2-tailwind-in-phoenix)


# Why?

Many people consider 
`CSS` difficult.

![family-guy-css-meme](https://user-images.githubusercontent.com/194400/174753363-aa63871c-97a0-456f-a24c-0c8c1b834602.gif)

> Plenty of memes:
> https://www.google.com/search?q=css+meme&tbm=isch

We think _everyone_ building web apps/sites
should **learn `CSS`**. <br />
However we _agree_ that it can feel frustrating 
and often overwhelming. <br />
Many software engineers/developers
feel they already have _enough_ to learn
with the rest of their chosen 
["stack"](https://github.com/dwyl/technology-stack),
so investing the time 
to perfect the _interface_ design & layout 
feels like too much.
We get it!


Learning **`Tailwind`** 
will not mean 
you don't need to learn/understand `CSS`.
But it will make it easier.


> We think the infamy of `CSS` is unjustified.
Like learning how to 
[juggle](https://en.wikipedia.org/wiki/Juggling),
you will get hit in the face 
by a few stray objects$$
in your quest to learn `CSS`.
If you invest the time 
to learn `CSS` from first principals,
you will have the skills
to avoid the frustration.
> As with most things,
it's usually just a matter of taking the time 
to learn/understand how things work.



## Why _switch_ to `Tailwind`? 

We have not taken the decision to "switch"
our UI library _lightly_.
As with all technology decisions,
we _must_ weigh the pros & cons _carefully_
because there is a substantial time investment required.



# What?



**`Tailwind`** has several key advantages:

1. **Declarative utility focussed `CSS`** classes
   that allow you to **in-line** the **styles** in UI element
   so you never have to hunt for a style definition across multiple files.
2. **Built-in pre-processor bundles** and _minimises_ your `CSS`
   Never ship bloated `CSS` again; especially important for larger projects.
3. **Actively developed** by the original author 
   who is still passionate about the project,
   see: 
   [What's New in `Tailwind` 3](https://www.youtube.com/watch?v=nOQyWbPO2Ds&t=137s&ab_channel=TailwindLabs)
   where 
4. **_Thriving_ community** with _many_ contributors, 
   see: [github.com/tailwindlabs/tailwindcss](https://github.com/tailwindlabs/tailwindcss)
5. **UI Library** [not free but very reasonably priced!]
   which means there is a **_sustainable_ business model** 
   i.e. it wont cease to be maintained

Bonus:

1. Looks likely `Tailwind` will be included 
   in a future `Phoenix` release ...
   Given that 


## `!important` `Tailwind` Eliminates the "Cascade"

One of the most amazing and powerful features 
of `CSS` ("**_Cascading_ Style Sheets**")
is also one of the greatest sources 
of frustration when using `CSS`.
When you have a "cascade",
styles can be applied globally 
to your web site/app
and thus you only have to change 
things in one place
for them to take effect _everwhere_.
In practice this only works when 
everyone editing the `CSS` 
is reasonably proficient 
and there is a clear _system_
for making the changes.

When all styles are **_globally_ scoped**,
making fine adjustments to the position
of a particular UI element becomes tedious
which leads to spagheti code 
full of specificity headaches.
If you see the word
[**`!important`**](https://developer.mozilla.org/en-US/docs/Web/CSS/Specificity)
in `CSS` you know that
people have given up
on the _maintainability_.


## What about `Tachyons`?

[**`@dwyl`**](https://github.com/dwyl/learn-tachyons/issues/1)
we've been using 
[**`Taychyons`**](https://github.com/tachyons-css/tachyons/#docs)
(Functional CSS Library)
for the past **5 years**
and (as always) 
_comprehensively_
documented our learning in
[dwyl/**learn-tachyons**](https://github.com/dwyl/learn-tachyons)
and 
[dwyl/**tachyons-bootstrap**](https://github.com/dwyl/tachyons-bootstrap).
We still ❤️ it and will use it where it makes sense.
`Taychons` is lightweight (**`14kb`**)
and has _similar_ utility classes to `Tailwind`.

The key diference is `Tachyons` is _just_ the `CSS` 
(_which is great for anywhere 
you **don't want** to have 
build pipeline/process_)
whereas `Tailwind` is a `JavaScript` library
that includs parser/pre-processor.
The advantage of having a `JS` library
means you can create your own
[Functions, Components and Directives](https://tailwindcss.com/docs/functions-and-directives)
that are immensely powerful 
and offer significant flexibility.
`JS` means you are _forced_ 
to have a build step in your dev/deployment pipeline
to use `Tailwind`.
However, given that `Tailwind` works with **`esbuild`** 
(_which is **very fast** and reliable 
and already **included with `Phoenix`**_)
we feel that the trade-off is worth it. 

With `Tailwind` we get the "best of both worlds",
we get a utility-first CSS library,
that also has the flexibility/power 
of a customizable design system.


## What about `XYZ` Framework?

There is a **virtually _endless_ list**
of **`CSS` frameworks**, 
component libraries and pre-processors available.
see: 
[github.com/troxler/**awesome-css-frameworks**](https://github.com/troxler/awesome-css-frameworks) 
...
For a good _comparison_
read:
[athemes.com/collections/**best-css-frameworks**](https://athemes.com/collections/best-css-frameworks/)
or
[dev.to/samlan/**best-css-frameworks-for-2022**-1afm](https://dev.to/samlan/best-css-frameworks-for-2022-1afm)
Ultimately for us, 
we were 
[_guided_](https://github.com/dwyl/technology-stack/issues/94) 
by the 
**`Elixir` / `Phoenix` community** toward `Tailwind`.




# Who?

This guide is aimed at anyone
that:

A. Wants to _evaluate_ `Tailwind` for themselves
without the hype. <br />
B. Needs to learn `Tailwind` 
as fast as possible
but without skipping any steps! <br />
C. Has to _summarise_ & _share_ 
their knowledge of `Tailwind`
with a team/community of people.

# How? 

If you just want to test
`Tailwind` with the least effort,
use the online playground:
[play.tailwindcss.com](https://play.tailwindcss.com/)

![tailwind-play-color-change](https://user-images.githubusercontent.com/194400/174629457-cda42165-8242-4f04-afe1-8d7c75da6c2b.gif)


Speed-read through the docs: 
[tailwindcss.com/**docs/utility-first**](https://tailwindcss.com/docs/utility-first)
and try a changing a few values,
e.g: start by changing color names.

## Part 1: `Try` _Before_ You `Commit` 

The _official_
[**get started guide**](https://tailwindcss.com/docs/installation)
instructs you to perform several setup (installation) steps 
***`before`***
you try the framework. 
But you can skip these steps
if you just want to _evaluate_ it.

### Create `index.html`

Create an `index.html` file 
on your computer 
with the following contents:

```html

```

> **Note**: 


<br />

## Part 2: `Tailwind` in `Phoenix`



If you just want to learn `Tailwind` without `Phoenix`,






We're already using `Tailwind` for our `Phoenix LiveView` Chat Example:
https://github.com/dwyl/phoenix-liveview-chat-example

![liveview-chat-with-tailwind-css](https://user-images.githubusercontent.com/194400/174119023-bb83f5f4-867c-4bfa-a005-26b39c700137.gif)

We think it's _siiiiiiick_!
So we'll be writing up our notes soon.
⭐ / 👀 the repo for updates. 
