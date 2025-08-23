│ Error: local-exec provisioner error
│
│   with aws_instance.roboshop,
│   on ec2.tf line 6, in resource "aws_instance" "roboshop":
│    6:     provisioner "local-exec" {
│
│ Error running command '172.31.34.218 > inventory': exit status 1. Output:
│ '172.31.34.218' is not recognized as an internal or external command,
│ operable program or batch file.
│
╵
Releasing state lock. This may take a few moments...

solution:
