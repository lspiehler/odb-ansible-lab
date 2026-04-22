## Prepare Environment
```
git config --global user.email "lspiehler@gmail.com"
git config --global user.name "Lyas Spiehler"
source ~/venv/azure/bin/activate
export ANSIBLE_CONFIG=$(pwd)/ansible.cfg
. .env
```

## List Static Inventory
```
ansible-inventory --list --yaml | more
```

## Ping Linux Host
```
ansible -m ping all --limit azure_rm_linux
```

## Ping Windows Hosts
```
ansible -m win_ping all --limit azure_rm_windows
```

## Run Ansible variables Playbook
```
ansible-playbook ansible-vars.yml
```

## Read file content using ad-hoc ansible command
```
ansible -m ansible.builtin.command -a "cat /tmp/example.txt" all --limit azure_rm_linux
```

## Run public IP Playbook
```
ansible-playbook --limit ODBTST public-ip.yml
```

## Run Example Playbooks
```
ansible-playbook --limit azure_rm_linux example-loop.yml
```

## Run Role Playbook
```
ansible-playbook --limit azure_rm_linux test-role.yml
```