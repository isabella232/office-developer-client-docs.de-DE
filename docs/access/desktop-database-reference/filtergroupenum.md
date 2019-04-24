---
title: FilterGroupEnum (Access Desktop Database Reference)
TOCTitle: FilterGroupEnum
ms:assetid: 141f8f9a-c188-5937-91cc-3155eaebebd2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248912(v=office.15)
ms:contentKeyID: 48543381
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: be2ce54fe743c46468850abc5dc16520e208ec9e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292419"
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


### <a name="adowfc-equivalent"></a>ADO/WFC-Äquivalent

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
<td><p>AdoEnums. Filtergroup. AFFECTEDRECORDS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Filtergroup. CONFLICTINGRECORDS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Filtergroup. FETCHEDRECORDS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Filtergroup. NONE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Filtergroup. PENDINGRECORDS</p></td>
</tr>
</tbody>
</table>

