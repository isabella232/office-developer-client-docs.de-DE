---
title: LockTypeEnum (Access PC-Datenbank-Referenz)
TOCTitle: LockTypeEnum
ms:assetid: 966b4952-5591-4a99-82d5-99cb9ae3fc72
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249667(v=office.15)
ms:contentKeyID: 48546448
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d4b9dc49e647bdcd3123ade065da0c74538c9a88
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715368"
---
# <a name="locktypeenum"></a>LockTypeEnum

**Betrifft**: Access 2013, Office 2013

Gibt den Sperrentyp für Datensätze während der Bearbeitung an.

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
<td><p><strong>adLockBatchOptimistic</strong></p></td>
<td><p>4</p></td>
<td><p>Gibt optimistische Batchaktualisierungen an. Erforderlich für den Batchaktualisierungsmodus.</p></td>
</tr>
<tr class="even">
<td><p><strong>adLockOptimistic</strong></p></td>
<td><p>3</p></td>
<td><p>Gibt das optimistische Sperren auf Datensatzbasis an. Der Anbieter verwendet optimistische Sperren, wobei die Datensätze nur gesperrt werden, wenn Sie die <a href="update-method-ado.md">Update</a>-Methode aufrufen.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adLockPessimistic</strong></p></td>
<td><p>2</p></td>
<td><p>Gibt das pessimistische Sperren auf Datensatzbasis an. Der Anbieter führt die erforderlichen Schritte aus, um eine erfolgreiche Bearbeitung der Datensätze sicherzustellen, indem die Datensätze unmittelbar nach der Bearbeitung an der Datenquelle gesperrt werden.</p></td>
</tr>
<tr class="even">
<td><p><strong>adLockReadOnly</strong></p></td>
<td><p>1</p></td>
<td><p>Gibt schreibgeschützte Datensätze an. Sie können die Daten nicht ändern.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adLockUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>Gibt keinen Sperrentyp an. Für Klone wird der Klon mit demselben Sperrentyp wie das Original erstellt.</p></td>
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
<td><p>AdoEnums.LockType.BATCHOPTIMISTIC</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.LockType.OPTIMISTIC</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.LockType.PESSIMISTIC</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.LockType.READONLY</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.LockType.UNSPECIFIED</p></td>
</tr>
</tbody>
</table>

