# Heat templates for stable/mitaka

In this directory you will find the following Heat templates:

* *cinder-encrypted.yaml:* builds an instance and attaches an encrypted Cinder volume to it
* *lbaas.yaml:* builds two instances behind a SSL enabled keystore

For these Heat templates to work, you will need to adapt some configuration
settings for the following services:

* `Cinder`
* `Heat`
* `Nova`
* `Neutron`

You will find commented configuration snippets for all affected files in the
`etc/` subdirectory. Both Heat templates contain a comment with an example Heat
client invocation at the top. You will probably have to modify this slighly for
your own use.

For encrypted Cinder volumes to work through Heat, you will also need to apply
the patch attached to this bug (only available for Mitaka right now, but stay
tuned):

https://bugs.launchpad.net/cinder/+bug/1631078
