# Update a bastion host

Bastionhost supports automatic and custom updates. An automatic update is performed during a default period, which may overlap with the peak hours of your business. This may affect your business. To prevent business interruptions, we recommend that you specify a custom period during which the impact of an update is minimized. This topic describes how to update a bastion host.

After a new version of Bastionhost is released, the Bastionhost console displays New Version in the Version section. You can click Upgrade to the right of New Version to specify the update time.

1.  Log on to the [Bastionhost console](https://yundun.console.aliyun.com/?p=bastion).

2.  On the Instances page, find your bastion host and check whether **New Version** is displayed in the Version section.

    ![New Version](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/1603506261/p293266.png)

    -   If New Version is displayed, click **Upgrade**.
    -   If New Version is not displayed, view the available update period for the region of your bastion host. If the period does not start, your bastion host cannot be updated. Wait until the period starts and configure the update settings again. For more information about the available update periods, see [\[Notice\] Update to Bastionhost V3.2.20](t2081510.md#).
3.  In the **Upgrade Version** dialog box, configure the parameters.

    For a custom update, you can select **Upgrade at Specific Time Range** or **Upgrade Now**.

    -   **Upgrade at Specific Time Range**

        A default period is displayed. If you do not want to use that period, select a different default period or specify a custom period.

        1.  In the Upgrade Version dialog box, set **Upgrade Method** to **Upgrade at Specific Time Range**.
        2.  Set **Upgrade Time** to **Default Time** or **Custom Time**.

            ![Upgrade Version dialog box](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/1603506261/p293267.png)

        3.  Specify **Specific Time Range**.

            **Note:** The valid values of **Specific Time Range** vary based on the setting of Upgrade Time.

            -   **Default Time**: Bastionhost provides three default periods. You can select a default period during which the impact of an update on your business is minimized.
            -   **Custom Time**: You must specify a period of 2 hours or a multiple of 2 hours, such as 4 hours. The period must also start on the hour. Example: 2021-05-22 15:00:00 to 2021-05-22 17:00:00.
    -   **Upgrade Now**

        Select **Upgrade Now**.

4.  After you configure the settings, click **OK**.

    Your bastion host is updated based on your settings.

    **Note:** If you do not specify a custom period for an update, your bastion host is automatically updated during a default period.


