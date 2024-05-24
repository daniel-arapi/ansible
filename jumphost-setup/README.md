
# Jumphost Server Setup

Installs the following
- CRB Repositories
- EPEL Community-Maintained Packages
- GCC Toolset
- OpenSSL
- Dnsmasq
- net-snmp
- PerfSonar Toolkit
- Docker
- Python 3.10.14
- Python 11
- Python 12


## Documentation

- `/plays/` - Contains all playbook files.
- `/hosts/` - Contains all host files.
- `/roles/` - Contains all roles directories.


Rolels are used to group tasks by purpose.

For example, the `/roles/docker/` contains all tasks related to installing Docker; and `/roles/python_3.10.14/` contains all tasks for installing Python version 3.10.14.

In both examples mentioned, there are several steps for installing these packages, therefore they have been grouped into roles.

The `/roles/dnf_installs/` role contains all packages that can be installed via DNF without any dependencies. Any straightforward DNF install without dependencies can be added here.

These roles are called individually from any playbook file located in the `/plays/` directory.

## Usage/Examples

```commandline
ansible-playbook plays/pb_server_setup.yml -i hosts/hosts.ini -Kk
```
