ERROR:
=====
TASK [common : installing dependies] *****************************************************
fatal: [cart.nagalakshmi.site]: FAILED! => {"changed": false, "cmd": "/bin/npm install", "msg": "npm error code ENOENT\nnpm error syscall open\nnpm error path /app/package.json\nnpm error errno -2\nnpm error enoent Could not read package.json: Error: ENOENT: no such file or directory, open '/app/package.json'\nnpm error enoent This is related to npm not being able to find a file.\nnpm error enoent\nnpm error A complete log of this run can be found in: /root/.npm/_logs/2026-05-13T05_40_33_372Z-debug-0.log", "rc": 254, "stderr": "npm error code ENOENT\nnpm error syscall open\nnpm error path /app/package.json\nnpm error errno -2\nnpm error enoent Could not read package.json: Error: ENOENT: no such file or directory, open '/app/package.json'\nnpm error enoent This is related to npm not being able to find a file.\nnpm error enoent\nnpm error A complete log of this run can be found in: /root/.npm/_logs/2026-05-13T05_40_33_372Z-debug-0.log\n", "stderr_lines": ["npm error code ENOENT", "npm error syscall open", "npm error path /app/package.json", "npm error errno -2", "npm error enoent Could not read package.json: Error: ENOENT: no such file or directory, open '/app/package.json'", "npm error enoent This is related to npm not being able to find a file.", "npm error enoent", "npm error A complete log of this run can be found in: /root/.npm/_logs/2026-05-13T05_40_33_372Z-debug-0.log"], "stdout": "", "stdout_lines": []}

Ans:
here i gave 
 - name: nodejs setup after app setup 
 but we need to give app setup nefore nodejs setup 

app-setup → downloads & unzips application files
nodejs → runs npm install
npm install needs package.json

Without app setup first, /app/package.json will not exist.