# Diagnose network issues

The System Settings page in the Bastionhost console provides a network issue diagnostics feature that allows you to check the connectivity between Bastionhost and specific host ports. You can use this feature to confirm the network accessibility and perform O&M operations more efficiently. This topic describes how to use the network issue diagnostics feature.

The network issue diagnostics feature can detect the connectivity of IPv4 addresses and domain names.

## Procedure

1.  Find your bastion host and click Manage. For more information, see [Log on to Bastionhost](/intl.en-US/User Guide (V3.2)/Administrator manual/Log on to Bastionhost.md).

2.  In the left-side navigation pane, click **System Settings**.

3.  On the System Settings page, click the **Network Diagnosis** tab.

4.  Specify **Target IP Address** and **Port**.

    ![](https://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/en-US/9935703061/p135091.png)

5.  Click **Test Connection**.

    If the connectivity test is successful, the message **The network is connected.** appears. If the connectivity test fails, the message **The network is disconnected.** appears. In this case, you must handle the network connection exception. For more information, see [Handle network connection exceptions](#section_rii_dn3_xyg).


## Handle network connection exceptions

If a connectivity test fails, check the following items to identify the cause:

-   Check whether the security group rules allow access from Bastionhost to the specific host port.
-   Check whether a cloud firewall is deployed for the specific host and whether policies that allow access from Bastionhost to the specific host port are configured.
-   Check whether a local firewall is deployed for the specific host and whether policies that allow access from Bastionhost to the specific host port are configured.

