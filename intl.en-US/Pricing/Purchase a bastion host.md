# Purchase a bastion host

Before you can use Bastionhost, you must purchase a bastion host. This topic describes how to purchase a bastion host.

1.  Log on to your Alibaba Cloud account and visit the [buy page of Bastionhost](https://common-buy-intl.alibabacloud.com/?&commodityCode=bastionhost_std_public_intl).

2.  Configure the parameters.

    The following table describes the parameters.

    |Parameter|Description|
    |---------|-----------|
    |**Region and Zone**|The region where you want to create a bastion host. **Note:** You cannot change the region after the bastion host is created. We recommend that you create the bastion host in the same region as the Elastic Compute Service \(ECS\) instances that you want to manage.

If the bastion host and ECS instances reside in different regions, they cannot communicate with each other over an internal network. You must use Cloud Enterprise Network to allow communication across the regions. For more information, see [What is CEN?]()

You can log on to the [ECS console](https://ecs.console.aliyun.com) to view the region where your ECS instances reside. For more information about regions, see [Regions and zones](). |
    |**Version**|The edition of the bastion host. You can select HA Edition or Basic Edition based on your business requirements. The following list compares the two editions:    -   **HA edition**: Bastionhost can run in dual-engine mode. This mode provides enhanced stability and reliability. When Bastionhost runs as normal, the two engines simultaneously work. This improves the O&M efficiency. If a single point of failure \(SPOF\) occurs, Bastionhost automatically switches between the two engines. This ensures business continuity. The HA edition uses higher specifications and provides higher performance. It ensures efficient and stable O&M in scenarios with 1,000 or more assets to manage.
    -   **Basic edition**: Bastionhost can run only in single-engine mode. In this mode, you can perform O&M and audit operations. |
    |**Plan**|The number of assets that you can add to the bastion host. For more information about service plans, see [Billing](/intl.en-US/Pricing/Billing.md). |
    |**Extra Bandwidth**|The extra public bandwidth of the bastion host. After you specify the number of assets, the public bandwidth of the bastion host is automatically configured. For more information, see [Billing](/intl.en-US/Pricing/Billing.md). If the bandwidth cannot meet your business requirements, you can specify **Extra Bandwidth**. The following list describes this parameter:    -   **Value range**: 10 Mbit/s to 500 Mbit/s
    -   **Increment**: 10 Mbit/s |
    |**Resource Group**|The resource group to which the bastion host belongs. Resource groups are designed for enterprise users. Enterprise users can use this feature to organize and manage the resources that are owned by multiple accounts and assigned to multiple projects. For more information about how to create a resource group, see [Create a resource group](). |
    |**Quantity**|The number of bastion hosts that you want to create.|
    |**Duration**|The validity period of the bastion host. **Note:** You can select **Auto-renewal**. If auto-renewal is enabled, you will receive a renewal notification before the bastion host expires. In this case, Bastionhost automatically renews your subscription. The subscription period of the automatically renewed bastion host is the same as Duration. |

3.  Click **Buy Now** and complete the payment.


**Related topics**  


[Billing](/intl.en-US/Pricing/Billing.md)

