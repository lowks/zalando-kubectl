===============
Zalando Kubectl
===============

.. image:: https://travis-ci.org/zalando-incubator/zalando-kubectl.svg?branch=master
   :target: https://travis-ci.org/zalando-incubator/zalando-kubectl
   :alt: Build Status

.. image:: https://coveralls.io/repos/zalando-incubator/zalando-kubectl/badge.svg
   :target: https://coveralls.io/r/zalando-incubator/zalando-kubectl
   :alt: Code Coverage

.. image:: https://img.shields.io/pypi/dw/zalando-kubectl.svg
   :target: https://pypi.python.org/pypi/zalando-kubectl/
   :alt: PyPI Downloads

.. image:: https://img.shields.io/pypi/v/zalando-kubectl.svg
   :target: https://pypi.python.org/pypi/zalando-kubectl/
   :alt: Latest PyPI version

.. image:: https://img.shields.io/pypi/l/zalando-kubectl.svg
   :target: https://pypi.python.org/pypi/zalando-kubectl/
   :alt: License

Kubernetes CLI (kubectl) wrapper in Python with OAuth token authentication.

This wrapper script ``zkubectl`` serves as a drop-in replacement for the ``kubectl`` binary:

* it downloads the current ``kubectl`` binary from Google
* it generates a new ``~/.kube/config`` with an OAuth Bearer token acquired via `zign`_.
* it passes through commands to the ``kubectl`` binary


Installation
============

Requires Python 3.4+.

.. code-block:: bash

    $ sudo pip3 install --upgrade zalando-kubectl

Usage
=====

.. code-block:: bash

    $ zkubectl login https://my-api-server.example.org
    $ zkubectl cluster-info

Unit Tests
==========

Run unit tests with Tox:

.. code-block:: bash

    $ sudo pip3 install tox
    $ tox

.. _zign: https://pypi.python.org/pypi/stups-zign
