# Docker Registry

This is the Git clone of the official Docker image for [distribution](https://registry.hub.docker.com/_/registry/).
See the Hub page for the full readme on how to use the Docker image and for information
regarding contributing and issues.

## Run a local registry: Quick Version

$ docker run -d -p 5000:5000 --restart always --name registry -v [/localpath/registry]:/var/lib/registry remonlam/registry:2.6.1

Now, use it from within Docker:

$ docker pull ubuntu
$ docker tag ubuntu localhost:5000/ubuntu
$ docker push localhost:5000/ubuntu
