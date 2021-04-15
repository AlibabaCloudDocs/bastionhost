# Archive audit logs in Log Service

Bastionhost allows you to archive audit logs in Log Service. The audit logs record all O&M activities. After you configure the archiving settings for audit logs, Bastionhost automatically delivers the audit logs that it receives to Log Service. Compared with Bastionhost, Log Service provides more powerful log storage, query, and analysis features, which can help you improve O&M and operational efficiency. This topic describes how to archive audit logs in Log Service.

Audit logs record the O&M activities that O&M engineers perform by using Bastionhost. Bastionhost allows you to store audit logs only for 180 days. If you want to store audit logs for a longer period of time, you can archive the audit logs in Log Service. In the [Log Service console](https://sls.console.aliyun.com), you can customize the log retention period. In addition, you can query and analyze audit logs. For more information, see [Overview](/intl.en-US/Index and query/Overview.md) and [Real-time log analysis](/intl.en-US/Index and query/Real-time log analysis.md).

**Note:** The archiving operation does not affect the audit logs that are stored in Bastionhost instances. You can still view these audit logs on the Session Audit page of the [Bastionhost console](https://yundun.console.aliyun.com/?p=bastion). For more information, see [Search for sessions and view session details](/intl.en-US/User Guide (V3.2)/Administrator manual/Session audit/Search for sessions and view session details.md).

## Procedure

1.  Log on to the [Log Service console](https://sls.console.aliyun.com).

2.  Activate Log Service as required.

3.  In the **Log Application** section, click **Log Audit Service**.

4.  On the Global Configurations tab, complete the settings for collecting audit logs.

    1.  In the **Region of the Central Project** drop-down list, select a region for centralized storage of logs.

    2.  Configure authorization for log collection.

        Both manual authorization and AccessKey pair-based authorization are available. You can configure authorization for log collection by using one of the following methods:

        -   **AccessKey Pair-Based Authorization**: Enter the AccessKey ID and AccessKey secret of an authorized RAM user.

            The AccessKey ID and AccessKey secret are only for temporary use. The RAM user must be attached the AliyunRAMFullAccess policy.

        -   **Manual Authorization**: For more information, see [Authorize Log Service to collect and synchronize logs](/intl.en-US/Application/Log Audit Service/Authorize Log Service to collect and synchronize logs.md).
    3.  Find Bastion Host in the Cloud Products column, turn on **Operations Log**, and then specify a retention period for audit logs in the **Storage Type** column.

        ![Audit configuration](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/9970548161/p186788.png)

5.  View audit logs.

    1.  On the left-side navigation submenu, click the ![Audit Query](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/7073638161/p186709.png) icon.

    2.  In the left-side navigation pane, click **Bastionhost** under **Central**.

    3.  View the audit logs on the Bastion Host tab.


