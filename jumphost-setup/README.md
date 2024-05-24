## How to Run

To run a playbook you will need to specify the playbook file and the host file.

Example:
```commandline
ansible-playbook plays/pb_server_setup.yml -i hosts/hosts.ini -Kk
```

## Directories

- `/plays` - Contains all playbook files.
- `/hosts` - Contains all host files.
- `/roles` - Contains all roles directories.

## Roles

In the `/roles` directory, tasks are grouped by their purpose. 

For example, the `/roles/docker/` directory contains a file including all tasks related to installing Docker.

Another example is the `/roles/python_3.10.14/` directory which contains a file with all the tasks for installing Python version 3.10.14.

In both examples mentioned above, there are multiple steps to installing packages, so they have been grouped into roles.


Whereas the `/roles/dnf_installs/` directory contains a file that lists all packages that can be installed via DNF without any dependencies. Any DNF install that does not have dependencies can be appended to that list.

These roles are called individually from a playbook file in the `/plays` directory.

