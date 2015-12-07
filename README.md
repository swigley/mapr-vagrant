# MapR Vagrant Box
This repository includes a sample `Vagrantfile` and the `Readme` on how to use the MapR Vagrant base box that we have created.
This box is based on the official [`ubuntu/trusty64` box](https://atlas.hashicorp.com/ubuntu/boxes/trusty64)

## Whats in the box:
* MapR 5.0.0
* Hive 0.13
* Impala 1.4.1
* Spark 1.3.1

## How to use the box:
Pretty simple stuff
```
vagrant init hellofresh/mapr
vagrant up
```

## What are the `mapr` user credentials?
```
Username: mapr
Password: mapr
```

## What do I need to do after I do `vagrant up`?
- Add `10.10.10.30 mapr-dev` to your `/etc/hosts` file. Make sure you change the IP if you had overwritten that in your vagrant file.
- Point your browser to `https://mapr-dev:8443`, login with the `mapr` user credentials, and add a community license to your installation.
- Code away!

## Can I use this in production?
We advise against it.

## I'm facing some trouble using your Vagrant box.
Please [open and issue here](https://github.com/hellofresh/mapr-vagrant/issues) or better yet help us fix it.
