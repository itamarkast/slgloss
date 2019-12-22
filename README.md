slgloss
======

A package for glossing sign language examples, including fingerspelling and nonmanuals, in LaTeX.

Sign language signs are conventionally glossed in smallcaps, with the scope of nanmanual markers denoted by a solid line running above the gloss. The type of nonmanual is denoted at the right edge of this line. Loci in space are denoted by subscript indices. This is the notational convention favored by most sign linguists, e.g. Sandler and Lillo-Martin (2006).

In an effort to keep these glosses integrated in running text we have adopted the typographic conventions of Brentari and Padden (2001) and Cormier et al. (2008) where fingerspelled forms are set in small-caps, separated by hyphens. Following from this, single finger spelled letters can be flanked by hyphens on either side.

_slgloss_ provides an easy way of typesetting these glosses for sign language linguists.

slgloss.sty provides three commands: **\slg{}**, **\fs{}** and **\fslist{}**. In addition, it allows use of subscript indices without explicitly entering math mode: **IX_a**.

By default, any text in slg will be transformed to lowercase, and then made into smallcaps. There is an option **nolowercase** that can be called when the package is loaded (eg **\usepackage[nolowercase]{slgloss}**) for scripts where lowercase transformations cause compilation errors.

For additional documentation see the following short guide by Fabian Bross: <http://fabianbross.de/sign_language_glossing.pdf>

\slg{}
------
**\slg{text}** typesets the input _<text>_ in small caps. Input may be lowercase or uppercase.

**\slg[nmm]{text}** typesets the input _<text>_ in small caps with the nonmanual _<nmm>_ marked above it with an overline.

Example: **\slg{POSS_a NAME} \slg[wh]{WHAT?}**

Use **\slgl[nmm]{text}** for the nonmanual _<nmm>_ to be left-aligned.

Use **\slgdash[nmm]{text}** to indicate optionality by using a dashed line above the gloss (rather than a solid one).

\fs{}
-----
Use **\fs{foo}** to typset the word foo in small caps with dashes between each letter: _F-O-O_.

\fslist{}
---
Use **\fslist{b,ac,r}** to typeset the letter _b_, the two letters _ac_ and the letter _r_ as three individual elements, with dashes on either side, in small caps, with commas, and _and_ at the end. It even deals with the final serial comma appropriately: _-B-, -AC-, and -R-_.

As a shorthand, use **\fslist{bar}** to typset the letters _b_, _a_, and _r_ as individual letters. Omitting the commas means that each letter will be typeset on its own; if you require combinations as with _-AC-_ above, use comma-separated input.

There is an optional argument that changes the conjunction used; the default is _and_: **\fslist[or]{b,ac,r}**, **\fslist[or]{bar}**.

License
---
Copyright (c) 2013 Itamar Kastner, Jonathan Keane

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
