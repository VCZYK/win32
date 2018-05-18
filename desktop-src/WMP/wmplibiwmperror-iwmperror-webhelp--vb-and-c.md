---
title: IWMPError webHelp method
description: The webHelp method launches the Windows Media Player Web Help page to display further information about the first error in the error queue (index zero).
ms.assetid: '30fc765a-04b2-44e5-99d8-0b4720ccbb25'
keywords: ["webHelp method Windows Media Player", "webHelp method Windows Media Player , IWMPError interface", "IWMPError interface Windows Media Player , webHelp method"]
topic_type:
- apiref
api_name:
- IWMPError.webHelp
api_location:
- Interop.WMPLib.dll
api_type:
- COM
---

# IWMPError::webHelp method

The **webHelp** method launches the Windows Media Player Web Help page to display further information about the first error in the error queue (index zero).

## Syntax


```CSharp
public void webHelp();
```

<span codelanguage="VisualBasic"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Public Sub webHelp()
Implements IWMPError.webHelp</code></pre></td>
</tr>
</tbody>
</table>



## Parameters

This method has no parameters.

## Return value

This method does not return a value.

## Remarks

The Web Help pages always contain the latest and most detailed information about Windows Media Player errors. This method automatically transfers the other information needed by Web Help, such as the operating system version being used.

To access the Web Help pages directly, use the following error code and support center links:

-   [Windows Media Player Error Code Information](http://support.microsoft.com/kb/886273)
-   [Windows Media Player Solution Center](http://go.microsoft.com/fwlink/p/?linkid=10187)

## Examples

The following example creates a button that launches the Microsoft Windows Media Player Web Help page in the browser. The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.


```CSharp
private void webHelpButton_Click(object sender, System.EventArgs e)
{
    // Launch the Microsoft Windows Media Player Web Help page in the browser.
    player.Error.webHelp();
}
```

<span codelanguage="VisualBasic"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Public Sub webHelpButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles webHelpButton.Click

    &#39; Launch the Microsoft Windows Media Player Web Help page in the browser.
    player.Error.webHelp()

End Sub</code></pre></td>
</tr>
</tbody>
</table>



## Requirements



|                      |                                                                                                                        |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9 Series or later<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## See also

<dl> <dt>

[**IWMPError Interface (VB and C#)**](iwmperror--vb-and-c.md)
</dt> </dl>

�

�




