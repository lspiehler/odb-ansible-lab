## Prepare Environment
```
# git config --global user.email "lspiehler@gmail.com"
# git config --global user.name "Lyas Spiehler"
# source ~/venv/azure/bin/activate
# export ANSIBLE_CONFIG=$(pwd)/ansible.cfg
# . .env
```

## List Static Inventory
```
ansible-inventory -i inventory.yml --list --yaml
```

## Ping Linux Host
```
ansible -i inventory.yml -m ping all
```