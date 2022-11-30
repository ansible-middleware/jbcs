# Ansible Collection - middleware_automation.jbcs

[![Build Status](https://github.com/ansible-middleware/jbcs/workflows/CI/badge.svg?branch=main)](https://github.com/ansible-middleware/jbcs/actions/workflows/ci.yml)


Collection to install and configure JBoss Core Services. 

<!--start requires_ansible-->
## Ansible version compatibility

This collection has been tested against following Ansible versions: **>=2.9.10**.

Plugins and modules within a collection may be tested with only specific Ansible versions. A collection may contain metadata that identifies these versions.
<!--end requires_ansible-->


## Installation

### Installing the Collection from Ansible Galaxy

Before using the collection, you need to install it with the Ansible Galaxy CLI:

    ansible-galaxy collection install middleware_automation.jbcs

You can also include it in a `requirements.yml` file and install it via `ansible-galaxy collection install -r requirements.yml`, using the format:

```yaml
---
collections:
  - name: middleware_automation.jbcs
```

The jbcs collection also depends on the following python packages to be present on the controller host:

* netaddr

A requirement file is provided to install:

    pip install -r requirements.txt


### Included roles

* [`jbcs`](https://github.com/ansible-middleware/jbcs/blob/main/roles/jbcs/README.md): role for installing the service.


## Usage

TODO


## License

Apache License v2.0 or later

See [LICENSE](LICENSE) to view the full text.

