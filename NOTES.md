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

## Run Show Vars Playbook
```
ansible-playbook show-vars.yml
```
