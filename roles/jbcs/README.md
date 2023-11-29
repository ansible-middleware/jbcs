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
|`ssl_enable`| Enable SSL | `True` |
|`ssl_port`| SSL listen port | `443` |
|`bundle`| Filename of JBCS install archive | `jbcs-httpd24-httpd-2.4.57-RHEL8-x86_64.zip` |
|`zip_path`| Destination for install archive download | `/opt/apps` |
|`offline_install`| Whether to use local archive or download one | `True` |
|`home`| Home directory | `/opt/jbcs/jbcs-httpd24-2.4/` |
|`bind_address`| Bind address | `localhost` |
|`listen_port`| HTTP listen port | `80` |
|`mod_cluster_enable`| Enable modcluster module | `True` |
|`mod_cluster_port`| Modcluster advertise port | `6666` |
|`mod_cluster_require`| Require argument for modcluster location | `all granted` |
|`mod_cluster_balancer`| Balancer name for modcluster cluster | `loadbalancer` |
|`user`| POSIX user for service | `apache` |
|`user_id`| POSIX uid for service | `48` |
|`group`| POSIX group for service | `apache` |
|`group_id`| POSIX gid for service | `48` |
|`service_name`| Name of systemd service | `jbcs` |
|`external_domain_name`| Name for virtualhost ServerName directive | `{{ ansible_nodename }}` |
|`configure_firewalld`| Whether to configure firewalld ports for jbcs | `True` |
|`port_check`| Whether to check open ports at end of playbook | `False` |
|`proxy_pass`| List of proxy pass directives/options. Element keys: path, url, reverse_path, reverse_url | `[]` |


Role Variables
--------------


License
-------

Apache License 2.0


Author Information
------------------

* [Guido Grazioli](https://github.com/guidograzioli)
* [Romain Pelisse](https://github.com/rpelisse)
