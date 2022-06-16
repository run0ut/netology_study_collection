# Ansible Collection - netology.study_collection

Description
------------

This collection consists of a number of things, developed during 16-month devops course at Netology online study platform

These thins you might find useful:
- Plugin to create or delete Yandex Cloud Compute instance [yc_create_instance](./plugins/modules/yc_create_instance.py)
- Plugin, dynamic inventory, for Yandex Cloud Compute [yc_inventory](./plugins/inventory/yc_inventory.py)
- Example [inventory file](./yc_inventory.yml), to use dynamic inventory plugin
- Role to create Yandex.Cloud Compute VM [create-vm](./roles/create-vm/)
- Role to create Yandex.Cloud Compute VM, simplified [create-vm-simple](./roles/create-vm-simple/)
- Role to destroy Yandex.Cloud Compute VM by name [destroy-vm](./roles/destroy-vm/)
- Role to wait for all hosts to become available [wait-vm](./roles/wait-vm/)

These things are not that interesting:
- Plugin [my_own_module](./plugins/modules/my_own_module.py) that creates a file with user defined content or default content, which is "Hi, Netology!" 
- Role [netology86-role](./roles/netology86-role/), that uses these module.
- Roles to deploy [Elasticsearch](./roles/elastic-role), [Kibana](./roles/kibana-role), [Logstash](roles/logstash-role) and [Filebeat](./roles/filebeat-role)
- Roles to deploy [minikube](./roles/install-kuber/) and [hello-node](./roles/run-hello-node/)
- [Playbook](./playbooks/playbook_with_dynamic_inventory.yml), that will create a YC instance and deploy complete ELK-stack and Filebeat on it

Dependencies
------------

CLI Yandex Cloud :
- [Documentation main page](https://cloud.yandex.com/en-ru/docs/cli/)
- [Getting started](https://cloud.yandex.com/en-ru/docs/cli/quickstart)

License
-------

MIT

