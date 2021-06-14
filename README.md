![plemiona-planer](https://plemiona-planer.pl/static/images/background.jpg)

## About

Docs for the [plemiona-planer.pl](https://plemiona-planer.pl) (Tribal Wars Planer) - django app and professional tool for creating outlines for off-game coordinators.

## Official Site and Discord

[plemiona-planer.pl](https://plemiona-planer.pl/en/)

[discord.gg/g5pcsCteCT](https://discord.gg/g5pcsCteCT)

## How to use this repo

This repo contains two folders, one for documentations written in MD format: `/docs`, and another one for images, which is the mirror of static folder strucutre in production, example path to some image would look like that for this reason: `/static/docs/pl/1_020_test-menu.png`. Images need to be in correct folder for diffrent languages (pl, en) and are more or less called in this convention: **S-N0-someName** where **S** is a chapter/section number, **N** is a number of image in this chapter, and **someName** is self-expressive.

You can create Pull Requests with changes in markdown docs and/or new images in a manner explained above.

## Some general convenctions in docs file:

#### 1. Fonts, colors

No stricte rules about font size, just use general mardkown sizes (follow rules from diffrent sections). There are only 2 colors allowed (not counting default black), **teal** and **red**, used as follows:

```
<span class="md-error">something bad or important - red color</span>
<span class="md-correct2">something-highlighted - teal color</span>
```

#### 2. Notes/Alerts

Standard note looks like this:

```
<div class="p-3 mb-2 bg-light text-dark"><i class="bi bi-info-square"></i> This is the note, icon in "i" tag at the beginning of this sentence</div>
```

Something very important:

```
<div class="p-3 mb-2" style="background: #CEF2F3 !important;">This is a very, very important note</div>
```

#### 3. Existing headers IDs

Consider subsection `## 1. Skrypt zbiórka wojska {#army-script}`. This `<h2>` element will have **ID** **army-script** (there are many many headers with **ID** like that). Do _NOT_ change (translate) `#army-script` regardless of used language. It is not so important to have it in specific language, and it may lead to weird bugs if someone change **ID** somewhere in docs and forget to do so in other file or files. Some of the **ID**s are also used directly in site code and thus completely unchangable, f.e. in tab where User creates new outline, there is a link to `#swiat-testowy-czyli-pierwsze-kroki-z-planerem` section, therefore after changing it to something else, link would be dead.

#### 4. Navigation hints (path in site - and equivalent documentation file)

Let's use English docs below, but it works for other languages too (`documentation_pl.md` instead of `documentation_en.md`)

`documentation_en.md`

[plemiona-planer.pl/en/documentation - docs tab](https://plemiona-planer.pl/en/documentation)

`planer_create_info_en.md` and `planer_create_example_en.md`

[plemiona-planer.pl/en/planer/create/ - new outline tab](https://plemiona-planer.pl/en/planer/create/)

`planer_deff_info_en.md` and `planer_deff_example_en.md`

[plemiona-planer.pl/en/planer/1000/get-deff - deff tab](https://plemiona-planer.pl/en/planer/1000/get-deff)

`planer_form_info_en.md` and `planer_form_example_en.md`

[plemiona-planer.pl/en/planer/1000/planer-form - form tab](https://plemiona-planer.pl/en/planer/1000/planer-form)

`planer_scripts_info_en.md` and `planer_scripts_examples_en.md`

[plemiona-planer.pl/en/planer/1000 - tab with troops](https://plemiona-planer.pl/en/planer/1000)
