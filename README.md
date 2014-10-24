docker-unattended-upgrade
=========================

Ubuntu image with daily unattended upgrade for security updates.

The image simply installs unattended-upgrade and supervisor with two simple scripts:

1. `install` to configure supervisor to run cron
2. `start` adds a cron job to call `unattended-upgrade` and start supervisor

This only to ensure that security updates are installed automatically in production untill a new update docker
image is pushed and deployed with latest security updates.

The image can be pulled from docker hub directly

`docker run itech/base-unattended-upgrade`

or used as a base image by defining the Dockerfile as following

    FROM itech/base-unattended-upgrade
    # Rest of your Dockerfile
