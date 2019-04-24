---
title: SynchronizeTypeEnum-Aufzählung (DAO)
TOCTitle: SynchronizeTypeEnum Enumeration
ms:assetid: f9546171-283d-e9bd-5178-41bd4f41c9a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837004(v=office.15)
ms:contentKeyID: 48548812
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: acd4ca20e9b6e17f28a17b012bb182060471e949
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308449"
---
# <a name="synchronizetypeenum-enumeration-dao"></a>SynchronizeTypeEnum-Aufzählung (DAO)


**Gilt für**: Access 2013, Office 2013

Hiermit geben Sie zusammen mit der **Synchronize**-Methode an, welche Synchronisierungsart auf zwei Replikate angewendet werden soll.

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
<td><p>dbRepExportChanges</p></td>
<td><p>1</p></td>
<td><p>Sendet Änderungen von der aktuellen Datenbank an die Zieldatenbank.</p></td>
</tr>
<tr class="even">
<td><p>dbRepImpExpChanges</p></td>
<td><p>4</p></td>
<td><p>Sendet und empfängt Daten im bidirektionalen Austausch.</p></td>
</tr>
<tr class="odd">
<td><p>dbRepImportChanges</p></td>
<td><p>2</p></td>
<td><p>Empfängt Änderungen von der Zieldatenbank.</p></td>
</tr>
<tr class="even">
<td><p>dbRepSyncInternet</p></td>
<td><p>16</p></td>
<td><p>Sendet und empfängt Daten im bidirektionalen Austausch.</p></td>
</tr>
</tbody>
</table>

