Error:
======
aws_security_group.allow_all_ports: Creating...

Error:
from_port (8080) and to_port (8080) must both be 0 to use the 'ALL' "-1" protocol.

Reason:
=======
I used:

protocol = "-1"

"-1" means ALL protocols.

When using ALL protocols, AWS requires:

from_port = 0
to_port   = 0

But I was using:

from_port = 8080
to_port   = 8080

This caused a protocol and port mismatch error.

Fix:
====
I changed:

protocol = "-1"

to

protocol = "tcp"

because port 8080 is a TCP port.

Correct code:

dynamic "ingress" {
  for_each = var.ingress_port

  content {
    from_port   = ingress.value["from_port"]
    to_port     = ingress.value["to_port"]
    protocol    = "tcp"
    cidr_blocks = var.cidr_blocks
  }
}

Root Cause:
===========
I missed using "tcp" protocol and mistakenly used "-1" (ALL protocol).