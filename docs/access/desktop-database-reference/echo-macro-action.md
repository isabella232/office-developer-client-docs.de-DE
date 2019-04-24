---
title: Echo-Makroaktion (Access-Desktop-Daten Bankreferenz)
TOCTitle: Echo macro action
ms:assetid: 38dfb2cf-8db5-44b3-91fa-e490932b940b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192516(v=office.15)
ms:contentKeyID: 48544227
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7d536ed47c780b7f9f1675a9879e86aeff80b67f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293623"
---
# <a name="echo-macro-action"></a>Echo-Makroaktion

**Gilt für**: Access 2013, Office 2013

Sie können die **Echo** -Aktion verwenden, um anzugeben, ob Echo eingeschaltet ist. Sie können diese Aktion beispielsweise verwenden, um die Ergebnisse eines Makros während der Ausführung ein-oder auszublenden.

## <a name="setting"></a>Einstellung

> [!NOTE]
> Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist.

Die **Echo** -Aktion hat die folgenden Argumente.

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
<td><p><strong>Echo ein</strong></p></td>
<td><p>Klicken Sie im Feld <strong>Echo on</strong> im Abschnitt <strong>Aktionsargumente</strong> des Bereichs Makro-Generator auf <strong>Ja</strong> (Echo aktivieren) oder <strong>Nein</strong> (Echo aus). Die Standardeinstellung ist <strong>Ja</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Statusleistentext</strong></p></td>
<td><p>Der Text, der in der Statusleiste angezeigt werden soll, wenn ECHO deaktiviert ist. Wenn Echo beispielsweise deaktiviert ist, kann in der Statusleiste angezeigt &quot;werden, dass das Makro gerade läuft.&quot;</p></td>
</tr>
</tbody>
</table>


Wenn ein Makro ausgeführt wird, zeigt die Bildschirmaktualisierung oft Informationen an, die für das Funktionieren des Makros nicht unbedingt erforderlich sind. Wenn Sie das Argument **Echo auf** **Nein**festlegen, wird das Makro ohne Aktualisieren des Bildschirms ausgeführt. Nach Abschluss des Makros schaltet Access das Echo automatisch wieder ein und zeichnet das Fenster neu. Die Einstellung **keine** für das Argument **Echo on wirkt sich** nicht auf die Funktionalität des Makros oder seiner Ergebnisse aus.

Die **Echo** -Aktion unterdrückt die Anzeige von modalen Dialogfeldern wie beispielsweise Fehlermeldungen oder Popupformularen wie z. b. Eigenschaftenblätter nicht. Sie können Dialogfelder und Popupformulare verwenden, um Informationen zu erfassen oder anzuzeigen, auch wenn ECHO deaktiviert ist. Verwenden Sie die **Warn** Meldungen-Aktion, um alle Nachrichten oder Dialogfelder außer Fehler Meldungsfeldern und Dialogfeldern zu unterdrücken, in denen der Benutzerinformationen eingeben muss.

Sie können die **Echo** -Aktion in einem Makro mehrmals ausführen. Auf diese Weise können Sie den Text der Statusleiste ändern, während das Makro ausgeführt wird.

Wenn Sie Echo deaktivieren, können Sie die **anzeigen Sanduhrzeiger** -Aktion verwenden, um den Mauszeiger in ein Sanduhrsymbol zu ändern (oder für das Mauszeiger Symbol, das Sie für "busy" festgelegt haben), um einen visuellen Hinweis darauf zu geben, dass das Makro ausgeführt wird.

Verwenden Sie die **Echo** -Methode des **DoCmd** -Objekts, um die **Echo** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.

## <a name="examples"></a>Beispiele

### <a name="set-the-value-of-a-control-by-using-a-macro"></a>Festlegen des Werts eines Steuerelements mithilfe eines Makros

Das folgende Makro öffnet das Formular zum Hinzufügen von Produkten über eine Schaltfläche im Formular für Lieferanten. Es zeigt die Verwendung der Aktionen **Echo**, **FensterSchließen**, **ÖffnenFormular**, **SetzenWert ** und **GeheZuSteuerelement**. Mit **** der SetValue-Aktion wird das Lieferanten-ID-Steuerelement im Formular Produkte auf den aktuellen Lieferanten im Formular Lieferanten festgelegt. Die **gotoCONTROL** -Aktion verschiebt dann den Fokus auf das Feld Kategorie-ID, in dem Sie mit der Eingabe von Daten für das neue Produkt beginnen können. Dieses Makro sollte der Schaltfläche zum Hinzufügen von Produkten im Formular für Lieferanten zugeordnet werden.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Aktion</p></th>
<th><p>Argumente: Einstellung</p></th>
<th><p>Kommentar</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Echo</strong></p></td>
<td><p><strong>Echo</strong>: <strong>Nein</strong></p></td>
<td><p>Beenden der Bildschirmaktualisierung, während das Makro ausgeführt wird</p></td>
</tr>
<tr class="even">
<td><p><strong>Fenster schließen</strong></p></td>
<td><p><strong>Objekttyp</strong>: <strong>Formularobjekt Name</strong>: Produktlisten <strong>Speicher</strong>: <strong>Nein</strong></p></td>
<td><p>Schließen des Produktlistenformulars</p></td>
</tr>
<tr class="odd">
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>Formular Name</strong>: Produkt <strong>Ansicht</strong>: <strong>FormData Modus</strong>: <strong>addwindow Mode</strong>: <strong>Normal</strong></p></td>
<td><p>Öffnen des Produktformulars</p></td>
</tr>
<tr class="even">
<td><p><strong>SetzenWert</strong></p></td>
<td><p><strong>Element</strong>: [Formulare]! [Products]! LieferantenNr <strong>Ausdruck</strong>: Lieferanten-Nr.</p></td>
<td><p>Legen Sie das Lieferanten-ID-Steuerelement auf den aktuellen Lieferanten im Formular Lieferanten fest.</p></td>
</tr>
<tr class="odd">
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Steuerelementname</strong>: CategoryID</p></td>
<td><p>Wechseln Sie zum Steuerelement Category ID.</p></td>
</tr>
</tbody>
</table>


### <a name="synchronize-forms-by-using-a-macro"></a>Synchronisieren von Formularen mithilfe eines Makros

Mit dem folgenden Makro wird das Produktlisten Formular in der unteren rechten Ecke des Formulars Lieferanten geöffnet, in dem die Produkte des aktuellen Lieferanten angezeigt werden. Es zeigt die Verwendung der Aktionen **Echo**, **MessageBox**, **GoToControl**, **StopMakro**, **OpenForm** und **MoveAndSizeWindow**. Es veranschaulicht außerdem die Verwendung eines bedingten Ausdrucks mit den Aktionen **MessageBox**, **GoToControl** und **StopMakro**. Dieses Makro sollte der Schaltfläche für die Überprüfung der Produkte im Lieferantenformular zugeordnet werden.

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
<td><p>...</p></td>
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

