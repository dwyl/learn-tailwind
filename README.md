<div align="center">

![tailwind-css-logo](https://user-images.githubusercontent.com/194400/174442927-3476e0a5-eca7-43fd-b68c-5a3f3248e1f8.svg)

Learn
**`Tailwind CSS`**
to craft
**pixel-perfect**
beautifully adaptive
web apps/sites
in less time.

![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/dwyl/learn-tailwind/ci.yml?label=build&style=flat-square&branch=main)
[![codecov.io](https://img.shields.io/codecov/c/github/dwyl/learn-tailwind/main.svg?style=flat-square)](https://codecov.io/github/dwyl/learn-tailwind?branch=main)
[![npm package version](https://img.shields.io/npm/v/tailwindcss.svg?style=flat-square)](https://www.npmjs.com/package/tailwindcss)
[![Hex.pm](https://img.shields.io/hexpm/v/phoenix?color=brightgreen&style=flat-square)](https://hex.pm/packages/phoenix)
[![contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat-square)](https://github.com/dwyl/learn-tailwind/issues)
[![HitCount](https://hits.dwyl.com/dwyl/learn-tailwind.svg)](https://hits.dwyl.com/dwyl/learn-tailwind)

</div>
<br />

Use these links to skip stright to the section that interests you:

- [Why?](#why)
  - [Why _Switch_ to `Tailwind`?](#why-switch-to-tailwind)
- [What?](#what)
  - [Top 10 Reasons We _Love_ **`Tailwind`**](#top-10-reasons-we-love-tailwind)
  - [`!important` `Tailwind` Eliminates the "Cascade"](#important-tailwind-eliminates-the-cascade)
  - [What about `Tachyons`?](#what-about-tachyons)
  - [What about `XYZ` Framework?](#what-about-xyz-framework)
  - [`Tailwind` in `Phoenix`](#tailwind-in-phoenix)
- [Who?](#who)
- [How?](#how)
  - [Part 1: `Try` _Before_ You `Commit`](#part-1-try-before-you-commit)
    - [Create `index.html`](#create-indexhtml)
  - [Colors!](#colors)
  - [Part 2: `Tailwind` in `Phoenix`](#part-2-tailwind-in-phoenix)
    - [Build Log (How we got here)](#build-log-how-we-got-here)
    - [More Detailed Example!](#more-detailed-example)
    - [Petal Components](#petal-components)

# Why?

Many people consider
[`CSS`](https://developer.mozilla.org/en-US/docs/Learn/CSS/First_steps/What_is_CSS)
difficult.

![family-guy-css-meme](https://user-images.githubusercontent.com/194400/174753363-aa63871c-97a0-456f-a24c-0c8c1b834602.gif)

> Plenty of memes:
> [google.com/search?q=**css+meme**](https://www.google.com/search?q=css+meme&tbm=isch)

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
But it will make it
**a _lot_ easier**.

> We think the infamy of `CSS` is unjustified.
> Like learning how to
> [juggle](https://en.wikipedia.org/wiki/Juggling),
> you will get hit in the face
> by a few stray objects
> in your quest to learn `CSS`.
> If you invest the time
> to learn `CSS` from first principals,
> you will have the skills
> to avoid the frustration.
> As with most things,
> it's usually just a matter of _making_ the time
> to learn/understand it.

## Why _Switch_ to `Tailwind`?

We have not taken the decision to _switch_
our UI library _lightly_.
As with all
[technology decisions](https://github.com/dwyl/technology-stack),
we _must_ weigh the pros & cons _carefully_
because there is a substantial time investment required.

We felt (still feel)
that the benefits of switching
(outlined below)
justify the cost -
learning time, updating code & maintenance.

We encourage you to read through this doc
and make up your own mind
if `Tailwind` is a good fit
for you and your team/project.

# What?

**`Tailwind` CSS**
is a utility-first CSS framework
that can be composed to build any design,
directly in your markup. ~
[**tailwindcss.com**](https://tailwindcss.com/)

> 💡 **Tip**: Read through the **`Tailwind` landing page**,
> it summarises the benefits very well.

**In-line styles**
directly in a UI element
so you never have to hunt
for a style definition across multiple files.
It means you don't suffer
the change-one thing
breaks many others pain
of traditional `CSS`.

This is a **_huge_ time saver**
even in a modest sized project.

## Top 10 Reasons We _Love_ **`Tailwind`**

1. **_Declarative_ utility focussed `CSS`** classes
   that allow you to **_locally_ scope**
   all presentation
   and avoid polluting the _global_ space.
2. **_Logical_ numeric property increments**
   mean it's **_immediately_ obvious** from reading
   the **`class`** **`bg-red-500`** `#ef4444` in your **`HTML`**
   that the background is red and the intensity is **`500`**  
   (on the scale 0-1000) 
   and therefore _logically_ the "hover background red 700"
   **`hover:bg-red-700`** `#b91c1c`
   is a deeper red.
   See: [Colors](#colors) section below.
3. **_Flexible_ function-like class names**
   let you define _precise_ values for attributes
   like `position`, `padding`, `margin`
   e.g: `m-[5px]` or `m-[2%]`
   when you need a very specific pixel dimension
   or a specific percentage.
   see:
   [tailwindcss.com/docs/margin#**arbitrary-values**](https://tailwindcss.com/docs/margin#arbitrary-values)
   This is a _huge_ improvement over being stuck with pre-defined values!
   Consider this compound class to create a 
   [gradient](https://tailwindcss.com/docs/gradient-color-stops): <br />
   `bg-gradient-to-r from-green-400 to-blue-500`<br />
   ![tailwind-gradient-demo](https://user-images.githubusercontent.com/194400/179341516-111598ad-4f26-4651-a70d-db57f0bcb601.png) <br />
   Even a complete beginner can _infer_ 
   what these 3 classes are doing: <br />
   "_Background gradient to right,_
   _from green level 400_ `#4ade80`, 
   _to blue level 500_ `#0ea5e9`". <br />
   > **Note**: Obvs we don't do this in _practice_, but it shows the power! 🌈
4. **_Superb_ visual documentation** with easy two-way search;
   lookup the `CSS` attirbute or `Tailwind` class 
   with _auto-completion_
   makes finding what you need _very_ fast!
5. **Built-in pre-processor bundles**
   and **_minimises_ your styles**
   so you never ship bloated `CSS` again;
   _especially_ important for larger projects.
6. **_Actively_ developed** by the original author
   who is
   [working _full_-time](https://adamwathan.me/going-full-time-on-tailwind-css/)
   and still passionate about the project,
   see:
   [What's New in `Tailwind` v3.1](https://www.youtube.com/watch?v=nOQyWbPO2Ds&t=137s&ab_channel=TailwindLabs)
   where the creator
   [Adam Wathan](https://adamwathan.me)
   summarises recent improvements.
7. **_Thriving_ community** with _many_ contributors
   and frequent improvements,
   see: [github.com/tailwindlabs/tailwindcss](https://github.com/tailwindlabs/tailwindcss)
8. **UI Library** [not free but very reasonably priced!]
   which means there is a **_sustainable_ business model**
   i.e: it wont cease to be maintained
   because the creator is getting paid to do it full-time.
9. **Free _complete_ themes, UI components/kits & resources**
   to kick-start your project.
   e.g:
   [tailwindtoolbox.com](https://www.tailwindtoolbox.com)
   ![tailwindtoolbox](https://user-images.githubusercontent.com/194400/174825181-04c74957-4f69-4c9f-9290-d297051eeee5.png)
10. Please add yours here!! 🙏

## `!important` `Tailwind` Eliminates the "Cascade"

One of the most amazing and powerful features
of `CSS`
(["**_Cascading_ Style Sheets**"](https://en.wikipedia.org/wiki/CSS))
is also one of the greatest sources
of _frustration_ when using it in _practice_.
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
[dwyl/**tachyons-bootstrap**](https://github.com/dwyl/tachyons-bootstrap). <br />
**`Tachyons`** preceeds **`Tailwind`**
by 3 years - inital release 2014 vs. 2017 -
so you could even say that one _inspired_
or layed the
[groundwork](https://en.wiktionary.org/wiki/lay_the_groundwork)
for the other.
We still ❤️ `Tachyons` and will use it where it makes sense.
**`Tachyons`** is lightweight (**`14kb`**)
and has **_very similar_ utility classes** to **`Tailwind`**;
we consider the two **_almost_ interchangeable**.
We won't be updating any of the projects that use **`Tachyons`**
to use **`Tailwind`** because none of them are "broken",
require zero maintenance and work well as-is!

The key diference is
approach taken to building the library.
`Tachyons` is _just_ the `CSS`
(_which is great for anywhere
you **don't want** to have
build pipeline/process_)
whereas `Tailwind` is a `JavaScript` library
that includes parser/pre-processor.

The _advantage_ of having a **`JS` library**
means you can create your own
[Functions, Components and Directives](https://tailwindcss.com/docs/functions-and-directives)
that are immensely powerful
and offer significant flexibility.

`JS` means you are _forced_
to have a build step in your dev/deployment pipeline
to use `Tailwind`.
However, given that `Tailwind` works with
[**`esbuild`**](https://esbuild.github.io/)
(_which is **very fast** and reliable
and already **included with `Phoenix`**_)
we feel that the trade-off is worth it.

With **`Tailwind`** we get the
["best of both worlds"](https://dictionary.cambridge.org/dictionary/english/best-of-both-worlds),
we get a utility-first CSS library,
that also has the flexibility/power
of a **_customizable_ design system**.

## What about `XYZ` Framework?

There is a **virtually _endless_ list**
of **`CSS` frameworks**,
component libraries and pre-processors available. <br />
see:
[github.com/troxler/**awesome-css-frameworks**](https://github.com/troxler/awesome-css-frameworks)
... <br />
For a good _comparison_
read:
[athemes.com/collections/**best-css-frameworks**](https://athemes.com/collections/best-css-frameworks/)
or
[dev.to/samlan/**best-css-frameworks-for-2022**-1afm](https://dev.to/samlan/best-css-frameworks-for-2022-1afm)

Ultimately for _us_,
we did our own research into the available alternatives
but kept an open mind.
We were
[_guided_](https://github.com/dwyl/technology-stack/issues/94)
by the
**`Elixir` / `Phoenix` community** toward **`Tailwind`**
and we have not been disapointed.

## `Tailwind` in `Phoenix`

As of `Phoenix 1.7`,
`Tailwind` is now included by `default`.
We 
[called it](https://github.com/dwyl/learn-tailwind/tree/25a08d3bbd976e76ae1c0ce631d72f18b5062fd4#tailwind-in-phoenix)
last year.
And we're _delighted_ our investment payed off!

<br />

# Who?

This guide is aimed at anyone
that:

**A.** Wants to **_evaluate_ `Tailwind`** for themselves
or their team without the hype/noise. <br />
**B.** Needs to **learn `Tailwind`**
as **_fast_ as possible**
but without skipping any steps! <br />
**C.** Has to **_summarise_ & _share_**
their knowledge of `Tailwind`
with a team/community of people.

> If you find this useful,
> please ⭐ on GitHub
> to let us and others know.
> Thanks! 🙏

# How?

If you just want to test
`Tailwind` with the least effort,
use the online playground:
[play.tailwindcss.com](https://play.tailwindcss.com/)

![tailwind-play-color-change](https://user-images.githubusercontent.com/194400/174629457-cda42165-8242-4f04-afe1-8d7c75da6c2b.gif)

Speed-read through the docs:
[tailwindcss.com/**docs/utility-first**](https://tailwindcss.com/docs/utility-first)
and try a changing a few values,
e.g: start by changing 
[solors](#colors)
names/levels.

## Part 1: `Try` _Before_ You `Commit`

The _official_
[**get started guide**](https://tailwindcss.com/docs/installation)
instructs you to perform several setup (installation) steps
**_`before`_**
you try the framework.
But you can skip these steps
if you just want to _evaluate_ it.

### Create `index.html`

Create an `index.html` file
on your computer
with the following contents:
https://raw.githubusercontent.com/tailwindtoolbox/Admin-Template/master/index.html

Open the file in your web brower,
you should see
something similar to:

![admin-dashboard-example](https://user-images.githubusercontent.com/194400/174832000-4ac4e3ee-9e76-4fcc-80d7-6a8cdb72aa8b.png)

Once you've made a few changes
in the `index.html` file
and seen the results
in your web browser,
you should have a decent idea
of the power of `Tailwind`.

If you have a decent Internet connection
and no bandwidth constraints,
we recommend watching
Designing with Tailwind CSS: The Utility-First Workflow:
[https://youtu.be/Ybybd3GCNn4](https://www.youtube.com/watch?v=Ybybd3GCNn4&list=PL7CcGwsqRpSM3w9BT_21tUU8JN2SnyckR&index=2)

[![Designing with Tailwind CSS](https://user-images.githubusercontent.com/194400/175198147-10656a1b-53e2-4061-b1f1-d27bc32dee08.png)](https://www.youtube.com/watch?v=Ybybd3GCNn4&list=PL7CcGwsqRpSM3w9BT_21tUU8JN2SnyckR&index=2)

made by
[Adam Wathan](https://adamwathan.me/)
[**`@adamwathan`**](https://github.com/adamwathan)
(Creator of Tailwind)

## Colors!

We are _huge_ fans of the numeric indexing of the built-in colors:
https://tailwindcss.com/docs/customizing-colors
![tailwind-colors](https://user-images.githubusercontent.com/194400/179340012-4dce92f1-b13d-4840-b1f5-77d4c9409f8a.png)

<br />

## Part 2: `Tailwind` in `Phoenix`

To run the _finished_ version of our
**`Tailwind` + `Phoenix` _Demo_**,
run:

```sh
git clone git@github.com:dwyl/learn-tailwind.git && cd learn-tailwind
mix setup
mix phx.server
```

### Build Log (How we got here)

Create a _barebones_ Phoenix App:

```sh
mix phx.new app --no-mailer --no-dashboard --no-gettext --no-ecto
```

Install the dependencies.
Then open the project in your editor.

Run the app:

```
mix phx.server
```

You should see output similar to the following in your terminal:

```sh
Generated app app
[info] Running AppWeb.Endpoint with cowboy 2.9.0 at 127.0.0.1:4000 (http)
[info] Access AppWeb.Endpoint at http://localhost:4000
[debug] Downloading esbuild from https://registry.npmjs.org/esbuild-darwin-64/-/esbuild-darwin-64-0.14.29.tgz
[watch] build finished, watching for changes...
```

That's a good sign, `esbuild` was downloaded
and the assets were compiled successfully.

Visit
[`localhost:4000`](http://localhost:4000)
from your browser.

You should see something similar to the following
(default `Phoenix` homepage):

![phoenix-default-homepage](https://user-images.githubusercontent.com/194400/174807257-34120dc5-723e-4b2c-9e8e-4b6f3aefca14.png)

That's nice. But a bit
[boring ...](https://www.google.com/search?q=boring+meme&source=lnms)
let's add some pizzazz! ✨

Open the `mix.exs` file and add `:tailwind` to `defp deps`:

```elixir
{:tailwind, "~> 0.1.9", runtime: Mix.env() == :dev},
```

Run:

```sh
mix deps.get
```

Once installed,
add the following lines to `config/config.exs`
to pick your tailwind version of choice:

```elixir
config :tailwind,
  version: "3.1.0",
  default: [
    args: ~w(
      --config=tailwind.config.js
      --input=css/app.css
      --output=../priv/static/assets/app.css
    ),
    cd: Path.expand("../assets", __DIR__)
  ]
```

Now you can install the library.
Run the following commands in order.

```sh
mix tailwind.install
mix tailwind default
```
These commands will generate the 
Tailwind CLI and
create a `assets/tailwind.config.js` file.
They will also create an executable
inside `_build/tailwind-TARGET`
where TARGET is your target system architecture.

For development, we want to enable watch mode.
So find the `watchers` section in `config/dev.exs`
and add:

```elixir
tailwind: {Tailwind, :install_and_run, [:default, ~w(--watch)]}
```

> **Note**: this enables the file system watcher.

Ensure that the `import "../css/app.css"` line
is no longer in `assets/js/app.js`
(should have automatically been removed by adding `Tailwind` ...)

Finally, back in your `mix.exs`,
make sure you have a `assets.deploy` alias for deployments,
which will also use the `--minify` option:

```elixir
"assets.deploy": ["tailwind default --minify", "esbuild default --minify", "phx.digest"]
```

Open the `lib/app_web/templates/page/index.html.heex`
and replace the contents with:

```html
<h1
  class="text-7xl text-white font-bold text-center w-full bg-slate-800 rounded-xl shadow-lg py-3 mt-3 ml-3"
>
  Hello TailWorld!
</h1>
```

Run the `Phoenix` App:

```sh
mix phx.server
```

Visit [**`localhost:4000`**](http://localhost:4000)
in your web browser:

![image](https://user-images.githubusercontent.com/194400/174838767-20bf201e-3179-4ff9-8d5d-751295d1d069.png)

Those semantic utility class names should give you a _flavour_
for what to expect in the UI.

Fix the failing tests!

Open `test/app_web/controllers/page_controller_test.exs`
and change the assertion from:

```elixir
assert html_response(conn, 200) =~ "Welcome to Phoenix!"
```

to:

```elixir
assert html_response(conn, 200) =~ "Hello TailWorld!"
```

### More Detailed Example!

We're using `Tailwind` for our `Phoenix LiveView` Chat Example:
https://github.com/dwyl/phoenix-liveview-chat-example

![liveview-chat-with-tailwind-css](https://user-images.githubusercontent.com/194400/174119023-bb83f5f4-867c-4bfa-a005-26b39c700137.gif)

We think it's _siiiiiiick_!
More examples to follow soon!

### Petal Components

<img width="545" alt="petal.build" src="https://user-images.githubusercontent.com/194400/193780264-16a4330d-df64-4f04-9c89-2d6b1146ad32.png">

Petal components are a set of reusable functions to help you build a nice UI:

![image](https://user-images.githubusercontent.com/6057298/193790320-a436dc02-d86f-49d9-9bc2-cfc7d76e4e91.png)


Follow the instructions steps at https://petal.build/components to install the
Petal components to your Phoenix project. After that you'll be able to call in your
templates the components with the syntax `<.component>...</.component>`, for example:

```heex
<.h2>Title</.h2>
```

see: 
- https://petal.build/
- https://hexdocs.pm/phoenix_live_view/Phoenix.Component.html
