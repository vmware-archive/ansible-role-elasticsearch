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
 
Copyright 2015 VMware, Inc.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

