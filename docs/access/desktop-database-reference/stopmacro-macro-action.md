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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704434"
---
# <a name="stopmacro-macro-action"></a>StopMacro-Makroaktion

**Betrifft**: Access 2013, Office 2013

Die **StoppMakro** -Aktion können Sie das derzeit ausgeführte Makro anzuhalten.

## <a name="setting"></a>Setting

Die **StoppMakro** -Aktion verfügt nicht über keine Argumente.

## <a name="remarks"></a>Bemerkungen

Normalerweise verwenden Sie diese Aktion, wenn eine Bedingung das Makro anzuhalten vornimmt. Sie können einen bedingten Ausdruck in der Aktionszeile des Makros verwenden, die diese Aktion enthält. Wenn der Ausdruck auf **True** (– 1) ausgewertet wird, beendet Microsoft Access das Makro aus.

Beispielsweise können Sie ein Makro erstellen, das einem Formular mit der täglichen Summen Reihenfolge für das Datum in einem benutzerdefinierten Dialogfeld geöffnet wird. Sie können einen bedingten Ausdruck verwenden, um sicherzustellen, dass das Steuerelement **Bestelldatum** im Dialogfeld ein gültiges Datum enthält. Wenn dies nicht der Fall, die **Abfrageergebnis** -Aktion kann eine Fehlermeldung angezeigt, und die **StoppMakro** -Aktion kann das Makro beenden.

Wenn das Makro die Aktionen **Echo** oder **Warnmeldungen** zum Aktivieren von Echo oder die Anzeige von systemmeldungen aus verwendet, wird von die **StoppMakro** -Aktion automatisch wieder aktiviert.

Diese Aktion ist in einem VBA-Modul (Visual Basic für Applikationen) nicht verfügbar.

## <a name="example"></a>Beispiel

Das folgende Makro veranschaulicht die Verwendung der **BeiFehler** -Aktion. In diesem Beispiel gibt die **BeiFehler** -Aktion an, dass Access führen Sie eine benutzerdefinierte Fehlerbehandlung Makro mit dem Namen Fehlerhandler, wenn ein Fehler auftritt. Wenn ein Fehler auftritt, wird das Untermakro CatchErrors aufgerufen. Wenn die Fehlernummer 2102 ist, eine bestimmte Nachricht wird angezeigt, und Ausführung von Makros wird unterbrochen. Andernfalls wird eine Meldung, die Beschreibung des Fehlers angezeigt und das Makro wird angehalten, damit Sie zusätzliche Hinweise zur Problembehandlung ausführen können. Das Fehlerhandler Makro zeigt eine Meldung angezeigt, die auf das **MacroError** -Objekt zum Anzeigen von Informationen zu dem Fehler verweist.

**Beispielcode von** der [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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
