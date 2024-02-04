# Algorithm for file updates in Python


## Project description

Use Python code to open a file containing allowed IP addresses, read the content of the file and finally remove IP addresses that no longer should be on the list.


## Open the file that contains the allow list

The following code will open the file and prepare for reading the file.


```
import_file = "allow_list.txt"

# First line of `with` statement

with open (import_file, "r") as file:
```



## Read the file contents

The previous line will cause an error without the following code line to read the file contents:

	`ip_addresses = file.read()`


## Convert the string into a list

The text document is one long string.  The following converts the one long string into a list format for easier data manipulation:


```
# Use `.split()` to convert `ip_addresses` from a string to a list

ip_addresses = ip_addresses.split()
```



## Iterate through the remove list

A simple for loop will iterate through the remove list:


```
for element in ip_addresses:
```



## Remove IP addresses that are on the remove list

The entire code up to this point plus more code at the end to remove the IP addresses on the remove list:


```
# Assign `import_file` to the name of the file 

import_file = "allow_list.txt"

# Assign `remove_list` to a list of IP addresses that are no longer allowed to access restricted information. 

remove_list = ["192.168.97.225", "192.168.158.170", "192.168.201.40", "192.168.58.57"]

# Build `with` statement to read in the initial contents of the file

with open(import_file, "r") as file:

  # Use `.read()` to read the imported file and store it in a variable named `ip_addresses`

  ip_addresses = file.read()

# Use `.split()` to convert `ip_addresses` from a string to a list

ip_addresses = ip_addresses.split()

# Build iterative statement to loop through ip_addresses

for element in ip_addresses:


  # Build conditional statement
  # If current element is in `remove_list`,


    if element in remove_list:

        # then current element should be removed from `ip_addresses`

        ip_addresses.remove(element)
```



## Update the file with the revised list of IP addresses 

Finally, the following lines of code are added to revise the file with the list of allowed IP addresses;


```
# Convert `ip_addresses` back to a string so that it can be written into the text file 

ip_addresses = " ".join(ip_addresses)    

# Build `with` statement to rewrite the original file

with open (import_file, "w") as file:

  # Rewrite the file, replacing its contents with `ip_addresses`

    file.write(ip_addresses)
```



## Summary

Python was used to quickly read and update the file with allowed IP addresses.  This entire process can be converted into a function if the algorithm will be used more than once.
