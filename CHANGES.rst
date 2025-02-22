2.0.0 (unreleased)
------------------

- Breaking change: inputs starting with ``"http://"`` or ``"https://"`` like
  ``PyQuery("http://example.com")`` will no longer fetch the contents of the URL.
  Users desiring the old behavior should switch to ``PyQuery(url="http://example.com")``.

- Add nextUntil method

- ``.remove()`` no longer inserts a space in place of the removed element

- Fix escaping of top-level element text in ``.html()`` output


1.4.3 (2020-11-21)
------------------

- No longer use a universal wheel


1.4.2 (2020-11-21)
------------------

- Fix exception raised when calling `PyQuery("<textarea></textarea>").text()`

- python2 is no longer supported

1.4.1 (2019-10-26)
------------------

- This is the latest release with py2 support

- Remove py33, py34 support

- web scraping improvements: default timeout and session support

- Add API methods to serialize form-related elements according to spec

- Include HTML markup when querying textarea text/value


1.4.0 (2018-01-11)
------------------

- Refactoring of `.text()` to match firefox behavior.


1.3.0 (2017-10-21)
------------------

- Remove some unmaintained modules: ``pyquery.ajax`` and ``pyquery.rules``

- Code cleanup. No longer use ugly hacks required by python2.6/python3.2.

- Run tests with python3.6 on CI

- Add a ``method`` argument to ``.outer_html()``


1.2.17 (2016-10-14)
-------------------

- ``PyQuery('<input value="">').val()`` is ``''``
- ``PyQuery('<input>').val()`` is ``''``


1.2.16 (2016-10-14)
-------------------

- ``.attr('value', '')`` no longer removes the ``value`` attribute

- ``<input type="checkbox">`` without ``value="..."`` have a ``.val()`` of
  ``'on'``

- ``<input type="radio">`` without ``value="..."`` have a ``.val()`` of
  ``'on'``

- ``<select>`` without ``<option selected>`` have the value of their first
  ``<option>`` (or ``None`` if there are no options)


1.2.15 (2016-10-11)
-------------------

- .val() should never raise

- drop py26 support

- improve .extend() by returning self


1.2.14 (2016-10-10)
-------------------

- fix val() for <textarea> and <select>, to match jQuery behavior


1.2.13 (2016-04-12)
-------------------

- Note explicit support for Python 3.5

1.2.12 (2016-04-12)
-------------------

- make_links_absolute now take care of whitespaces

- added pseudo selector :has()

- add cookies arguments as allowed arguments for requests


1.2.11 (2016-02-02)
-------------------

- Preserve namespaces attribute on PyQuery copies.

- Do not raise an error when the http response code is 2XX

1.2.10 (2016-01-05)
-------------------

- Fixed #118: implemented usage ``lxml.etree.tostring`` within ``outer_html`` method

- Fixed #117: Raise HTTP Error if HTTP status code is not equal to 200

- Fixed #112: make_links_absolute does not apply to form actions

- Fixed #98: contains act like jQuery


1.2.9 (2014-08-22)
------------------

- Support for keyword arguments in PyQuery custom functions

- Fixed #78: items must take care or the parent

- Fixed #65 PyQuery.make_links_absolute() no longer creates 'href' attribute
  when it isn't there

- Fixed #19. ``is_()`` was broken.

- Fixed #9. ``.replaceWith(PyQuery element)`` raises error

- Remove official python3.2 support (mostly because of 3rd party semi-deps)


1.2.8 (2013-12-21)
------------------

- Fixed #22: Open by filename fails when file contains invalid xml

- Bug fix in .remove_class()


1.2.7 (2013-12-21)
------------------

- Use pep8 name for methods but keep an alias for camel case method.
  Eg: remove_attr and removeAttr works
  Fix #57

- .text() now return an empty string instead of None if there is no text node.
  Fix #45

- Fixed #23: removeClass adds class attribute to elements which previously
  lacked one


1.2.6 (2013-10-11)
------------------

- README_fixt.py was not include in the release. Fix #54.


1.2.5 (2013-10-10)
------------------

- cssselect compat. See https://github.com/SimonSapin/cssselect/pull/22

- tests improvments. no longer require a eth connection.

- fix #55

1.2.4
-----

- Moved to github. So a few files are renamed from .txt to .rst

- Added .xhtml_to_html() and .remove_namespaces()

- Use requests to fetch urls (if available)

- Use restkit's proxy instead of Paste (which will die with py3)

- Allow to open https urls

- python2.5 is no longer supported (may work, but tests are broken)

1.2.3
-----

- Allow to pass this in .filter() callback

- Add .contents() .items()

- Add tox.ini

- Bug fixes: fix #35 #55 #64 #66

1.2.2
-----

- Fix cssselectpatch to match the newer implementation of cssselect. Fixes issue #62, #52 and #59 (Haoyu Bai)

- Fix issue #37 (Caleb Burns)

1.2.1
-----

- Allow to use a custom css translator.

- Fix issue 44: case problem with xml documents

1.2
---

- PyQuery now uses `cssselect <http://pypi.python.org/pypi/cssselect>`_. See issue 43.

- Fix issue 40: forward .html() extra arguments to ``lxml.etree.tostring``

1.1.1
-----

- Minor release. Include test file so you can run tests from the tarball.


1.1
---

- fix issues 30, 31, 32 - py3 improvements / webob 1.2+ support


1.0
---

- fix issues 24

0.7
---

- Python 3 compatible

- Add __unicode__ method

- Add root and encoding attribute

- fix issues 19, 20, 22, 23 

0.6.1
------

- Move README.txt at package root

- Add CHANGES.txt and add it to long_description

0.6
----

- Added PyQuery.outerHtml

- Added PyQuery.fn

- Added PyQuery.map

- Change PyQuery.each behavior to reflect jQuery api


