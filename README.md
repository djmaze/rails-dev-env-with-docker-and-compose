## Installation

* Optionally, install [docker-ssh-agent-forward](https://github.com/djmaze/docker-ssh-agent-forward) if you need to install private gems or deploy via SSH.
* Copy the script [bundle-package-all-with-docker](bundle-package-all-with-docker) into your path:

      curl -sL https://github.com/djmaze/rails-dev-env-with-docker-and-compose/raw/master/bundle-package-all-with-docker | sudo tee /usr/local/bin/bundle-package-all-with-docker 1>/dev/null
      sudo chmod +x /usr/local/bin/bundle-package-all-with-docker

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

