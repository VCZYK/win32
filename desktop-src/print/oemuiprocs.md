﻿---
Description: 'The OEMUIPROCS structure is obsolete.The OEMUIPROCS structure contains the address of the DrvGetDriverSetting and DrvUpdateUISetting functions that are exported by Microsoft printer drivers.'
ms.assetid: '67dfb4bd-c43c-4da3-833d-34050d49dea3'
title: OEMUIPROCS structure
---

# OEMUIPROCS structure

The OEMUIPROCS structure is obsolete.

The OEMUIPROCS structure contains the address of the [**DrvGetDriverSetting**](drvgetdriversetting.md) and [**DrvUpdateUISetting**](drvupdateuisetting.md) functions that are exported by Microsoft printer drivers.

## Syntax


```C++
typedef struct _OEMUIPROCS {
  PFN_DrvGetDriverSetting DrvGetDriverSetting;
  PFN_DrvUpdateUISetting  DrvUpdateUISetting;
} OEMUIPROCS, *POEMUIPROCS;
```



## Members

<dl> <dt>

**DrvGetDriverSetting**
</dt> <dd>

Pointer to the printer driver's **DrvGetDriverSetting** function. (To obtain this function's address in kernel mode, see [**DRVPROCS**](drvprocs.md).)

</dd> <dt>

**DrvUpdateUISetting**
</dt> <dd>

Pointer to the printer driver's **DrvUpdateUISetting** function.

</dd> </dl>

## Remarks

[**DrvGetDriverSetting**](drvgetdriversetting.md) and [**DrvUpdateUISetting**](drvupdateuisetting.md) have been superseded by COM-based interfaces.

The OEMUIPROCS structure's address is contained in an [**OEMUIOBJ**](oemuiobj.md) structure.

## Requirements



|                   |                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Printoem.h (include Printoem.h)</dt> </dl> |



 

 

[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bprint\print%5D:%20OEMUIPROCS%20structure%20%20RELEASE:%20%285/12/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/en-us/default.aspx. "Send comments about this topic to Microsoft")



