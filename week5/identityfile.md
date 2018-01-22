###Week 1: Identity File

-----

With the [IP address allocated](assignip.md), we'll now work with the file downloaded from AWS when we [setup our EC2 instance](server.md). It may be worth taking a detour into [understanding the Bash shell](bashintro.md) first. 

This downloaded identity file contains your access credentials for getting into your AWS machine, but we have to prepare it first. Please make a duplicate of it before continuing, and place the file on your Desktop.

In Terminal, move to your desktop.

`cd ~/Desktop/`

`ls`

`proto_class.pem.txt`

Let's remove the unnecessary .txt part of the file name.

`mv proto_class.pem.txt proto_class.pem`

`ls`

`proto_class.pem`

And move this file to a special place on your computer.

`cd ~`

`mv ~/Desktop/proto_class.pem .ssh/`

The `.ssh` directory is a hidden directory in your home folder. You won't see it there, though, in the Finder or even with `ls`. Files and directories which have names beginning with a `.` are hidden from view. To see them, add the `-a` option to `ls`.

`ls -a ~`

```
.			              			
..			            		
.CFUserTextEncoding	      		
.DS_Store		        			
.Trash						  
.bash_history					
.bash_sessions					
.bashrc					    
.cups										
.ssh			
Applications
Desktop
Documents
Downloads
Library
Movies
Music
Pictures
Public
```

Let's `cd` into the `.ssh` directory.

`cd ~/.ssh`

One change needs to be made to the .pem file. Let's use the `chmod` command to lock down this file's permissions.

`chmod 400 proto_class.pem`

Use `man chmod` to read more about what this command does. At a very basic level `chmod` uses three numbers to determine who can access this file. 

- The first number controls permissions for the owner of the file, which is your current logged-in user
- The second number controls permissions for a group users which includes the current user
- The third number controls permissions for anyone

Any file can be readable, writable, and/or executable (so you can run it as a program). Numbers are used to represent these abilities.

- 0 : No Access
- 1 : Execute 
- 2 : Write
- 4 : Read

You can add numbers together to define specific permissions.

- 3 : Execute and Write
- 5 : Execute and Read
- 6 : Read and Write
- 7 : Read, Write, and Execute


The command fired earlier `chmod 400 proto_class.pem` sets no access for the world, no access for members of the user's group, and Read access for the current user. This is now a highly secure file that only the current user can read.

Let's now take this file and [connect directly to our server](serveraccess.md).
