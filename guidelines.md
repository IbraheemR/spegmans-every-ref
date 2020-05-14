---
title: Guidelines
description: This page aims to both provide guidelines for working on this site, and in doing so establish the project's aims. 
author: ibraheem_rodrigues
---

{% include toc.md %}

## Contributing

Contributions are welcome, as long as they fit the style, aims and ethos of this project, detailed here.

If you have any suggestions or issues either submit a [github issue]({{site.github.issues_url}}) or [email me](site.author.email).

If you want to create content for this project, please first read over these guidelines.

You should either:

- Fork this repo, make your changes/additions and then submit a pull request.
- Get in touch using one of the links above

Seed `README.md` for how to run the jekyll site locally.

## Key Terms
All pages should be written in markdown. This site uses [kramdown-flavour markdown](https://kramdown.gettalong.org/) as is standard for Jekyll sites.

These are the key terms, that should be used when referring to parts of the project.

- **Spegman's Every Ref.** (aka 'The Project', 'The Guide', 'The Site')
  - [**Categories**](#categories) - Information groups, defined in `_categories/`
  - **Content** - Everything in the `_content/` folder
    - [**Pages**](#pages) (aka 'Guides')
  - [**Infrastructure** ](#infrastructure) (aka 'The Code') - Anything that is a part of the site, but not directly viewable by the end user


## Categories

Categories are defined with a markdown file in the `_categories` folder.

The name/path of the file will determine the url of the category index page, e.g `misc.md` => `site.com/misc/`.

### Category Template
```md
---
title: Miscellaneous # Mandatory, the name of category
description: Blah blah blah # Optional, will show up on category index page.
---

<!-- Optional content here. Will show up on category index page -->
```

### Current Categories

| Category      | ID            | Description                                                    |
|---------------|---------------|----------------------------------------------------------------|
| Miscellaneous | `misc`        | Anything that does not belong in another category.             |
| Mathematics   | `mathematics` | Math(s) related reference. Geometry, Numbers, Set tTheory etc. |
| Science       | `science`     | Scientific reference - Physics, Chemistry, Biology etc.        |
| Languages     | `language`    | Languages, alphabets and linguistics reference                 |

## Pages

Page files should be under their respective [category](#current-categories) in the `_content` folder, and must include the front matter as defined [below](#page-template).

Files can put in one of two places:
1. `<category_path>/<name>.md` (e.g.`misc/spoons.md`)
2. `<category_path>/<name>/index.md` (e.g. `misc/spoons/index.md`)

File names should seperate words with underscores `_` (snake case)

### Page Template
```md
---
title: Spoons # Mandatory
description: Common and popular spoons # Optional
author: j_spegman # Mandatory
category: misc # Mandatory

redirect_from: # List of pages to redirect to this page from. Used when a page is moved or to link pages with similar names, e.g `/science/glass_colours` redirects from `/science/glass_colors` ([use british english](#standardisation))

image: spoon.png #  Optional, for SEO
---

Spoons come in 3 flavours...
```

### A note on titles

If you have specified a title, on any page, you should not be using `<h1>` elements (`# Title`), so SEO reasons (only 1 `<h1>` should be on each page). There is a simple remedy - simple start immediately with `<h2>`/`## Title` elements.

### Adding media
If you wish to add media to use in a page (images, etc.):
- Use [file structure 2](#structuring-a-page)
- Put media files in the same folder as the page's `index.md`

Media which is used in several pages in a category may be included in the category folder.

### Adding a Table of Contents
To include a table of contents in on page, add the following code at the top, immediately following the front matter.
This will summarise sections of your page in a tree, as denoted by titles/headers. (`<h2>`/`## Subtitle` will be a child of `<h1>`/`## Title`, etc)

{% raw %}
```md
---
# Blah, blah front matter
---

{% include toc.md %}

<!-- Content here -->
```
{% endraw %}


## Writing Guidelines

Guides should be factual and to the point. However this guide is as much about interest as it is about factuality - while all included information must be true, we do not aim to be encyclopedic.

We aim to collect things that are useful, unusual, or tell a story of the human endevour to understand and categorise the world around us.

### Standardisation

For the sake of consistency:

- Spelling should be in **British English**. If words like `colour`/`color` are used in a title, be sure to [redirect from](#page-template) the alternative spelling.
- Use CE/BCE as opposed to AD/BC
- Dates should be in the DD/MM/YYYY format
- Times should be given in 24 hour format (00:00 - 23:59)

### Block Quotes

To quote directly from a source, or elsewhere in the guide, use a block quote:

```md
> To be, or not to be
```

When you give attribution, either link to a source as [below](#citing-sources-and-giving-attribution) or use the following syntax for direct attribution:

```md
> To be, or not to be
>
> *Hamlet by William Shakespeare, Act 3 Scene 1*
```

```md
> To be, or not to be
>
> [*Hamlet by William Shakespeare, Act 3 Scene 1*](http://shakespeare.mit.edu/hamlet/hamlet.3.1.html)
```

### Maths / Chemisty
We use MathJAX to render mathematical equations.
[This](https://mhchem.github.io/MathJax-mhchem/) extension handles chemistry.

Use `$$` to define equations:
```
$$ y = mx + c $$
```

> $$ y = mx + c $$


This works for both inline and block level (automatically detected, note `$...$` is not supported by kramdown):

```
Quadratic equations have the form $$ y = ax^2 + bx + c $$
```

> Quadratic equations have the form $$ y = ax^2 + bx + c $$

To force it to render in the opposite level (inline to block and vicea versa) use `\$$ ... $$`

```
If $$ y = 0 $$ you can find x: \$$ x=\frac{-b\pm\sqrt{b^2-4ac}}{2a} $$
```

> If $$ y = 0 $$ you can find x: \$$ x =\frac{-b\pm\sqrt{b^2-4ac}}{2a} $$

The [LaTeX Wiki](https://en.wikibooks.org/wiki/LaTeX/Mathematics#Symbols) has a good reference for typesetting equations.

### Citing sources and giving attribution
To cite sources or give attribution use kramdown's footnote syntax. This supports both numbered and worded footnotes, however everything will be rendered to numbers. Prefer short descriptive words to numbers, as below

```md
Spoons are most commonly made of steel. [^spoons_website] <!-- Link to footnote -->

Spoons come in many flavours. [^spoons_website] <!-- Use it again-->

[^spoons_website]: [https://spoons.info](https://spoons.info) (Accessed 01/04/2020) <!-- Define the footnote -->
```

#### Citation Templates

```md
<!-- Physical reference -->
[^book]: <Surname>, <Firstname>. <Book title> <Pub date>, p<Page number>. 
<!-- Web reference -->
[^web]: [<Page URL>](<Page URL>) (Accessed <Date>) 
<!-- Media attribution -->
[^image]: [<Image owner>](<Owner or image link>) [<License type>](<License Link>) 

<!-- Examples -->
[^spoon_book]: Spooner, Daniel. Spoons of Northumbria 2004, p42.
[^spoons_website]: [https://spoons.info](https://spoons.info) (Accessed 01/04/2020)
[^spoons_image]: [Andrew Gustar](https://flic.kr/p/djVV3o) [CC BY ND 2.0](https://creativecommons.org/licenses/by-nd/2.0/)
```

See the [kramdown footnote docs](https://kramdown.gettalong.org/syntax.html#footnotes) for more.


## Infrastructure

### Important Files

| Name                | File            | Description                                                       |
|---------------------|-----------------|-------------------------------------------------------------------|
| Home                | `index.md`      | Site homepage.                                                    |
| Guidelines          | `guidelines.md` | Information related to contributing to the reference.             |
| README              | `README.md`     | Information related to developing the technical side of the site. |
| WIP/Planned Content | `wip.md`        | Record of work-in-progress or planned pages                       |


### Adding an author
To add yourself as an author, add an entry to `/_data/authors.yml`, like follows:

```yml
j_spegman:
    name: Jeg Spegman
    email: jeg@speg.info
    url: https://twitter.com/spegman
```

Your name will link to `url` (see top of page)

See the [template](#page-template) for how to add an author to a page.

### Versioning

We aim to follow [Semantic Versioning](https://semver.org/), however as the original specification is not intended for non-code applications, the following guidelines will be used to follow semver's spirit - chiefy to communicate intent.

> Under this scheme, version numbers and the way they change convey meaning about the underlying code and what has been modified from one version to the next.
>
> [*https://semver.org/*](https://semver.org/)

Versions should be tagged with github released on the master branch.

#### Content Related Versioning

Changes to the content of the site (specifically everything under `/_content/`) should increment the version numbers for the following reasons:

`MAJOR.MINOR.PATCH`

- MAJOR - changes which overhaul content/formatting structure
- MINOR - content additions and removals
- PATCH - content updates and fixes (spelling, accuracy, etc.)

**Important notes when changing pages (MINOR changes):**

If a page is moved or marged with another, the new page should redirect from the old page url:

```yml
---
redirect_from: /misc/old_page
---
```

If a page is deleted, a file should be left in its place informing any users of this change.

Whether these temporary pages should be kept after a MAJOR change should be decided on a case by case basis.

## Deploying to netlify

Deploys are triggered by creating a new tag on github. This will trigger a github action to build the site, and deploy it on netlify.