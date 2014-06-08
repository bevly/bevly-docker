# Bevly Docker build

This project sets up a Docker container for the Bevly server
components, building the different pieces and assembling them into a
container.

## Prequisites

1. [Docker](https://www.docker.io/)
2. [npm](https://www.npmjs.org/)
3. [Bower](http://bower.io/)
4. A unixy environment for the shell scripts; either an actual Unix,
   or msys on Windows.

## Build

Run this command to create a bevly/bevly Docker image:

    $ ./create-deploy-image

You may then run the image directly, or package it up with `docker
save` and ship it to the production server.