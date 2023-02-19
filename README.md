# Garage Docker Ansible Deploy

![Garage Logo](docs/assets/garage-logo.svg)

Garage is an open-source distributed object storage service tailored for self-hosting. This playbook helps you to set up
such a cluster:

- on your own Debian/CentOS/RedHat server(s). Raspberry Pi is also supported
- with everything run in [Docker](https://www.docker.com/) containers
- powered by [the official Garage container image](https://hub.docker.com/r/dxflrs/garage)
- [interoperates nicely](docs/configuring-playbook-interoperability.md) with [related](#related) Ansible playbooks or other services using Traefik for reverse-proxying

## Planned Features

* Reverse Proxy automatically managed by [Traefik](https://traefik.io).
* Documentation explaining on how to run this playbook on multiple nodes
* Gatway node support

## Installing

To configure and install Garage on your own server(s), follow the [README in the docs/ directory](docs/README.md).

## Support

- Matrix room: [#garage-docker-ansible-deploy:hyteck.de](https://matrix.to/#/#garage-docker-ansible-deploy:hyteck.de)

- Github issues: [moan0s/garage-docker-ansible-deploy/issues](https://github.com/moan0s/garage-docker-ansible-deploy/issues)

## Related

This playbook started as a copy of these projects and aims to have a similar layout and reuse some roles. Check them out!

- [matrix-docker-ansible-deploy](https://github.com/spantaleev/matrix-docker-ansible-deploy) - for deploying a fully-featured [Matrix](https://matrix.org) homeserver

- [gitea-docker-ansible-deploy](https://github.com/spantaleev/gitea-docker-ansible-deploy) - for deploying a [Gitea](https://gitea.io) (self-hosted [Git](https://git-scm.com/) service) server

- [vaultwarden-docker-ansible-deploy](https://github.com/spantaleev/vaultwarden-docker-ansible-deploy) - for deploying a [Vaultwarden](https://github.com/dani-garcia/vaultwarden) password manager server (unofficial [Bitwarden](https://bitwarden.com/) compatible server)

# Miscellaneous

Set `garage_garage_debian_buster: true` to avoid a bug with debian buster (tested on a raspi 3A) ([more information](https://github.com/dani-garcia/vaultwarden/issues/2497))

# Developer Notes

`Use ansible_facts[‘distribution_major_version’]` instead of `garage_garage_debian_buster`