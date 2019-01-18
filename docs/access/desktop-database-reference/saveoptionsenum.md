---
title: SaveOptionsEnum (Access PC-Datenbank-Referenz)
TOCTitle: SaveOptionsEnum
ms:assetid: 2a4e4c7a-6331-7270-0514-cc549c721ffd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249053(v=office.15)
ms:contentKeyID: 48543906
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 77a617dc54d8acd145648d926e10cf7c9a3cf252
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705995"
---
# <a name="saveoptionsenum"></a>SaveOptionsEnum

**Betrifft**: Access 2013, Office 2013

Gibt an, ob eine Datei erstellt oder gespeichert werden sollte, wenn die Speicherung in einem [Stream](stream-object-ado.md)-Objekt erfolgt. Die Werte können mit einem AND-Operator kombiniert werden.

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
<td><p><strong>adSaveCreateNotExist</strong></p></td>
<td><p>1</p></td>
<td><p>Standardwert. Erstellt eine neue Datei, wenn die vom <em>FileName</em>-Parameter angegebene Datei nicht bereits vorhanden ist.</p></td>
</tr>
<tr class="even">
<td><p><strong>adSaveCreateOverWrite</strong></p></td>
<td><p>2</p></td>
<td><p>Überschreibt die Datei mit den Daten des aktuell geöffneten <strong>Stream</strong>-Objekts, wenn die vom <em>Filename</em>-Parameter angegebene Datei bereits vorhanden ist.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC-Entsprechung

Diese Konstanten haben keine ADO/WFC-Entsprechungen.

