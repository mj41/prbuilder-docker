prbuilder-docker
================

[prbuilder-docker](https://github.com/mj41/prbuilder-docker) is set of tools and documentation to build your presentation programmatically with [Presentation::Builder](https://github.com/mj41/Presentation-Builder) (Perl 5) inside [Docker container](https://registry.hub.docker.com/u/mj41/prbuilder/).

Example
-------

See [github.com/mj41/git-course-mj41](https://github.com/mj41/git-course-mj41) repository. 
![Example of Presentation::Builder code and results](https://raw.githubusercontent.com/mj41/prbuilder-docker/master/docs/git-course-example.png)
File [git-course-mj41.pl](https://github.com/mj41/git-course-mj41/blob/master/git-course-mj41.pl#L200)
contains slides definitions (the left side of the image above) to generate presentation's slides 
(the right side of the image) programmatically.

See whole git-course-mj41 presentation on [mj41.cz/static/git-course-mj41-v5](http://mj41.cz/static/git-course-mj41-v5/).

Prerequisities:
* [Docker](https://docs.docker.com/) installed
* internet connection to download [mj41/prbuilder](https://registry.hub.docker.com/u/mj41/prbuilder/) Docker image

HowTo (git-course-mj41 example):

    docker info
    docker pull mj41/prbuilder:stable

    mkdir ~/devel/my-slides
    cd ~/devel/my-slides
    git clone git@github.com:mj41/git-course-mj41.git
    git clone git@github.com:mj41/prbuilder-docker.git
    cd prbuilder-docker
    ./bin/build-slides `pwd`/../git-course-mj41/ git-course-mj41.pl
    firefox `pwd`/../git-course-mj41/final-slides/index.html

Links
-----

* [reveal.js source](https://github.com/hakimel/reveal.js) and [docs](http://lab.hakim.se/reveal-js/#/) 
* [Presentation::Builder](https://github.com/mj41/Presentation-Builder)
* [git-course-mj41](https://github.com/mj41/git-course-mj41)
