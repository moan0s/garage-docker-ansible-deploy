# 2023-03-10

The systemd services are renamed to use a `-` instead of `_`. If you already use this playbook that means:
* Stop all garage nodes (`ansible-playbook -i inventory/hosts setup.yml --tags=stop`)
* Delete the old service files (e.g `/etc/systemd/systemd/garage_node1.service`)
* Pull the new playbook
* Rerun the playbook & start the services ``
* Check if everything works again.

# 2023-02-27

First version of this playbook is announced publicly