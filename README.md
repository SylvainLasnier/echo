echo docker tutorial image
==========================

This is a docker tutorial.  
This image run a tiny container send an echo


I use tiny OS Busybox to this test. The image size is 2.5Mb

You could use this image following these steps :

    docker pull  sylvainlasnier/echo
    docker run --rm sylvainlasnier/echo Hello World!
    Hello World!

You could also rebuild this image following these steps :

Edit Dockerfile file

    FROM busybox
    MAINTAINER I do it myself
    
    ENTRYPOINT ["/bin/echo"]

Build the image

    docker build -t myecho .

Check the running image

    docker images 
    REPOSITORY               TAG                 IMAGE ID            CREATED             VIRTUAL SIZE
    myecho                     latest              4eceb31af65a        10 minutes ago      2.489 MB

Enjoy

    docker run --rm myecho Hello World!
    Hello World!

You are an docker expert!

Have fun and try my other [docker images](https://hub.docker.com/u/sylvainlasnier/) ^^
