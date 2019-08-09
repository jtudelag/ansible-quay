Set of Roles
============

The ansible roles found in this directory are associated with configuring a docker set up.

Effectively, the `docker.yml` task will install packages for docker and add users to the docker user group.

It will also configure docker storage, start and enabled docker service.


Role Variables
--------------
```
docker_dev: /dev/vdb
docker_vg: docker-vol
docker_data_size: 100%VG
docker_dm_basesize: "10G"
container_root_lv_name: dockerlv
container_root_lv_mount_path: /var/lib/docker
```


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

Example Inventory
----------------

```
docker_install: True
docker_username: bob
```


License
-------

Apache License 2.0


Author Information
------------------

Red Hat Community of Practice & staff of the Red Hat Open Innovation Labs.
