# Configuring the playbook

## Preparing the inventory and your variables file (`vars.yml`)

Follow these steps inside the playbook directory:

- create a directory to hold your configuration (`mkdir inventory/host_vars/<your-domain>`)

- copy the sample configuration file (`cp examples/host-vars.yml inventory/host_vars/<your-domain>/vars.yml`)

- edit the configuration file (`inventory/host_vars/<your-domain>/vars.yml`) to your liking. See more in [Configuring Services](#configuring-services).

- copy the sample inventory hosts file (`cp examples/hosts inventory/hosts`)

- edit the inventory hosts file (`inventory/hosts`) to your liking


## Configuring Services

Doing the above preparation step, you're all set to proceed to [Installing](installing.md) with our default recommended configuration.

However, you may wish to tweak a few other things before installing (or any time later) and take a look at the various `defaults/main.yml` files in `roles/` and see if there's anything you'd like to copy over and override in your `vars.yml` configuration file.


## Installing

Once you've configured everything, you can proceed to [Installing](installing.md).

After installation, you can continue changing settings in `vars.yml` and re-running the installation step to make your server consistent with the configuration.
