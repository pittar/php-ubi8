# PHP 7.4 and 8.0 UBI8 Images - Without s2i

## Base

The `Containerfile` in the `base` directory will build a base PHP container image.

## App

The `Containerfile` in the `app` directory will use the base image in its `FROM` line, then simply add in PHP files.


## Build

In both cases, you can build the images with podman or docker:

```
# From base dir.
cd base/7.4 
podman build -t php74-ubi8-base .

# OR, build PHP 8.0

cd base/8.0
podman build -t php80-ubi8-base .

# From app dir.
podman build -t php-app .
```

Based on [this Red Hat Blog entry](https://developers.redhat.com/blog/2020/03/24/red-hat-universal-base-images-for-docker-users#red_hat_enterprise_linux_and_docker).

More to come!
