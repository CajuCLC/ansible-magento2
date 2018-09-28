# ansible-magento2

[![N|Solid](https://magebr.com/sites/default/files/Logo.png)](https://magebr.com/)

This is an Ansible playbook to install Magento 2 Open Source on a single server using Amazon Linux.
Follow the steps below to get it all set up!

### Requirements
* Brand new AWS EC2 running Amazon Linux.
    * It needs at least 2 GB of Memory RAM.
    * It was tested successfully on a t2.small instance.
* Magento Repo Keys: https://devdocs.magento.com/guides/v2.2/install-gde/prereq/connect-auth.html

### Installation
All variables are inside `group_vars/all.yml` and I added as many comments as possible so you can edit as you like.

Edit file `hosts.yml`, add the AWS EC2 public IP by replacing `AWS_IP` with the IP.

After editing the files, you can run the command:
```
ansible-playbook -i hosts.yml ansible-magento2.yml -k -vvv --private-key ~/.ssh/id_rsa --become
```

It should take 5 to 10 minutes depending on the size of the instance.

That should be it. Have fun with your Magento 2 installation.