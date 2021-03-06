.. Requests documentation master file, created by
   sphinx-quickstart on Sun Feb 13 23:54:25 2011.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Requests: HTTP for Humans
=========================

Release v\ |version|. (:ref:`Installation <install>`)

Requests is an :ref:`ISC Licensed <isc>` HTTP library, written in Python, for human beings.

Most existing Python modules for sending HTTP requests are extremely verbose
and cumbersome. Python's builtin **urllib2** module provides most of
the HTTP capabilities you should need, but the api is thoroughly **broken**.
It requires an *enormous* amount of work (even method overrides) to perform the simplest of tasks.

Things shouldn’t be this way. Not in Python.

::

    >>> r = requests.get('https://api.github.com', auth=('user', 'pass'))
    >>> r.status_code
    200
    >>> r.headers['content-type']
    'application/json'

See `the same code, without Requests <https://gist.github.com/973705>`_.

Requests allow you to send **GET**, **HEAD**, **PUT**,
**POST**, and **DELETE** HTTP requests. You can add headers, form data,
multipart files, and parameters with simple Python dictionaries, and access the
response data in the same way. It's powered by :py:class:`urllib2`, but it does
all the hard work and crazy hacks for you.

Testimonals
-----------

`Twitter, Inc <http://twitter.com>`_ and `The Library of Congress <http://www.loc.gov/>`_ use Requests internally.

**Daniel Greenfeld**
    Nuked a 1200 LOC spaghetti code library with 10 lines of code thanks to @kennethreitz's request library. Today has been AWESOME.

**Kenny Meyers**
    Python HTTP: When in doubt, or when not in doubt, use Requests. Beautiful, simple, Pythonic.

**Rich Leland**
   Requests is awesome. That is all.

**Steve Pike**
  I can never remember how to do it the regular way. ``import requests; requests.get()`` is just so easy!


User Guide
----------

This part of the documentation, which is mostly prose, begins with some background information about Requests, then focuses on step-by-step instructions for getting the most out of Requests.

.. toctree::
   :maxdepth: 2

   user/intro
   user/install
..   user/quickstart
   user/advanced


API Documentation
-----------------

If you are looking for information on a specific function, class or method,
this part of the documentation is for you.

.. toctree::
   :maxdepth: 2

   api


Developer Guide
---------------

If you want to contribute to the project, this part of the documentation is for
you.

.. toctree::
   :maxdepth: 2

   dev/internals
