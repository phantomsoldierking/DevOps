---
sidebar_position: 3
title: Terraform Commands
description: Terraform commands and their usage
tags: ["Terraform", "Infrastructure as Code", "HashiCorp"]
keywords: ["Terraform", "Infrastructure as Code", "HashiCorp"]
slug: "/terraform/commands"
---

1. Terraform Init

It is used to initialize a working directory containing Terraform configuration files. 

```bash
terraform init
```

2. Terraform Plan

It is used to create an execution plan. It shows what Terraform will do when you call apply. 

```bash
terraform plan
```

3. Terraform Apply

It is used to apply the changes required to reach the desired state of the configuration. 

```bash
terraform apply
```

4. Terraform Validate

We can run this command before applying the changes to check whether the configuration is syntactically valid and internally consistent. 

```bash
terraform validate
```

It will print the exact in the console if there is any error in the configuration file.

5. Terraform Format

It is used to rewrite Terraform configuration files to canonical format and style. 

```bash
terraform fmt
```

6. Terraform Show

It is used to provide human-readable output of current state of the resources. 

```bash
terraform show
```

We can also output the state in JSON format by using the following command:

```bash
terraform show -json
```

7. Terraform Providers

To know the list of providers used in the configuration file, we can use the following command:

```bash
terraform providers
```

To mirror the provider configurations from the configuration file, we can use the following command:

```bash
terraform providers mirror ./path/to/new_local_file
```

8. Terraform Output

It is used to extract the output variables from the state file. 

```bash
terraform output
```

9. Terraform Refresh

It is used to update the state file according to the real-world infrastructure. 

```bash
terraform plan
```

or 

```bash
terraform apply -refresh-only
```

10. Terraform Graph

It is used to generate a visual representation of the configuration and state file. 

```bash
terraform graph
```

11. Terraform Destroy

It is used to destroy the Terraform-managed infrastructure. 

```bash
terraform destroy
```

## AWS Commands

0. AWS Help

It is used to get help for the AWS CLI. 

```bash
aws help
```

Or to get help for a specific command, we can use the following command:

```bash
aws <command> help
aws iam help
```

1. AWS Configure

It is used to configure the AWS CLI. 

```bash
aws configure
```

2. To create an IAM user

```bash
aws iam create-user --user-name <user-name>
aws iam create-user --user-name lucy
```

To break it down here `iam` is command, `create-user` is the subcommand, `--user-name` is the option and `lucy` is the value of the option.

And the output for the above command will be:

```json
{
    "User": {
        "Path": "/",
        "UserName": "lucy",
        "Tags": [],
        "UserId": "AIDAJJQJH4K7E7EXAMPLE",
        "Arn": "arn:aws:iam::123456789012:user/lucy",
        "CreateDate": "2021-09-29T10:00:00+00:00"
    }
}
```

3. To see the list of IAM users

```bash
aws iam list-users
```

4. To delete an IAM user

```bash
aws iam delete-user --user-name <user-name>
aws iam delete-user --user-name lucy
```

5. To add a user to an IAM group

```bash
aws iam add-user-to-group --user-name <user-name> --group-name <group-name>
aws iam add-user-to-group --user-name lucy --group-name developers
```

1. To see attached policies to a user

```bash
aws iam list-attached-user-policies --user-name <user-name>
aws iam list-attached-user-policies --user-name lucy
```

1. To attach a policy to a user

```bash
aws iam attach-user-policy --user-name <user-name> --policy-arn <policy-arn>
aws iam attach-user-policy --user-name lucy --policy-arn arn:aws:iam::aws:policy/AmazonS3FullAccess
```

1. To create an IAM group

```bash
aws iam create-group --group-name <group-name>
aws iam create-group --group-name developers
```

1. To see the list of IAM groups

```bash
aws iam list-groups
```

1. To see attached policies to a group

```bash
aws iam list-attached-group-policies --group-name <group-name>
aws iam list-attached-group-policies --group-name developers
```

1. To attach a policy to a group

```bash
aws iam attach-group-policy --group-name <group-name> --policy-arn <policy-arn>
aws iam attach-group-policy --group-name developers --policy-arn arn:aws:iam::aws:policy/AmazonS3FullAccess
```


