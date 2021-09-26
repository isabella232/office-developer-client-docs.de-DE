---
title: FilterGroupEnum (Access-Desktopdatenbankreferenz)
TOCTitle: FilterGroupEnum
ms:assetid: 141f8f9a-c188-5937-91cc-3155eaebebd2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248912(v=office.15)
ms:contentKeyID: 48543381
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d4527f0fdcd0a6b3840559009c7828d9a6c39f02
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626554"
---
# <a name="filtergroupenum"></a>FilterGroupEnum

**Gilt für**: Access 2013, Office 2013

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
<td><p><strong>adFilterConflictingRecords</strong></p></td>
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

