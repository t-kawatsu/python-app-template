===================
python-app-template
===================

This is the template repository for python applications that are constructed with Docker.


Stack
-----
- Python 3.9
- Docker
- Poetry
- Make


Requirements
------------
- Docker

You need a runtime that installed docker machine for building.


Development
-----------
.. code-block:: bash

  # Build docker image
  $ docker build -t [YOUR APP NAME]-dev/app docker/

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


Troubleshooting
---------------


Lisence
-------

