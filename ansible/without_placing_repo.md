error:

TASK [mongodb : copy mongodb repo] ****************************************************************************************************
An exception occurred during task execution. To see the full traceback, use -vvv. The error was: If you are using a module and expect the file to exist on the remote, see the remote_src option
fatal: [mongodb.lakshmireddy.site]: FAILED! => {"changed": false, "msg": "Could not find or access 'mongo.repo'\nSearched in:\n\t/home/ec2-user/ansible-roboshop-roles/roles/mongodb/files/mongo.repo\n\t/home/ec2-user/ansible-roboshop-roles/roles/mongodb/mongo.repo\n\t/home/ec2-user/ansible-roboshop-roles/roles/mongodb/tasks/files/mongo.repo\n\t/home/ec2-user/ansible-roboshop-roles/roles/mongodb/tasks/mongo.repo\n\t/home/ec2-user/ansible-roboshop-roles/files/mongo.repo\n\t/home/ec2-user/ansible-roboshop-roles/mongo.repo on the Ansible Controller.\nIf you are using a module and expect the file to exist on the remote, see the remote_src option"}

PLAY RECAP ****************************************************************************************************************************
mongodb.lakshmireddy.site  : ok=1    changed=0    unreachable=0    failed=1    skipped=0    rescued=0    ignored=0

solution:
here it will searach in all possible locations for the mongo.repo file
/home/ec2-user/ansible-roboshop-roles/roles/mongodb/files/mongo.repo
/home/ec2-user/ansible-roboshop-roles/roles/mongodb/mongo.repo
/home/ec2-user/ansible-roboshop-roles/roles/mongodb/tasks/files/mongo.repo
home/ec2-user/ansible-roboshop-roles/roles/mongodb/tasks/mongo.repo
home/ec2-user/ansible-roboshop-roles/mongo.repo

we will place the file under the 
/home/ec2-user/ansible-roboshop-roles/roles/mongodb/files/mongo.repo

