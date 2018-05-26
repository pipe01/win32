---
title: Dialog Boxes
description: This section discusses dialog boxes. A dialog box is a temporary window an application creates to retrieve user input.
ms.assetid: 51960c28-a178-4ad3-b45e-426fec42a945
keywords:
- user interface,dialog boxes
- dialog boxes,about
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# Dialog Boxes

A dialog box is a temporary window an application creates to retrieve user input. An application typically uses dialog boxes to prompt the user for additional information for menu items. A dialog box usually contains one or more controls (child windows) with which the user enters text, chooses options, or directs the action.

Windows also provides predefined dialog boxes that support common menu items such as **Open** and **Print**. Applications that use these menu items should use the common dialog boxes to prompt for this user input, regardless of the type of application.

### In This Section



| Name                                                                           | Description                                                                                     |
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [About Dialog Boxes](about-dialog-boxes.md)                                   | Discusses using dialog boxes in the user interface for your applications.<br/>            |
| [Dialog Box Programming Considerations](dlgbox-programming-considerations.md) | This overview discusses some programming considerations concerning dialog boxes.<br/>     |
| [Using Dialog Boxes](using-dialog-boxes.md)                                   | You use dialog boxes to display information and prompt for input from the user.<br/>      |
| [Dialog Box Reference](dialog-box-reference.md)                               | The API Reference<br/>                                                                    |
| [Common Dialog Box Library](common-dialog-box-library.md)                     | Discusses using the common dialog boxes in the user interface for your applications.<br/> |



 

### Dialog Box Functions



