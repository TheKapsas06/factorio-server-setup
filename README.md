# Ansible repository for setting up factorio server
All of the ansible is in a role in `roles/factorio-server`.

## To use this roles as it is
### First run
#### Create inventory file
There is an example inventory file in `inventory/hosts.example.yaml`.\
Copy that file to `inventory/hosts.yaml` and change to the host you want to run it on.

You can also create `inventory/group_vars` for variables or create variable straight into `hosts.yaml`

#### Run playbook
When running this playbook for the first time run it with the tag `init`.
> If you have existing factorio save file you can add it to `roles/factorio-server/files/save.zip` and changed the variables `factorioserver_save` to `from_file`
```
ansible-playbook setup-factorio.yaml -t init
```
This way it will also init the save file with zero touch install.


### Second run
For the second run don't use the `init` tag.
This will skip creating a new save file.
```
ansible-playbook setup-factorio.yaml
```

### Variables
All of the default variables will be store and explained in `roles/factorio-server/defaults/main.yml`.

Factorio server version is set with the variable `factorioserver_version` under `roles/factorio-server/vars/main.yml`.

If you want to create a ansible-vault file to use you can do it under the root folder `.vault`.