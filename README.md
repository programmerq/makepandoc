#Pandoc docker image

I had some documentation that I generated with pandoc + make, so I created this image to work with it.

An example project might look like this:

README.md:

    Hello World!

Makefile:

    README.html: README.md
    	pandoc -f markdown -t html -o README.html README.md

Then to use this image, simply run:

    docker run --rm -v $(pwd):/sources programmerq/pandoc
