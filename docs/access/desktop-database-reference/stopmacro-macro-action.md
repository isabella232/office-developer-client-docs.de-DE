---
title: StopMacro-Makroaktion
TOCTitle: StopMacro macro action
ms:assetid: 6bbf9026-4536-43f2-aa43-3f2ecea01005
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195473(v=office.15)
ms:contentKeyID: 48545455
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fe319e0f7a811d3bcd3b2fc18c4a3d951187fbe8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308498"
---
# <a name="stopmacro-macro-action"></a>StopMacro-Makroaktion

**Gilt für**: Access 2013, Office 2013

Sie können die **stopmakro** -Aktion verwenden, um das derzeit ausgeführte Makro zu beenden.

## <a name="setting"></a>Einstellung

Die **stopmakro** -Aktion hat keine Argumente.

## <a name="remarks"></a>Bemerkungen

Diese Aktion wird in der Regel verwendet, wenn eine Bedingung das Beenden des Makros erforderlich macht. Sie können einen bedingten Ausdruck in der Aktionszeile des Makros verwenden, die diese Aktion enthält. Wenn der Ausdruck **true** ergibt (– 1), beendet Microsoft Access das Makro.

Sie können beispielsweise ein Makro erstellen, das ein Formular öffnet, in dem die Gesamtsummen für das in einem benutzerdefinierten Dialogfeld eingegebene Datum angezeigt werden. Sie können einen bedingten Ausdruck verwenden, um sicherzustellen, dass das Steuerelement **Order Date** im Dialogfeld ein gültiges Datum enthält. Wenn dies nicht der Fall ist, kann die **MessageBox** -Aktion eine Fehlermeldung anzeigen, und die **stopmakro** -Aktion kann das Makro beenden.

Wenn das Makro die Aktionen **Echo** oder **Warn** Meldungen zum Ausschalten von Echo oder der Anzeige von Systemnachrichten verwendet hat, werden Sie von der **stopmakro** -Aktion automatisch wieder aktiviert.

Diese Aktion ist in einem VBA-Modul (Visual Basic für Applikationen) nicht verfügbar.

## <a name="example"></a>Beispiel

The following macro demonstrates the use of the **OnError** action. In this example, the **OnError** action specifies that Access run a custom error handling macro named ErrorHandler when an error occurs. Wenn ein Fehler auftritt, wird das CatchErrors-unter Makro aufgerufen. Wenn die Fehlernummer 2102 ist, wird eine bestimmte Meldung angezeigt, und die Ausführung des Makros wird angehalten. Andernfalls wird eine Meldung mit dem Fehler angezeigt, und das Makro wird angehalten, damit Sie zusätzliche Problembehandlung durchführen können. The ErrorHandler macro displays a message box that refers to the **MacroError** object to display information about the error.

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
