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

Before to code a section, look at section

### Different kind of sections

There are different kind of sections, with the letter that defines them.

 * Hero (r) : The first thing that the user sees when the landing page open. This is by far the most important section.
 * Nav (n) : Navigation
 * ComparisonTable (ct) : A table where user can notice the unfair advantage you have over his competitors.
 * Feature (f) : Just what your service offers.
 * Callback (w) : Remind your customer that he can subscribe.
 * Values (v): Numbers and ratios are convincing arguments.
 * Trust (t): Dedicated to build trust with your customer.
 * Pricing (p): Show your customer how much it will cost.
 * Footer (ft): On the bottom of the page.

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

### a README is mandatory for each section

Each selector must start with the name of the section, to avoid naming collision.

Example : .r3-expla

###

## Updating docs

wip
