# nmisra-arapv

In this branch, I write down my notes from examining the files.

Setup / compilation
-----------------
1. Make sure XeTeX is installed (`type xelatex`)
2. Install Sanskrit2003NM font (included here)
3. Install Charis SIL font (download from http://software.sil.org/charis/)
4. Run `xelatex arapvcover.tex`
5. Run `xelatex arapv.tex` 2 or 3 times. (If you run it only once, the page numbers and cross-references will be incorrect or missing.)

Structure
--------
There are two "main" files: `arapvcover.tex` and `arapv.tex`

`arapvcover.tex` contains the back cover, spine, and front cover as a single sheet, which can be used for binding a printed book. It is small (64 lines excluding comments and blank lines) and relatively self-contained.

`arapv.tex` is the actual PDF of the book (including front and back covers). It uses `\includepdf` with `arapvcover.pdf` twice, to include the relevant part of the cover as the first and last pages.
