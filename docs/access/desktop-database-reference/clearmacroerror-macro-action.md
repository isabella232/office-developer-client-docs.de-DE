---
title: ClearMacroError-Makroaktion
TOCTitle: ClearMacroError macro action
ms:assetid: 1091747e-e957-38c6-6454-5169f091323e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845338(v=office.15)
ms:contentKeyID: 48543296
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm109100
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f42386674ff76d550fb47a971860b4e1a5905236
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296374"
---
# <a name="clearmacroerror-macro-action"></a>ClearMacroError-Makroaktion


**Gilt für**: Access 2013, Office 2013


Die **ClearMacroError** -Aktion können Sie um Informationen zu einem Fehler zu löschen, die im **MacroError** -Objekt gespeichert ist.

## <a name="setting"></a>Einstellung

Die **ClearMacroError** -Aktion hat keine Argumente.

## <a name="remarks"></a>Bemerkungen

- Tritt ein Fehler in einem Makro, werden Informationen zu dem Fehler im **MacroError** -Objekt gespeichert. Wenn Sie Fehlermeldungen unterdrückt nicht die **[BeiFehler](onerror-macro-action.md)** -Aktion verwendet haben, wird das Makro beendet und die Fehlerinformationen in eine Standardfehlermeldung angezeigt. Wenn Sie Fehlermeldungen unterdrückt die **BeiFehler** -Aktion verwendet haben, sollten Sie die im **MacroError** -Objekt in einer Bedingung oder in einer benutzerdefinierten Fehlermeldung gespeicherte Informationen verwenden.
    
  Nachdem ein Fehler behandelt wurde, ist die Informationen im **MacroError** -Objekt nicht mehr aktuell, daher es ratsam ist, deaktivieren Sie das Objekt mit der Aktion **ClearMacroError**. Dies setzt die Fehlernummer im **MacroError** -Objekt auf 0 und löscht alle anderen Informationen zu dem Fehler, der in das Objekt, wie die Beschreibung des Fehlers, Makroname, Name der Aktion, Bedingung und Argumente gespeichert ist. Auf diese Weise können Sie **MacroError** -Objekt einem späteren Zeitpunkt erneut überprüfen, um festzustellen, ob ein anderer Fehler aufgetreten ist.

- **MacroError** -Objekt wird automatisch gelöscht, wenn alle Makro beendet wird, daher Sie keine verwenden Sie die Aktion **ClearMacroError** am Ende eines Makros müssen.

- **MacroError** -Objekt enthält Informationen zu nur einem Fehler zu einem Zeitpunkt. Wenn mehr als einen Fehler in einem Makro aufgetreten ist, enthält das **MacroError** -Objekt nur Informationen zu den letzten Fehler.

- Um die **ClearMacroError** -Aktion in einem VBA-Modul auszuführen, verwenden Sie die **ClearMacroError** -Methode des **DoCmd** -Objekts.

## <a name="example"></a>Beispiel

Das folgende Makro verwendet die **BeiFehler** -Aktion mit dem **nächsten** Argument Fehlermeldungen unterdrückt, und klicken Sie dann die **ÖffnenFormular** -Aktion zum Öffnen eines Formulars verwendet. In diesem Beispiel wird ein Fehler absichtlich erstellt, durch die **GeheZuDatensatz** -Aktion verwenden, um zum vorherigen Datensatz zu wechseln. Die Bedingung ** \[MacroError\].\[ \>Zahl\]\<0** testet das **MacroError** -Objekt. Wenn ein Fehler aufgetreten ist, die Fehlernummer ungleich NULL ist, und die **Abfrageergebnis** -Aktion ausführt. Das Meldungsfeld zeigt den Namen der Aktion, die (in diesem Fall die **GeheZuDatensatz** -Aktion) den Fehler verursacht hat, und die Fehlernummer wird angezeigt. Schließlich werden beim Ausführen der Aktion **ClearMacroError** **MacroError** -Objekt gelöscht.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Bedingung</p></th>
<th><p>Aktion</p></th>
<th><p>Argumente</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><strong>OnError</strong></p></td>
<td><p><strong>Wechseln Sie zu</strong>: <strong>Weiter</strong></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>Formular Name</strong>: CategoryForm-<strong>Ansicht</strong>: <strong>FormWindow-Modus</strong>: <strong>Normal</strong></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>GoToRecord</strong></p></td>
<td><p><strong>Objekttyp</strong>: <strong>formobject Name</strong>: CategoryForm<strong>Record</strong>: Previous</p></td>
</tr>
<tr class="even">
<td><p>[MacroError].[Number]&lt;&gt;0</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Message</strong>: =&quot;Error # &quot; &amp; [MacroError]. Anzahl &amp; &quot; [ &quot; MacroError &amp; ]. ActionName &amp; &quot; &quot; <strong>Beep</strong>: <strong>jatyp</strong>: Informationen</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>ClearMacroError</strong></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

