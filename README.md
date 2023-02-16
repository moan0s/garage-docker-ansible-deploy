# Garage Docker Ansible Deploy

```bash
ansible-playbook -i inventory/hosts setup.yml --tags=setup-all
```

# Miscellaneous

Set `garage_garage_debian_buster: true` to avoid a bug with debian buster (tested on a raspi 3A) ([more information](https://github.com/dani-garcia/vaultwarden/issues/2497))