---
Description: Represents the settings for a network adapter within the guest operating system, which will be applied at the time of a failover.
ms.assetid: d7f2d471-7328-4181-b94e-b9127814706e
title: Msvm\_FailoverNetworkAdapterSettingData class
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# Msvm\_FailoverNetworkAdapterSettingData class

Represents the settings for a network adapter within the guest operating system, which will be applied at the time of a failover.

The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.

## Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FailoverNetworkAdapterSettingData : CIM_SettingData
{
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
  uint16  ProtocolIFType;
  boolean DHCPEnabled;
  string  IPAddresses[];
  string  Subnets[];
  string  DefaultGateways[];
  string  DNSServers[];
};
```

## Members

The **Msvm\_FailoverNetworkAdapterSettingData** class has these types of members:

-   [Properties](#properties)

### Properties

The **Msvm\_FailoverNetworkAdapterSettingData** class has these properties.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> </dl>

A short description of the object. This property is inherited from [**CIM\_ManagedElement**](https://msdn.microsoft.com/library/mt432218), and it is always set to **Null**.

</dd> <dt>

**DefaultGateways**
</dt> <dd> <dl> <dt>

Data type: **string** array
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**ArrayType**](https://msdn.microsoft.com/library/aa393650) ("Indexed")
</dt> </dl>

An array of strings that specify the default IP gateways configured on the network adapter within the guest operating system. The maximum number of default IP gateways that may be configured on a single network adapter is five.

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> </dl>

A description of the object. This property is inherited from [**CIM\_ManagedElement**](https://msdn.microsoft.com/library/mt432218), and it is always set to **Null**.

</dd> <dt>

**DHCPEnabled**
</dt> <dd> <dl> <dt>

Data type: **boolean**
</dt> <dt>

Access type: Read-only
</dt> </dl>

Specifies whether DHCP is enabled on the IPv4 interface of the network adapter within the guest operating system.

</dd> <dt>

**DNSServers**
</dt> <dd> <dl> <dt>

Data type: **string** array
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**ArrayType**](https://msdn.microsoft.com/library/aa393650) ("Indexed")
</dt> </dl>

An array of strings that specify the DNS servers configured on the network adapter within the guest operating system.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> </dl>

A display name for the object. This property is inherited from [**CIM\_ManagedElement**](https://msdn.microsoft.com/library/mt432218), and it is always set to **Null**.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: **Key**
</dt> </dl>

Uniquely identifies an instance of this class. This property is inherited from [**CIM\_SettingData**](https://msdn.microsoft.com/library/cc136911), and it is always set to **Null**.

</dd> <dt>

**IPAddresses**
</dt> <dd> <dl> <dt>

Data type: **string** array
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**ArrayType**](https://msdn.microsoft.com/library/aa393650) ("Indexed")
</dt> </dl>

An array of strings that specify the IP addresses configured on the network adapter within the guest operating system.

</dd> <dt>

**ProtocolIFType**
</dt> <dd> <dl> <dt>

Data type: **uint16**
</dt> <dt>

Access type: Read-only
</dt> </dl>

Identifies the Internet protocols that the settings specified by this instance apply to. This must be one of the following values.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)


</dt> <dd></dd> <dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>**IPv4** (4096)


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>**IPv6** (4097)


</dt> <dd></dd> <dt>

<span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>

<span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>**IPv4/v6** (4098)


</dt> <dd>

IPv4/IPv6

</dd> </dl>

</dd> <dt>

**Subnets**
</dt> <dd> <dl> <dt>

Data type: **string** array
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**ArrayType**](https://msdn.microsoft.com/library/aa393650) ("Indexed")
</dt> </dl>

An array of strings that specify the subnets configured on the network adapter within the guest operating system. Each element in this array applies to the corresponding element in the **IPAddresses** array.

</dd> </dl>

## Requirements



|                                     |                                                                                                         |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows 8 \[desktop apps only\]<br/>                                                              |
| Minimum supported server<br/> | Windows Server 2012 \[desktop apps only\]<br/>                                                    |
| Namespace<br/>                | Root\\Virtualization\\V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

 



