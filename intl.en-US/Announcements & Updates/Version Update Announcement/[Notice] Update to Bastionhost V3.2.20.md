# \[Notice\] Update to Bastionhost V3.2.20

Dear Alibaba Cloud users,

From July 12, 2021, Alibaba Cloud starts to roll out updates based on Bastionhost V3.2.20. The features of Bastionhost V3.2.20 include new features and the features that are optimized based on V3.2.18.

## New features

Bastionhost V3.2.20 introduces the following new features:

-   O&M is supported for LANs and optimized for hybrid scenarios in which data centers, heterogeneous clouds, and virtual private clouds \(VPCs\) are involved. This feature is available in HA Edition.
-   The alert notification feature is supported. Notifications are sent in the following scenarios: commands are approved or rejected, passwords are changed, storage alerts are reported, shared keys expire, or weekly reports are generated.
-   O&M logs can be backed up and exported.

For more information about the supported features, see [Release notes](/intl.en-US/Announcements & Updates/Release notes.md).

## Update methods

You can update your bastion host in custom or automatic mode.

-   **Custom**: You can specify a custom period during which you want to update your bastion host. The period must be within the [Available update periods](#section_e9o_dmy_efj) for the region of your bastion host. For more information, see [Update a bastion host](/intl.en-US/Announcements & Updates/Update a bastion host.md).

    **Note:** If you choose the automatic mode, your bastion host is updated during a default period. Bastionhost randomly determines default periods based on [Available update periods](#section_e9o_dmy_efj).

    If you want to update your bastion host during a custom period, we recommend that you specify the custom period at the beginning of the [Available update periods](#section_e9o_dmy_efj) for the region of your bastion host. If you do not specify the custom period at the beginning of the available update period, your bastion host may be automatically updated when a default period starts.

-   **Automatic**: Your bastion host is automatically updated when a default period starts. If you do not specify a custom period for an update, your bastion host is automatically updated during a default period.

    **Note:** The default period may overlap with the peak hours of your business. This may affect your business. To prevent business interruptions, we recommend that you specify a custom period during which the impact of an update is minimized.


## Impact

If your bastion host is being updated, it is in the Updating Configuration state, and your business may be interrupted for a few seconds. We recommend that you specify a custom period to update your bastion host in the off-peak hours of your business.

## Available update periods

The available update periods vary based on the region of your bastion host. The following table lists available update periods for specific regions.

**Note:** During the available update period for the region of your bastion host, you can specify a custom period to update your bastion host or wait until your bastion host is automatically updated.

|Available update period|Region|
|-----------------------|------|
|2021-07-12 to 2021-07-16|The following regions support updates during this period:-   China \(Zhangjiakou\) \(region ID: cn-zhangjiakou\)
-   Singapore \(Singapore\) \(region ID: ap-southeast-1\) |
|2021-07-19 to 2021-07-23|The following regions support updates during this period:-   China \(Shenzhen\) \(region ID: cn-shenzhen\)
-   China \(Chengdu\) \(region ID: cn-chengdu\)
-   China \(Qingdao\) \(region ID: cn-qingdao\)
-   China \(Hohhot\) \(region ID: cn-huhehaote\)
-   Germany \(Frankfurt\) \(region ID: eu-central-1\) |
|2021-07-26 to 2021-07-30|The following regions support updates during this period:-   China \(Shanghai\) \(region ID: cn-shanghai\)
-   US \(Virginia\) \(region ID: us-east-1\)
-   US \(Silicon Valley\) \(region ID: us-west-1\)
-   Japan \(Tokyo\) \(region ID: ap-northeast-1\)
-   Australia \(Sydney\) \(region ID: ap-southeast-2\) |
|2021-08-02 to 2021-08-06|The following regions support updates during this period:-   China \(Hangzhou\) \(region ID: cn-hangzhou\)
-   China \(Beijing\) \(region ID: cn-beijing\)
-   China \(Hong Kong\) \(region ID: cn-hongkong\)
-   China \(Heyuan\) \(region ID: cn-heyuan\)
-   India \(Mumbai\) \(region ID: ap-south-1\)
-   Indonesia \(Jakarta\) \(region ID: ap-southeast-5\)
-   Malaysia \(Kuala Lumpur\) \(region ID: ap-southeast-3\)
-   UK \(London\) \(region ID: eu-west-1\)
-   UAE \(Dubai\) \(region ID: me-east-1\) |

**Note:** For Alibaba Gov Cloud and Alibaba Finance Cloud, Alibaba Cloud will roll out updates based on Bastionhost V3.2.20 from August 2, 2021 to August 6, 2021. During this period, you can specify a custom period to update your bastion host or wait until your bastion host is automatically updated.

