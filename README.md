ansible-kafka
---------
This Ansible playbook will build a Kafka cluster with Zookeeper.


---




## [Requirements] (id:requirements)

- Ansible >= 2.0.

- Expects RHEL/CentOS 6/7 or Ubuntu 14 hosts.

- Building the Rackspace Cloud environment requires the `pyrax` Python module: [pyrax link](https://github.com/rackspace/pyrax).


## [Features] (id:features)

- It installs Zookeeper for Kafka (Zookeeper is installed on the first 3 nodes only).



- The data drives can be customized and can be put on top of Rackspace Cloud Block Storage.

- It includes init scripts for both Zookeeper and Kafka.



  



## [Configuration] (id:configuration)

To customize, change the variables under `playbooks/group_vars` and `playbooks/roles` folders:

1. **playbooks/group_vars/all**: contains cluster and cloud settings
1. **playbooks/roles/zookeeper/defaults/main.yml**: Zookeeper specific settings
1. **playbooks/roles/kafka/defaults/main.yml**: Kafka specific settings

For a one-node cluster, set `nodes_count` in `playbooks/group_vars/all` to 1.

