## Introduction

Chatwoot CTL(`cwctl`) is CLI tool to install and manage a self hosted Chatwoot Linux installation.

`cwctl` aims to abstract away the common bash interactions with a Chatwoot installation and provide an easy to use syntax. This is not intended to be a full replacement.

If you are running a Chatwoot v2.7.0 instance or later, `cwctl` would have been already installed for you as part of installation.

Check if `cwctl` is already installed by

```shellscript
cwctl --version
```

If `cwctl` is not present, follow the steps below to install Chatwoot CTL.

### Install or Upgrade Chatwoot CTL

If you used an older version of install script(< 2.0), you will not have `cwctl` in your PATH. To install/upgrade Chatwoot CTL,

```shellscript
wget https://get.chatwoot.app/linux/install.sh -O /usr/local/bin/cwctl && chmod +x /usr/local/bin/cwctl
cwctl --help
```

The above command requires root access to install `cwctl` to `/usr/local/bin`.

### Help

To learn more about the options supported by `cwctl`,

```shellscript
sudo cwctl --help
```

### Upgrading to a newer version of Chatwoot

Whenever a new version of Chatwoot is released, use the following steps to upgrade your instance.

```shellscript
sudo cwctl --upgrade
```

This will upgrade your Chatwoot instance to the latest stable release. If you are running a custom branch in production do not use this to upgrade.

### Upgrading to a specific version or branch

`cwctl` also supports experimental upgrades to a specific Chatwoot version or branch. This is useful when an instance is several releases behind and needs to be upgraded through intermediate versions instead of jumping directly to the latest release. You can also use this to upgrade from a branch such as `develop`.

```shellscript
# Upgrade to a specific released version
sudo cwctl -U v4.3.0

# Upgrade from a branch
sudo cwctl -U develop
```

`-U` / `--Upgrade` is experimental and is not recommended for production environments without testing. When using a release tag like `v4.3.0`, Git may print a pull warning because tags are checked out in a detached HEAD state.

Before upgrading, take a backup, review the release notes for the target version, and keep the Chatwoot repository clean. The upgrade will abort if local code changes are detected.

### Setup Nginx with SSL after installation

To set up Nginx with SSL after initial setup(if you answered `no` to webserver/SSL setup during the first install)

Please add an A record pointing to your Chatwoot instance IP before proceeding.

```shellscript
sudo cwctl --webserver
```

### Restart Chatwoot

```shellscript
sudo cwctl --restart
```

### Running Rails Console

```shellscript
sudo cwctl --console
```

### Viewing Logs

For Chatwoot web(rails) server logs use,

```shellscript
sudo cwctl --logs web
```

For Chatwoot worker(sidekiq) server logs use,

```shellscript
sudo cwctl --logs worker
```

### Version

To check the version of Chatwoot CTL,

```shellscript
sudo cwctl --version
```