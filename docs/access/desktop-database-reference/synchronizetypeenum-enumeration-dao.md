---
title: SynchronizeTypeEnum Enumeration (DAO)
TOCTitle: SynchronizeTypeEnum Enumeration
ms:assetid: f9546171-283d-e9bd-5178-41bd4f41c9a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837004(v=office.15)
ms:contentKeyID: 48548812
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 872ba8a4ab3340e6e1d973181b653b7f22961cb3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473034"
---
# <a name="synchronizetypeenum-enumeration-dao"></a>SynchronizeTypeEnum Enumeration (DAO)


**Betrifft**: Access 2013 | Office 2013

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
