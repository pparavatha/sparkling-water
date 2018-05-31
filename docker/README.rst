Docker Support
==============

Create DockerFile
-----------------
At the project root folder

    $ gradle createDockerFile -x test

DockerFile will be created in the directory docker/sparkling-water/base/

Container requirements
----------------------

To run Sparkling Water in the container, the host has to provide a
machine with at least 5G of total memory. If this is not met, Sparkling
Water scripts print warning but still attempt to run.

Building a container image
--------------------------

    $ cd docker/sparkling-water/base/

    $ docker build -t sparkling-water-base:v0.1 -f Dockerfile .

Run bash inside container
-------------------------

    $ docker run -i --name sparkling-water-base-instance-v0.1 -t sparkling-water-base:v0.1  /bin/bash


Run Sparkling Shell inside container
------------------------------------

    $ docker run -i --name sparkling-water-base-instance-v0.1 -t sparkling-water-base:v0.1  bin/sparkling-shell

Running examples in container
-----------------------------

    $ docker run -i --name sparkling-water-base-instance-v0.1 -t sparkling-water-base:v0.1  bin/run-example.sh

