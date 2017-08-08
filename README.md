WP-CLI Automated Tests
======================

This repository runs automated tests for the nightly Phar builds of WP-CLI.

[![Build Status](https://travis-ci.org/wp-cli/phar-build.svg?branch=master)](https://travis-ci.org/wp-cli/phar-build)

## Usage Instructions

The testing is set up through the use of environment variables in the Travis CI matrix configuration.

### Testing source packages

`$TEST_PACKAGE` enables tests against source packages. You can select which commands/packages to test.

The following options can be set:

* **`none`** - No packages are tested.
* **`all`** - The framework as well as all bundled commands are tested.
* **`commands`** - Only the command packages are tested.
* **`<package name>`** - Only the package named <package name> is tested.

### Testing against Phar distributions

`$TEST_PHAR` enables tests against the Phar distributions. You can select which distribution to test. The selected distribution will be tested against all bundled commands/packages.

The following options can be set:

* **`none`** - Skip phar testing.
* **`nightly`** - Use the nightly phar.
* **`stable `** - Use the latest stable phar release.
* **`all`** - Use both the latest stable release phar as well as the nightly phar.
