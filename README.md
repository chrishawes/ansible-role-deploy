# ansible-role-deploy

## Testing
To test, first create your VM.
```
$ vagrant up
```

Run the following command to _deploy_ this file to the VM:
```
$ ansible-playbook --private-key=~/.vagrant.d/insecure_private_key -u vagrant -i .vagrant/provisioners/ansible/inventory/vagrant_ansible_inventory -M ../ test.yml
```

### Usage

The following variables are used:

| Variable  | Meaning | Default |
| ------------- | ------------- |------------- |
| deploy_user  | User the will own the deployed paths  | www-data |
| deploy_group  | Group the will own the deployed paths  | www-data |
| deploy_folder_mode  | Permissions for deployed paths  | 0755 |
| deploy_unarchive  | If you're deploying an archive, this will extract it | true |
| deploy_keep  | Number of previous artifacts to keep | 5 |
| deploy_pre_commands  | List of commands to run pre-deploy | echo |
| deploy_post_commands  | List of commands to run post-deploy | echo |

Take a look at `test.yml` to get a better idea.
