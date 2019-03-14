# python paramico
You want to get data from your server. you use it. 

## Input your information
```python
ssh_key_location = "/your/private/key/location.pem"
server_ip = "user server ip"
username = "your user name"
password = "your password"   # If you will use private key, you don't have fill it.
```

## input your command.
You can choice to use many or one command. 
### If you want to one command, you will use it.
```python
print("Executing {$",command,"}")
stdin , stdout, stderr = con.exec_command(command)
print(stdout.readlines())
print("===== Errors ======")
print(stderr.readlines())
```

### If you want to many command, you will use it.

```python
for command in commands:
	print("Executing {$", f"{command}", "}")
	stdin , stdout, stderr = con.exec_command(command)
	print(stdout.read())
	print("===== Errors ======")
	print(stderr.read())
```

I will update to add connect sftp and get file to local ASAP.

### Reference
> http://www.paramiko.org/index.html
> http://docs.paramiko.org/en/latest/index.html