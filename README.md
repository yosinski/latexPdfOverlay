About
==================

[latexPdfOverlay](https://github.com/yosinski/latexPdfOverlay)
simplifies the often cumbersome process of filling in PDF forms
occasionally required by various prehistoric entities.

You first create a [LaTeX](http://www.latex-project.org/) template
which specifies which fields exist and where they are positioned, and
then run the
[```fillpdf```](https://github.com/yosinski/latexPdfOverlay/blob/master/fillpdf)
script with command line arguments specifying the desired values of the fields.





Installation 
==================

Requirements: [LaTeX](http://www.latex-project.org/) (which probably
also includes the required package
[tikz](http://www.texample.net/tikz/examples/)).

To install, simply put ```fillpdf``` somewhere on your PATH.



Usage
==================

Here are a few examples:

    fillpdf --name "John Doe" --foo bar --date "3/22/13" template.tex form_blank.pdf output.pdf

To debug, add the --debug option to overlay a grid and display field names, and/or the --keep option to keep the intermediate latex files:

    fillpdf --debug template.tex form_blank.pdf output.pdf
    fillpdf --keep --debug template.tex form_blank.pdf output.pdf

