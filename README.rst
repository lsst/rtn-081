.. image:: https://img.shields.io/badge/rtn--081-lsst.io-brightgreen.svg
   :target: https://rtn-081.lsst.io
.. image:: https://github.com/lsst/rtn-081/workflows/CI/badge.svg
   :target: https://github.com/lsst/rtn-081/actions/

###############################################################################################################
Rubin Observatory Operations: Enabling collaborative ground-up budget planning across a multi-team organization
###############################################################################################################

RTN-081
=======

Change is inevitable in large, big-budget operational programs. 
Embracing, rather than resisting, change is key to being proactive. 
It also keeps teams motivated as it’s another avenue for leadership to ``listen'' to what is going on at the team level. 
At Rubin Observatory, an agile approach to budgeting has been implemented, following related experience in previous High Energy Physics experiments. 
Annually, a ground-up review, to address changing needs, priorities and emerging issues, is carried out across all departments of the Rubin Operations organization. 
This ``annual scrub'' provides an opportunity to adapt and be nimble to changing situations that can affect resources and budgets. 
This paper provides details on the importance of an annual budget scrub, the processes followed, the tools used, and how the cycle continues year on year.

Links
=====

- Live drafts: https://rtn-081.lsst.io
- GitHub: https://github.com/lsst/rtn-081

Build
=====

This repository includes lsst-texmf_ as a Git submodule.
Clone this repository::

    git clone --recurse-submodules https://github.com/lsst/rtn-081

Compile the PDF::

    make

Clean built files::

    make clean

Updating acronyms
-----------------

A table of the technote's acronyms and their definitions are maintained in the `acronyms.tex` file, which is committed as part of this repository.
To update the acronyms table in ``acronyms.tex``::

    make acronyms.tex

*Note: this command requires that this repository was cloned as a submodule.*

The acronyms discovery code scans the LaTeX source for probable acronyms.
You can ensure that certain strings aren't treated as acronyms by adding them to the `skipacronyms.txt <./skipacronyms.txt>`_ file.

The lsst-texmf_ repository centrally maintains definitions for LSST acronyms.
You can also add new acronym definitions, or override the definitions of acronyms, by editing the `myacronyms.txt <./myacronyms.txt>`_ file.

Updating lsst-texmf
-------------------

`lsst-texmf`_ includes BibTeX files, the ``lsstdoc`` class file, and acronym definitions, among other essential tooling for LSST's LaTeX documentation projects.
To update to a newer version of `lsst-texmf`_, you can update the submodule in this repository::

   git submodule update --init --recursive

Commit, then push, the updated submodule.

.. _lsst-texmf: https://github.com/lsst/lsst-texmf
