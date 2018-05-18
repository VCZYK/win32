---
title: MOM\_OPEN message
description: The MOM\_OPEN message is sent to a MIDI output callback function when a MIDI output device is opened.
ms.assetid: '1374a07c-02fa-4b43-82df-cbd96302aec5'
keywords: ["MOM_OPEN message Windows Multimedia"]
topic_type:
- apiref
api_name:
- MOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
---

# MOM\_OPEN message

The **MOM\_OPEN** message is sent to a MIDI output callback function when a MIDI output device is opened.


```C++
MOM_OPEN 
dwParam1 = reserved 
dwParam2 = reserved 
```



## Parameters

<dl> <dt>

<span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*
</dt> <dd>

Reserved; do not use.

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*
</dt> <dd>

Reserved; do not use.

</dd> </dl>

## Return Value

This message does not return a value.

## Requirements



|                                     |                                                                                                           |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows�2000 Professional \[desktop apps only\]<br/>                                                |
| Minimum supported server<br/> | Windows�2000 Server \[desktop apps only\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Mmsystem.h (include Windows.h)</dt> </dl> |



## See also

<dl> <dt>

[MIDI Messages](midi-messages.md)
</dt> </dl>

�

�




