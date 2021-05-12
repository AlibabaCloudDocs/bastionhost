# Apply for a free trial of Bastionhost

Bastionhost offers a 7-day free trial. This topic describes how to apply for a free trial of Bastionhost.

## Prerequisites

Before you can apply for a free trial, your Alibaba Cloud account must meet the following conditions:

-   Your Alibaba Cloud account is not used to purchase bastion hosts.
-   Your Alibaba Cloud account is not used for a free trial of Bastionhost.

**Note:** The Alibaba Cloud accounts that belong to the same enterprise or use the same mobile phone number are considered as one account in this situation. If such an Alibaba Cloud account is used to apply for a free trial of Bastionhost, you cannot apply for another free trial for this account. This also applies if the Alibaba Cloud account is used to purchase bastion hosts.

## Step 1: Apply for a free trial

1.  Visit the [free trial application page of Bastionhost](https://www.alibabacloud.com/campaign/bastionhost-free-trial-form) and log on to your Alibaba Cloud account.

2.  On the Apply for Bastionhost Free Trial page, enter the information such as your contact details, asset quantity, and compliance requirements.

3.  Click **Register Now**.

    After you submit your application, the Bastionhost team reviews your materials within one to three business days. Then, the team sends the review results to you by using text messages, emails, or internal messages. You can perform [Step 2: Activate the free trial](#section_nao_0ec_1xh) only after your application is approved.


## Step 2: Activate the free trial

After your application is approved, you must activate the free trial within seven calendar days. Otherwise, you cannot use the free trial. The following procedure describes how to activate the free trial of Bastionhost:

1.  Visit the [buy page of Bastionhost](https://common-buy-intl.alibabacloud.com/?&commodityCode=bastionhost_std_public_intl) and log on to your Alibaba Cloud account.

2.  Configure the parameters based on the following table.

    |Parameter|Example|Description|
    |---------|-------|-----------|
    |**Region and Zone**|Singapore|The region where you want to create a bastion host. **Note:** You cannot change the region after the bastion host is created. We recommend that you create the bastion host in the same region as the Elastic Compute Service \(ECS\) instances that you want to manage.

If the bastion host and ECS instances reside in different regions, they cannot communicate with each other over an internal network. You must use Cloud Enterprise Network to allow communication across the regions. For more information, see [What is CEN?]()

You can log on to the [ECS console](https://ecs.console.aliyun.com) to view the region where your ECS instances reside. For more information about regions, see [Regions and zones](). |
    |**Version**|HA Edition|The edition of the bastion host. You can select HA Edition or Basic Edition based on your business requirements. The following list compares the two editions:    -   **HA edition**: Bastionhost can run in dual-engine mode. This mode provides enhanced stability and reliability. When Bastionhost runs as normal, the two engines simultaneously work. This improves the O&M efficiency. If a single point of failure \(SPOF\) occurs, Bastionhost automatically switches between the two engines. This ensures business continuity. The HA edition uses higher specifications and provides higher performance. It ensures efficient and stable O&M in scenarios with 1,000 or more assets to manage.
    -   **Basic edition**: Bastionhost can run only in single-engine mode. In this mode, you can perform O&M and audit operations. |
    |**Plan**|20 Assets \(Trial Use\)|The number of assets that you can add to the bastion host. For the free trial, you can select only **20 Assets \(Trial Use\)**.|
    |**Extra Bandwidth**|5 Mbit/s|The extra public bandwidth of the bastion host. By default, Bastionhost provides 8 Mbit/s public bandwidth for the free trial. If the bandwidth cannot meet your business requirements, you can specify **Extra Bandwidth**.|
    |**Resource Group**|Default Resource Group|The resource group to which the bastion host belongs.|
    |**Quantity**|1|The number of bastion hosts that you want to create. For the free trial, you can select only **1** or **2**.|
    |**Duration**|1 Week|The validity period of the bastion host. For the free trial, you can select only **1 Week**.|

3.  Click **Buy Now** and complete the payment.

    If your free trial application is approved, the order cost is USD 0.

4.  On the Pay page, click **Console** to open the Bastionhost console.

5.  In the upper-left corner of the Bastionhost console, select the region you specify when you configure the parameters.

6.  Find the newly created bastion host and click **Run** on the right.

7.  In the **Run** panel, select a VPC, vSwitch, and security group for the bastion host.

    **Note:** The selected VPC and vSwitch cannot be changed after the bastion host is created. Proceed with caution.

8.  Click **OK**.

    Then, the bastion host changes to the **Creating** state. It takes about 5 minutes to create the bastion host. Wait for a few minutes.

    After the bastion host is created, you can perform O&M and audit operations. For more information about how to deploy host assets, users, and O&M rules on Bastionhost, see [Overview of Bastionhost V3.2](/intl.en-US/Quick Start/V3.2/Overview.md).

    **Note:** If you have questions about the free trial, you can contact customer service in the DingTalk group \(number: 33097550\).


