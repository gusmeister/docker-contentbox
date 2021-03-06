# Changelog

## v3.1.3

* Adding healtcheck URIs back again
* Removed redundant calls to CommandBox layer
* Added warmup servers to main tags due to lucee orm bug.

## v3.1.2

* Don't warm up servers to reduce image size
* Add Adobe 11, 2018 images that where not running
* Tag versions of each of the warmed up engines, instead of just latest

## v3.1.1

* Remove some cleanup scripts to avoid issues

## v3.1.0

* Added new environment variables to control heap size: `JVM_HEAPSIZE` which defaults to `512mb`
* Updated CommandBox main image to 4.2.0
* Upgrade to ContentBox v4.1.0
* Removed legacy media root directory and leverage new custom module location: `/app/modules_app/contentbox-custom`
* Added Adobe 2018 Tag
* Updated distributed example with Redis

## v3.0.0

* Optimize for size
* Remove static healthcheck and just rely on the CommandBox image healthcheck, which makes more sense
* Removed some debugging files
* Updated CommandBox to 4.0.0
* `ORM_DIALECT` was not being used in the right place.
* `EXPRESS` and `HEADLESS` was not evaluated to a boolean, just existence 
* Removed usage of lowercase `install`, `be`, and `express`, you must use uppercase env variables.
* Added `lucee5` to snapshot releases
* Renamed `HEADLESS` flag so we don't clash with the CommandBox image. New Setting is `REMOVE_CBADMIN`
* Added Alpine version for ContentBox

## v2.4.0

* Added Router to handle full rewrites, which it should by default
* Rewrites should be added by default if no server.json is defined

## v2.3.0

* Added ContentBox v4.0.0 support
* Added new `HEADLESS` environment setting so the admin does not get deployed if passed

## v2.2.0

* Updated config for conflicted distributed cache setting