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


### Directory Structure
.:
  install-xdr-linux.yml  - Linux Install playbook
  lab                    - Inventory list of lab servers
  production             - Inventory list of production servers

./group_vars:
  linux_servers.yml        - Variables for linux servers (includes local/remote location and name of XDR install file and remote location of XDR agent install)

./roles:
  linux-xdr                - Linux XDR Role

./roles/linux-xdr:
  files                    - Files Used by XDR Role  
  tasks                    - Tasks Used by XDR Role

./roles/linux-xdr/tasks:
  install-xdr.yml          - Runs All Installation tasks
  main.yml                 - Runs All Included Tasks
  test-xdr.yml             - Tests Installation 
  
  
