# Authorize Bastionhost to access cloud resources

When you use Bastionhost for the first time, authorize it to access other cloud resources. This topic describes how to perform the authorization.

-   A bastion host is created. For more information, see [Create a Bastionhost instance](/intl.en-US/Pricing/Create a Bastionhost instance.md).
-   You are using an Alibaba Cloud account, or a RAM user who has permissions to create or delete service linked roles.

When you use Bastionhost for the first time, Alibaba Cloud automatically creates a service linked role AliyunServiceRoleForBastionhost, which allows Bastionhost to access other cloud services. You do not need to manually create or modify a service linked role. For more information, see [Service linked roles](/intl.en-US/RAM Role Management/Service linked roles.md).

## Procedure

1.  Log on to the [Bastionhost console](https://yundun.console.aliyun.com/?p=bastion).

2.  In the **Welcome to Bastionhost** dialog box, click **Create**.

    When you log on to the Bastionhost console for the first time after your bastion host is created, the console prompts you to authorize Bastionhost to access other cloud resources.

    After you click **Create**, Alibaba Cloud automatically creates the AliyunServiceRoleForBastionhost role. You can view the created role on the RAM Roles page of the [RAM console](https://ram.console.aliyun.com/roles). Your bastion host can access other cloud services, such as Alibaba Cloud Elastic Compute Service \(ECS\) and Virtual Private Cloud \(VPC\), or perform server O&M and audit only after the AliyunServiceRoleForBastionhost role is created.


## Service linked role for Bastionhost

If you want to use Bastionhost for O&M, it needs to access other cloud services, such as ECS and VPC. To obtain the access permissions, you must assume the AliyunServiceRoleForBastionhost role that is automatically created for Bastionhost.

The following list provides details of the AliyunServiceRoleForBastionhost role:

-   Role: AliyunServiceRoleForBastionhost
-   Permission policy: AliyunServiceRolePolicyForBastionhost

    **Note:** This is a system policy. You are not allowed to modify the name or content of this policy.

-   Example:

    ```
    {
        "Version": "1",
        "Statement": [
            {
                "Action": [
                    "ecs:DescribeInstances",
                    "ecs:DescribeImages",
                    "ecs:DescribeZones",
                    "ecs:DescribeRegions",
                    "ecs:DescribeTags",
                    "ecs:DescribeSecurityGroups",
                    "ecs:DescribeSecurityGroupAttribute",
                    "ecs:AuthorizeSecurityGroup",
                    "ecs:DescribeSecurityGroups",
                    "ecs:DescribeSecurityGroupReferences",
                    "ecs:CreateSecurityGroup",
                    "ecs:RevokeSecurityGroup",
                    "ecs:DeleteSecurityGroup",
                    "ecs:ModifySecurityGroupAttribute",
                    "ecs:ModifySecurityGroupPolicy",
                    "ecs:ModifySecurityGroupRule",
                    "ecs:CreateNetworkInterface",
                    "ecs:DeleteNetworkInterface",
                    "ecs:DescribeNetworkInterfaces",
                    "ecs:CreateNetworkInterfacePermission",
                    "ecs:DescribeNetworkInterfacePermissions",
                    "ecs:DeleteNetworkInterfacePermission",
                    "ecs:DetachNetworkInterface",
                    "ecs:AttachNetworkInterface"
                ],
                "Resource": "*",
                "Effect": "Allow"
            },
            {
                "Action": [
                    "vpc:DescribeVpcAttribute",
                    "vpc:DescribeVSwitchAttributes"
                ],
                "Resource": "*",
                "Effect": "Allow"
            },
            {
                "Action": "ram:DeleteServiceLinkedRole",
                "Resource": "*",
                "Effect": "Allow",
                "Condition": {
                    "StringEquals": {
                        "ram:ServiceName": "bastionhost.aliyuncs.com"
                    }
                }
            }
        ]
    }
    ```


## Delete the AliyunServiceRoleForBastionhost role

If you no longer use Bastionhost, you can delete its service linked role AliyunServiceRoleForBastionhost. Before you can delete the AliyunServiceRoleForBastionhost role, you must release your bastion host. Then, perform the following steps:

1.  Log on to the [RAM console](https://ram.console.aliyun.com/roles).

2.  In the left-side navigation pane, click **RAM Roles**.

3.  Search for the AliyunServiceRoleForBastionhost role and click **Delete** in the Actions column.

4.  In the **Delete RAM Role** message, click **OK**.


## FAQ

The system does not create the AliyunServiceRoleForBastionhost role for my RAM user. What do I do?

The system creates and deletes the AliyunServiceRoleForBastionhost role only if your RAM user has the required permissions. To obtain the required permissions, add the following permission policy to your RAM user. For more information, see [Grant permissions to a RAM role](/intl.en-US/RAM Role Management/Grant permissions to a RAM role.md).

```
{
    "Statement": [
        {
            "Action": [
                "ram:CreateServiceLinkedRole"
            ],
            "Resource": "acs:ram:*:ID of your Alibaba Cloud account:role/*",
            "Effect": "Allow",
            "Condition": {
                "StringEquals": {
                    "ram:ServiceName": [
                        "bastionhost.aliyuncs.com"
                    ]
                }
            }
        }
    ],
    "Version": "1"
}                
```

