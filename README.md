# ReleasePlots
Tag figures in a LaTeX document for release and create according list of figures for release.

This repository provides `ReleasePlot.sty` and annotating `releaseplot.{pdf,tex}` file, highlighting the use case of this small package. Have a look at the PDF for all the details.

## Purpose
In an internal document of our experiment, some figures are more important than others. To mark the more important ones, a tag is added to the caption of the figures (`[RELEASE]`).  
Since the figures are already tagged, they can be summarized into a list of figures for release, printed by `\listofreleaseplots`. See it work in the PDF of the repository!

## Usage
Figures can be tagged with the command `\plotRelease`. The command has two versions.

1. Usage in a `caption` which has the additional square-brackets argument, i.e. `\caption[optional]{\plotRelease mandatory}`. If used like this, `\plotRelease` will take the optional title for the list of figures for release
2. Usage in a `caption` which does not have the additional argument, but only the curly-bracket title, i.e. `caption{\plotrelease*[text]}`. In that case please use the starred version of the command, `\plotRelease*`, and provide the title for the list of figures for release in square brackets.

If there are entries to the list of figures, the list can be printed with `\listofreleaseplots`.

## Modification
The package provides a few macros enabling modification of appearance of the tag. They are:

* `\RPTagColor`: The color of the tag
* `\RPText`: The text of the tag
* `\RPChapterTitle`: The title of the chapter of the list of figures (= the title of the list of figures)

Check the PDF or the package description for their default values.

## Dependencies
The package was designed to work with the document class `memoir`.

Some basic mechanisms are in place for it to work with other classes, but the result of `\listofreleaseplots` is a bit broken.

All other required packages should be part of every default LaTeX installation (and are available at CTAN in any case).
