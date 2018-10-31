---
title: FilterGroupEnum (Access PC-Datenbank-Referenz)
TOCTitle: FilterGroupEnum
ms:assetid: 141f8f9a-c188-5937-91cc-3155eaebebd2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248912(v=office.15)
ms:contentKeyID: 48543381
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: fc2c41ddd672ff303584762f6091bab4c128de99
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862695"
---
# <a name="filtergroupenum"></a>FilterGroupEnum

**Betrifft**: Access 2013 | Office 2013

Gibt die Gruppe der Datensätze an, die aus einem [Recordset](recordset-object-ado.md) gefiltert werden sollen.

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
<td><p><strong>adFilterAffectedRecords</strong></p></td>
<td><p>2</p></td>
<td><p>Filter zum Anzeigen von Datensätzen, die vom letzten <a href="delete-method-ado-recordset.md">Delete</a>-, <a href="resync-method-ado.md">Resync</a>-, <a href="updatebatch-method-ado.md">UpdateBatch</a>- oder <a href="cancelbatch-method-ado.md">CancelBatch</a>-Aufruf betroffen sind.</p></td>
</tr>
<tr class="even">
<td><p><strong>vorliegt</strong></p></td>
<td><p>5</p></td>
<td><p>Filter zum Anzeigen der Datensätze, für die die letzte Batchaktualisierung fehlgeschlagen ist.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFilterFetchedRecords</strong></p></td>
<td><p>3</p></td>
<td><p>Filter zum Anzeigen der Datensätze im aktuellen Cache – also die Ergebnisse des letzten Aufrufs zum Abrufen von Datensätzen aus der Datenbank.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFilterNone</strong></p></td>
<td><p>0</p></td>
<td><p>Entfernt den aktuellen Filter und stellt alle Datensätze für die Ansicht wieder her.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFilterPendingRecords</strong></p></td>
<td><p>1</p></td>
<td><p>Filter zum Anzeigen von Datensätzen, die geändert, jedoch noch nicht an den Server gesendet wurden. Nur für den Batchaktualisierungsmodus anwendbar.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC-Entsprechung

Paket: **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Konstante</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.FilterGroup.AFFECTEDRECORDS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.FilterGroup.CONFLICTINGRECORDS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.FilterGroup.FETCHEDRECORDS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.FilterGroup.NONE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.FilterGroup.PENDINGRECORDS</p></td>
</tr>
</tbody>
</table>

