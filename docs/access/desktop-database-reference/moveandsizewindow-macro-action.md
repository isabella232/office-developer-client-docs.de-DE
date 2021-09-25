---
title: MoveAndSizeWindow-Makroaktion
TOCTitle: MoveAndSizeWindow macro action
ms:assetid: 86bcf45f-90ce-4ca2-a7fb-efbe5347d137
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197001(v=office.15)
ms:contentKeyID: 48546090
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 83d4306a7a15b42beb9fe1743b923e6a137f4bf9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597177"
---
# <a name="moveandsizewindow-macro-action"></a>MoveAndSizeWindow-Makroaktion

**Gilt für**: Access 2013, Office 2013

Wenn Sie ihre Dokumentfensteroptionen so festgelegt haben, dass überlappende Fenster anstelle von Dokumenten mit Registerkarten verwendet werden, können Sie die **MoveAndSizeWindow-Aktion** verwenden, um das aktive Fenster zu verschieben oder seine Größe zu ändern. Informationen zum Festlegen von Dokumentfensteroptionen finden Sie im Abschnitt "Hinweise".

## <a name="setting"></a>Einstellung

Die **MoveAndSizeWindow-Aktion** hat die folgenden Argumente.

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
<td><p><strong>Right</strong></p></td>
<td><p>Die neue horizontale Position der linken oberen Ecke des Fensters, gemessen vom linken Rand des enthaltenden Fensters. Geben Sie die Position im <strong>Feld "Rechts"</strong> im Abschnitt <strong>"Aktionsargumente"</strong> im Bereich "Makro-Generator" ein.</p></td>
</tr>
<tr class="even">
<td><p><strong>Down</strong></p></td>
<td><p>Die neue vertikale Position der linken oberen Ecke des Fensters, gemessen vom oberen Rand des enthaltenden Fensters.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Width</strong></p></td>
<td><p>Die neue Fensterbreite.</p></td>
</tr>
<tr class="even">
<td><p><strong>Height</strong></p></td>
<td><p>Die neue Fensterhöhe.</p></td>
</tr>
</tbody>
</table>


Wenn Sie ein Argument leer lassen, verwendet Microsoft Access die aktuelle Einstellung des Fensters.

Sie müssen einen Wert für mindestens ein Argument eingeben.

> [!NOTE]
> Jede Maßeinheit ist in Zoll oder Zentimetern, abhängig von den regionalen Einstellungen in Windows Systemsteuerung.

## <a name="remarks"></a>HinwBemerkungeneise

Gehen Sie folgendermaßen vor, um eine Anwendung so einzurichten, dass sie überlappende Fenster anstelle von Dokumenten mit Registerkarten verwendet:

1.  Klicken Sie auf **"Optionen".**

2.  Klicken Sie auf **"Aktuelle Datenbank".**

3.  Klicken Sie im Abschnitt **Anwendungsoptionen** unter **Dokumentfensteroptionen** auf **Überlappende Fenster**.

4.  Klicken Sie auf **"OK",** und schließen Sie die Datenbank, und öffnen Sie sie erneut.

Diese Aktion ähnelt dem Klicken auf **"Verschieben"** oder **"Größe"** im **Steuerelementmenü** des Fensters. Mit den Menübefehlen verwenden Sie die Pfeiltasten der Tastatur, um das Fenster zu verschieben oder seine Größe zu ändern. Mit der **MoveAndSizeWindow-Aktion** geben Sie die Positions- und Größenmaße direkt ein. Sie können auch die Maus verwenden, um Fenster zu verschieben und die Größe zu ändern.

Sie können diese Aktion in jedem Fenster und in jeder Ansicht verwenden.

> [!TIP]
> - Wenn Sie ein Fenster verschieben möchten, ohne seine Größe zu ändern, geben Sie Werte für die Argumente **"Rechts"** und **"Unten"** ein, lassen sie jedoch die Argumente **"Width"** und **"Height"** leer.
> - Wenn Sie die Größe eines Fensters ändern möchten, ohne es zu verschieben, geben Sie Werte für die Argumente **"Width"** und **"Height"** ein, lassen aber die Argumente **"Right"** und **"Down"** leer.

Verwenden Sie die **MoveSize-Methode** des **DoCmd-Objekts,** um die **MoveAndSizeWindow-Aktion** in einem VBA-Modul (Visual Basic for Applications) auszuführen.

## <a name="example"></a>Beispiel

**Synchronisieren von Formularen mithilfe eines Makros**

Das folgende Makro öffnet ein Produktlistenformular in der unteren rechten Ecke des Lieferantenformulars, in dem die Produkte des aktuellen Lieferanten angezeigt werden. Es zeigt die Verwendung der Aktionen **Echo**, **MessageBox**, **GoToControl**, **StopMakro**, **OpenForm** und **MoveAndSizeWindow**. Es veranschaulicht außerdem die Verwendung eines bedingten Ausdrucks mit den Aktionen **MessageBox**, **GoToControl** und **StopMakro**. Dieses Makro sollte der Schaltfläche für die Überprüfung der Produkte im Lieferantenformular zugeordnet werden.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Bedingung</p></th>
<th><p>Aktion</p></th>
<th><p>Argumente: Einstellung</p></th>
<th><p>Kommentar</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><strong>Echo</strong></p></td>
<td><p><strong>Echo</strong>: <strong>Nein</strong></p></td>
<td><p>Beenden der Bildschirmaktualisierung, während das Makro ausgeführt wird</p></td>
</tr>
<tr class="even">
<td><p>IsNull([Supplier ID])</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Message</strong>: Wechseln Sie zum Datensatz des Lieferanten, dessen Produkte Sie anzeigen möchten, und klicken Sie dann erneut auf die Schaltfläche für die Überprüfung der Produkte. <strong>Signalton</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Einen Lieferanten auswählen</p></td>
<td><p>Wenn im Lieferantenformular kein aktueller Lieferant vorhanden ist, zeigen Sie eine Meldung an.</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Steuerelementname</strong>: Firma</p></td>
<td><p>Verschieben Sie den Fokus auf das CompanyName-Steuerelement.</p></td>
</tr>
<tr class="even">
<td><p>...</p></td>
<td><p><strong>StopMacro</strong></p></td>
<td><p></p></td>
<td><p>Halten Sie das Makro an.</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>Formularname</strong>: <strong>Produktlistenansicht</strong>: <strong>DatasheetFilter-Name:</strong> <strong>Bedingung:</strong>[Lieferanten-ID] = [Formulare]! [Lieferanten]! [SupplierID] <strong>Datenmodus:</strong> <strong>Schreibgeschützter Fenstermodus:</strong> <strong>Normal</strong></p></td>
<td><p>Öffnen Sie das Produktlistenformular, und ziegen Sie die Produkte des aktuellen Lieferanten an.</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>MoveAndSizeWindow</strong></p></td>
<td><p><strong>Rechts</strong>: 0,7799 &quot; <strong>Abwärts</strong>: 1,8&quot;</p></td>
<td><p>Positionieren Sie das Produktlistenformular in der unteren rechten Ecke des Lieferantenformulars.</p></td>
</tr>
</tbody>
</table>

