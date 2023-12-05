jbcs
====

Install JBoss Core Service.


Dependencies
------------

The roles depends on:

* [middleware_automation.common](https://github.com/ansible-middleware/common)


Role Defaults
-------------

| Parameter | Description | Default |
|:---------|:------------|:--------|
|`jbcs_ssl_enable`| Enable SSL | `True` |
|`jbcs_ssl_port`| SSL listen port | `443` |
|`jbcs_bundle`| Filename of JBCS install archive | `jbcs-httpd24-httpd-2.4.57-RHEL8-x86_64.zip` |
|`jbcs_zip_path`| Destination for install archive download | `/opt/apps` |
|`jbcs_offline_install`| Whether to use local archive or download one | `True` |
|`jbcs_home`| Home directory | `/opt/jbcs/jbcs-httpd24-2.4/` |
|`jbcs_bind_address`| Bind address | `localhost` |
|`jbcs_listen_port`| HTTP listen port | `80` |
|`jbcs_mod_cluster_enable`| Enable modcluster module | `True` |
|`jbcs_mod_cluster_port`| Modcluster advertise port | `6666` |
|`jbcs_mod_cluster_require`| Require argument for modcluster location | `all granted` |
|`jbcs_mod_cluster_balancer`| Balancer name for modcluster cluster | `loadbalancer` |
|`jbcs_user`| POSIX user for service | `apache` |
|`jbcs_user_id`| POSIX uid for service | `48` |
|`jbcs_group`| POSIX group for service | `apache` |
|`jbcs_group_id`| POSIX gid for service | `48` |
|`jbcs_service_name`| Name of systemd service | `jbcs` |
|`jbcs_external_domain_name`| Name for virtualhost ServerName directive | `{{ ansible_nodename }}` |
|`jbcs_configure_firewalld`| Whether to configure firewalld ports for jbcs | `True` |
|`jbcs_port_check`| Whether to check open ports at end of playbook | `False` |
|`jbcs_proxy_pass`| List of proxy pass directives/options. Element keys: path, url, reverse_path, reverse_url | `[]` |
|`jbcs_patch`| Enable security patches install | `True` |
|`jbcs_distro`|Target instance distributrion version | `RHEL8` |
|`jbcs_arch`| Target instance architecture | `x86_64` |
|`jbcs_bundle_prefix`| Filename prefix for JBCS install archives | `jbcs-httpd24-httpd` |


Role Variables
--------------

* No required variables at this time

License
-------

Apache License 2.0


Author Information
------------------

* [Guido Grazioli](https://github.com/guidograzioli)
* [Romain Pelisse](https://github.com/rpelisse)
