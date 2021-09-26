---
title: UpdateCriteriaEnum-Aufzählung (DAO)
TOCTitle: UpdateCriteriaEnum Enumeration
ms:assetid: 1f83a0c6-bdc8-9c3e-380b-524f611f6476
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845853(v=office.15)
ms:contentKeyID: 48543644
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ca550cf77b70d27cd1fbc8b7b21af98fe10d7e54
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621626"
---
# <a name="updatecriteriaenum-enumeration-dao"></a>UpdateCriteriaEnum-Aufzählung (DAO)


**Gilt für**: Access 2013, Office 2013

Hiermit geben Sie zusammen mit der **UpdateOptions**-Methode an, wie eine Batchaktualisierung erstellt wird.

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
<td><p>dbCriteriaAllCols</p></td>
<td><p>4 </p></td>
<td><p>Verwendet die Schlüsselspalte(n) und alle Spalten in der WHERE-Klausel.</p></td>
</tr>
<tr class="even">
<td><p>dbCriteriaDeleteInsert</p></td>
<td><p>16 </p></td>
<td><p>Verwendet für jede geänderte Zeile ein DELETE/INSERT-Anweisungspaar.</p></td>
</tr>
<tr class="odd">
<td><p>dbCriteriaKey</p></td>
<td><p>1</p></td>
<td><p>Verwendet nur die Schlüsselspalte(n) in der WHERE-Klausel.</p></td>
</tr>
<tr class="even">
<td><p>dbCriteriaModValues</p></td>
<td><p>2</p></td>
<td><p>Verwendet die Schlüsselspalte(n) und alle aktualisierten Spalten in der WHERE-Klausel.</p></td>
</tr>
<tr class="odd">
<td><p>dbCriteriaTimestamp</p></td>
<td><p>8 </p></td>
<td><p>Verwendet nur die Zeitstempelspalte, soweit vorhanden (ein Laufzeitfehler wird generiert, falls im Resultset keine Zeitstempelspalte vorhanden ist).</p></td>
</tr>
<tr class="even">
<td><p>dbCriteriaUpdate</p></td>
<td><p>32</p></td>
<td><p>Verwendet für jede geänderte Zeile eine UPDATE-Anweisung.</p></td>
</tr>
</tbody>
</table>

