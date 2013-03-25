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



Usage Examples
==================

Let's say you were given the following innocuous (Comic Sans notwithstanding) form to fill out:

[![form-blank](https://github.com/yosinski/latexPdfOverlay/raw/master/screenshots/form-blank.png)](https://github.com/yosinski/latexPdfOverlay/raw/master/screenshots/form-blank.png)

First, create a template file like the included [```example_template.tex```](https://github.com/yosinski/latexPdfOverlay/raw/master/example_template.tex). Then, compile in debug mode to check alignments, etc:

    ./fillpdf --debug example_template.tex example_form.pdf output.pdf

This produces the following debug ```output.pdf```:

[![form-debug](https://github.com/yosinski/latexPdfOverlay/raw/master/screenshots/form-debug.png)](https://github.com/yosinski/latexPdfOverlay/raw/master/screenshots/form-debug.png)

When you get the alignment right, then you can run the script again to produce the final output with the appropriate values filled in:

    ./fillpdf --name "John Doe" --why "for research" --sure yes --months "9 months (please rush)" --grovel "I had the receipt but then my small dog ate it and then a larger dog ate my smaller dog, so I cannot turn the receipt in. Please accept instead the attached impressionist watercolor painting of the receipt and observed food chain." example_template.tex example_form.pdf output.pdf && skimreload output.pdf

[![form-filled](https://github.com/yosinski/latexPdfOverlay/raw/master/screenshots/form-filled.png)](https://github.com/yosinski/latexPdfOverlay/raw/master/screenshots/form-filled.png)





![-](http://s.yosinski.com/1px_latexPdfOverlay.png)
