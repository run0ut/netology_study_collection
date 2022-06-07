# Collections Plugins Directory

<details><summary>defailt description</summary>

This directory can be used to ship various plugins inside an Ansible collection. Each plugin is placed in a folder that
is named after the type of plugin it is in. It can also include the `module_utils` and `modules` directory that
would contain module utils and modules respectively.

Here is an example directory of the majority of plugins currently supported by Ansible:

```
└── plugins
    ├── action
    ├── become
    ├── cache
    ├── callback
    ├── cliconf
    ├── connection
    ├── filter
    ├── httpapi
    ├── inventory
    ├── lookup
    ├── module_utils
    ├── modules
    ├── netconf
    ├── shell
    ├── strategy
    ├── terminal
    ├── test
    └── vars
```

A full list of plugin types can be found at [Working With Plugins](https://docs.ansible.com/ansible-core/devel/plugins/plugins.html).
 
</details>

## modules/my_own_module.py

Just a simple module, doinf nothing fancy

## modules/yc_create_instance.py 

Creates Yandex.Cloud instance. 

Example:
```yml
- name: Create instance
  hosts: localhost
  tasks:
    - name: Create new Yandex Cloud Compute instance
      netology86.yandex_cloud_elk.yc_create_instance:
        network_interface: "net-ru-central1-a"
        name: "test-instance"
        status: "running"
```

## inventory/yc_inventory.py 

Yandex.Cloud dynamic inventory plugin.

* Inventory file possible names:
    * `yc.yaml`
    * `yc.yml`
    * `yc_inventory.yaml`
    * `yc_inventory.yml`
* Example inventory file:

    `yc_inventory.yaml`
    ```yml
    plugin: netology86.yandex_cloud_elk.yc_inventory
    ```
* Example usage:
    ```bash
    ansible -i yc_inventory.yaml -m ansible.builtin.ping all
    ```
