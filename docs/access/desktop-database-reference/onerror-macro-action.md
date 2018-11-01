---
title: BeiFehler-Makroaktion
TOCTitle: OnError Macro Action
ms:assetid: 5c6073c4-2c0f-0ed2-83b0-477636e2d81c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194562(v=office.15)
ms:contentKeyID: 48545088
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm62274
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e755683b4c040b37f0da12f7e67e8c400e62edb4
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882140"
---
# <a name="onerror-macro-action"></a>BeiFehler-Makroaktion

**Betrifft**: Access 2013, Office 2013

Mit der **BeiFehler** -Aktion können Sie angeben, was geschehen soll, wenn in einem Makro ein Fehler auftritt.

## <a name="setting"></a>Einstellung

Die **BeiFehler** -Aktion hat die folgenden Argumente.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Aktionsargument</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Gehe zu</p></td>
<td><p>Geben Sie das allgemeine Verhalten an, das auftreten soll, wenn ein Fehler entdeckt wird. Klicken Sie auf den Dropdownpfeil, und klicken Sie dann auf eine der folgenden Einstellungen:</p>
<div class="tableSection">
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Einstellung</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Nächste</strong></p></td>
<td><p>Microsoft Office Access 2007 zeichnet die Details des Fehlers im <strong>MacroError</strong>-Objekt auf, das Makro wird jedoch nicht beendet. Das Makro wird mit der nächsten Aktion fortgesetzt.</p></td>
</tr>
<tr class="even">
<td><p><strong>Makroname</strong></p></td>
<td><p>Access beendet das aktuelle Makro und führt das im Argument <strong>Makroname</strong> genannte Makro aus.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Fail</strong></p></td>
<td><p>Access beendet das aktuelle Makro und zeigt eine Fehlermeldung an.</p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p>Makroname</p></td>
<td><p>Wenn das Argument Gehe zu auf den Namen des Makros festgelegt ist, geben Sie den Namen des Makros zur Fehlerbehandlung verwendet werden. Der eingegebene Name muss einen Namen in der Spalte <strong>Makroname den Namen</strong> des aktuellen Makros übereinstimmen; Sie können nicht den Namen eines anderen Makro-Objekts eingeben. Im folgenden Beispiel wird das Makro <strong>Fehlerhandler</strong> in das gleiche Makroobjekt wie die <strong>BeiFehler</strong> -Aktion enthalten. Dieses Argument muss leer bleiben, wenn das Argument Gehe zu auf <strong>nächste</strong> oder <strong>Fehler</strong>festgelegt ist.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

- Die **BeiFehler** -Aktion wird gewöhnlich zu Beginn eines Makros platziert, sie kann jedoch auch später im Makro platziert werden. Die in der Aktion eingerichteten Regeln werden bei jedem Ausführen der Aktion wirksam.

- Wenn Sie das Argument Gehe zu auf **Fehler** festlegen, verhält Access sich so, als befände sich keine **BeiFehler** -Aktion im Makro. Das heißt, wenn ein Fehler entdeckt wird, beendet Access das Makro, und es wird eine Standardfehlermeldung angezeigt. Die Hauptverwendung für die Einstellung **Fehler** besteht im Ausschalten jeder zuvor im Makro eingerichteten Fehlerbehandlung.

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
