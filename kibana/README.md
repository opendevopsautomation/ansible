Kibana
=========

A kibana 7.x role with x-pack security

Requirements
------------

ansible_vault to encrypt the sensitive information. e.g  ansible-vault encrypt_string --vault-id ~/.ansible_vault 'example@123' --name 'es_pass'
We are assuming that this role is running from central ansible node and elasticsearch nodes are accessible from ansible to fetch the certificates.


Role Variables
--------------

cert_pass has same encrypted password which was used to generate the elasticsearch certificates.
es_username is the username used to access elasticsearch
es_pass is password of the elasticsearch user.
extra_config used for additional configuration.
es_host is the host vars of elasticsearch cluster.
To override default variable,define it in hostvars, group vars etc


Dependencies
------------

Running elasticsearch cluster with proper credentials to establish a connection.

Example Playbook
----------------

    - hosts: "{{ target_host }}"
      roles:
         - { role: kibana, tags: ['kibana'] }

Author Information
------------------


* **Open DevOps Automation** - *work* - [github](https://github.com/opendevopsautomation)
