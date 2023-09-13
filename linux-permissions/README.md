## File Permissions in Linux

### Project Description
What can be accomplished through Linux commands is seemingly endless and way more efficient than using a GUI. From viewing directories and files to editing user permissions, knowing the command line in Linux is a very helpful skill to have.

### Check File and Directory Details
Use the command "ls" which is shorthand for list.

### Permissions String
* drwxrwxrwx owner group other (the d indicates that this is a directory)
* -rwxrwxrwx owner group other (the dash indicates that this is a file)
* lrw-rwx-r-- owner group other  (the l indicates a link)

r = read permissions

w = write permissions

x = execute permissions

The first set of rwx (characters 2-4) are the directory or file permissions of the owner of the file

The second set of rwx (characters 5-7) are the permissions of the group listed

The third set of rwx (characters 8-10) are the permissions of all other users

### Change File Permissions
Use the command "chmod" along with some extra parameters that I will give examples of below:
1. chmod u+w document.txt >> This gives the owner (user) "write" permissions to the document.txt file
2. chmod g-r document.txt >> This removes "read" permissions from the group with regards to the document.txt file
3. chmod o-x document.txt >> This removes "execute" permissions from all other users with regards to the document.txt file
4. chmod a+r document.txt >> This gives "read" permissions to all including the owner, group and all other users

### Change File Permissions on a Hidden File
Use the command "ls -la" to list all permissions of hidden files and directories in the current working directory
The "chmod" commands work the same as mentioned before except when entering the hidden directory or file into the command, you must include the "." before the directory/file name

### Change Directory Permissions
Similar to changing file permissions, you would use "chmod", add your parameters (ie g+w) and then type out the directory name
