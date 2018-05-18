﻿---
Description: 'Adds data to a specified hash object.'
ms.assetid: '8E32BBC4-C2DD-4174-9FF1-9001E4A7D87B'
title: 'A\_SHAUpdate function'
---

# A\_SHAUpdate function

Adds data to a specified hash object.

## Syntax


```C++
void RSA32API A_SHAUpdate(
  _Inout_ A_SHA_CTX     *Context,
  _Out_   UNSIGNED CHAR *Buffer,
          UNSIGNED INT  BufferSize
);
```



## Parameters

<dl> <dt>

*Context* \[in, out\]
</dt> <dd>

The SHA context.

</dd> <dt>

*Buffer* \[out\]
</dt> <dd>

The hash table.

</dd> <dt>

*BufferSize* 
</dt> <dd>

The size of the buffer.

</dd> </dl>

## Return value

This function does not return a value.

## Remarks

This function can be called multiple times to compute the hash on long data streams or discontinuous data streams. The [**A\_SHAFinal**](a-shafinal.md) function must be called before retrieving the hash value.

This function is very similar to SHAUpdate, but is called directly from the library, rather than being routed through the cryptography infrastructure. For more information, see [Windows NTCryptographic Providers](https://msdn.microsoft.com/en-us/library/cc723484.aspx).

## Requirements



|                    |                                                                                      |
|--------------------|--------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Sha.h</dt> </dl>     |
| Library<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |
| DLL<br/>     | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 



