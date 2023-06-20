# AWS_Backup_EBS_DLM


___________ In this template we are creating a **AWS_backup_EC2--using tags**  and **EBS_DLM_Policy** using a cloud Formation ___________

AWS BACKUP : Taking a backup of resource to have it as a handy to recover when needed 
EBS_DLM    : Automate the lifecycle of EBS snapshots using and it counts 


______________________________________________________________________________________________________________________________
_____________________we have a parameters for resource of EC2-Backup and EBS_life_cycle_____________________
   
   step :1 

        we have create a ***EC2*** using a tags with { key , value }

   step : 2
         we create a role for DLM which is managed policy 

   step : 3
         we create a ***DLM_Policy***  with target tags as ec2 
         
   step : 4 
        we create a backup plan with a cronjob attach which will automate your backup and mention the life cycle of backup 
        
   step : 5 
         we create a ***BackUp_Vault*** : where our recovery point of resource is stored and has a kms key for encryption 
         
   step  : 6 
         Backup plan selection : specifing the backup_plan id with the list of tag in which the ec2 tag has to be selected fot backup

______________________________________________________________________________________________________________________________________________

                         *** So as per the code the AWS_BACKUP has to be done every 5 hours ***
         
