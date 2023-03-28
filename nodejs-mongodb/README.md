# Notice

This is currently broken.  The outout of Docker build is:
```shell
docker build -t tomjfrog.jfrog.io/docker-examples-virtual/nodejs-mongodb:1 .
[+] Building 1.2s (6/19)                                                                                                                                                                                        
 => [internal] load build definition from Dockerfile                                                                                                                                                       0.0s
 => => transferring dockerfile: 940B                                                                                                                                                                       0.0s
 => [internal] load .dockerignore                                                                                                                                                                          0.0s
 => => transferring context: 2B                                                                                                                                                                            0.0s
 => [internal] load metadata for docker.io/library/ubuntu:precise                                                                                                                                          0.8s
 => [internal] load build context                                                                                                                                                                          0.0s
 => => transferring context: 1.25kB                                                                                                                                                                        0.0s
 => CACHED [ 1/15] FROM docker.io/library/ubuntu:precise@sha256:18305429afa14ea462f810146ba44d4363ae76e4c8dfc38288cf73aa07485005                                                                           0.0s
 => ERROR [ 2/15] RUN apt-get install -y python-software-properties python python-setuptools ruby rubygems                                                                                                 0.3s
------
 > [ 2/15] RUN apt-get install -y python-software-properties python python-setuptools ruby rubygems:
5 0.246 Reading package lists...
5 0.252 Building dependency tree...
5 0.253 Reading state information...
5 0.255 Package python is not available, but is referred to by another package.
5 0.255 This may mean that the package is missing, has been obsoleted, or
5 0.255 is only available from another source
5 0.255 However the following packages replace it:
5 0.255   python-minimal
5 0.255 
5 0.255 E: Unable to locate package python-software-properties
5 0.255 E: Package 'python' has no installation candidate
5 0.255 E: Unable to locate package python-setuptools
5 0.255 E: Unable to locate package ruby
5 0.255 E: Unable to locate package rubygems
------
executor failed running [/bin/sh -c apt-get install -y python-software-properties python python-setuptools ruby rubygems]: exit code: 100
```