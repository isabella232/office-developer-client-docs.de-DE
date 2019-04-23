---
title: MoveAndSizeWindow-Makroaktion
TOCTitle: MoveAndSizeWindow macro action
ms:assetid: 86bcf45f-90ce-4ca2-a7fb-efbe5347d137
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197001(v=office.15)
ms:contentKeyID: 48546090
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c1b127995a2f9a0af7da80e9df862259b570870e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288806"
---
# <a name="moveandsizewindow-macro-action"></a>MoveAndSizeWindow-Makroaktion

**Gilt für**: Access 2013, Office 2013

Wenn Sie Ihre Dokumentfensteroptionen für die Verwendung von überlappenden Fenstern anstelle von Dokumenten im Registerformat festgelegt haben, können Sie die **verschiebenundgrößeändernfenster** -Aktion verwenden, um das aktive Fenster zu verschieben oder die Größe zu ändern. Informationen zum Festlegen von Dokumentfensteroptionen finden Sie im Abschnitt "Hinweise".

## <a name="setting"></a>Einstellung

Die **verschiebenundgrößeändernfenster** -Aktion hat die folgenden Argumente.

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
<td><p>Die neue horizontale Position der linken oberen Ecke des Fensters, gemessen vom linken Rand des enthaltenden Fensters. Geben Sie die Position in das <strong>Rechte</strong> Feld im Abschnitt <strong>Aktionsargumente</strong> des Bereichs Makro-Generator ein.</p></td>
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
> Jede Maßeinheit ist in Zoll oder Zentimetern abhängig von den regionalen Einstellungen in der Windows-Systemsteuerung.

## <a name="remarks"></a>Bemerkungen

Gehen Sie folgendermaßen vor, um eine Anwendung für die Verwendung von überlappenden Fenstern anstelle von Registerkarten Dokumenten einzurichten:

1.  Klicken Sie auf **Optionen**

2.  Klicken Sie auf **aktuelle Datenbank**.

3.  Klicken Sie im Abschnitt **Anwendungsoptionen** unter **Dokumentfensteroptionen** auf **Überlappende Fenster**.

4.  Klicken Sie auf **OK**, und schließen Sie die Datenbank, und öffnen Sie Sie erneut.

Diese Aktion ähnelt dem Klicken auf **verschieben** oder **Größe** im **System** Menü des Fensters. Mit den Menübefehlen können Sie die Pfeiltasten der Tastatur verwenden, um das Fenster zu verschieben oder die Größe zu ändern. Mit der **verschiebenundgrößeändernfenster** -Aktion geben Sie die Positions-und größenmessungen direkt ein. Sie können die Maus auch zum Verschieben und Vergrößern von Fenstern verwenden.

Sie können diese Aktion für ein beliebiges Fenster in einer beliebigen Ansicht verwenden.

> [!TIP]
> - Wenn Sie ein Fenster ohne Größenänderung verschieben möchten, geben Sie Werte für die Argumente **right** und **down** ein, lassen jedoch die Argumente **Width** und **height** leer.
> - Um die Größe eines Fensters zu ändern, ohne es zu bewegen, geben Sie Werte für die Argumente **Breite** und **Höhe** ein, lassen jedoch die Argumente **Rechts** und **abwärts** leer.

Verwenden Sie die **Move** -Methode des **DoCmd** -Objekts, um die **VERSCHIEBENUNDGRÖßEÄNDERNFENSTER** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.

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
<td><p>IsNull ([Lieferanten-ID])</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Message</strong>: Wechseln Sie zum Datensatz des Lieferanten, dessen Produkte Sie anzeigen möchten, und klicken Sie dann erneut auf die Schaltfläche für die Überprüfung der Produkte. <strong>Beep</strong>: <strong>jatyp</strong>: <strong>Keinetitel</strong>: Wählen Sie einen Zulieferer aus</p></td>
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
<td><p><strong>Formularname</strong>: Produktlisten <strong>Ansicht</strong>: <strong>Datenblatt Filtername</strong>: <strong>Where Condition</strong>: [Supplier ID] = [Forms]! [Lieferanten]! LieferantenNr <strong>Datenmodus</strong>: <strong>Lese-schreibgeschütztfenstermodus-Modus</strong>: <strong>Normal</strong></p></td>
<td><p>Öffnen Sie das Produktlistenformular, und ziegen Sie die Produkte des aktuellen Lieferanten an.</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>Verschiebenundgrößeändernfenster</strong></p></td>
<td><p><strong>rechts</strong>: 0,7799&quot; <strong>unten</strong>: 1,8&quot;</p></td>
<td><p>Positionieren Sie das Produktlistenformular in der unteren rechten Ecke des Lieferantenformulars.</p></td>
</tr>
</tbody>
</table>

