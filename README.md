# PHP 7.4 UBI Image - Without s2i

## Base

The `Containerfile` in the `base` directory will build a base PHP container image.

## App

The `Containerfile` in the `app` directory will use the base image in its `FROM` line, then simply add in PHP files.


## Build

In both cases, you can build the images with podman or docker:

```
# From base dir.
podman build -t php74-ubi8-base .

# From app dir.
podman build -t php-app .
```
