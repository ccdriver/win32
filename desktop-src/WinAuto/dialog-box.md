---
title: Dialog Box (MSAA UI Element Reference)
description: A dialog box is a temporary window that an application creates to retrieve user input.
ms.assetid: 7d132c2c-eab1-4132-b2b6-fa1f8b142f58
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# Dialog Box (MSAA UI Element Reference)

> [!Note]  
> This topic describes **Dialog Box** objects for purposes of MSAA UI Element Reference. How to create **Dialog Box** objects in various UI frameworks is not described here. See the API reference documentation for the UI framework you're using.

 

A dialog box is a temporary window that an application creates to retrieve user input. An application uses dialog boxes to prompt the user for additional information about commands that the user has chosen from a menu. A dialog box contains one or more controls (child windows) with which the user enters text, chooses options, or directs the action of the command.

The window class name for dialog boxes is "\#32770".

## IAccessible Methods

A dialog box supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:



| Method                                                                    | Comments                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | If the dialog box contains a default push button, the [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) method calls [**PostMessage**](https://msdn.microsoft.com/library/windows/desktop/ms644944) with the [**BM\_CLICK**](https://msdn.microsoft.com/library/windows/desktop/bb775985) button message to click the default push button. |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                                                                                                                                                                                                        |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                                                                                                                                                                                                        |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                                                                                                                                                                                                        |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                                                                                                                                                                                                        |



 

## IAccessible Properties

A dialog box supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:



| Property                                                                                 | Comments                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get\_accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)                 | The **ChildCount** property is equal to the number of child window controls on the dialog box.                                                                                                                                                                                                                                                                                                                                                                           |
| [**get\_accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)           | If the dialog box contains a default push button, the **DefaultAction** property is "Press".                                                                                                                                                                                                                                                                                                                                                                             |
| [**get\_accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**get\_accKeyboardShortcut**](https://msdn.microsoft.com/library/windows/desktop/dd318482) | Typically, dialog boxes do not have keyboard shortcuts. If the window text for the dialog box contains an ampersand (&) character, Microsoft Active Accessibility returns a non-Null string as the **KeyboardShortcut** property.                                                                                                                                                                                                                                        |
| [**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                             | The **Name** property is the window text, or caption, that is displayed in the title bar of the dialog box.                                                                                                                                                                                                                                                                                                                                                              |
| [**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                         | The **Parent** property is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md#role-system-window) ) that surrounds the dialog box and has the same **Name** property and window class name as the dialog box.                                                                                                                                                                                                                                                        |
| [**get\_accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                             | The **Role** property is [**ROLE\_SYSTEM\_DIALOG**](object-roles.md#role-system-dialog) or [**ROLE\_SYSTEM\_PROPERTYPAGE**](object-roles.md#role-system-propertypage).                                                                                                                                                                                                                                                                                                 |
| [**get\_accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                           | The **State** property is a combination of one or more of the following [values](object-state-constants.md):[**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md#state-system-invisible) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md#state-system-unavailable) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md#state-system-focused) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md#state-system-focusable)<br/> |



 

## Remarks

The dialog object does not support the [**get\_accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) method. To obtain an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer to a control on a dialog box, clients must obtain the window handle of the control and then call [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).

## Related topics

<dl> <dt>

[IAccessible Interface](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




