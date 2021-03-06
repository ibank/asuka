.. Asuka documentation master file, created by
   sphinx-quickstart on Wed Oct 10 10:32:18 2012.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

アスカ
======

Asuka is a deploy system for Python web apps and it is intended to be
designed to highly depend on Distribute_ (a modern fork of setuptools_),
GitHub_, and `Amazon Web Services`_.

.. _Distribute: http://pypi.python.org/pypi/distribute
.. _setuptools: http://pypi.python.org/pypi/setuptools
.. _GitHub: https://github.com/
.. _Amazon Web Services: http://aws.amazon.com/


Motivation
----------

The main reason why we started to make this is to move fast we should be able
to easily deploy web apps without much risks.  For this we're highly inspired
by `GitHub's internal deploy system`__.

Here's the list of missions we target:

- Every feature (every branch) should be deployed to the testing server
  (EC2_ instance) with isolated state for each other.  It makes features
  able to be independently verified by collaborators.

- If a feature seems to have no problem it should be able to merge into
  the upstream (master).  Fortunately GitHub has made it very easy:
  *pull requests*.

- Every deploy should be able to anytime be rolled back including database
  schema, in a minute at least.

.. _EC2: http://aws.amazon.com/ec2/
__ https://github.com/blog/1241-deploying-at-github


How to install
--------------

Use :program:`pip` or :program:`easy_install`:

.. sourcecode:: console

   $ pip install git+git://github.com/crosspop/asuka.git#egg=Asuka-0.1.0
   $ easy_install https://github.com/crosspop/asuka/tarball/master#egg=Asuka


How to run server
-----------------

It installs :program:`asuka-server` command on your system.
Makes a configuration file (it uses YAML) first by copying :file:`sample.yml`,
and then pass it to :program:`asuka-server` command:

.. sourcecode:: console

   $ asuka-server yourapp.yml


Reference
---------

.. toctree::
   :maxdepth: 2

   asuka


Indices and tables
------------------

- :ref:`genindex`
- :ref:`modindex`
- :ref:`search`
