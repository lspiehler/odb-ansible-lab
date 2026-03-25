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
ansible-inventory --list --yaml
```

## Ping Linux Host
```
ansible -m ping all
```

## Run Ansible variables Playbook
```
ansible-playbook ansible-vars.yml
```

## Read file content using ad-hoc ansible command
```
ansible -m ansible.builtin.command -a "cat /tmp/ip.txt" all
```

## Run public IP Playbook
```
ansible-playbook public-ip.yml
```