# Notebook -> LaTeX article

With the `plainbase` template only markdown cells are included.
Code cells and output -- including plots -- are ignored.
The motivation being to create a LaTeX file that takes less cleaning up,
if it is to be used e.g. as a starting point for a journal article.

Inline plots are ignored because I want a vector format, and SVG doesn't work with LaTeX.
See the sample notebook for how one can add figures. 
I won't claim it's ideal.


`scrarctl` inherits `plainbase` and defines the documentclass, so use

    jupyter nbconvert --to latex --template scrartcl <notebook>.ipyn


If you want a bibliography, add e.g.

    \bibligraphystyle{plainnat}
    \bibliography{refs}

in a raw cell.
