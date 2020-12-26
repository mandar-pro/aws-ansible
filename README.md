# aws-ansible
Create aws infrastructure with ansible &amp; cloudformation

## Prerequisites:

Packages:
 - ansible: 2.9.10
 - aws-cli: 1.16.198

collections:
 - amazon.aws: install with following command.<br>
   ```ansible-galaxy collection install amazon.aws```

authentication_details:
 - *aws access key* & *aws secret key* with necesaary access to create resources
 - set the keys in *./roles/aws-infra/vars/main.yml* file

## Usage

Create aws resources. It will result in creation of cloudformation stack containing all the necessary resources.<br>
```ansible-playbook aws-infra.yml```

Delete above created resources.<br>
```ansible-playbook aws-infra.yml --tags delete```