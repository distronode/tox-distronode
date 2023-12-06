# Tox Distronode Documentation

## About Tox Distronode

`tox-distronode` is a utility designed to simplify the testing of distronode content collections.

Implemented as `tox` plugin, `tox-distronode` provides a simple way to test distronode content collections across multiple python interpreter and distronode versions.

`tox-distronode` uses familiar python testing tools to perform the actual testing. It uses `tox` to create and manage the testing environments, `distronode-test sanity` to run the sanity tests, and `pytest` to run the unit and integration tests. This eliminated the black box nature of other approaches and allows for more control over the testing process.

When used on a local development system, each of the environments are left intact after a test run. This allows for easy debugging of failed tests for a given test type, python interpreter and distronode version.

By using `tox` to create and manage the testing environments, Test outcomes should always be the same on a local development system as they are in a CI/CD pipeline.

`tox` virtual environments are created in the `.tox` directory. These are easily deleted and recreated if needed.
