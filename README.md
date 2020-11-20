# TKG_AKO_AMKO

These playbooks install AKO and AMKO onto TKG Guest Clusters

Modify Variables in Group Vars

Requirements:
Ansible
ansible-galaxy collection install community.kubernetes.helm


INSTRUCTIONS
Run akorole.yaml  first, include names of clusters in extra vars as cli argument. File dictates what deployment to run. Hack.yaml deploys  app, service, sec ingress and HostRule CRD for WAF

ansible-playbook akorole.yaml -Kk -u chris --extra-vars='{"clusters":[ "cluster2", "cluster3", "cluster4"], "file": "hack"}'


Next run AMKO.yaml 

ansible-playbook amko.yaml 

Will install AMKO on cluster last in list



