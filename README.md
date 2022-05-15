# Webarchitects yq Ansible role

[![pipeline status](https://git.coop/webarch/yq/badges/main/pipeline.svg)](https://git.coop/webarch/yq/-/commits/main)

An ansible role to install [yq](https://github.com/mikefarah/yq) on Debian and Ubuntu using binary files downloaded from GitHub.

This role installs a `dpkg_arch.fact` script into `/etc/ansible/facts.d` so that the `dpkg` architecture is available in order to determine which binary to download.

This role has four [default variables](defaults/main.yml):

| Variable name   | Default value   | Comment                                                                                                                |
|-----------------|-----------------|------------------------------------------------------------------------------------------------------------------------|
| `yq`            | `true`          | Run the tasks in this role, set to `false` for all tasks to be skipped                                                 |
| `yq_completion` | `- bash`        | An array of shell completions to install, currently only `bash` is supported                                           |
| `yq_dpkg`       | `/usr/bin/dpkg` | The path for `dpkg`, used by the `dpkg_arch.fact` script                                                               |
| `yq_version`    | `latest`        | Set to a [release version number](https://github.com/mikefarah/yq/releases) to install a version other than the latest |

The primary URL of this repo is [`https://git.coop/webarch/yq`](https://git.coop/webarch/yq) however it is also [mirrored to GitHub](https://github.com/webarch-coop/ansible-role-yq) and [available via Ansible Galaxy](https://galaxy.ansible.com/chriscroome/yq).

If you use this role please use a tagged release, see [the release notes](https://git.coop/webarch/yq/-/releases).

This role can also be used with the [localhost repo](https://git.coop/webarch/localhost) to install `yq` locally.
