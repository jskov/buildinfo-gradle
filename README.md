# buildinfo-gradle

A Gradle plugin that enables [reproducible builds](https://reproducible-builds.org/) by providing [buildinfo](https://reproducible-builds.org/docs/jvm) when publishing Maven artifacts.

## Using the Plugin

Add plugin activation to the build file header (substitute the relevant version):

    plugins {
        ...
        id 'dk.mada.buildinfo' version '1.n.n'
    }

And make sure the plugin can be fetched from MavenCentral:

    pluginManagement {
        repositories {
            gradlePluginPortal()
            mavenCentral()
        }
    }


## Development

For testing snapshot builds in other projects:

```console
$ ./gradlew -t publishToMavenLocal -Pversion=0.0.1
```
