============
pyexcel-ods3
============

.. image:: https://api.travis-ci.org/chfw/pyexcel-ods3.png
    :target: http://travis-ci.org/chfw/pyexcel-ods3

.. image:: https://codecov.io/github/chfw/pyexcel-ods3/coverage.png
    :target: https://codecov.io/github/chfw/pyexcel-ods3

**pyexcel-ods** is a plugin to `pyexcel <https://github.com/chfw/pyexcel>`_ and provides the capbility to read, manipulate and write data in ods fromat using python 2.7, python 3.3 and python 3.4

Usage
=====

Import it in your file to enable this plugin::

    from pyexcel.ext import ods3

Reading from an ods file
------------------------

Here is the sample code::

    from pyexcel import Reader
    from pyexcel.ext import ods3
    from pyexcel.utils import to_array
    import json
    
    # "example.ods"
    reader = Reader("example.ods")
    data = to_array(reader)
    print json.dumps(data)

Writing to an ods file
----------------------

Here is the sample code::

    from pyexcel import Writer
    from pyexcel.ext import ods3
    
    array = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
    writer = Writer("output.ods")
    writer.write_array(array)
    writer.close()


Dependencies
============

1. pyexcel >= 0.0.4
2. lxml
3. ezodf2