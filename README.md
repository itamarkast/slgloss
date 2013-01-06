stokoe
======

A package for glossing sign language examples, including fingerspelling and nonmanuals, in LaTeX.

Sign language signs are conventionally glossed in smallcaps, with the scope of nanmanual markers denoted by a solid line running above the gloss. The type of nonmanual is denoted at the right edge of this line. Loci in space are denoted by subscript indices. This is the notational convention favored by most sign linguists, e.g. Sandler and Lillo-Martin (2006).

There are numerous ways of glossing ASL lexical items. In an effort to keep these glosses integrated in running text we have adopted the clear and elegant typographic conventions of Cormier et al. (2008). Not only is this consistent with separating ASL forms from the text as well as reliably marking the difference between ASL native signs (smallcaps) and fingerspelled forms (smallcaps, with hyphens) but it also is easier to read than many other systems. Following from this, single finger spelled letters can be flanked by hyphens on either side.

_stokoe_ (named after William Stokoe) provides an easy way of typesetting these glosses for sign language linguists.

stokoe.sty provides three commands: **\slg{}**, **\fs{}** and **\fslist{}**. In addition, it allows use of subscript indices without explicitly entering math mode: **IX_a**.

\slg{}
------
**\slg{text}** typesets the input _<text>_ in small caps. Input may be lowercase or uppercase.

**\slg[nmm]{text}** typesets the input _<text>_ in small caps with the nonmanual _<nmm>_ marked above it with an overline.

Example: **\slg{POSS_a NAME} \slg[wh]{WHAT?}**

\fs{}
-----
Use **\fs{foo}** to typset the word foo in small caps with dashes between each letter: _F-O-O_.

\fslist{}
---
Use **\fslist{b,ac,r}** to typeset the letter _b_, the two letters _ac_ and the letter _r_ as three individual elements, with dashes on either side, in small caps, with commas, and _and_ at the end. It even deals with the final serial comma appropriately: _-B-, -AC-, and -R-_.

As a shorthand, use **\fslist{bar}** to typset the letters _b_, _a_, and _r_ as individual letters. Omitting the commas means that each letter will be typeset on its own; if you require combinations as with _-AC-_ above, use comma-separated input.

There is an optional argument that changes the conjunction used; the default is _and_: **\fslist[or]{b,ac,r}**, **\fslist[or]{bar}**.

Terms of Use
---
