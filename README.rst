=========================
Cookiecutter Latex-thesis
=========================

Write your thesis with Latex using this Cookiecutter_ template.

* GitHub repo: https://github.com/Oli4/cookiecutter-latex-thesis/

Features
--------

* Title page and declaration of authorship set up already
* Makefile: Compile document or parts of it; Clean your source folder; Compress your pdf
* Many packages already configured (biblatex, booktabs, graphicx, 
  hyperref, acro, ...)

Quickstart
----------

Install the latest Cookiecutter if you haven't installed it yet::

    pip install -U cookiecutter

Generate your \Latex document::

    cookiecutter https://github.com/Oli4/cookiecutter-latex-thesis.git

Make sure biber and texlive is installed, you need it for compiling your document.:

    sudo apt install texlive-full texlive-bibtex-extra biber

Installing texlive-full is probably an overkill but I haven't figured out yet, which parts of texlive are required by this template. You can also just run the make command to start compilation and solve the errors step by step installing only the required parts on after the other. 

Now you can start writing your thesis.

Similar Cookiecutter Templates
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

* `selimb/cookiecutter-latex-article`_: A template for writing lab reports,
  essays and project reports.

Fork This / Create Your Own
~~~~~~~~~~~~~~~~~~~~~~~~~~~

If you prefer a different setup feel free to create your own version. 

* Once you have your own version working, add it to the Similar Cookiecutter
  Templates list above with a brief description.

* It's up to you whether or not to rename your fork/own version. Do whatever
  you think sounds good.

Or Submit a Pull Request
~~~~~~~~~~~~~~~~~~~~~~~~

I would love to see you improving this template and making it even easier to start 
writing a thesis with Latex.

.. _Cookiecutter: https://github.com/audreyr/cookiecutter

.. _`selimb/cookiecutter-latex-article`: https://github.com/selimb/cookiecutter-latex-article

Credits
-------
The template is based on code and ideas found here: https://github.com/deeplearningais/latex-thesis-template