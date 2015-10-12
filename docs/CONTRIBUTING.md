LandingSkeleton has a few guidelines to facilitate your contribution and streamline
the process of getting changes merged in and released.

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**

- [Setting up LandingSkeleton locally](#setting-up-landingskeleton-locally)
- [Adding a new section](#adding-a-new-section)
  - [Don't reinvent the wheel](#dont-reinvent-the-wheel)
  - [Different kind of sections](#different-kind-of-sections)
  - [Write code for only one section at a time](#write-code-for-only-one-section-at-a-time)
  - [Naming convention](#naming-convention)
  - [Folder and file structure](#folder-and-file-structure)
  - [Start and end of file](#start-and-end-of-file)
  - [Things to avoid](#things-to-avoid)
  - [Use of font and typefaces](#use-of-font-and-typefaces)
  - [Use of external dependencies](#use-of-external-dependencies)
- [Run doctoc](#run-doctoc)
- [Make a pull request](#make-a-pull-request)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->


## Setting up LandingSkeleton locally

* For the LandingSkeleton repository.

* `git clone` your fork onto your computer.

* There are no external dependencies, so just run a web server at the root of the project.

## Adding a new section

The strength of the tool lies into the number of section you can combine.
Every suggestion for a new section is warmly welcomed.
Here are a few guidelines when you want to add a new section to the tool.


### Don't reinvent the wheel

Be inspired by an existing section of an existing landing page of an existing company. They already did a great job of creation, so don't suffer from [NIH syndrom](https://en.wikipedia.org/wiki/Not_invented_here)

Notice that all sections are minimalistic, with lots of whitespace, white background, black text. Try to stick to it, so that your section can be combined with any other section.


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

Here is the naming convention to prefix css class name: nameNumber. The number is the first available number for the given section.

Example : is there are already 2 hero_section, your new hero section will be name section_hero_3, and css selector must ALL start with .r3- to avoid naming collision.

### Folder and file structure

Folders and files will be as follow :

```
section_hero_3/
├── demo.html
├── section_hero_3.css
├── section_hero_3.html
└── README.md
```

Each filename should speak by itself. Please note you **MUST** provide a demo and a README for each section.

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


### Start and end of file

Each css file MUST start with comment

```
/* section_hero_1  Start of CSS
–––––––––––––––––––––––––––––––––––––––––––––––––– */
```

Each css file MUST ends with comment

```
/* section_hero_1  End of CSS
–––––––––––––––––––––––––––––––––––––––––––––––––– */
```

It is because user will copy/paste CSS in order to add section.
Thus, it will be easier to remove the right section and to locate code.

** Same principle apply for HTML file, see section_hero_2.html for an example**

### Pictures are not commited

Because each picture is made to be deleted and replaced, there is no point commiting it into the repository. Instead, send it to a cloud service and reference them. See section_hero_1 for example.

### Things to avoid

Never use an existing logo
Never use real name of people
Never use real photo of people

There are tons of free pictures and icons, fake name are easy to create.

### Use common properties as much as possible

Look at file css/shared.css

It is a collection of shared properties through sections.

For example, by using the same marginbottom40 in each section, they become "compatible" each others.

### Use of font and typefaces

Remember that each section must be compatible for each other, so you DON'T have the choice for properties like font-family, font-size, font-weight etc, you must use the ones currently used by default.

The end user have the ability to change them, etc but each section MUST conform to the default settings when you code them.

### Use of external dependencies

You should avoid use of external dependencies (jQuery, fontawesome) as much as possible. In order not to decrease display speed of the landing page. Unless stricly necessary AND well documented in the README.md of the section.

## Run doctoc

Run doctoc to create table of content for each README

```
npm install -g doctoc
doctoc .
```

## Make a pull request

See [official Github guide](https://help.github.com/articles/using-pull-requests/)


