# Webarchitects yc Ansible role

An ansible role to install [yq](https://github.com/mikefarah/yq) on Debian and Ubuntu using binary files downloaded from GitHub.

This role installs a `dpkg_arch.fact` script into `/etc/ansible/facts.d` so that the `dpkg` architecture is available in order to determine which binary to download.

This role has two [default variables](defaults/main.yml):

| Variable name | Default value | Comment                                                                                                                |
|---------------|---------------|------------------------------------------------------------------------------------------------------------------------|
| `yq`          | `true`        | Run the tasks in this role, set to `false` for all tasks to be skipped                                                 |
| `yq_version`  | `latest`      | Set to a [release version number](https://github.com/mikefarah/yq/releases) to install a version other than the latest |

