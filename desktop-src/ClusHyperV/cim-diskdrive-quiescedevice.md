---
title: QuiesceDevice method of the CIM\_DiskDrive class
description: Deprecated description Temporarily suspends or resumes activity on the numeric sensor.This method is deprecated. Instead we recommend that you use the RequestStateChange method.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\markl
ms.assetid: '6b718c24-c0db-43a2-9fe3-fd2d24a61a02'
ms.prod: 'windows-server-dev'
ms.technology:
- 'failover-cluster-hyperv'
- 'windows-management-instrumentation'
ms.tgt_platform: multiple
keywords: ["QuiesceDevice method", "QuiesceDevice method, CIM_DiskDrive class", "CIM_DiskDrive class, QuiesceDevice method"]
topic_type:
- apiref
api_name:
- CIM_DiskDrive.QuiesceDevice
api_location:
- VMMS.exe
api_type:
- COM
---

# QuiesceDevice method of the CIM\_DiskDrive class

**Deprecated description:** Temporarily suspends or resumes activity on the numeric sensor.

This method is deprecated. Instead we recommend that you use the [**RequestStateChange**](https://msdn.microsoft.com/library/dn792198) method.

## Syntax


```mof
uint32 QuiesceDevice(
  [in]�boolean Quiesce
);
```



## Parameters

<dl> <dt>

*Quiesce* \[in\]
</dt> <dd>

**true** if the numeric sensor is to temporarily suspend activity or resume activity; **false** to resume activity.

</dd> </dl>

## Return value

The possible return values are:

<dl> <dt>


</dt> <dd>

0

The operation completed successfully.

</dd> <dt>


</dt> <dd>

1

The operation was not completed because it is not supported.

</dd> <dt>


</dt> <dd>

2

The operation is not supported when the device is in the current state.

</dd> <dt>


</dt> <dd>

3�...

The operation was not completed because an error occurred.

</dd> </dl>

## Requirements



|                                     |                                                                                                        |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | None supported<br/>                                                                              |
| Minimum supported server<br/> | Windows Server�2016<br/>                                                                         |
| Namespace<br/>                | Root\\HyperVCluster\\v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsHyperVCluster.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>VMMS.exe</dt> </dl>                    |



## See also

<dl> <dt>

[**CIM\_DiskDrive**](cim-diskdrive.md)
</dt> </dl>

�

�




