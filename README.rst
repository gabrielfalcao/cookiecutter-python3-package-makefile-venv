{{cookiecutter.project_name}}
=============================

This project is based on the project `Makefile Python Venv Basic
<https://github.com/gabrielfalcao/Makefile-python-basic>`_ which uses
the python3 builtin module `venv
<https://docs.python.org/3/library/venv.html>`_ and uses a Makefile to
automate development tests such as running tests, making releases,
generating documentation, etc.

Check that project's documentation for more information.


Next steps to configure your python project
--------------------------------------------

**Running Tests**
.................

.. code:: bash

   # to run both unit and functional tests:
   make tests

   # or separately:
   make unit
   make functional


**Configuring open-source license**
...................................

1. Follow the `python packaging guide for licenses <https://packaging.python.org/tutorials/packaging-projects/#creating-a-license>`_.
2. Edit the file ``LICENSE`` with a copy of the license you chose as explained in the guide above.
3. Edit ``setup.py`` with the proper `trove<https://pypi.org/classifiers/>`_  `classifier<https://pypi.org/classifiers/>`_ for the license chosen.


**Making a new release**
........................

Before making a release, make sure to configure your `pypi credentials <https://workshop-from-your-editor-to-pypi.readthedocs.io/en/latest/pypirc-credentials.html>`_....

1. Set the new version in ``version.py``.
2. Add proper version changes in ``CHANGELOG.rst``.
3. run ``make release``.


**Adding docs**
---------------

I recommend using `Sphinx <https://www.sphinx-doc.org/en/master/>`_ for documenting your project.

Sphinx is the unspoken official tool for documentation in the python
ecosystem, it supports many plugins but the `Intersphinx
<https://www.sphinx-doc.org/en/master/usage/extensions/intersphinx.html>`_
plugin is among the ones I find most useful because it creates a
binary file called ``objects.inv`` that allows other Sphinx-powered
documentation to make direct reference to the documentation of
internal python APIs.
