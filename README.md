\freehck.k8s_label_nodes
=========

Set labels to kubernetes nodes

Description
-----------

This role just sets labels to kubernetes nodes.

Role Variables
--------------

`k8s_label_nodes_with_list`: the list with nodes and their labels, look example below

Example
-------

    - hosts: k8s-master
      become: true
      vars:
        k8s_label_nodes_with_list:
          - nodes:
              - "k8s-node-1"
              - "k8s-node-2"
              - "k8s-node-3"
            labels:
              - "elasticsearch-cluster=main"
              - "storage-class-affinity=fast-ssd"
      roles:
        - role: freehck.k8s_label_nodes

Install
-------

This role can be installed from [Ansible Galaxy](https://galaxy.ansible.com/):

`ansible-galaxy install freehck.k8s_label_nodes`

License
-------

MIT

Author Information
------------------

Dmitrii Kashin, <freehck@freehck.ru>
