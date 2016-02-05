# Single-node MapR Vagrant Box
This repository includes a sample `Vagrantfile` and the `Readme` on how to use the Single-node MapR Vagrant base box that we have created.
This box is based on the official [`ubuntu/trusty64` box](https://atlas.hashicorp.com/ubuntu/boxes/trusty64) and is based on virtualbox as a provider.

## Whats in the box:
* MapR 5.0.0
* Hive 0.13
* Impala 1.4.1
* Spark 1.5.2

## Requirements
* [Virtualbox](https://www.virtualbox.org/wiki/Downloads)
* [Vagrant](https://www.vagrantup.com/downloads.html)

## How to use the box:
Pretty simple stuff:
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

## Known Issues
Sometimes Impala doesn't work properly and is unable to read the databases from the HiveServer2. This can be solved by restarting impala, by running the following as `mapr` user:
```bash
maprcli node services impalastore restart -nodes `hostname`
maprcli node services impalacatalog restart -nodes `hostname`
maprcli node services impalaserver restart -nodes `hostname`
```
## I'm facing some trouble using your Vagrant box.
Please [open and issue here](https://github.com/hellofresh/mapr-vagrant/issues) or better yet help us fix it.

### We're hiring!
https://www.hellofresh.com/jobs/de/

### Contributors
[Mohannad Ali](https://www.github.com/mandoz)
