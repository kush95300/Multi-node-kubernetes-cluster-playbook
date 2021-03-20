# Multi-node-kubernetes-cluster-playbook

Hi Guys
</br>
I have created this repository to setup kubernetes cluster over aws in a few minutes. So, use this playbook. This is created for educational and learning purpose. You can find roles at ansible-galaxy also.

# Follow these step to use this playbook:

> Step 1: Edit secret.yml vault using vault_pass and put your IAM credentials. </br>
> Step 2: Update Master Parameter in master.yml  </br>
> Step 3: Update Master Parameter in slave.yml </br>
> Step 4: Play Playbook using command : <b>" ansible-playbook multi-node-cluster.yml --vault-password-file vault_pass "</b> </br>

NOTE: On playbook failure, delete inventory or host file group entry.
 Example: 
  
 [k8sMasterA]                                                                    
 13.2.2.2  ansible-user=ec2-user ssh_private_key_file=/path/to/key ansible_connection=ssh    

 [k8sSlaveA]                                                                    
 13.2.2.2  ansible-user=ec2-user ssh_private_key_file=/path/to/key ansible_connection=ssh    
 
### Delete above groups on playbook failure.

# Quick Reference

##### Maintained by: Kaushal Soni
##### Detailed instruction setup :   updating soon... 
 
# Supported Parameters

Following parameters are there : 

| Sr.|  PARAMETER | NAME  | USE  |
| ------------ | ------------ | ------------ | ------------ |
| 1.| **i_name**    (String) ( Recommended change ) | Instance Name  |  It is name tag for instance. |
| 2.|   **key**    (String) | Aws key name  | It is the aws key which in ec2 key section. NOTE:  write keyname only (not  Key extt. like: newkey.pem or newkey.ppk )   | 
| 3.|  **i_type**    (String) | Instance type | Aws Instance type like: t2.micro , t2.medium etc.    |
| 4. |   **img**    (String) | Aws AMI ID  | It denotes AMI iD. AMI ID is the image through which instance will launch. e.g. - ami-xxxxxxxxx  |
| 5. |   **subnet**    (String) | Aws VPC Subnet ID  | It denotes VPC subnet ID. e.g. - subnet-xxxxxxxxx)   |
| 6. |  **SG**    (String) | Security Group ID  | It is the Ec2 Security Group ID. e.g. - sg-xxxxxxxxxx   |
| 7. |  **counts**    (Number) | counts  | Counts denotes number of instance to launch. e.g. - 2   |
| 8. |   **zone**    (String) | Availability Zone or region  | It is the AZ from where resorces are used. e.g. - 'ap-south-1'   |
| 9. |  **inventory**    (String) | inventory file path  | it denotes inventory file path ( as it write group tag in inventory ). e.g. - "/etc/ansible/hosts"   |
| 10. |  **grp_tag**     (String) () Recommended change )  |  Inventory Group Tag  | It denotes inventory group tag, so that after launching instance inventory entry automatically done.  |
| 11. |   **tag**    (String) ( Recommended change )  | Instance Tag  | It is Instance tag to differenciate or compare instances.|
| 12. |   **ssh_key_full_path**    (String) | Aws key path (Local path,)  | It denotes full key path, where key is there, so that it can write it in inventory as automatic entry..  |
|13. |   <b>access_pass </b>     (String) ( Required )| AWS IAM user Access Key  | It denotes aws access key. |
|14. |   <b>secret_pass</b>     (String) ( Required ) | AWS IAM user Secret key  | It denotes aws secret key. |


Use there parameters for better use.

# License

Free to use.

# Support & Contact
<b>

Email: Kaushal95300@gmail.com

Linkedin : https://www.linkedin.com/in/kaushal-soni-988650146/

Github : https://github.com/kush95300 </b>


<br>
