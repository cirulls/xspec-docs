Installation on Mac and Linux
-----------------------------

Requirements
^^^^^^^^^^^^

Make sure :doc:`requirements` are complete.

Installation
^^^^^^^^^^^^

For this installation the Saxon JAR (e.g. ``saxon9he.jar``) is assumed
to be in ``~/saxon``.

1. Extract `the source code archive file`_ of the latest ``master``
   branch, or alternatively clone the ``master`` branch of XSpec from
   GitHub:

   .. code:: bash

      git clone https://github.com/xspec/xspec.git

   For this installation XSpec is assumed to be extracted or cloned to
   ``~/xspec``.

2. Set up the Saxon environment variable. You can either set
   ``SAXON_CP`` to the full classpath containing the Saxon jar file:

   .. code:: bash

      export SAXON_CP=~/saxon/saxon9he.jar

   or alternatively set ``SAXON_HOME`` to the location of the Saxon jar
   file:

   .. code:: bash

      export SAXON_HOME=~/saxon

   You can check that the environment variable is set with:

   .. code:: bash

      echo $SAXON_CP

   ``SAXON_CP`` has precedence over ``SAXON_HOME``.

   If you want to make the change permanent, set the environment
   variable in your shell profile (e.g. ``~/.bashrc`` or
   ``~/.bash_profile``).

3. Open up a terminal, navigate to ``~/xspec``, make sure that the file
   ``bin/xspec.sh`` is executable, and test the shell script with this
   command:

   .. code:: bash

      bin/xspec.sh -h

   The output should be the following usage summary:

   .. code:: console

      Usage: xspec [-t|-q|-s|-c|-j|-catalog file|-h] file

        file           the XSpec document
        -t             test an XSLT stylesheet (the default)
        -q             test an XQuery module (mutually exclusive with -t and -s)
        -s             test a Schematron schema (mutually exclusive with -t and -q)
        -c             output test coverage report (XSLT only)
        -j             output JUnit report
        -catalog file  use XML Catalog file to locate resources
        -e             treat failed tests as error
        -h             display this help message

Congratulations! You have successfully installed XSpec!

To make the XSpec script more portable and invoke it from anywhere, add
a script invoking ``xspec.sh`` in ``/usr/bin``. To move ``xspec.sh`` out
of the XSpec installation directory, you must set the environment
variable ``XSPEC_HOME`` to the location where XSpec is stored.

.. _requirements: requirements
.. _the source code archive file: https://github.com/xspec/xspec/archive/master.zip
