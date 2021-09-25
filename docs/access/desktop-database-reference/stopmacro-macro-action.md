---
title: StopMacro-Makroaktion
TOCTitle: StopMacro macro action
ms:assetid: 6bbf9026-4536-43f2-aa43-3f2ecea01005
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195473(v=office.15)
ms:contentKeyID: 48545455
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 143a1be5e4a21dd8fadf17bf9f50b82f84bfc9db
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601779"
---
# <a name="stopmacro-macro-action"></a>StopMacro-Makroaktion

**Gilt für**: Access 2013, Office 2013

Sie können die **StopMacro-Aktion** verwenden, um das aktuell ausgeführte Makro zu beenden.

## <a name="setting"></a>Einstellung

Die **StopMacro-Aktion** hat keine Argumente.

## <a name="remarks"></a>HinwBemerkungeneise

In der Regel verwenden Sie diese Aktion, wenn eine Bedingung das Beenden des Makros erforderlich macht. Sie können einen bedingten Ausdruck in der Aktionszeile des Makros verwenden, die diese Aktion enthält. Wenn der Ausdruck auf **"True"** (–1) ausgewertet wird, beendet Microsoft Access das Makro.

Sie können z. B. ein Makro erstellen, das ein Formular mit den Täglichen Auftragssummen für das in ein benutzerdefinierte Dialogfeld eingegebene Datum öffnet. Sie können einen bedingten Ausdruck verwenden, um sicherzustellen, dass das Steuerelement **Bestelldatum** im Dialogfeld ein gültiges Datum enthält. Andernfalls kann die **MessageBox-Aktion** eine Fehlermeldung anzeigen, und die **StopMacro-Aktion** kann das Makro beenden.

Wenn das Makro die **Echo-** oder **Warnmeldungsaktionen** verwendet hat, um Echo oder die Anzeige von Systemmeldungen zu deaktivieren, werden diese durch die **StopMacro-Aktion** automatisch wieder aktiviert.

Diese Aktion ist in einem VBA-Modul (Visual Basic für Applikationen) nicht verfügbar.

## <a name="example"></a>Beispiel

The following macro demonstrates the use of the **OnError** action. In this example, the **OnError** action specifies that Access run a custom error handling macro named ErrorHandler when an error occurs. Wenn ein Fehler auftritt, wird das CatchErrors-Untermakro aufgerufen. Wenn die Fehlernummer 2102 ist, wird eine bestimmte Meldung angezeigt, und die Makroausführung wird angehalten. Andernfalls wird eine Meldung angezeigt, die den Fehler beschreibt, und das Makro wird angehalten, sodass Sie zusätzliche Problembehandlungen ausführen können. The ErrorHandler macro displays a message box that refers to the **MacroError** object to display information about the error.

**Der Beispielcode stammt von:**[Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    /* MACRO: mcrThrowErrors                                  */
    /* PURPOSE: Error handling using macros in Access 2010    */
    
    OnError
        Go to Macro Name
        Macro Name CatchErrors
    
    OpenForm 
        Form Name frmSamples
        View Form
        Filter Name
        Where Condition
        Data Mode
        Window Mode Normal
    
    MessageBox 
        Message This message appears after the OpenForm action
        Beep Yes
        Type None
        Title
    
    
    /* SUBMACRO: CatchErrors                                   */
    
    SubMacro: CatchErrors
        If [MacroError].[Number]=2101 Then
            MessageBox
                Message Cannot find the specified form!
                Beep Yes
                Type Critical
                Title
            StopMacro
    
        Else
            MessageBox
                Message =[MacroErro].[Description]
                Beep Yes
                Type None
                Title Unhandled Error
    
            SingleStep
        End If
    
    End SubMacro
```
