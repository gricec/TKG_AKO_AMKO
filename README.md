# TKG_AKO_AMKO

ako.yaml

Creates TKG Guest Clusters and installs AKO on each along with simple app and type loadBalancer service

run

ansible-playbook ako.yaml -Kk -u chris   --extra-vars='{"cluster": "cluster3", "file": "blusecing3"}' 

amko.yaml


installs AMKO

ansible-playbook -kK -u chris amko.yaml
