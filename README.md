# Garage Docker Ansible Deploy

```bash
ansible-playbook -i inventory/hosts setup.yml --tags=setup-all
```

# Miscellaneous

Set `garage_garage_debian_buster: true` to avoid a bug with debian buster (tested on a raspi 3A) ([more information](https://github.com/dani-garcia/vaultwarden/issues/2497))

# Made possible by

[spantaleev](https://github.com/spantaleev/matrix-docker-ansible-deploy) as they develop amazing roles like [matrix-docker-ansible-deploy](https://github.com/spantaleev/nextcloud-docker-ansible-deploy) and [matrix-docker-ansible-deploy](https://github.com/spantaleev/nextcloud-docker-ansible-deploy).
This playbook started as a copy of these projects and aims to have a similar layout and reuse some roles.