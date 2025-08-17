ERROR:

TASK [extract the cart files] *********************************************************************************************************
An exception occurred during task execution. To see the full traceback, use -vvv. The error was: If you are using a module and expect the file to exist on the remote, see the remote_src option
fatal: [cart.lakshmireddy.site]: FAILED! => {"changed": false, "msg": "Could not find or access '/tmp/cart.zip' on the Ansible Controller.\nIf you are using a module and expect the file to exist on the remote, see the remote_src option"}

PLAY RECAP ****************************************************************************************************************************
cart.lakshmireddy.site     : ok=7    changed=5    unreachable=0    failed=1    skipped=0    rescued=0    ignored=0

SOLUTION:

we need to give remote src is yes 