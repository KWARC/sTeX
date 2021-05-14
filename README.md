sTeX: An Infrastructure for Semantic Preloading of LaTeX Documents
====
![CI Status](https://github.com/slatex/sTeX/workflows/CI/badge.svg)

This repository contains the sTeX package collection, a version of TeX/LaTeX that allows
to markup TeX/LaTeX documents semantically without leaving the document format,
essentially turning it into a document format for mathematical knowledge management (MKM).

## Copyright & License
Copyright (c) 2019 Michael Kohlhase

The package is distributed under the terms of the LaTeX Project Public License (LPPL)

## Documentation
See the [academic literature](https://kwarc.github.io/bibs/sTeX/) for the intuition and
develpment and the 
[documentation of the sTeX package](https://github.com/slatex/sTeX/blob/master/sty/stex/stex.pdf)
for details. We have also started the [sTeX Wiki](https://github.com/slatex/sTeX/wiki) for
community driven documentation. 

## Setup

The GIT version can just be cloned in a directory `<sTeXDIR>` of your choosing. 
```
cd <sTeXDIR>
git clone https://github.com/slatex/sTeX.git
```
Then update your  `TEXINPUTS` environment variable, e.g. by placing the following line in your `.bashrc`:
```
export TEXINPUTS="$(TEXINPUTS):<sTeXDIR>//:$(TEXINPUTS)
```
For a LaTeX IDE, update the directory path where `pdflatex` looks for paths accordingly.

## MathHub

If you want to use [MathHub](https://mathhub.info)-compatible organization into
mathematical archives (and that is usually a good idea) then you have to create a
**MathHub root directory**, e.g. `~/localmh/MathHub`, and set the `MATHHUB` environment
variable adding the following to your `.bashrc`.
```
export MATHHUB="$(HOME)/localmh/MathHub"
```

## OMDoc/RichHTML Transformation 

sTeX documents can be transformed to [OMDoc](http://omdoc.org) via the
[sTeX Plugin](https://github.com/sLaTeX/LaTeXML-Plugin-sTeX/) for
[LaTeXML](https://github.com/brucemiller/LaTeXML) available at
https://github.com/sLaTeX/LaTeXML-Plugin-sTeX/.

## Manifest
The sTeX distribution contains the following directories
* `sty`: The packages and classes of the sTeX distribution
* `lib`: bibTeX bibliography and Makefile inputs for the package/class generation and documentation
* `bin`: a couple of utilities that make your life easier
* `doc`: a space for documentation, currently only blue notes (ideas for the future)
* `example`: a worked example of an sTeX paper.   
* `test`: the [sTeX test suite](https://github.com/sLaTeX/stex-tests) imported via `git
  subrepo`; run `make -B test` at top level to test; run `git subrepo pull test` to
  update; and run `git subrepo push test` to contribute tests back upstream. 

<!--  LocalWords:  bashrc pdflatex subrepo subrepo
 -->
