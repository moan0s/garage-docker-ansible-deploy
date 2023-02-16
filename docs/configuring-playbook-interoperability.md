# Configuring interoperability with other services

This playbook tries to get you up and running with minimal effort - installing all required services (e.g. Docker).

Sometimes, you're using a server to host multiple services. In such cases these are undesirable:

- multiple playbooks trying to install Docker, etc.

Below, we offer some suggestions for how to make this playbook more interoperable. Feel free to cherry-pick the parts that make sense for your set up.


## Disabling Docker installation

If you're installing [Docker](https://www.docker.com/) on your server in another way, disable this component from the playbook:

```yaml
nextcloud_playbook_docker_installation_enabled: false
```

## Disabling timesyncing (systemd-timesyncd / ntp) installation

If you're installing `systemd-timesyncd` or `ntp` on your server in another way, disable this component from the playbook:

```yaml
devture_timesync_installation_enabled: false
```
