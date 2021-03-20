# Follow these step to use this playbook:

> Step 1: Edit secret.yml vault using vault_pass and put your IAM credentials. </br>
> Step 2: Update Master Parameter in master.yml  </br>
> Step 3: Update Master Parameter in slave.yml </br>
> Step 4: Play Playbook using command " ansible-playbook multi-node-cluster.yml --vault-password-file vault_pass " </br>

NOTE: On playbook failure, delete inventory or host file group entry.
 Example: 
  
 [k8sMasterA]                                                                    
 13.2.2.2  ansible-user=ec2-user ssh_private_key_file=/path/to/key ansible_connection=ssh    

 [k8sSlaveA]                                                                    
 13.2.2.2  ansible-user=ec2-user ssh_private_key_file=/path/to/key ansible_connection=ssh    
 
### Delete above groups on playbook failure.


 
Thanks

Created By Kaushal Soni 
