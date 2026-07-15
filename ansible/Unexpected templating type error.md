
question: '<' not supported between instances of 'AnsibleUnsafeText' and 'int'

Error:
TASK [load the products] ***********************************************************************************
fatal: [172.31.39.46]: FAILED! => {"msg": "The conditional check 'catalogue_output.stdout < 0' failed. The error was: Unexpected templating type error occurred on ({% if catalogue_output.stdout < 0 %} True {% else %} False {% endif %}): '<' not supported between instances of 'AnsibleUnsafeText' and 'int'. '<' not supported between instances of 'AnsibleUnsafeText' and 'int'\n\nThe error appears to be in '/home/ec2-user/ansible-roboshop/catalogue.yaml': line 76, column 5, but may\nbe elsewhere in the file depending on the exact syntax problem.\n\nThe offending line appears to be:\n\n\n  - name: load the products\n    ^ here\n"}

solution:
=====
Here 
  - name: load the products
    ansible.builtin.command: mongosh --host 172.31.43.42 < /app/db/master-data.js
    when: catalogue_output.stdout | int < 0
    
catalogue_output.stdout returns output as a string (AnsibleUnsafeText), but I was comparing it with an integer using:
