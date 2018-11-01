---
title: RightsEnum (Access PC-Datenbank-Referenz)
TOCTitle: RightsEnum
ms:assetid: 7647b9d5-5271-fdcf-489d-5a8beb931ca5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249485(v=office.15)
ms:contentKeyID: 48545693
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 535c80bf5cd3dbfecae0e004082ce20d01c31fde
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877387"
---
# <a name="rightsenum"></a>RightsEnum

**Betrifft**: Access 2013, Office 2013

Gibt die Rechte oder Berechtigungen einer Gruppe oder eines Benutzers für ein Objekt an.

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Konstante</p></th>
<th><p>Wert</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adRightCreate</strong></p></td>
<td><p>16384<br />
(&amp;H4000)</p></td>
<td><p>Der Benutzer oder die Gruppe verfügt über die Berechtigung, neue Objekte dieses 'Typs zu erstellen.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRightDelete</strong></p></td>
<td><p>65536<br />
(&amp;H10000)</p></td>
<td><p>Der Benutzer oder die Gruppe verfügt über die Berechtigung, Daten aus einem Objekt zu löschen. Für Objekte wie <strong>Tables</strong> verfügt der Benutzer über die Berechtigung, Datenwerte aus Datensätzen zu löschen.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRightDrop</strong></p></td>
<td><p>256<br />
(&amp;H100)</p></td>
<td><p>Der Benutzer oder die Gruppe verfügt über die Berechtigung, Objekte aus dem Katalog zu entfernen. Beispielsweise kann <strong>Tables</strong> durch einen DROP TABLE SQL-Befehl gelöscht werden.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRightExclusive</strong></p></td>
<td><p>512<br />
(&amp;H200)</p></td>
<td><p>Der Benutzer oder die Gruppe verfügen über die Berechtigung, exklusiv auf das Objekt zuzugreifen.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRightExecute</strong></p></td>
<td><p>536870912<br />
(&amp;H20000000)</p></td>
<td><p>Der Benutzer oder die Gruppe verfügt über die Berechtigung, das Objekt auszuführen.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRightFull</strong></p></td>
<td><p>268435456<br />
(&amp;H10000000)</p></td>
<td><p>Der Benutzer oder die Gruppe verfügt über alle Berechtigungen für das Objekt.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRightInsert</strong></p></td>
<td><p>32768<br />
(&amp;H8000)</p></td>
<td><p>Der Benutzer oder die Gruppe verfügt über die Berechtigung, das Objekt einzufügen. Für Objekte wie <strong>Tables</strong> verfügt der Benutzer über die Berechtigung, Daten in die Tabelle einzufügen.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRightMaximumAllowed</strong></p></td>
<td><p>33554432 (&amp;H2000000)</p></td>
<td><p>Der Benutzer oder die Gruppe verfügt über die durch den Anbieter maximal zulässige Anzahl von Berechtigungen. Spezifische Berechtigungen sind anbieterabhängig.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRightNone</strong></p></td>
<td><p>0</p></td>
<td><p>Der Benutzer oder die Gruppe verfügt über keine Berechtigungen für das Objekt.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRightRead</strong></p></td>
<td><p>-2147483648<br />
(&amp;H80000000)</p></td>
<td><p>Der Benutzer oder die Gruppe verfügt über eine Leseberechtigung für das Objekt. Für Objekte wie <a href="table-object-adox.md">Tables</a> verfügt der Benutzer über die Berechtigung, Daten in der Tabelle zu lesen.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRightReadDesign</strong></p></td>
<td><p>1024<br />
(&amp;H400)</p></td>
<td><p>Der Benutzer oder die Gruppe verfügt über die Berechtigung, den Entwurf für das Objekt zu lesen.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRightReadPermissions</strong></p></td>
<td><p>131072<br />
(&amp;H20000)</p></td>
<td><p>Der Benutzer oder die Gruppe kann die spezifischen Berechtigungen für ein Objekt im Katalog anzeigen, aber nicht ändern.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRightReference</strong></p></td>
<td><p>8192<br />
(&amp;H2000)</p></td>
<td><p>Der Benutzer oder die Gruppe verfügt über die Berechtigung, auf das Objekt zu verweisen.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRightUpdate</strong></p></td>
<td><p>1073741824<br />
(&amp;H40000000)</p></td>
<td><p>Der Benutzer oder die Gruppe verfügt über die Berechtigung, das Objekt zu aktualisieren. Für Objekte wie <strong>Tables</strong> verfügt der Benutzer über die Berechtigung, die Daten in der Tabelle zu aktualisieren.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRightWithGrant</strong></p></td>
<td><p>4096<br />
(&amp;H1000)</p></td>
<td><p>Der Benutzer oder die Gruppe verfügt über die Berechtigung, Berechtigungen für das Objekt zu erteilen.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRightWriteDesign</strong></p></td>
<td><p>2048<br />
(&amp;H800)</p></td>
<td><p>Der Benutzer oder die Gruppe verfügt über die Berechtigung, den Entwurf des Objekts zu bearbeiten.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRightWriteOwner</strong></p></td>
<td><p>524288<br />
(&amp;H80000)</p></td>
<td><p>Der Benutzer oder die Gruppe verfügt über die Berechtigung, den Besitzer des Objekts zu ändern.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRightWritePermissions</strong></p></td>
<td><p>262144<br />
(&amp;H40000)</p></td>
<td><p>Der Benutzer oder die Gruppe kann die spezifischen Berechtigungen für ein Objekt im Katalog bearbeiten.</p></td>
</tr>
</tbody>
</table>

