Planning failed. Terraform encountered an error while generating this plan.

╷
│ Error: Incorrect attribute value type
│
│   on main.tf line 3, in resource "aws_instance" "bastion":
│    3:   vpc_security_group_ids = local.bastion_sg_id
│
│ Inappropriate value for attribute "vpc_security_group_ids": set of string
│ required.
╵
Releasing state lock. This may take a few moments...


SOLUTION:
  vpc_security_group_ids = local.bastion_sg_id  now it is change to list
   vpc_security_group_ids = [local.bastion_sg_id]