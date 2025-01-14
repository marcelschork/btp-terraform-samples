# Multiple subaccounts with entitlements, subscriptions and role collection assigments

## Overview

This sample shows how to create a multi account setup reflecting a multi stage landscape. The subaccounts will be entitled with different services and subscribe to different applications. Additionally different role collections are assigned to different users.

## Content of setup

The setup comprises the following resources:

- Creation of three SAP BTP subaccounts
- Entitlements of services
- Subscriptions to applications
- Role collection assignments to users
- Creation of CF environments
- Management of users and roles on org and space level

## Deploying the resources

To deploy the resources you must:

1. Create a file `secret.auto.tfvars` and maintain the credentials for the BTP and CF provider

   ```hcl
   username = "<Email address of your BTP user>"
   password = "<Password of your BTP user>"
   ```

2. Change the variables in the `variables.tf` file to meet your requirements
3. Initialize your workspace:

   ```bash
   terraform init
   ```

4. You can check what Terraform plans to apply based on your configuration:

   ```bash
   terraform plan
   ```

5. Apply your configuration to provision the resources:

   ```bash
   terraform apply
   ```

## In the end

You probably want to remove the assets after trying them out to avoid unnecessary costs. To do so execute the following command:

```bash
terraform destroy
```
