ERROR:

"${var.project}/${var.environment}/vpc_id"

Plan: 1 to add, 0 to change, 0 to destroy.
aws_ssm_parameter.vpc: Creating...
╷
│ Error: creating SSM Parameter (roboshop/dev/vpc_id): operation error SSM: PutParameter, https response error StatusCode: 400, RequestID: e9f3d831-c919-4daa-b16c-253060924e9a, api error ValidationException: Parameter name must be a fully qualified name.
│
│   with aws_ssm_parameter.vpc,
│   on parameters.tf line 1, in resource "aws_ssm_parameter" "vpc":
│    1: resource "aws_ssm_parameter" "vpc" {
│

Solution:
"/${var.project}/${var.environment}/vpc_id"