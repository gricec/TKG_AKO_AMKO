# TKG_AKO_AMKO

These playbooks install AKO and AMKO onto TKG Guest Clusters

Modify Variables in Group Vars

Requirements:
Ansible
ansible-galaxy collection install community.kubernetes.helm


INSTRUCTIONS
Run akorole.yaml  first, include names of clusters in extra vars as cli argument

ansible-playbook akorole.yaml -Kk -u chris --extra-vars='{"clusters":[ "cluster2", "cluster3", "cluster4"], "file": "green"}'


Creates TKG Guest Clusters and installs AKO on each along with simple app and type loadBalancer service

Run AMKO.yaml 

ansible-playbook amko.yaml 

Will install AMKO on cluster last in list



