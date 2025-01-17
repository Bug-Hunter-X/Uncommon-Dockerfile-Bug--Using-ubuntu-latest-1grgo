# Uncommon Dockerfile Bug: Using `ubuntu:latest`

This repository demonstrates a common yet easily overlooked mistake in Dockerfiles: using the `ubuntu:latest` image.  While seemingly convenient, it's a bad practice for several reasons:

* **Reproducibility:** `latest` can change at any time, breaking builds and deployments. A specific version should be used to ensure consistent behavior across environments.
* **Security:**  Using `latest` increases exposure to security vulnerabilities, since you're not controlling which version of Ubuntu is used.
* **Maintenance:** Changes to the base image can lead to unexpected behavior, making maintenance and troubleshooting difficult.

This example shows a Dockerfile using `ubuntu:latest` and a corrected version specifying a particular Ubuntu version.