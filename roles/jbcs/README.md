jbcs
====

Install JBoss Core Service.


Dependencies
------------

The roles depends on:

* the `redhat_csp_download` role from [middleware_automation.redhat_csp_download](https://github.com/ansible-middleware/redhat-csp-download) collection if Red Hat Single Sign-on zip have to be downloaded from RHN.


Role Defaults
-------------

| Variable | Description | Default |
|:---------|:------------|:--------|
|`jbcs_ssl_enable`| Enable SSL | `True` |
|`jbcs_ssl_port`| SSL listen port | `443` |
|`jbcs_bundle`| Filename of JBCS install archive | `jbcs-httpd24-httpd-2.4.37-SP11-RHEL8-x86_64.zip` |
|`jbcs_zip_path`| Destination for install archive download | `/opt/apps` |
|`jbcs_home`| Home directory | `/opt/jbcs/jbcs-httpd24-2.4/` |
|`jbcs_bind_address`| Bind address | `localhost` |
|`jbcs_listen_port`| HTTP listen port | `80` |
|`jbcs_mod_cluster_enable`| Enable modcluster module | `False` |
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


Role Variables
--------------


License
-------

Apache License 2.0


Author Information
------------------

* [Guido Grazioli](https://github.com/guidograzioli)
* [Romain Pelisse](https://github.com/rpelisse)
