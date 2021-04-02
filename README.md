# Installing Cortex XDR Agent with Ansible

## Requirements
** SSH Installed on remote hosts
** Strongly Recommend using SSH Keys On Remote Hosts
** Remote User with SUDO privledges

## Install On Linux
1. Download Agent File to roles/linux-xdr/files
2. Set file name in group_vars/linux_servers.yml
3. Set Host Names in production and lab files
4. Execute Playbook - "ansible-playbook -i lab -user <remote username> --ask-become-pass install-xdr-linux.yml"

### Details
