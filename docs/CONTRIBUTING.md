<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [Setting up LandingSkeleton locally](#setting-up-landingskeleton-locally)
- [Adding a new section](#adding-a-new-section)
  - [Hook it to an example](#hook-it-to-an-example)
  - [Different kind of sections](#different-kind-of-sections)
  - [Write code for only one section at a time](#write-code-for-only-one-section-at-a-time)
  - [Naming convention](#naming-convention)
  - [Folder and file structure](#folder-and-file-structure)
- [add a README for your section](#add-a-readme-for-your-section)
- [](#)
- [Updating docs](#updating-docs)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

LandingSkeleton has a few guidelines to facilitate your contribution and streamline
the process of getting changes merged in and released.

1. [Setting up LandingSkeleton locally](#setting-up-landingskeleton-locally)
2. [Adding a new section](#adding-a-new-section)
  1. [Different kind of sections](#different-kind-of-sections)
  2. [Naming convention](#naming-convention)
  3. [Folder and file structure](#Folder-and-file-structure)
3. [Updating docs](#updating-docs)


## Setting up LandingSkeleton locally

* For the LandingSkeleton repository.

* `git clone` your fork onto your computer.

* There are no external dependencies, so just run a web server at the root of the project.

## Adding a new section

The strength of the tool lies into the number of section you can combine.
Every suggestion for a new section is warmly welcomed.
Here are a few guidelines when you want to add a new section to the tool.

### Hook it to an example

Before to code a section, you must provide reference the not-yet-existing section into an example_N.html.

This way,

 - User can see an example of your section,
 - You can work, iterate on the section you're working on through a real, working sample.

 For example, see how section_hero_2 is used in example_2.html

### Different kind of sections

There are different kind of sections, with the letter that defines them.

 * **Hero (r)** : The first thing that the user sees when the landing page open. This is by far the most important section.
 * **Nav (n)** : Navigation
 * **ComparisonTable (ct)**: A table where user can notice the unfair advantage you have over his competitors.
 * **Feature (f)**: Just what your service offers.
 * **Callback (w)**: Remind your customer that he can subscribe.
 * **Values (v)**: Numbers and ratios are convincing arguments.
 * **Trust (t)**: Dedicated to build trust with your customer.
 * **Pricing (p)**: Show your customer how much it will cost.
 * **Footer (ft)**: On the bottom of the page.
 * **Separator (s)**: Separates two sections.
 * And any section that you might find useful to increase conversion. Feel free to suggest a name if it doesn't exists in the list above.


### Write code for only one section at a time

 Please not that you **MUST NOT** code two section together. Do not mix a nav section with a hero section, even if it is very tempting. The goal of the tool is to combine sections between them as much as possible, in order to find the highest conversion rate possible. If two sections are linked, this is no more possible.

### Naming convention

Here is the naming convention : name-number. The number is the first available number for the given section.

Example : is there are already 2 hero_section, your new hero section will be name section_hero_3, and css selector must ALL start with .r3- to avoid naming collision.

### Folder and file structure

Folders and files will be as follow :

```
section_hero_3/
├── section_hero_3.css
├── section_hero_3.html
└── README.md
```

Selectors within section_hero_3.css will be for exemple as follow

```
.r3 {
  /* CSS code*/
}
.r3 q {
  /* CSS code*/
}
.r3-heading {
  /* CSS code*/
}
```

Look at section_hero_2 for an example of how things works.

## add a README for your section

It is mandatory to add a README for your section.

###

## Updating docs

wip
