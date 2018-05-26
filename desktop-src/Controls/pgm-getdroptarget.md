---
title: PGM\_GETDROPTARGET message
description: Retrieves a pager controls IDropTarget interface pointer. You can send this message explicitly or use the Pager\_GetDropTarget macro.
ms.assetid: 6b548c30-2d32-4372-90e4-346a27dda218
keywords:
- PGM_GETDROPTARGET message Windows Controls
topic_type:
- apiref
api_name:
- PGM_GETDROPTARGET
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

# PGM\_GETDROPTARGET message

Retrieves a pager control's [**IDropTarget**](https://msdn.microsoft.com/library/windows/desktop/ms679679) interface pointer. You can send this message explicitly or use the [**Pager\_GetDropTarget**](/windows/win32/Commctrl/nf-commctrl-pager_getdroptarget?branch=master) macro.

## Parameters

<dl> <dt>

*wParam* 
</dt> <dd>Must be zero.</dd> <dt>

*lParam* 
</dt> <dd>

Pointer to an [**IDropTarget**](https://msdn.microsoft.com/library/windows/desktop/ms679679) pointer that receives the interface pointer. It is the caller's responsibility to call [**Release**](https://msdn.microsoft.com/library/windows/desktop/ms682317) on this pointer when it is no longer needed.

</dd> </dl>

## Return value

The return value for this message is not used.

## Requirements



|                                     |                                                                                       |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows Vista \[desktop apps only\]<br/>                                        |
| Minimum supported server<br/> | Windows Server 2003 \[desktop apps only\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 




