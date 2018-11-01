---
title: RecordsetOptionEnum-Enumeration (DAO)
TOCTitle: RecordsetOptionEnum Enumeration
ms:assetid: 3a9d8664-dcb6-cb60-7cf6-e229eb699ef1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192649(v=office.15)
ms:contentKeyID: 48544266
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3410eac81975df5ba69ef13d62c4cfede220449b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886431"
---
# <a name="recordsetoptionenum-enumeration-dao"></a>RecordsetOptionEnum-Enumeration (DAO)


**Betrifft**: Access 2013, Office 2013

Verwenden Sie die **OpenRecordset** -Methode, um die Merkmale eines neuen **Recordset** -Objekts anzugeben.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Wert</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>dbAppendOnly</p></td>
<td><p>8</p></td>
<td><p>Damit können Benutzer neue Datensätze zum Dynaset hinzufügen, vorhandene Datensätze können von den Benutzern jedoch nicht gelesen werden.</p></td>
</tr>
<tr class="even">
<td><p>dbConsistent</p></td>
<td><p>32</p></td>
<td><p>Wendet Aktualisierungen nur auf die Felder an, die keine Auswirkungen auf andere Datensätze im Dynaset haben (nur Dynaset- und Momentaufnahmetyp).</p></td>
</tr>
<tr class="odd">
<td><p>dbDenyRead</p></td>
<td><p>2</p></td>
<td><p>Verhindert, dass andere Benutzer Recordset-Datensätze (nur Tabellentyp) lesen.</p></td>
</tr>
<tr class="even">
<td><p>dbDenyWrite</p></td>
<td><p>1</p></td>
<td><p>Verhindert, dass andere Benutzer Recordset-Datensätze ändern.</p></td>
</tr>
<tr class="odd">
<td><p>Bei der Ausführung</p></td>
<td><p>2048</p></td>
<td><p>Führt die Abfrage aus, ohne zunächst die SQLPrepare ODBC-Funktion aufzurufen.</p></td>
</tr>
<tr class="even">
<td><p>dbFailOnError</p></td>
<td><p>128</p></td>
<td><p>Setzt die Aktualisierungen zurück, wenn ein Fehler auftritt.</p></td>
</tr>
<tr class="odd">
<td><p>dbForwardOnly</p></td>
<td><p>256</p></td>
<td><p>Erstellt einen Vorwärtsbildlauf-Datensatzes des Typs Momentaufnahme (nur Momentaufnahmentyp).</p></td>
</tr>
<tr class="even">
<td><p>dbInconsistent</p></td>
<td><p>16</p></td>
<td><p>Wendet Aktualisierungen auf alle Dynaset-Felder an, sogar wenn andere Datensätze betroffen sind (nur Dynaset- und Momentaufnahmetyp).</p></td>
</tr>
<tr class="odd">
<td><p>dbReadOnly</p></td>
<td><p>4</p></td>
<td><p>Öffnet den Datensatz schreibgeschützt.</p></td>
</tr>
<tr class="even">
<td><p>dbRunAsync</p></td>
<td><p>1024</p></td>
<td><p>Führt die Abfrage asynchron aus.</p></td>
</tr>
<tr class="odd">
<td><p>dbSeeChanges</p></td>
<td><p>512</p></td>
<td><p>Generiert einen Laufzeitfehler, wenn ein anderer Benutzer Daten ändert, die Sie bearbeiten (nur Dynaset-Typ).</p></td>
</tr>
<tr class="even">
<td><p>dbSQLPassThrough</p></td>
<td><p>64</p></td>
<td><p>Sendet eine SQL-Anweisung an eine ODBC-Datenbank (nur Momentaufnahmetyp).</p></td>
</tr>
</tbody>
</table>

