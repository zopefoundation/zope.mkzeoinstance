Changelog
=========

4.2 (unreleased)
----------------

- Add support for Python 3.7, 3.8 and 3.9.

- Drop support for Python 3.4.


4.1 (2017-05-26)
----------------

- Fix generated ``runzeo`` and ``zeoctl`` scripts to run with ZEO 5.


4.0 (2017-02-28)
----------------

- 100% unit test coverage.

- Drop support for Python 2.6.

- Add support for Python 3.4, 3.5, and 3.6.

- Move dependency from ``ZODB3`` -> [``zdaemon``, ``ZODB``, ``ZEO``].
  Even though this package doesn't actually import anything from the last
  two, the generated instance won't be usable unless the host python
  has them installed.

3.9.6 (2014-12-23)
------------------

- Add support for testing on Travis, and with tox.


3.9.5 (2011-10-31)
------------------

- Place the socket used by the ``zeoctl`` control process to conmmunicate
  with its ``runzeo`` daemaon in ``$INSTANCE_HOME/var``, instead of
  ``$INSTANCE_HOME/etc`` (which would idealy not be writable by the process).
  See: https://bugs.launchpad.net/zope.mkzeoinstance/+bug/175981


3.9.4 (2010-04-22)
------------------

- Rename the script / package ``mkzeoinstance`` to avoid clashing with the
  script bundled with ZODB.

- Add an option to spell the host interface to be listened on, as well as
  the port the generated ZEO server configuration.  Thanks to Igor Stroh
  for the patch.  See: https://bugs.launchpad.net/zodb/+bug/143361

- Fix generated templates to cope with the move of ``zdaemon`` code into
  its own project.

- Fork from the version of the ``mkzeoinst`` script contained in
  ZODB 3.9.4.
