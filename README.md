# Github Backups

Configures a VM with necessary dependencies to execute the [github-backup](https://github.com/ddollar/github-backup)
gem.

## Vagrant Steps
1. Obtain vault password
2. `make all` - Creates the VM, downloads Ansible roles, creates inventory/ssh config
3. `ansible-playbook setup.yml --ask-vault-pass` - Runs the setup playbook and backups
4. (optional) `ansible-playbook backup.yml --ask-vault-pass` - Only runs the backups, assumes an existing environment is
   provisioned.

