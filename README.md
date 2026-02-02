# AWS-CLI-Commands
AWS Command Line commands which we use on daily purpose

#### AWS Configure:
- To configure a new AWS account in CLI:
```
aws configure
```
Provide access key, secret key, default region and format as json (in small) and it will make an entry in home directory .aws folder and credentials and config files

**Note:** To create access key, login to AWS Account -> Top right (Drop down) -> Security credentials -> Scroll to Access Key and create access key

- To list the accounts:
```
aws configure list-profiles
```

- To add another account, name it with meaningful account name:
```
aws configure --profile <profile name>
```
give access key, secret key, default region and format as json (in small)

To list all the accounts:
```
aws configure list-profiles
```

- To remove old profile:
delete the unwanted profile -
```
vi ~/.aws/credentials
```
remove config here -
```
vi ~/.aws/config
```
**- Swtich between accounts** [only when you have configured two or more account]

Verify which account it is configured:
```
aws sts get-caller-identity
```

to view list of account:
```
aws configure list-profile
```

Configure to particular account:
```
export AWS_PROFILE=<account name>
```

Verify once again which account it is configured:
```
aws sts get-caller-identity
```

or you can always add --profile <profile name>
```
Example: aws s3 ls --profile herovired
aws s3 ls --profile default
```
