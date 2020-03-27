# ansible-quay
Ansible roles &amp; playbooks to install Quay &amp; Clair (Non OpenShift environment).

Based on code of the infra-ansible Red Hat CoP repository: https://github.com/redhat-cop/infra-ansible.

A heavy-lifting to the Ansible code to install Quay 3.X. in stand-alone mode. Also to install Clair.

If using the same PostgreSQL instance for both Quay and Clair, you should set the same db username and password for both.

Run Ansible roles in this order:
  * config-docker
  * config-redis
  * config-postgresql  
  * config-quay-enterprise
  * Go to Quay config URL to finish configuration and generate a PEM certificate to be used by Clair. Then restart Quay with systemctl.
  * config-clair
