This directory describes what each script performs in the **SHELL PERMISSIONS** Project

Requirements

General

Allowed editors: vi, vim, emacs

All your scripts will be tested on Ubuntu 20.04 LTS

All your scripts should be exactly two lines long ($ wc -l file should print 2)

All your files should end with a new line (why?)

The first line of all your files should be exactly #!/bin/bash

You are not allowed to use backticks, &&, || or ;

All your files must be executable

0.0-iam_betty

Create a script that switches the current user to the user betty.

You should use exactly 8 characters for your command (+1 character for the new line)

You can assume that the user betty will exist when we will run your script

#!/bin/bash

su betty

1.1-who_am_i

Write a script that prints the effective username of the current user.

#!/bin/bash

whoami

2. 2-groups

Write a script that prints all the groups the current user is part of.

#!/bin/bash

groups

3.3-new_owner

Write a script that changes the owner of the file hello to the user betty

#!/bin/bash

sudo chown betty hello

4.4-empty

Write a script that creates an empty file called hello.

#!/bin/bash

touch hello

5.5-execute

Write a script that adds execute permission to the owner of the file hello.

The file hello will be in the working directory

#!/bin/bash

chmod u+x hello

6.6-multiple_permissions

Write a script that adds execute permission to the owner and the group owner, and read permission to other users, to the file hello

The file hello will be in the working directory

#!/bin/bash

chmod 754 hello

7. 7-everybody

Write a script that adds execution permission to the owner, the group owner and the other users, to the file hello

The file hello will be in the working directory

You are not allowed to use commas for this script

#!/bin/bash

chmod 751 hello

8. 8-James_Bond

Write a script that sets the permission to the file hello as follows:

Owner: no permission at all

Group: no permission at all

Other users: all the permissions
    

The file hello will be in the working directory.

You are not allowed to use commas for this script

#!/bin/bash

chmod 007 hello

9. 9-John_Doe

Write a script that sets the mode of the file hello to this:

-rwxr-x-wx

The file hello will be in the working directory

You are not allowed to use commas for this script

#!/bin/bash

chmod 753 hello

10.10-mirror_permissions

Write a script that sets the mode of the file hello the same as olleh’s mode.

The file hello will be in the working directory

The file olleh will be in the working directory

Note: the mode of olleh will not always be 664. Make sure your script works for any mode.

#!/bin/bash

chmod --reference=olleh hello

11.11-directories_permissions

Create a script that adds execute permission to all subdirectories of the current directory for the owner, the group owner and all other users.

Regular files should not be changed.

#!/bin/bash

chmod -R 755 */

12. 12-directory_permissions

Create a script that creates a directory called my_dir with permissions 751 in the working directory.

#!/bin/bash

mkdir -m 751 my_dir

13.13-change_group

Write a script that changes the group owner to school for the file hello


The file hello will be in the working directory

#!/bin/bash

chgrp school hello

14. 100-change_owner_and_group

Write a script that changes the owner to vincent and the group owner to staff for all the files and directories in the working directory.

#!/bin/bash

sudo chown vincent:staff *

15. 101-symbolic_link_permissions

Write a script that changes the owner and the group owner of _hello to vincent and staff respectively.

The file _hello is in the working directory

The file _hello is a symbolic link

#!/bin/bash

sudo chown -h vincent staff _hello

16.102-if_only

Write a script that changes the owner of the file hello to betty only if it is owned by the user guillaume

The file hello will be in the working directory

#!/bin/bash

sudo chown --from=guillaume betty hello

17.103-Star_Wars

Write a script that will play the StarWars IV episode in the terminal.

#!/bin/bash

telnet towel.blinkenlights.nl


