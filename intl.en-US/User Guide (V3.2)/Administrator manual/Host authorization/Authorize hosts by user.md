# Authorize hosts by user

Host authorization is to associate users with host assets in Bastionhost. If you authorize hosts by user, a user can access only the hosts authorized to the user. This topic describes how to authorize hosts and their accounts by user. This topic also describes how to maintain these hosts and accounts.

## Authorize hosts

To authorize hosts for a user, follow these steps:

1.  Find your bastion host and click Manage. For more information, see [Log on to Bastionhost](/intl.en-US/User Guide (V3.2)/Administrator manual/Log on to Bastionhost.md).

2.  In the left-side navigation pane, choose **Users** \> **Users**.

3.  Find the target user and click **Authorize Hosts** in the **Actions** column.

    ![Authorize hosts for a user (1)](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/3400843951/p65171.png)

4.  On the **Authorized Hosts** tab that appears, click **Authorize Hosts**.

5.  In the Authorize Hosts pane that appears, select one or more hosts you want to authorize for the user to maintain and click **OK**.

    ![Authorize hosts for a user (2)](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/2400843951/p65174.png)


## Remove authorized hosts

If a user does not need to maintain certain hosts, follow these steps to remove the authorized hosts to achieve the principle of least privilege:

1.  Find your bastion host and click Manage. For more information, see [Log on to Bastionhost](/intl.en-US/User Guide (V3.2)/Administrator manual/Log on to Bastionhost.md).

2.  In the left-side navigation pane, choose **Users** \> **Users**.

3.  Find the target user and click **Authorize Hosts** in the **Actions** column.

    ![Click Authorize Hosts](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/3400843951/p65171.png)

4.  On the Authorized Hosts tab that appears, select the authorized hosts you want to remove and click **Remove** in the lower-left corner.

    ![Remove authorized hosts](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/3400843951/p65202.png)

5.  In the message that appears, click **Remove**.


## Authorize the accounts of a single host

To authorize the accounts of a single host for a user, follow these steps:

1.  Find your bastion host and click Manage. For more information, see [Log on to Bastionhost](/intl.en-US/User Guide (V3.2)/Administrator manual/Log on to Bastionhost.md).

2.  In the left-side navigation pane, choose **Users** \> **Users**.

3.  Find the target user and click **Authorize Hosts** in the **Actions** column.

    ![Authorize hosts for a user (1)](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/3400843951/p65171.png)

4.  On the **Authorized Hosts** tab that appears, find the target host and click the information in the **Authorized Accounts** column.

    ![Authorize the accounts of a single host](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/3400843951/p65177.png)

5.  In the Select Accounts pane that appears, select one or more accounts and click **Update**.

    **Note:** If the host does not have an account, you can click **Create Host Account** in the Select Accounts pane to create one first.


## Authorize the accounts of multiple hosts

To authorize the accounts of multiple hosts for a user at a time, follow these steps:

1.  Find your bastion host and click Manage. For more information, see [Log on to Bastionhost](/intl.en-US/User Guide (V3.2)/Administrator manual/Log on to Bastionhost.md).

2.  In the left-side navigation pane, choose **Users** \> **Users**.

3.  Find the target user and click **Authorize Hosts** in the **Actions** column.

    ![Authorize hosts for a user (1)](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/3400843951/p65171.png)

4.  On the Authorized Hosts tab that appears, select the target hosts and select **Batch Authorize Accounts** from the **Batch** drop-down list.

    ![Authorize the accounts of multiple hosts](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/3400843951/p65187.png)

5.  In the Batch Authorize Accounts pane that appears, specify **Accounts**.

    ![Batch Authorize Accounts pane](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/3400843951/p65196.png)

    **Note:** Currently, you can select only one host account at a time during the authorization of host accounts.

6.  Click **Update**.


## Remove the authorized accounts of multiple hosts

To remove the authorized accounts of multiple hosts for a user at a time, follow these steps:

1.  Find your bastion host and click Manage. For more information, see [Log on to Bastionhost](/intl.en-US/User Guide (V3.2)/Administrator manual/Log on to Bastionhost.md).

2.  In the left-side navigation pane, choose **Users** \> **Users**.

3.  Find the target user and click **Authorize Hosts** in the **Actions** column.

    ![Click Authorize Hosts](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/3400843951/p65171.png)

4.  On the **Authorized Hosts** tab that appears, select the target hosts.

5.  Select **Batch Remove Authorized Accounts** from the **Batch** drop-down list.

    ![Authorized Hosts tab](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/0867558161/p65214.png)

6.  In the Batch Remove Authorized Accounts pane that appears, specify Accounts.

    ![Batch Remove Authorized Accounts pane](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/4400843951/p65216.png)

    **Note:** Currently, you can select only one host account at a time during the removal of authorized host accounts.

7.  Click **Update**.


