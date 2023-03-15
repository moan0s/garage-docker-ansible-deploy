# 2023-03-15

* BREAKING CHANGE: Most variables have changed their name. Check `examples/host-vars.yml` to find the new names (usually `garage_garage_<var>` -> `garage_<var>`)
* Moved the main role to https://github.com/moan0s/role-garage to make it usable in [Mother-of-All-Self-Hosting Ansible playbook](https://github.com/mother-of-all-self-hosting/mash-playbook)

# 2023-03-10

The systemd services are renamed to use a `-` instead of `_`. If you already use this playbook that means:

* Stop all garage nodes (`ansible-playbook -i inventory/hosts setup.yml --tags=stop`)
* Delete the old service files (e.g `/etc/systemd/systemd/garage_node1.service`)
* Pull the new playbook
* Rerun the playbook & start the services ``
* Check if everything works again.

# 2023-02-27

First version of this playbook is announced publicly