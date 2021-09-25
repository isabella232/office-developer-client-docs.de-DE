---
title: RecordStatusEnum-Aufzählung (DAO)
TOCTitle: RecordStatusEnum Enumeration
ms:assetid: bf4492f2-8d8f-f10f-7a3c-d6296d2ce96b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822784(v=office.15)
ms:contentKeyID: 48547483
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d17ebad865cb0430b78d17808a0d9f79bb8210f1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572760"
---
# <a name="recordstatusenum-enumeration-dao"></a>RecordStatusEnum-Aufzählung (DAO)


**Gilt für**: Access 2013, Office 2013

Hiermit geben Sie zusammen mit der **RecordStatus**-Eigenschaft den Aktualisierungsstatus des aktuellen Datensatzes an, wenn dieser Teil einer Batchaktualisierung ist.

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
<td><p>dbRecordDBDeleted</p></td>
<td><p>4 </p></td>
<td><p>Der Datensatz wurde lokal und in der Datenbank gelöscht.</p></td>
</tr>
<tr class="even">
<td><p>dbRecordDeleted</p></td>
<td><p>3</p></td>
<td><p>Der Datensatz wurde gelöscht, er wurde jedoch noch nicht in der Datenbank gelöscht.</p></td>
</tr>
<tr class="odd">
<td><p>dbRecordModified</p></td>
<td><p>1</p></td>
<td><p>Der Datensatz wurde geändert und nicht in der Datenbank aktualisiert.</p></td>
</tr>
<tr class="even">
<td><p>dbRecordNew</p></td>
<td><p>2</p></td>
<td><p>Der Datensatz wurde mit der <strong>AddNew</strong>-Methode eingefügt, aber noch nicht in die Datenbank eingefügt.</p></td>
</tr>
<tr class="odd">
<td><p>dbRecordUnmodified</p></td>
<td><p>0</p></td>
<td><p>(Standard) Der Datensatz wurde nicht geändert, oder er wurde erfolgreich aktualisiert.</p></td>
</tr>
</tbody>
</table>

