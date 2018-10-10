---
title: MessageBox Macro Action
TOCTitle: MessageBox Macro Action
ms:assetid: 326a0e68-38fb-4f81-b319-5a70caa5aec4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192304(v=office.15)
ms:contentKeyID: 48544077
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dd2600164941555c584bb91b827debfd4074ea18
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474772"
---
# <a name="messagebox-macro-action"></a>MessageBox Macro Action


**Betrifft**: Access 2013 | Office 2013




Sie können die **MessageBox** -Aktion verwenden, um ein Nachrichtenfeld mit einer Warnung oder einer Informationsmeldung anzuzeigen. Sie können die **MessageBox** -Aktion beispielsweise mit Validierungsmakros verwenden. Wenn bei einem Steuerelement oder einem Datensatz ein Fehler bezüglich einer Überprüfungsbedingung im Makro auftritt, können eine Fehlermeldung in einem Nachrichtenfeld angezeigt und Anweisungen zu der Art von Daten gegeben werden, die eingegeben werden sollten.

## <a name="setting"></a>Einstellung

Die **MessageBox** -Aktion hat die folgenden Argumente.

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
<td><p><strong>Message</strong></p></td>
<td><p>Der Text im Nachrichtenfeld. Geben Sie den Nachrichtentext in das Feld <strong>Nachricht</strong> im Abschnitt <strong>Aktionsargumente</strong> des Makro-Generators ein. Sie können bis zu 255 Zeichen oder einen Ausdruck (mit einem vorangestellten Gleichheitszeichen) eingeben.  </p></td>
</tr>
<tr class="even">
<td><p><strong>Beep</strong></p></td>
<td><p>Gibt an, ob aus dem Lautsprecher des Computers ein Signalton ertönt, wenn die Meldung angezeigt wird. Klicken Sie auf <strong>Ja</strong> (Signalton abspielen) oder <strong>Nein</strong> (Signalton nicht abspielen). Die Standardeinstellung ist <strong>Ja</strong>.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Type</strong></p></td>
<td><p>Der Typ des Nachrichtenfelds. Jeder Typ weist ein anderes Symbol auf. Klicken Sie auf <strong>Keiner</strong>, <strong>Kritisch</strong>, <strong>Warnung?</strong>, <strong>Warnung!</strong>, oder <strong>Information</strong>. Der Standardwert lautet <strong>Keine</strong>.  </p></td>
</tr>
<tr class="even">
<td><p><strong>Title</strong></p></td>
<td><p>Der in der Titelleiste des Nachrichtfelds angezeigte Text. Sie können beispielsweise die Anzeige der Titel haben &quot;Kundennummer&quot;. Wenn Sie dieses Argument leer lassen &quot;Microsoft Access&quot; wird angezeigt.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Sie können die **MessageBox** -Aktion verwenden, um eine formatierte Fehlermeldung zu erstellen, ähnlich wie integrierte Meldungen, die von Microsoft Access angezeigt werden. Mit der **MessageBox** -Aktion können Sie eine Nachricht in drei Abschnitten für das Message-Argument bereitstellen. Trennen Sie die Abschnitte mit dem "@"-Zeichen voneinander.

Das folgende Beispiel zeigt ein formatiertes Meldungsfeld mit einer unterteilten Meldung. Der erste Textabschnitt in der Nachricht wird als fett formatierte Überschrift angezeigt. Der zweite Abschnitt wird als reiner Text unterhalb dieser Überschrift angezeigt. Der dritte Abschnitt wird als reiner Textt unter dem zweiten Abschnitt mit einer leeren Zeile dazwischen angezeigt.

Geben Sie die folgende Zeichenfolge in das **Message** -Argument ein:

**Falsche Schaltfläche\!@This Schaltfläche nicht work.@Try eine andere.**

Die **MessageBox** -Aktion kann nicht in einem VBA-Modul (Visual Basic für Applikationen) ausgeführt werden. Verwenden Sie stattdessen die **Msg** -Funktion.

## <a name="examples"></a>Beispiele

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
<td><p>IsNull([SupplierID])</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Message</strong>: Wechseln Sie zum Datensatz des Lieferanten, dessen Produkte Sie anzeigen möchten, und klicken Sie dann erneut auf die Schaltfläche für die Überprüfung der Produkte. <strong>Signalton</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Lieferanten auswählen</p></td>
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


** Überprüfen der Gültigkeit von Daten mithilfe eines Makros**

Mit dem folgenden Gültigkeitsprüfungsmakro werden die Postleitzahlen überprüft, die im Lieferantenformular eingegeben werden. Es zeigt die Verwendung der Aktionen **StopMacro**, **MessageBox**, **CancelEvent** und **GoToControl**. Mit einem Bedingungsausdruck werden das Land, die Region und die Postleitzahl überprüft, die im Formular in einem Datensatz eingegeben werden. Wenn die Postleitzahl nicht das richtige Format für das Land oder die Region aufweist, wird vom Makro ein Meldungsfeld angezeigt, und das Speichern des Datensatzes wird abgebrochen. Sie kehren dann zum PostalCode-Steuerelement zurück, in dem Sie den Fehler korrigieren können. Dieses Makro sollte mit der **BeforeUpdate** -Eigenschaft des Lieferantenformulars verbunden sein.

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
<td><p>IsNull([CountryRegion])</p></td>
<td><p><strong>StopMacro</strong></p></td>
<td><p></p></td>
<td><p>Wenn „Land/Region" den Wert <strong>Null</strong> hat, kann die Postleitzahl nicht überprüft werden.</p></td>
</tr>
<tr class="even">
<td><p>[Land/Region] In (&quot;Frankreich&quot;,&quot;Italien&quot;,&quot;Spanien&quot;) und Länge([Postleitzahl]) &lt; &gt; 5</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Message</strong>: Die Postleitzahl muss 5 Zeichen lang sein. <strong>Signalton</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postleitzahl fehlerhaft</p></td>
<td><p>Zeigt eine Meldung an, wenn die Postleitzahl nicht 5 Zeichen lang ist.</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p><strong>CancelEvent</strong></p></td>
<td><p></p></td>
<td><p>Bricht das Ereignis ab.</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Steuerelementname</strong>: PostalCode</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>[Land/Region] In (&quot;Australien&quot;,&quot;Singapur&quot;) und Länge([Postleitzahl]) &lt; &gt; 4</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Message</strong>: Die Postleitzahl muss 4 Zeichen lang sein. <strong>Signalton</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postleitzahl fehlerhaft</p></td>
<td><p>Zeigt eine Meldung an, wenn die Postleitzahl nicht 4 Zeichen lang ist.</p></td>
</tr>
<tr class="even">
<td><p>...</p></td>
<td><p><strong>CancelEvent</strong></p></td>
<td><p></p></td>
<td><p>Bricht das Ereignis ab.</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Steuerelementname</strong>: PostalCode</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>([Land/Region] = &quot;Kanada&quot;) Und ([Postleitzahl] nicht wie&quot;[A-Z] [0-9] [A-Z] [0-9] [A-Z] [0-9]&quot;)</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Meldung</strong>: Die Postleitzahl ist ungültig. Beispiel für kanadische Postleitzahl: H1J 1 c 3 <strong>Signalton</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: PLZ Codefehler</p></td>
<td><p>Zeigt eine Meldung an, wenn eine für Kanada ungültige Postleitzahl angegeben wird. (Beispiel für eine kanadische Postleitzahl: H1J 1C3).</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p><strong>CancelEvent</strong></p></td>
<td><p></p></td>
<td><p>Bricht das Ereignis ab.</p></td>
</tr>
</tbody>
</table>

