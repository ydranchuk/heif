## Building source:
Prerequisites: **[cmake](https://cmake.org/)** and compiler supporting C++11 in PATH.
```
cd heif/build
cmake --help
cmake ../srcs -G"Unix Makefiles"
cmake --build . --config Release
```

## Building Java API
Prerequisites: Java version 8 or newer, Gradle.

First build the C/C++ library as desscribed above.

After that
```
cd heif/build/java-desktop
gradlew build
```

## Publish Library
Follow the [GitHub instructions](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-apache-maven-registry#authenticating-to-github-packages) to create `.m2/settings.xml` file.
Define env variables:
```
GITHUB_ACTOR=<username>
GITHUB_TOKEN=<token>
```
And run `gradlew publish` command
