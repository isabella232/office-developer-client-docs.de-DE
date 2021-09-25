---
title: LockTypeEnum (Access-Desktopdatenbankreferenz)
TOCTitle: LockTypeEnum
ms:assetid: 966b4952-5591-4a99-82d5-99cb9ae3fc72
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249667(v=office.15)
ms:contentKeyID: 48546448
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 754b998336ae8399e7f61257884faaf62a871f88
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568824"
---
# <a name="locktypeenum"></a>LockTypeEnum

**Gilt für**: Access 2013, Office 2013

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
<td><p>4 </p></td>
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

