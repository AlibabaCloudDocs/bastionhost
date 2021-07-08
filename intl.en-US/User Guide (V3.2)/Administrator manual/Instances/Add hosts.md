# Add hosts

This topic describes how to add hosts to Bastionhost. You can import Alibaba Cloud ECS instances under your Alibaba Cloud account or hosts from other sources to Bastionhost. Only after you add a host to Bastionhost, O&M personnel can perform O&M operations on the host.

## Import ECS instances

Follow these steps to import ECS instances under your Alibaba Cloud account to Bastionhost. This operation does not affect the current status of the ECS instances under your Alibaba Cloud account.

1.  Find your bastion host and click Manage. For more information, see [Log on to Bastionhost](/intl.en-US/User Guide (V3.2)/Administrator manual/Log on to Bastionhost.md).

2.  In the left-side navigation pane, choose **Assets** \> **Hosts**.

3.  On the Hosts page, click **Import ECS Instances**.

4.  In the Select Region dialog box, select the region where the ECS instances to be imported reside and click **OK**.

    ![Select region](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/4894343951/p64878.png)

5.  In the Import ECS Instances dialog box, select the ECS instances to be imported and click **Import**.

    ![Import ECS instances](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/4894343951/p64879.png)


## Import hosts from other sources

You can select **Create Host**, **Import RDS Host Groups**, or **Import Hosts from File** from the Import Other Hosts drop-down list to add hosts.

1.  Find your bastion host and click Manage. For more information, see [Log on to Bastionhost](/intl.en-US/User Guide (V3.2)/Administrator manual/Log on to Bastionhost.md).

2.  In the left-side navigation pane, choose **Assets** \> **Hosts**.

3.  Select **Create Host**, **Import RDS Host Groups**, or **Import Hosts from File** from the **Import Other Hosts** drop-down list.

    ![Import Other Hosts](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/4894343951/p64884.png)

    The three methods for **Import Other Hosts** are as follows:

    -   **Create Host**

        You can use this method to manually add a host. Select **Create Host**. In the Create Host pane, specify Operating System, Host IP Address, Hostname, and Remarks to manually add a host.

        ![Create Host](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/4894343951/p98201.png)

    -   **Import RDS Host Groups**

        You can use this method to import RDS dedicated cluster hosts. Select **Import RDS Host Groups**. In the Import RDS Host Groups dialog box, select the RDS dedicated cluster hosts you want to import, and click **Import**.

    -   **Import Hosts from File**

        You can use this method to import multiple hosts to Bastionhost at a time. Select **Import Hosts from File**. In the Import Hosts pane, click **Download Host Template** and fill in host information in the template file. Click **Upload** to upload the file. In the Preview dialog box, select the hosts to be imported and click **Import**. In the Import Hosts pane, click **Import Hosts** to import the hosts.

        ![Preview of host import](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/4894343951/p98207.png)

        **Note:** The downloaded template package contains template files in the XLS, CSV, and XLSX formats for you to select.


## What to do next

-   After you add hosts to Bastionhost, you must create accounts for the hosts. For more information, see [Create an account for hosts](/intl.en-US/User Guide (V3.2)/Administrator manual/Host management/Create an account for hosts.md).
-   If the default port for the O&M protocol \(RDP or SSH\) is not used in a host, you need to change the matching service port in Bastionhost. For more information, see [Change the service port of a host](/intl.en-US/User Guide (V3.2)/Administrator manual/Host management/Change the service port of a host.md).

