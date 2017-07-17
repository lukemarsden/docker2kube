# Docker2Kube

Go:

* _from_ a Docker image for a program that runs on a port
* _to_ the simplest possible Kubernetes config that runs that program

In more technical words:

Create a boilerplate Kubernetes deployment-service pair for a given container image.

## Usage

```
$ cd myprogram
$ ls
Dockerfile main.go
$ docker build -t myprogram:v1 .
[...]
$ cd ..
$ mkdir myprogram-config
$ git init .
$ docker2kube myprogram:v1
$ git add *.yaml
$ git commit -am "Initial config"
```

## What next?

Once you've pushed Kubernetes config to a git repo, the practice known as _GitOps_ will help you get configs in version control reliably into a running application.

TODO: link to a public doc about _GitOps_.
