# Docker Registry

This is the Git clone of the official Docker image for [distribution](https://registry.hub.docker.com/_/registry/).<br>
See the Hub page for the full readme on how to use the Docker image and for information regarding contributing and issues.

## Build image yourself
Copy this repo to you're machine.<br>
$ docker build -t registry:2.6.1 .

## Run a local registry
$ docker run -d -p 5000:5000 --restart always --name registry -v [/localpath/registry]:/var/lib/registry remonlam/registry:2.6.1

Now, use it from within Docker:<br>
<br>
$ docker pull ubuntu<br>
$ docker tag ubuntu localhost:5000/ubuntu<br>
$ docker push localhost:5000/ubuntu<br>
