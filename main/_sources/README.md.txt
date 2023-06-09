# Ansible Collection - middleware_automation.jbcs
<!--start build_status -->
[![Build Status](https://github.com/ansible-middleware/jbcs/workflows/CI/badge.svg?branch=main)](https://github.com/ansible-middleware/jbcs/actions/workflows/ci.yml)

<!--end build_status -->
Collection to install and configure JBoss Core Services as a reverse proxy / modcluster instance.

<!--start requires_ansible-->
## Ansible version compatibility

This collection has been tested against following Ansible versions: **>=2.9.10**.

Plugins and modules within a collection may be tested with only specific Ansible versions. A collection may contain metadata that identifies these versions.
<!--end requires_ansible-->


## Installation

<!--start galaxy_download -->
### Installing the Collection from Ansible Galaxy

Before using the collection, you need to install it with the Ansible Galaxy CLI:

    ansible-galaxy collection install middleware_automation.jbcs

<!--end galaxy_download -->

You can also include it in a `requirements.yml` file and install it via `ansible-galaxy collection install -r requirements.yml`, using the format:

```yaml
---
collections:
  - name: middleware_automation.jbcs
```


### Included roles

* [`jbcs`](https://github.com/ansible-middleware/jbcs/blob/main/roles/jbcs/README.md): role for installing the service.


### Usage

Using all default values, the collection is invoked from a playbook as follows:

```
- name: Converge
  hosts: all
  collections:
    - middleware_automation.jbcs
  roles:
    - jbcs
```

<!--start support -->
<!--end support -->

## License

Apache License v2.0 or later

See [LICENSE](LICENSE) to view the full text.

