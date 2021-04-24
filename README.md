# kubernetes_on_aws_ansible
### https://galaxy.ansible.com/prithviraj_singh/aws_kubernetes
Download the collection using the following command:
    ansible-galaxy collection install prithviraj_singh.aws_kubernetes
## Prerequisite:
1. Ansible (latest)
2. PIP
3. Virtualenv
4. setuptools
5. Python
6. Whatever is required for the package plugins specific for each system.
7. Yum, on the ec2 instances
8. AWS configured on your base system (Alternatively you can define and export environmental variables AWS_ACCESS_KEY_ID and AWS_SECRET_ACCESS_KEY, with the required value).
9. Key with names key1 and key2 should not pre-exist on the account.

## How to use
1. Install the collection using the command given above or if that does not work you will require to download the tarball of the collection from https://galaxy.ansible.com/prithviraj_singh/aws_kubernetes and then untar the tarball. You can also choose to give the path to install the collection using -p as an option for this.
2. Once the collection has been installed, run the playbook located inside the collection /some/path/ansible_collections/prithviraj_singh/aws_kubernetes/ named as playbook.yml. To run the playbook you can use the command:
    ansible-playbook /path/to/playbook/playbook.yml
3. Once the playbook has ran successfully, you can check out the AWS instances that have been spawned over ap-south-1.
4. Connect to the instance named as master, login as ec2-user, use the command:
    kubectl get nodes
    #prints all the nodes, including master
That's it!!!

### Additionally:-
you can change the attributes of the cluster by changing the variable located inside /some/path/ansible_collections/prithviraj_singh/aws_kubernetes/roles/aws_instances/vars/main.yml, /some/path/ansible_collections/prithviraj_singh/aws_kubernetes/roles/worker_nodes/vars/main.yml and /some/path/ansible_collections/prithviraj_singh/aws_kubernetes/roles/kubernetes_role/vars/main.yml
### Note:-
If you wish to change the EC2’s image, make sure to change the username for initial login to the provided user inside ansible_collection/prithvi_singh/aws_kubrnetes/playbook.yml . Also, creating a master-node with RHEL-8 image doesn’t work (somehow, if you know the reason and fix for it please let me know).

##### Consider checking these out:-
https://prithvirajsingh1604.medium.com/spawn-a-kubernetes-multi-node-cluster-over-aws-with-ansible-collections-61661d6fccc0 
https://divya-kurothe.medium.com/ 
Please rate the collection, your feedbacks are very highly appreciated😁.   
 *That's all!!!*    
 **You are awesome**
### *Created by*:
Prithviraj Singh <prithvirajsingh1604@gmail.com> and Divya Kurothe.
