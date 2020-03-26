Set of Roles
============

The ansible roles found in this directory are associated with configuring a docker set up.

Effectively, the `docker.yml` task will install packages for docker and add users to the docker user group.

Since EL 7.4, equivalent Fedora or other modern Linux distributions, OverlayFS became the default Docker storage driver and there for no longer needs a backing device mapper.



Dependencies
------------
There are no strict dependencies for this role beyond ansible and docker.

Example Playbooks
----------------

```
- hosts: bastion
  roles:
    - role: config-docker
```


License
-------

Apache License 2.0


Author Information
------------------

Red Hat Community of Practice & staff of the Red Hat Open Innovation Labs.
