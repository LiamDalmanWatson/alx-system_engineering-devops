0-iam_betty: switches the current user to the user betty
1-who_am_i: prints the effective username of the current user
2-groups: prints all the groups the current user is part of
3-new_owner: changes the wner of the file hello to the user betty
4-empty: creates an empty file called hello
5-execute: adds execute permission to the owner of the file hello
6-multiple_permissions: adds execute permission to the owner and the group owner, and read permission to others, to the file hello
7-everybody: adds execution permission to the owner, the group and the other users, to file hello
8-James_Bond: sets permission to the file hello
9-sets the mode of the file hello
10-sets the mode of the file hello to the same as olleh's mode
11-a script that adds execute permission to all subdirectories of the current dirctory for the owner, the group and all others
12-directory_permissions:creates a directory called my_dir with permissions 751 in the working directory.
13-change_group:changes the group owner to school for the file hello
100-change_owner_and_group: changes the owner to vincent and the group owner to staff for all files and directories in the working directory
101-symbolic_link_permissions:changes the owner and the group owner of _hello to vincent and staff respectively
102-if_only:changes the owner of the file hello to betty only if it is owned by the user guillaume.
103-Star_Wars:script that will play the StarWars IV episode in the terminal.


0-iam_betty
#!/bin/bash
su betty

================
1-who_am_i

#!/bin/bash
id -un

================
2-groups

#!/bin/bash
groups

================
3-new_owner

#!/bin/bash
chown betty hello

===============
4-empty

#!/bin/bash
touch hello

==============
5-execute

#!/bin/bash
chmod u+x hello

==============
6-multiple_permissions

#!/bin/bash
chmod u+x,g+x,o+r hello

==============
7-everybody

#!/bin/bash
chmod ugo+x hello

==============
8-James_Bond

#!/bin/bash
chmod 007 hello

==============
9-John_Doe

#!/bin/bash
chmod 753 hello

==============
10-mirror_permissions

#!/bin/bash
chmod --reference=olleh hello

==============
11-directories_permissions

#!/bin/bash
chmod -R ugo+X .

==============
12-directory_permissions

#!/bin/bash
mkdir -m 751 my_dir

==============
13-change_group

#!/bin/bash
chgrp school hello

==============
100-change_owner_and_group

#!/bin/bash
chown -hR vincent:staff .

==============
101-symbolic_link_permissions

#!/bin/bash
chown -h vincent:staff _hello

==============
102-if_only

#!/bin/bash
chown --from=guillaume betty hello
