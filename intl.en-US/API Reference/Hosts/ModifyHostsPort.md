# ModifyHostsPort

Changes the service port of one or more hosts.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Yundun-bastionhost&api=ModifyHostsPort&type=RPC&version=2019-12-09)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|ModifyHostsPort|The operation that you want to perform.

 Set the value to **ModifyHostsPort**. |
|HostIds|String|Yes|\["1","2","3"\]|The ID of the host for which you want to change the service port. The value is a JSON string. You can add up to 100 host IDs.

 **Note:** You can call the [ListHosts](~~200665~~) operation to query the ID of the host. |
|InstanceId|String|Yes|bastionhost-cn-st220aw\*\*\*\*|The ID of the Bastionhost instance where you want to change the service port of the host.

 **Note:** You can call the [DescribeInstances](~~153281~~) operation to query the ID of the Bastionhost instance. |
|Port|String|Yes|22|The new service port of the host. The port number must be an integer in the range of 22 to 65535. |
|ProtocolName|String|Yes|SSH|The new protocol that is used to connect to the host. Valid values:

 -   **SSH**
-   **RDP** |
|RegionId|String|No|cn-hangzhou|The region ID of the Bastionhost instance where you want to change the service port of the host.

 **Note:** For more information about the mapping between region IDs and region names, see [Regions and zones](~~40654~~). |

All Alibaba Cloud API operations must include common request parameters. For more information about common request parameters, see [Common parameters](~~148139~~).

For more information about sample requests, see the "Examples" section of this topic.

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|EC9BF0F4-8983-491A-BC8C-1B4DD94976DE|The ID of the request. |
|Results|Array of Item| |The call result of the operation. |
|Code|String|OK|The return code that indicates whether the call was successful. Valid values:

 -   **OK**: The call was successful.
-   **UNEXPECTED**: An unknown error has occurred.
-   **INVALID\_ARGUMENT**: A request parameter is invalid.
-   **OBJECT\_NOT\_FOUND**: The specified host is invalid.
-   **OBJECT\_AlREADY\_EXISTS**: The specified new port already exists on the host. |
|HostId|String|1|The ID of the host. |
|Message|String|N/A|This parameter is obsolete. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=ModifyHostsPort
&HostIds=["1","2","3"]
&InstanceId=bastionhost-cn-st220aw****
&Port=22
&ProtocolName=SSH
&<Common request parameters>
```

Sample success responses

`XML` format

```
<ModifyHostsPortResponse>
      <RequestId>EC9BF0F4-8983-491A-BC8C-1B4DD94976DE</RequestId>
      <Results>
            <Message></Message>
            <HostId>1</HostId>
            <Code>OK</Code>
      </Results>
</ModifyHostsPortResponse>
```

`JSON` format

```
{
	"RequestId": "EC9BF0F4-8983-491A-BC8C-1B4DD94976DE",
	"Results": [{
		"Message": "",
		"HostId": "1",
		"Code": "OK"
	}]
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Yundun-bastionhost).