| Name                                                           | Description                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateDialog**](/windows/win32/Winuser/nf-winuser-createdialoga?branch=master)                           | Creates a modeless dialog box from a dialog box template resource.<br/>                                                                                                                                                                                                                                                                                                                                                                   |
| [**CreateDialogIndirect**](/windows/win32/Winuser/nf-winuser-createdialogindirecta?branch=master)           | Creates a modeless dialog box from a dialog box template in memory.<br/>                                                                                                                                                                                                                                                                                                                                                                  |
| [**CreateDialogIndirectParam**](/windows/win32/Winuser/nf-winuser-createdialogindirectparama?branch=master) | Creates a modeless dialog box from a dialog box template in memory. Before displaying the dialog box, the function passes an application-defined value to the dialog box procedure as the *lParam* parameter of the [**WM\_INITDIALOG**](wm-initdialog.md) message. An application can use this value to initialize dialog box controls. <br/>                                                                                           |
| [**CreateDialogParam**](/windows/win32/Winuser/nf-winuser-createdialogparama?branch=master)                 | Creates a modeless dialog box from a dialog box template resource. Before displaying the dialog box, the function passes an application-defined value to the dialog box procedure as the *lParam* parameter of the [**WM\_INITDIALOG**](wm-initdialog.md) message. An application can use this value to initialize dialog box controls. <br/>                                                                                            |
| [**DefDlgProc**](/windows/win32/Winuser/nf-winuser-defdlgprocw?branch=master)                               | Calls the default dialog box window procedure to provide default processing for any window messages that a dialog box with a private window class does not process. <br/>                                                                                                                                                                                                                                                                 |
| [**DialogBox**](/windows/win32/Winuser/nf-winuser-dialogboxa?branch=master)                                 | Creates a modal dialog box from a dialog box template resource. [**DialogBox**](/windows/win32/Winuser/nf-winuser-dialogboxa?branch=master) does not return control until the specified callback function terminates the modal dialog box by calling the [**EndDialog**](/windows/win32/Winuser/nf-winuser-enddialog?branch=master) function.<br/>                                                                                                                                                                                 |
| [**DialogBoxIndirect**](/windows/win32/Winuser/nf-winuser-dialogboxindirecta?branch=master)                 | Creates a modal dialog box from a dialog box template in memory. [**DialogBoxIndirect**](/windows/win32/Winuser/nf-winuser-dialogboxindirecta?branch=master) does not return control until the specified callback function terminates the modal dialog box by calling the [**EndDialog**](/windows/win32/Winuser/nf-winuser-enddialog?branch=master) function.<br/>                                                                                                                                                                |
| [**DialogBoxIndirectParam**](/windows/win32/Winuser/nf-winuser-dialogboxindirectparama?branch=master)       | Creates a modal dialog box from a dialog box template in memory. Before displaying the dialog box, the function passes an application-defined value to the dialog box procedure as the *lParam* parameter of the [**WM\_INITDIALOG**](wm-initdialog.md) message. An application can use this value to initialize dialog box controls. <br/>                                                                                              |
| [**DialogBoxParam**](/windows/win32/Winuser/nf-winuser-dialogboxparama?branch=master)                       | Creates a modal dialog box from a dialog box template resource. Before displaying the dialog box, the function passes an application-defined value to the dialog box procedure as the *lParam* parameter of the [**WM\_INITDIALOG**](wm-initdialog.md) message. An application can use this value to initialize dialog box controls. <br/>                                                                                               |
| [*DialogProc*](/windows/win32/Winuser/nf-winuser-defdlgproca?branch=master)                                 | An application-defined callback function used with the [**CreateDialog**](/windows/win32/Winuser/nf-winuser-createdialoga?branch=master) and [**DialogBox**](/windows/win32/Winuser/nf-winuser-dialogboxa?branch=master) families of functions. It processes messages sent to a modal or modeless dialog box. The **DLGPROC** type defines a pointer to this callback function. [*DialogProc*](/windows/win32/Winuser/nf-winuser-defdlgproca?branch=master) is a placeholder for the application-defined function name. <br/>                                                    |
| [**EndDialog**](/windows/win32/Winuser/nf-winuser-enddialog?branch=master)                                 | Destroys a modal dialog box, causing the system to end any processing for the dialog box.<br/>                                                                                                                                                                                                                                                                                                                                            |
| [**GetDialogBaseUnits**](/windows/win32/Winuser/nf-winuser-getdialogbaseunits?branch=master)               | Retrieves the system's dialog base units, which are the average width and height of characters in the system font. For dialog boxes that use the system font, you can use these values to convert between dialog template units, as specified in dialog box templates, and pixels. For dialog boxes that do not use the system font, the conversion from dialog template units to pixels depends on the font used by the dialog box.<br/> |
| [**GetDlgCtrlID**](/windows/win32/Winuser/nf-winuser-getdlgctrlid?branch=master)                           | Retrieves the identifier of the specified control. <br/>                                                                                                                                                                                                                                                                                                                                                                                  |
| [**GetDlgItem**](/windows/win32/Winuser/nf-winuser-getdlgitem?branch=master)                               | Retrieves a handle to a control in the specified dialog box. <br/>                                                                                                                                                                                                                                                                                                                                                                        |
| [**GetDlgItemInt**](/windows/win32/Winuser/nf-winuser-getdlgitemint?branch=master)                         | Translates the text of a specified control in a dialog box into an integer value. <br/>                                                                                                                                                                                                                                                                                                                                                   |
| [**GetDlgItemText**](/windows/win32/Winuser/nf-winuser-getdlgitemtexta?branch=master)                       | Retrieves the title or text associated with a control in a dialog box. <br/>                                                                                                                                                                                                                                                                                                                                                              |
| [**GetNextDlgGroupItem**](/windows/win32/Winuser/nf-winuser-getnextdlggroupitem?branch=master)             | Retrieves a handle to the first control in a group of controls that precedes (or follows) the specified control in a dialog box. <br/>                                                                                                                                                                                                                                                                                                    |
| [**GetNextDlgTabItem**](/windows/win32/Winuser/nf-winuser-getnextdlgtabitem?branch=master)                 | Retrieves a handle to the first control that has the **WS\_TABSTOP** style that precedes (or follows) the specified control. <br/>                                                                                                                                                                                                                                                                                                        |
| [**IsDialogMessage**](/windows/win32/Winuser/nf-winuser-isdialogmessagea?branch=master)                     | Determines whether a message is intended for the specified dialog box and, if it is, processes the message. <br/>                                                                                                                                                                                                                                                                                                                         |
| [**MapDialogRect**](/windows/win32/Winuser/nf-winuser-mapdialogrect?branch=master)                         | Converts the specified dialog box units to screen units (pixels). The function replaces the coordinates in the specified [**RECT**](https://msdn.microsoft.com/library/windows/desktop/dd162897) structure with the converted coordinates, which allows the structure to be used to create a dialog box or position a control within a dialog box. <br/>                                                                                                                                     |
| [**MessageBox**](/windows/win32/Winuser/nf-winuser-messagebox?branch=master)                               | Displays a modal dialog box that contains a system icon, a set of buttons, and a brief application-specific message, such as status or error information. The message box returns an integer value that indicates which button the user clicked.<br/>                                                                                                                                                                                     |
| [**MessageBoxEx**](/windows/win32/Winuser/nf-winuser-messageboxexa?branch=master)                           | Creates, displays, and operates a message box. The message box contains an application-defined message and title, plus any combination of predefined icons and push buttons. The buttons are in the language of the system user interface. <br/>                                                                                                                                                                                          |
| [**MessageBoxIndirect**](/windows/win32/Winuser/nf-winuser-messageboxindirecta?branch=master)               | Creates, displays, and operates a message box. The message box contains application-defined message text and title, any icon, and any combination of predefined push buttons.<br/>                                                                                                                                                                                                                                                        |
| [**SendDlgItemMessage**](/windows/win32/Winuser/nf-winuser-senddlgitemmessagea?branch=master)               | Sends a message to the specified control in a dialog box.<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| [**SetDlgItemInt**](/windows/win32/Winuser/nf-winuser-setdlgitemint?branch=master)                         | Sets the text of a control in a dialog box to the string representation of a specified integer value. <br/>                                                                                                                                                                                                                                                                                                                               |
| [**SetDlgItemText**](/windows/win32/Winuser/nf-winuser-setdlgitemtexta?branch=master)                       | Sets the title or text of a control in a dialog box. <br/>                                                                                                                                                                                                                                                                                                                                                                                |



 

### Dialog Box Messages



| Name                                    | Description                                                                                                                                                                                                         |
|-----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DM\_GETDEFID**](dm-getdefid.md)     | Retrieves the identifier of the default push button control for a dialog box. <br/>                                                                                                                           |
| [**DM\_REPOSITION**](dm-reposition.md) | Repositions a top-level dialog box so that it fits within the desktop area. An application can send this message to a dialog box after resizing it to ensure that the entire dialog box remains visible.<br/> |
| [**DM\_SETDEFID**](dm-setdefid.md)     | Changes the identifier of the default push button for a dialog box. <br/>                                                                                                                                     |



 

