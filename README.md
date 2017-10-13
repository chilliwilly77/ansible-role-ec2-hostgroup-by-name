# ec2 hostgroup by name

This role adds ec2 instances with the same name to a hostgroup. This must be used with the
Ansible ec2 dynamic inventory configuration. See [ansible docs](http://docs.ansible.com/ansible/latest/intro_dynamic_inventory.html#example-aws-ec2-external-inventory-script) 
for more details on ec2 dynamic inventory and the setup.

## Variables

The following variables can be set:

| Name          | Required | Description                                         | Example   | Default        |
| ------------- | -------- | --------------------------------------------------- | --------- | -------------- |
| hostgroup     | yes      | Ansible hostgroup to assign matching instance names | routers   | NA             |
| instance_name | yes      | ec2 instance names to add to hostgroup              | router    | NA             |
| region        | yes      | The AWS region to use                               | eu-west-1 | env.AWS_REGION |
