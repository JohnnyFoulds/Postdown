Postdown
=========

|Python Version| |PyPI version|

    *Generate markdown API document from Postman.*

The purpose of this fork is to fix issue I ran into when attempting to use this tool with a ``Collection v2.1`` export.

* Correct handling of both with sub-folders and without.
* Correct dictionary key check that throws exceptions.
* Removed author from footer as it did not seem appropriate - the original still gets credit though the Postman link.
* Do not render empty query tables.
* Do not render empty Examples sections.
* Removed overused horizontal rule.
* Added logging to aid debugging.

There are still some unsafe checks left for the moment to allow for validation that no new errors are introduced.


Installation
-------------

.. code:: shell

    pip install -e git+https://github.com/JohnnyFoulds/Postdown#egg=postdown


Usage
------

* **Export JSON from postman**
    Export your collection from Postman(Only support to Collection v2 for now).
    You could get a JSON file.

    .. figure:: https://raw.githubusercontent.com/TitorX/Postdown/master/imgs/step-1.png

        Step One: Select the collection which you wanna export.


    .. figure:: https://raw.githubusercontent.com/TitorX/Postdown/master/imgs/step-2.png

        Step Two: Find the import button and click it.


    .. figure:: https://raw.githubusercontent.com/TitorX/Postdown/master/imgs/step-3.png

        Step Three: Export your collection as *collection v2*.



* **Run** ``postdown`` **to generate markdown document**::

        postdown xxx.json xxx.md


And you will get your API document which is markdown formatting.



`Click here to see an example generated. <https://github.com/TitorX/Postdown/tree/master/demo>`_





.. |Python Version| image:: https://img.shields.io/badge/python-2&3-brightgreen.svg?style=flat-square
    :target: https://pypi.python.org/pypi/Postdown
.. |PyPI version| image:: https://img.shields.io/pypi/v/Postdown.svg?style=flat-square
    :target: https://pypi.python.org/pypi/Postdown

