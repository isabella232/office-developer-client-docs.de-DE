---
title: MoveAndSizeWindow Macro Action
TOCTitle: MoveAndSizeWindow Macro Action
ms:assetid: 86bcf45f-90ce-4ca2-a7fb-efbe5347d137
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197001(v=office.15)
ms:contentKeyID: 48546090
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d423668f5ef53abf4216fa8f976c674474a752ed
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474608"
---
# <a name="moveandsizewindow-macro-action"></a>MoveAndSizeWindow Macro Action


**Betrifft**: Access 2013 | Office 2013


Wenn Sie das Dokument im Fensteroptionen auf überlappende Fenster anstelle von Dokumente im Registerkartenformat verwenden eingerichtet haben, können Sie die **Verschiebenundgrößeändernfenster** -Aktion verwenden, verschieben oder die Größe des aktiven Fensters. Informationen zum Festlegen der Dokumentfensteroptionen finden Sie unter "Hinweise".

## <a name="setting"></a>Einstellung

Die **Verschiebenundgrößeändernfenster** -Aktion hat die folgenden Argumente.

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
<td><p>Die neue horizontale Position der linken oberen Ecke des Fensters, gemessen vom linken Rand des enthaltenden Fensters. Geben Sie die Position im Feld <strong>rechts</strong> im Abschnitt <strong>Aktionsargument</strong> des Makro-Generators.</p></td>
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
> <P>Jeder Messung ist in Zoll oder Zentimeter, abhängig von den regionalen Einstellungen in Windows-Systemsteuerung.</P>



## <a name="remarks"></a>Hinweise

Zum Einrichten einer Anwendung auf überlappende Fenster anstelle von Dokumente im Registerkartenformat verwenden, verwenden Sie die folgende Schritte aus:

1.  und klicken Sie dann auf **Optionen**

2.  Klicken Sie auf **aktuelle Datenbank**.

3.  Klicken Sie im Abschnitt **Anwendungsoptionen** unter **Dokumentfensteroptionen** auf **Überlappende Fenster**.

4.  Klicken Sie auf **OK**, und schließen und öffnen Sie die Datenbank erneut.

Diese Aktion entspricht dem Klicken auf **Verschieben** oder **Größe** im **Systemmenü des Fensters** . Mit den Menübefehlen im verwenden Sie die Pfeiltasten der Tastatur verschieben oder die Größe des Fensters. Die **Verschiebenundgrößeändernfenster** -Aktion verwenden Geben Sie die Position und Größe Maße direkt. Sie können auch die Maus zum Verschieben und Größe von Windows verwenden.

Sie können diese Aktion für jedes Fenster in jeder Ansicht verwenden.

**Tipps**

  - Um ein Fenster verschieben, ohne seine Größe zu ändern, geben Sie Werte für die **rechts** und **unten** Argumente, aber lassen Sie die **Breite** und **Höhe** Argumente leer.

  - Um ein Fenster Größe ändern möchten, ohne es zu verschieben, geben Sie Werte für die **Breite** und **Höhe** Argumente, aber lassen Sie die Argumente **rechts** und **Abwärts** leer.

Um die **Verschiebenundgrößeändernfenster** -Aktion in einem Visual Basic für Applikationen (VBA)-Modul auszuführen, verwenden Sie die **MoveSize** -Methode des **DoCmd** -Objekts.

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
<td><p>IsNull ([Lieferanten-Nr])</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Message</strong>: Wechseln Sie zum Datensatz des Lieferanten, dessen Produkte Sie anzeigen möchten, und klicken Sie dann erneut auf die Schaltfläche für die Überprüfung der Produkte. <strong>Signalton</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Lieferanten auswählen</p></td>
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
<td><p><strong>Formularname</strong>: Produkt Liste <strong>Anzeigen</strong>: <strong>DatasheetFilter Name</strong>: <strong>Bedingung</strong>: [Lieferanten-Nr] = [Formulare]! [Lieferanten]! [Lieferanten-Nr] <strong>Datenmodus</strong>: <strong>OnlyWindow Lesemodus</strong>: <strong>Normal</strong></p></td>
<td><p>Öffnen Sie das Produktlistenformular, und ziegen Sie die Produkte des aktuellen Lieferanten an.</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>MoveAndSizeWindow</strong></p></td>
<td><p><strong>Rechts</strong>: 0.7799&quot; <strong>nach unten</strong>: 1,8&quot;</p></td>
<td><p>Positionieren Sie das Produktlistenformular in der unteren rechten Ecke des Lieferantenformulars.</p></td>
</tr>
</tbody>
</table>

