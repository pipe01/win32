---
title: TVM\_SETINDENT message
description: Sets the width of indentation for a tree-view control and redraws the control to reflect the new width. You can send this message explicitly or by using the TreeView\_SetIndent macro.
ms.assetid: 377da8fe-c8e6-479b-a283-f1811cbc3e58
keywords:
- TVM_SETINDENT message Windows Controls
topic_type:
- apiref
api_name:
- TVM_SETINDENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# TVM\_SETINDENT message

Sets the width of indentation for a tree-view control and redraws the control to reflect the new width. You can send this message explicitly or by using the [**TreeView\_SetIndent**](/windows/win32/Commctrl/nf-commctrl-treeview_setindent?branch=master) macro.

## Parameters

<dl> <dt>

*wParam* 
</dt> <dd>

Width, in pixels, of the indentation. If this parameter is less than the system-defined minimum width, the new width is set to the system-defined minimum.

</dd> <dt>

*lParam* 
</dt> <dd>Must be zero.</dd> </dl>

## Return value

No return value.

## Remarks

The system-defined minimum indent value is typically five pixels, but it is not fixed. To retrieve the exact value of the minimum indent on a particular system, send a **TVM\_SETINDENT** message with *wParam* set to zero. Then send a [**TVM\_GETINDENT**](tvm-getindent.md) message to retrieve the minimum indent value.

## Requirements



|                                     |                                                                                       |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows Vista \[desktop apps only\]<br/>                                        |
| Minimum supported server<br/> | Windows Server 2003 \[desktop apps only\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## See also

<dl> <dt>

[**TreeView\_SetIndent**](/windows/win32/Commctrl/nf-commctrl-treeview_setindent?branch=master)
</dt> </dl>

 

 




