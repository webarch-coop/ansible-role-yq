# Webarchitects yq Ansible role

[![pipeline status](https://git.coop/webarch/yq/badges/main/pipeline.svg)](https://git.coop/webarch/yq/-/commits/main)

An ansible role to install [yq](https://github.com/mikefarah/yq) on Debian and Ubuntu using binary files downloaded from GitHub.

## Role Variables

This role has four [default variables](defaults/main.yml), set `yq` to `true` for the tasks in this role to be run, it defaults to `false`, see also the [meta/argument_specs.yml](meta/argument_specs.yml).

| Variable name   | Default value | Comment                                                                                                                |
|-----------------|---------------|------------------------------------------------------------------------------------------------------------------------|
| `yq`            | `false`       | Run the tasks in this role, set to `false` for all tasks to be skipped                                                 |
| `yq_completion` | `- bash`      | An array of shell completions to install, currently only `bash` is supported                                           |
| `yq_verify`     | `true`        | Verify all variables that start with `yq_`                                                                             |
| `yq_version`    | `latest`      | Set to a [release version number](https://github.com/mikefarah/yq/releases) to install a version other than the latest |

## Usage

This role can also be used with the [localhost repo](https://git.coop/webarch/localhost) to install `yq` locally.

## Repository

The primary URL of this repo is [`https://git.coop/webarch/yq`](https://git.coop/webarch/yq) however it is also [mirrored to GitHub](https://github.com/webarch-coop/ansible-role-yq) and [available via Ansible Galaxy](https://galaxy.ansible.com/chriscroome/yq).

If you use this role please use a tagged release, see [the release notes](https://git.coop/webarch/yq/-/releases).

## Copyright

Copyright 2022-2023 Chris Croome, &lt;[chris@webarchitects.co.uk](mailto:chris@webarchitects.co.uk)&gt;.

This role is released under [the same terms as Ansible itself](https://github.com/ansible/ansible/blob/devel/COPYING), the [GNU GPLv3](LICENSE).
