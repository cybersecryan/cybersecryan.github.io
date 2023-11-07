## Algorithm for updating "allow list" in Python

### Project description
#### Develop an algorithm for updating an allow list based on IP address for users who have access to sensitive medical information.

### Open the file that contains the allow list
```
with open(“allow_list.txt”, “r”) as file:
```

### Read the file contents 
```
with open(“allow_list.txt”, “r”) as file:
  ip_addresses = file.read()
```

### Convert the string into a list
```
with open(“allow_list.txt”, “r”) as file:
	ip_addresses = file.read()
ip_addresses = ip_addresses.split()
```

### Iterate through the remove list
```
with open(“allow_list.txt”, “r”) as file:
	ip_addresses = file.read()
ip_addresses = ip_addresses.split()
for element in ip_addresses:
```

### Remove IP addresses that are on the remove list
```
with open(“allow_list.txt”, “r”) as file:
	ip_addresses = file.read()
ip_addresses = ip_addresses.split()
for element in ip_addresses:
if element in ip_addresses:
	ip_addresses.remove(element)
```

### Update the file with the revised list of IP addresses 
```
with open(“allow_list.txt”, “r”) as file:
	ip_addresses = file.read()
ip_addresses = ip_addresses.split()
for element in ip_addresses:
if element in ip_addresses:
	ip_addresses.remove(element)
ip_addresses = “ “.join(ip_addresses) 	## converts file back into string
with open(“allow_list.txt”, “w”) as file:
	file.write(ip_addresses)
```
### Summary
#### This algorithm makes updating an allow list more automated by quickly iterating through the text file to determine whether or not a certain IP address should be allowed access to this sensitive medical information.

