---
Description: 'The DecideAllocator method negotiates an allocator with the output pin.'
ms.assetid: '5c04f440-b177-4caa-989f-3aa783c4b348'
title: 'CPullPin.DecideAllocator method'
---

# CPullPin.DecideAllocator method

The `DecideAllocator` method negotiates an allocator with the output pin.

## Syntax


```C++
virtual HRESULT DecideAllocator(
  �IMemAllocator �������*pAlloc,
  �ALLOCATOR_PROPERTIES *pProps
);
```



## Parameters

<dl> <dt>

*pAlloc* 
</dt> <dd>

Pointer to the [**IMemAllocator**](imemallocator.md) interface of the input pin's preferred allocator, or **NULL**.

</dd> <dt>

*pProps* 
</dt> <dd>

Pointer to an optional [**ALLOCATOR\_PROPERTIES**](allocator-properties.md) structure that contains the input pin's buffer requirements.

</dd> </dl>

## Return value

Returns S\_OK if successful, or an error code otherwise.

## Remarks

This method calls the [**IAsyncReader::RequestAllocator**](iasyncreader-requestallocator.md) method to negotiate an allocator. It passes the *pAlloc* parameter directly to the **RequestAllocator** method. It passes the *pProps* parameter to **RequestAllocator** if *pProps* is non-**NULL**; otherwise, it creates an **ALLOCATOR\_PROPERTIES** structure with a default request of three 64K buffers.

## Requirements



|                    |                                                                                                                                                                                            |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Library<br/> | <dl> <dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt> </dl> |



## See also

<dl> <dt>

[**CPullPin Class**](cpullpin.md)
</dt> <dt>

[**CPullPin::Connect**](cpullpin-connect.md)
</dt> </dl>

�

�



