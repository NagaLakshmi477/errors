Error:

[ ec2-user@ip-172-31-25-202 ~/ansible ]$ ansible-inventory -i inventory.aws_ec2.yaml --graph
[WARNING]:  * Failed to parse /home/ec2-user/ansible/inventory.aws_ec2.yaml with auto plugin:
Failed to describe instances: An error occurred (UnauthorizedOperation) when calling the
DescribeInstances operation: You are not authorized to perform this operation. User:
arn:aws:iam::352742379477:user/roboshop is not authorized to perform: ec2:DescribeInstances
because no identity-based policy allows the ec2:DescribeInstances action
[WARNING]:  * Failed to parse /home/ec2-user/ansible/inventory.aws_ec2.yaml with yaml plugin:
Plugin configuration YAML file, not YAML inventory
[WARNING]:  * Failed to parse /home/ec2-user/ansible/inventory.aws_ec2.yaml with ini plugin:
Invalid host pattern 'plugin:' supplied, ending in ':' is not allowed, this character is reserved
to provide a port.
[WARNING]: Unable to parse /home/ec2-user/ansible/inventory.aws_ec2.yaml as an inventory source
[WARNING]: No inventory was parsed, only implicit localhost is available
@all:
  |--@ungrouped:


solution:
Missed AWS configuration and IAM user does not have ec2:DescribeInstances permission.