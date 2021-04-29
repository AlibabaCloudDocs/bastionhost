# Billing

This topic describes the billing of Bastionhost. Bastionhost supports only the subscription billing method. You can purchase a bastion host that runs the Basic or HA edition to perform intelligent audit and security O&M.

## Billing cycle

The billing cycle starts from the date that you purchase your bastion host and ends on the date that your bastion host expires.

## Billing method

Monthly subscription fee × Subscription duration in month

## Specifications

Bastionhost is priced based on the number of assets that can be managed. The following table describes the specifications that you must specify to purchase a bastion host. We recommend that you purchase a bastion host based on the number of assets that you want to manage. The bastion hosts that have different editions and specifications provide the same features. The following list describes the specifications:

-   Number of assets: the number of server assets that a bastion host can manage.
-   Number of concurrent sessions: the number of O&M sessions that O&M personnel can initiate in a bastion host. O&M sessions refer to SSH- and RDP-based remote connections.

    For example, 20 O&M personnel are employed, and each of them initiates five sessions on average. In this case, 100 concurrent sessions are initiated in total. This example is for reference only. You must calculate the number of concurrent sessions based on actual conditions.

-   HA and Basic editions:
    -   **HA edition**: Bastionhost can run in dual-engine mode. This mode provides enhanced stability and reliability. When Bastionhost runs as normal, the two engines simultaneously work. This improves the O&M efficiency. If a single point of failure \(SPOF\) occurs, Bastionhost automatically switches between the two engines. This ensures business continuity. The HA edition uses higher specifications and provides higher performance. It ensures efficient and stable O&M in scenarios with 1,000 or more assets to manage.
    -   **Basic edition**: Bastionhost can run only in single-engine mode. In this mode, you can perform O&M and audit operations.
-   Public bandwidth: After you specify the number of assets, the public bandwidth of the bastion host is automatically configured. For more information, see the **Product specifications** column in the following table. If the bandwidth cannot meet your requirements, you can specify the **Extra Bandwidth** parameter when you purchase the bastion host. The following list describes this parameter:
    -   **Value range**: 10 Mbit/s to 500 Mbit/s
    -   **Increment**: 10 Mbit/s
    -   **Price**: For more information, see the following table.
-   Duration: You can purchase a bastion host for one of the following periods:
    -   One month, three months, and six months
    -   One year, two years, and three years

|Billable items|Number of assets|Number of concurrent sessions|Product specifications|Price in China \(Hong Kong\), Singapore \(Singapore\), Australia \(Sydney\), Malaysia \(Kuala Lumpur\), Indonesia \(Jakarta\), Japan \(Tokyo\), Germany \(Frankfurt\), UK \(London\), US \(Virginia\), US \(Silicon Valley\), and India \(Mumbai\)|Price in China \(Shanghai\), China \(Shenzhen\), China \(Qingdao\), China \(Beijing\), China \(Hohhot\), and China \(Chengdu\)|Price in UAE \(Dubai\)|
|--------------|----------------|-----------------------------|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|----------------------|
|Basic fee|Basic edition|50|50|-   Bandwidth: 8 Mbit/s
-   Storage: 1 TB

|USD 400 per month|USD 250 per month|USD 750 per month|
|100|100|USD 600 per month|USD 400 per month|USD 1,000 per month|
|200|100|USD 700 per month|USD 550 per month|USD 1,300 per month|
|500|500|-   Bandwidth: 16 Mbit/s
-   Storage: 2 TB

|USD 1,100 per month|USD 800 per month|USD 2,000 per month|
|HA edition|50|50|-   Bandwidth: 8 Mbit/s
-   Storage: 1 TB

|USD 700 per month|USD 400 per month|Not supported|
|100|100|USD 1,000 per month|USD 700 per month|Not supported|
|200|100|USD 1,300 per month|USD 950 per month|Not supported|
|500|500|-   Bandwidth: 16 Mbit/s
-   Storage: 2 TB

|USD 1,900 per month|USD 1,400 per month|Not supported|
|1,000|1,000|USD 3,900 per month|USD 2,500 per month|Not supported|
|2,000|1,000|USD 6,000 per month|USD 4,000 per month|Not supported|
|5,000|2,000|Bandwidth: 32 Mbit/s, storage: 2 TB|USD 8,800 per month|USD 5,800 per month|Not supported|
|Extra bandwidth|Increment: 10 Mbit/s|N/A|N/A|USD 15 per Mbit/s per month|USD 12 per Mbit/s per month|USD 20 per Mbit/s per month|

## Expiration

If you do not renew your bastion host after it expires, the bastion host stops providing services. If you do not renew the bastion host within the retention period of seven days, the bastion host is released. In this case, the configuration data and audit logs of the bastion host are deleted.

## Refunds

Bastionhost does not offer a money-back guarantee.

## References

[Purchase a bastion host](/intl.en-US/Pricing/Create a Bastionhost instance.md)

