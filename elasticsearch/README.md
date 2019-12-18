Elasticsearch
=========

A Elasticsearch 7.x role with x-pack security

Requirements
------------
```
Java
Ansible v2.6.x
ansible_vault to encrypt the sensitive information. e.g  ansible-vault encrypt_string --vault-id ~/.ansible_vault 'example@123' --name 'ca_password'

```

Role Variables
--------------
```
ca_password used to generate ca for elasticsearch certificates.
keystore_password path to your PKCS12 keystore (can be the same as truststore_password)
es_ssl_keystore_password set this if your keystore is protected with a password
es_ssl_truststore_password set this if your truststore is protected with a password
es_master_ip is the host vars of master nodes of elasticsearch cluster.
To override default variable,define it in hostvars, group vars etc
```

Dependencies
------------

Pre-installed Java

Example Playbook
----------------

    - hosts: "{{ target_host }}"
      roles:
         - { role: elasticsearch, tags: ['elasticsearch'] }

Reference
------------
[Official Elasticsearch repo](https://github.com/elastic/ansible-elasticsearch/blob/master/README.md)         

Author Information
------------------


* **Open DevOps Automation** - *work* - [github](https://github.com/opendevopsautomation)
