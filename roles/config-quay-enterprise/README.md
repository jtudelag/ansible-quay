# Quay Enterprise

Ansible Role to help configure [Quay Enterprise](https://coreos.com/quay-enterprise/) on a standalone instance.

## Requirements

A Linux Distribution which supports `systemd` and `package` modules along with docker install and configured.

## Role Variables

This role contains a number of variables to customize the deployment of Quay Enterprise. The following are some of the most important that may need to be configured

| Name | Description | Default|
|---|---|---|
|quay_database_type|Database to use (`postgresql` or `mysql`)|`postgresql`|
|quay_image|Quay Enterprise image|`quay.io/redhat/quay:v3.0.4`|

## Dependencies

* [config-docker](../config-docker)

## Example Inventory

## Example Playbook

```
- name: Install Quay Enterprise
  hosts: quay_enterprise
  roles:
    - role: config-quay-enterprise
```

## License

Apache License 2.0

## Author Information

Red Hat Community of Practice & staff of the Red Hat Open Innovation Labs.
