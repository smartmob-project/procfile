procfile -- a procfile Parser for Python
========================================

Installing
----------

Find `procfile on PyPI`_.  Install it using pip_::

   $ pip install procfile

.. _`procfile on PyPI`: https://pypi.python.org/pypi/procfile
.. _pip: https://pip.readthedocs.org/

Contributing
------------

Contributions welcome!  Fork `procfile on GitHub`_ and send in a pull request!

.. _`procfile on GitHub`: https://github.com/smartmob-project/procfile

Getting started
---------------

.. testcode::

   import json
   import procfile
   process_types = procfile.loads('''
   web: gunicorn myapp.wsgi
   ''')
   print(json.dumps(process_types, indent=2, sort_keys=True))

.. testoutput::

   {
     "web": {
       "cmd": "gunicorn myapp.wsgi",
       "env": []
     }
   }

API reference
-------------

.. automodule:: procfile

   .. autofunction:: loads
   .. autofunction:: load
   .. autofunction:: loadfile
