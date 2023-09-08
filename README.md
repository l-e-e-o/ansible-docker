# Ansible Role: docker
A simple Ansible role to install [Docker](https://www.docker.com/).

## Configuration options
| Variable              | Default                                                                                                                                        | Explanation                                                                                                                                                                                                                                |
| --------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `docker_edition`      | `ce`                                                                                                                                           | `ce` for Community Edition or `ee` for Enterprise Edition                                                                                                                                                                                  |
| `docker_packages`     | <code>- "docker-[ce/ee]"<br>- "docker-[ce/ee]-cli"<br><br>- "containerd.io"<br>- "docker-buildx-plugin"<br>- "docker-compose-plugin"</code> | Docker packages to install                                                                                                                                                                                                                 |
| `docker_log_max_size` | `10m`                                                                                                                                          | Sets the docker daemon [configuration variable](https://docs.docker.com/config/containers/logging/local/#options) `log-opts.max-size` in `/etc/docker/daemon.json` to prevent the accumulation of large amounts of logs consuming storage. |
| `docker_log_max_file` | `3`                                                                                                                                            | Sets the docker daemon [configuration variable](https://docs.docker.com/config/containers/logging/local/#options) `log-opts.max-file` in `/etc/docker/daemon.json` to prevent the accumulation of large amounts of logs consuming storage. |
| `http_proxy` | `""` | Proxy for HTTP |
| `https_proxy` | `""` | Proxy for HTTPS |
| `no_proxy` | `""` | Proxy exception list |

## Supported distributions
Currently this role supports the following distributions:

- Ubuntu
  - 20.04
  - 22.04
  - 22.10
  - 23.04