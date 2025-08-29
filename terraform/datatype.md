│ Error: Incorrect attribute value type
│
│   on parameters.tf line 10, in resource "aws_ssm_parameter" "public_subnet_ids":
│   10:   value = module.vpc.public_subnet_ids
│     ├────────────────
│     │ module.vpc.public_subnet_ids is tuple with 2 elements
│
│ Inappropriate value for attribute "value": string required.
╵
Releasing state lock. This may take a few moments...

SOLUTION:

we are getting values 
vpc_ids = [
  "subnet-03b4aa2e7908fbd6f",
  "subnet-028e880f61f9b0baa",
]
we need to change using join:
subnet-03b4aa2e7908fbd6f,subnet-028e880f61f9b0baa


join(",",module.vpc.public_subnet_ids)