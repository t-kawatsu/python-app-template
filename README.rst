===================
python-app-template
===================

.. image:: https://github.com/t-kawatsu/ai-recipe/actions/workflows/test.yml/badge.svg

This is the template repository for python applications that are constructed with Docker.


Stack
-----
- Python 3.9
- Docker
- Poetry
- Make
- Github Actions ( CI / CD tool )


Requirements
------------
- Docker

You need a runtime that installed docker machine for building.


Development
-----------
.. code-block:: bash

  # Build docker image
  $ docker build -t [YOUR APP NAME]-dev/app docker/

  # Set up
  $ docker run --rm -it -v `pwd`:/usr/src/app ai-recipe-dev make setup

  # Run docker image
  $ docker run --rm -it -v `pwd`:/usr/src/app [YOUR APP NAME]-dev/app [cmd]

  # Setup app
  $ make setup

  # Lint
  $ make lint

  # Test
  $ make test

  # Build
  $ make build

  # Run
  $ make run


Deployment
----------

Build Docker image for production
.. code-block:: bash

  # Build
  $ docker build -f docker/Dockerfile.prod -t [YOUR APP NAME]/app --no-cache .

  # Run
  $ docker run --rm -it [YOUR APP NAME]/app


Troubleshooting
---------------


Lisence
-------

LISENCE_.

.. _LISENCE: LISENCE
