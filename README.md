Heroku buildpack: Racket
========================

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) for Racket apps.
It uses [Racket](http://racket-lang.org).

Usage
-----

Example usage:

    $ cat Procfile
    web: run/bin/heroku-setup
    $ ls
    Procfile heroku-setup.rkt

    $ heroku create --stack cedar --buildpack http://github.com/onixie/heroku-buildpack-racket.git

    $ git push heroku master
    ...
    -----> Heroku receiving push
    -----> Fetching custom buildpack
    -----> Racket Framework app detected
    -----> Building Racket Runtime Environment
    ...

The buildpack will detect that your app has a `heroku-setup.rkt` in the root directory.

Hacking
-------

To use this buildpack, fork it on Github.  Push up changes to your fork, then create a test app with `--buildpack <your-github-url>` and push to it.
