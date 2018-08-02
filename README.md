Role Name

This role is to install and configite kafka with zookeeper on cluster 


Requirements

RedHat or Debin OS Family 


Role Variables

Are in defaults/main.yml, vars/main.yml


Dependencies

Java 8 or 7 need to be installed before 


Example Playbook

ansible-playbook elastic-search.yml 


- hosts: cluster-kafka
  remote_user: root
  tasks: 
    - include_role: 
	name: kafka-cluster

change the hosts accordingly 


License

BSD
