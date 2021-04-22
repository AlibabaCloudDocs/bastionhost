# Pre-sales FAQ

This topic provides answers to some commonly asked questions about Bastionhost.

Bastionhost provides more features and improves user experience over scheduled version updates. Differences exist in features between different versions of Bastionhost instances. For more information, see [Versions and documents](/intl.en-US/.md). Pre-sales FAQ is divided into the following sections based on different versions of Bastionhost instances:

-   **FAQ about all versions of Bastionhost**
    -   [Can I synchronize ECS instances that reside in different VPCs to a Bastionhost instance?](#section_uh3_qy4_ydb)
    -   [Can I use a single Bastionhost instance to perform O&M audit on the ECS instances that reside in different VPCs or regions or are deployed under different accounts?](#section_gpt_4y4_ydb)
    -   [Am I charged for enabling SMS-based two-factor authentication?](#section_rtp_my4_ydb)
    -   [What is the operating system of Bastionhost instances? Can I replace this existing operating system with another one?](#section_egv_ly4_ydb)
    -   [Why are the available regions different when I purchase Bastionhost instances under different Alibaba Cloud accounts?](#section_w5r_jy4_ydb)
    -   [Can Bastionhost instances be customized?](#section_c1n_hy4_ydb)
-   **FAQ about Bastionhost V3.2**

    [Which countries and regions support the SMS-based two-factor authentication feature of Bastionhost?](#section_gxg_c0m_3tj)

-   **FAQ about Bastionhost V2 and V3.1**
    -   [Do Bastionhost instances provide stable performance?](#section_cqp_v62_kpu)
    -   [Can I log on to the operating system of Bastionhost instances?](#section_329_moy_toz)

## Can I synchronize ECS instances that reside in different VPCs to a Bastionhost instance?

The answer depends on whether the VPCs belong to the same Alibaba Cloud account.

-   **If the VPCs belong to different Alibaba Cloud accounts**, you cannot synchronize the ECS instances to a Bastionhost instance. We recommended that you deploy Bastionhost instances separately under each Alibaba Cloud account. Alternatively, you can manually add ECS instances to your Bastionhost instance.

    **Note:** If you want to perform O&M on ECS instances under different Alibaba Cloud accounts, make sure that the ECS instances are configured with public IP addresses. This way, you can access the ECS instances over the Internet from your Bastionhost instance.

-   **If the VPCs belong to the same Alibaba Cloud account**, you can synchronize all the ECS instances to a Bastionhost instance.

    **Note:** Before you perform O&M on the ECS instances that reside in different VPCs, make sure that you can access the ECS instances over an internal network by using Alibaba Cloud Express Connect or over the Internet from your Bastionhost instance.


## Can I use a single Bastionhost instance to perform O&M audit on the ECS instances that reside in different VPCs or regions or are deployed under different accounts?

Yes, you can perform O&M audit on the ECS instances that reside in different VPCs or regions or are deployed under different accounts only if you can access the ECS instances from your Bastionhost instance.

For example, you created more than 10 ECS instances under the same Alibaba Cloud account in the China \(Qingdao\), China \(Beijing\), and China \(Zhangjiakou\) regions. If you can access these ECS instances from your Bastionhost instance, you can perform O&M audit on these ECS instances.

For example, you created 13 ECS instances under the same Alibaba Cloud account. Nine ECS instances reside in the classic network and the other four ECS instances reside in a VPC. If you can access all these ECS instances from your Bastionhost instance, you can perform O&M audit on these ECS instances.

**Note:** If you cannot access all these ECS instances from your Bastionhost instance, you may need to deploy multiple Bastionhost instances to perform O&M audit on different ECS instances.

You can use the following methods to enable communications between ECS instances and Bastionhost instances:

-   If the ECS instances for which you want to perform O&M are accessible over the Internet, add rules that allow access from Bastionhost in the security groups of the ECS instances. For more information, see [Add security group rules](/intl.en-US/Security/Security groups/Add security group rules.md).
-   If the ECS instances for which you want to perform O&M are deployed in a VPC, connect this VPC to Bastionhost by using a Cloud Enterprise Network \(CEN\). For more information, see [What is CEN?]().

## Am I charged for enabling SMS-based two-factor authentication?

No, you are not charged for enabling SMS-based two-factor authentication. For more information about how to enable SMS-based two-factor authentication, see [Enable two-factor authentication](/intl.en-US/User Guide (V3.2)/Administrator manual/Authentication settings/Enable two-factor authentication.md).

## What is the operating system of Bastionhost instances? Can I replace this existing operating system with another one?

Bastionhost instances run the CentOS operating system, which cannot be replaced.

## Why are the available regions different when I purchase Bastionhost instances under different Alibaba Cloud accounts?

Servers under different Alibaba Cloud account types implement physical isolation and network isolation. You can purchase Bastionhost instances in specific regions based on your account types, such as Alibaba Gov Cloud and Alibaba Finance Cloud accounts. For example, you can use only an Alibaba Gov Cloud account to purchase the Bastionhost instances deployed in the **China North 2 Ali Gov** region. You can go to the [buy page](https://common-buy.aliyun.com/) of Bastionhost to view the available regions for your account.

## Can Bastionhost instances be customized?

No, you can select only the specifications that are offered by Alibaba Cloud. The following table lists the available specifications. For more information, see [Billing](/intl.en-US/Pricing/Billing.md).

## Which countries and regions support the SMS-based two-factor authentication feature of Bastionhost?

The following table lists the countries and regions that support the SMS-based two-factor authentication feature of Bastionhost.

|Region|Country or special administrative region: calling code|
|------|------------------------------------------------------|
|China|Hong Kong \(China\): +852|
|Macau \(China\): +853|
|Taiwan \(China\): +886|
|Mainland China: +86|
|Outside China|Russia: +7|
|Singapore: +65|
|Malaysia: +60|
|Indonesia: +62|
|Germany: +49|
|Australia: +61|
|US: +1|
|Dubai: +971|
|Japan: +81|
|UK: +44|
|India: +91|
|South Korea: +82|
|Philippines: +63|
|Switzerland: +41|
|Sweden: +46|

## Do Bastionhost instances provide stable performance?

Yes, Bastionhost instances provide stable performance. Bastionhost instances run on ECS instances. The annual availability of Bastionhost instances exceeds 99.95%.

The protocol engine used for Bastionhost has passed the traffic test on the data volume of more than 1 PB. Core O&M functions of Bastionhost work stably.

## Can I log on to the operating system of Bastionhost instances?

No, you cannot log on to the operating system of Bastionhost instances. This helps ensure compliance audit of log data in Bastionhost and prevent artificial destruction.

