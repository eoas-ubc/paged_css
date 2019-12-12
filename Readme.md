# Four versions of the same jupyter notebook

This folder contains four versions of a noteboo:

1. [quiz4_2019t1.ipynb](json version)

2. [quiz4_2019t1.py](python version) (made using https://jupytext.readthedocs.io/en/latest/index.html)

3. html version made with

        jupyter nbconvert --to html quiz4_2019t1.ipynb

4. pdf version made with a latex template

        jupyter nbconvert --to html quiz4_2019t1.ipynb


# The project

## step 1

It would be very nice to skip the latex and print directly to pdf from chrome but
the css for the jupyter html doesn't support the headers, page numbers and page breaks
we need for the quiz (this is done using the latex fancyhdr package).

So step 1 would be to hand edit this html file so that we get something that prints with
chrome to a pdf with a header and page numbers.  It looks like CSS3 should be capable of
this.  Some google searches turned up:

- https://print-css.rocks/lesson/lesson-page-numbers
- https://print-css.rocks/lesson/lesson-pagination

- https://www.smashingmagazine.com/2018/05/print-stylesheets-in-2018/
- https://www.smashingmagazine.com/2015/01/designing-for-print-with-css/

- https://www.pagedmedia.org/paged-js/

## step 2

After we get the basic pagination in this example, we should be able to create a template
and a python script to transfrom the jupyter html into printable html, and then just
use chrome headless in batch mode (I hope)