### Dialog Box Notifications



| Name                                      | Description                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM\_CTLCOLORDLG**](wm-ctlcolordlg.md) | Sent to a dialog box before the system draws the dialog box. By responding to this message, the dialog box can set its text and background colors using the specified display device context handle. <br/>                                                                                                                                                                                       |
| [**WM\_ENTERIDLE**](wm-enteridle.md)     | Sent to the owner window of a modal dialog box or menu that is entering an idle state. A modal dialog box or menu enters an idle state when no messages are waiting in its queue after it has processed one or more previous messages. <br/>                                                                                                                                                     |
| [**WM\_GETDLGCODE**](wm-getdlgcode.md)   | Sent to the window procedure associated with a control. By default, the system handles all keyboard input to the control; the system interprets certain types of keyboard input as dialog box navigation keys. To override this default behavior, the control can respond to the [**WM\_GETDLGCODE**](wm-getdlgcode.md) message to indicate the types of input it wants to process itself.<br/> |
| [**WM\_INITDIALOG**](wm-initdialog.md)   | Sent to the dialog box procedure immediately before a dialog box is displayed. Dialog box procedures typically use this message to initialize controls and carry out any other initialization tasks that affect the appearance of the dialog box. <br/>                                                                                                                                          |
| [**WM\_NEXTDLGCTL**](wm-nextdlgctl.md)   | Sent to a dialog box procedure to set the keyboard focus to a different control in the dialog box. <br/>                                                                                                                                                                                                                                                                                         |



 

### Dialog Box Structures



| Name                                           | Description                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DLGITEMTEMPLATE**](/windows/win32/Winuser/ns-winuser-dlgitemtemplate?branch=master)     | Defines the dimensions and style of a control in a dialog box. One or more of these structures are combined with a [**DLGTEMPLATE**](/windows/win32/Winuser/ns-winuser-dlgtemplate?branch=master) structure to form a standard template for a dialog box. <br/>                                                                                                                                   |
| [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) | Describes an extended dialog box. For a description of the format of an extended dialog box template, see [**DLGTEMPLATEEX**](dlgtemplateex.md).<br/>                                                                                                                                                                                                |
| [**DLGTEMPLATE**](/windows/win32/Winuser/ns-winuser-dlgtemplate?branch=master)             | Defines the dimensions and style of a dialog box. This structure, always the first in a standard template for a dialog box, also specifies the number of controls in the dialog box and therefore specifies the number of subsequent [**DLGITEMTEMPLATE**](/windows/win32/Winuser/ns-winuser-dlgitemtemplate?branch=master) structures in the template. <br/>                                     |
| [**DLGTEMPLATEEX**](dlgtemplateex.md)         | An extended dialog box template begins with a **DLGTEMPLATEEX** header that describes the dialog box and specifies the number of controls in the dialog box. For each control in a dialog box, an extended dialog box template has a block of data that uses the [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) format to describe the control. <br/> |
| [**MSGBOXPARAMS**](/windows/win32/Winuser/ns-winuser-tagmsgboxparamsa?branch=master)           | Contains information used to display a message box. The [**MessageBoxIndirect**](/windows/win32/Winuser/nf-winuser-messageboxindirecta?branch=master) function uses this structure.<br/>                                                                                                                                                                                                           |



 

 

 




