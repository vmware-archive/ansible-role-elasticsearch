# ansible-role-elasticsearch

Ansible playbook to automate installing and maintaining elasticsearch containers.

## Requirements

This role currently requires a working VMware Photon server with enabled Docker environment.

## Role Variables

```yaml
# Memory limit for the container, where zero means no limit.
memory_limit: 0MB

# Temporary space (path) to use for building the container.
elasticsearch_docker_build: /tmp/elasticsearch

#  The Docker image to produce or update.
elasticsearch_docker_image: openedge/elasticsearch

#  The default cluster name for the elasticsearch nodes.
elasticsearch_cluster_name: default_clustername

#  The log level. Typical values are INFO, WARN or DEBUG.
elasticsearch_log_level: INFO
```

## Example playbook

```
---
- hosts: elasticsearch
  sudo: True
  roles:
    - elasticsearch
  vars:
    - ... forthcoming
```

# License and Copyright
 
Copyright 2015 VMware, Inc.  All rights reserved.

SPDX-License-Identifier: Apache-2.0 OR GPL-3.0-only

This code is Dual Licensed Apache-2.0 or GPLv3

