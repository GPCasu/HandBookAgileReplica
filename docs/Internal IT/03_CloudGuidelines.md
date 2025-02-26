# Cloud Guidelines

This document provides a set of guidelines for cloud environment usage.
Aim of these guidelines is to ease the management and billing review of our internal cloud accounts.

### Resource Creation

Regardless of the cloud environment you are working on, we strongly suggest you to create resources using terragrunt/terraform.

### AWS

#### Region

We use Irland as default region. Of course, services that require specific region are exonerated. 

#### S3

We follow AWS guidelines for bucket naming convention, therefore buckets should be named with this pattern: `<prefix>-<region>-<accountId>`

#### Tags

Each resource must include tags. Here the list that must be provided

```
scope: project-name
alwaysOn: true|false (Only true or false are allowed. If false, an automated or manual process could stop it outside office hours)
ownedBy: name.surname@agile.it
createdBy: name.surname@agilelab.it
```

A service control policy is attached to aws account, allowing tags enforcement.
So, if a tag is missing then a Not Authorized error occurs.

Using tags, resource and cost tracking is easier. For example, users can find their own tagged resources by "Resource Groups & Tag Editor" console or AWS CLI.

#### EC2

Whenever possible, use **spot** ec2.

#### IAM Role

All users are assigned the same role. This role allows the use of AWS without any particular restrictions.
In this way, we try to make the use of AWS more effective by removing slowdowns due to the lack of adequate privileges.
Each user is responsible for maintaining their own resources, removing or stopping them when they are no longer needed, paying attention to budget consumption.

#### Users Access
Every user is provided console and programmatic access.
