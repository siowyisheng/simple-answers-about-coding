Simple Sphinx
===============

Sphinx generates project documentation, which can be hosted easily at
`readthedocs <https://readthedocs.org/>`_.

Your project should be in a `github <https://github.com/>`_ repository. Then,
sign up for a `readthedocs account <https://readthedocs.org/accounts/signup/>`_ with
your github account.


Setup new project
-------------------

1. Install sphinx with pip::

    $ pip install sphinx

2. As best practice, use a separate ``docs`` folder. From your project folder::

    $ mkdir docs
    $ cd docs

3. Use the sphinx quickstart and follow the prompts::

    $ sphinx-quickstart

4. From your `readthedocs dashboard <https://readthedocs.org/dashboard/>`_, import
your github project repository.

5. You can soon access the documentation online, either from your
dashboard or the provided URL.

Develop documentation
----------------------

We create and edit documentation in .rst files, written in restructuredText (`quickstart <http://docutils.sourceforge.net/docs/user/rst/quickstart.html>`_).

To make a header, insert a row of special characters
underneath, which cannot be shorter than the header::

    My Header
    ---------

To make a sub-header, use a different special character::

    My Header
    ----------

    My Sub-header
    *************

To make a link, follow this syntax::

    `My Link <http://www.cutestpaw.com/tag/cats/>`_

.. warning:: Note the space before ``<`` and the ``_`` after the `````.

To show code, one way is to use literal blocks::

    ::

        print('hello world!')

    Or with text before the code::

        for i in range(5):
            print(i)

.. warning:: Note the empty line after ``::``.

To make a list::

    1. Python
    2. Javascript
    3. C#

To format text::

    **Bold**, *italics*, ``code``.

To insert an image::

    .. image:: https://picsum.photos/200/300
        :width: 200px
        :height: 100px
        :align: center
        :alt: alternate text

.. note::  This is a note box.

To insert a note box::

    .. note::  This is a note box.

.. warning:: This is a warning box.

To insert a warning box::

    .. warning:: This is a warning box.


Preview documentation
----------------------

Use `vscode <https://code.visualstudio.com/>`_ and install the
`reStructuredText extension <https://marketplace.visualstudio.com/items?itemName=lextudio.restructuredtext>`_.
The extension allows you to preview your documentation with
*Open Locked Preview to the Side* (find it with *Ctrl/Cmd+Shift+P*.)

You can view the HTML locally. Within your ``docs`` folder::

    $ make html
    $ open _build/html/index.html

Deploy documentation
---------------------

If your github project was imported into readthedocs, your
documentation will be automatically built and deployed when a changed
version is pushed to github. Find the URL from your `readthedocs dashboard <https://readthedocs.org/dashboard/>`_.


*(Optional)* Setup RTD Theme
-----------------------------
This page uses the RTD theme 🌈.

::

    $ pip install sphinx_rtd_theme

In your conf.py file, set ``html_theme``::

    html_theme = "sphinx_rtd_theme"
