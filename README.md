## Installation

Copy / symlink these scripts to somewhere in your `PATH`.

## Getting started with an existing app

(Note: You have to prefix all commands with `sudo -E` if you need to run Docker as root).

* Use the [`ruby`](https://hub.docker.com/_/ruby/) base image (with the version needed) in your Dockerfile.

* In your project directory, fetch all gems one-time:

      bundle-package-all-with-docker

* Then do a `docker build` as usual.

You need to re-run `bundle-package-all-with-docker` when your Gemfile is changed.

## Setting up a new rails app

In a new directory, run:

    touch Gemfile
    bundle-package-all-with-docker
    gem install rails
    rails new

## Using Docker Compose

TBD

