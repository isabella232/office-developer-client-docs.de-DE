---
title: RecordCreateOptionsEnum
TOCTitle: RecordCreateOptionsEnum
ms:assetid: 153dc8ff-680c-1482-d386-4c4b33ffc589
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248917(v=office.15)
ms:contentKeyID: 48543405
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1bc0d378428c00882c49f7783892ca2bf4d4638c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300693"
---
# <a name="recordcreateoptionsenum"></a>RecordCreateOptionsEnum


**Gilt für**: Access 2013, Office 2013

Specifies whether an existing **Record** should be opened or a new **Record** created for the [Record](record-object-ado.md) object [Open](open-method-ado-record.md) method. The values can be combined with an AND operator.

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
<td><p><strong>adCreateCollection</strong></p></td>
<td><p>0x2000</p></td>
<td><p>Erstellt einen neuen <strong>Datensatz</strong> an dem durch <em>Source</em> -Parameter angegebenen Knoten, anstatt einen vorhandenen <strong>Datensatz</strong>zu öffnen. Wenn die Quelle auf einen vorhandenen Knoten zeigt, tritt ein Laufzeitfehler auf, es sei <strong></strong> denn, die addcreatecollection wird mit <strong>adOpenIfExists</strong> oder <strong>adCreateOverwrite</strong>kombiniert.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCreateNonCollection</strong></p></td>
<td><p>0</p></td>
<td><p>Erstellt einen neuen <strong>Datensatz</strong> vom Typ <a href="recordtypeenum.md">adSimpleRecord</a>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCreateOverwrite</strong></p></td>
<td><p>0x4000000</p></td>
<td><p>Ändert die Erstellungskennzeichen <strong></strong>addcreatecollection, <strong>adCreateNonCollection</strong>und <strong>adCreateStructDoc</strong>. Wenn oder mit diesem Wert und einem der Werte für die Erstellungs Kennzeichnung verwendet wird, wenn die Quell-URL auf einen vorhandenen Knoten oder <strong>Datensatz</strong>verweist, wird der vorhandene <strong>Datensatz</strong> überschrieben, und an seiner Stelle wird ein neuer erstellt. Dieser Wert kann nicht zusammen mit <strong>adOpenIfExists</strong>verwendet werden.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCreateStructDoc</strong></p></td>
<td><p>0x80000000</p></td>
<td><p>Erstellt einen neuen <strong>Datensatz</strong> vom Typ <a href="recordtypeenum.md">adStructDoc</a>, statt einen vorhandenen <strong>Datensatz</strong>zu öffnen.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFailIfNotExists</strong></p></td>
<td><p>-1</p></td>
<td><p>Standardwert. Führt zu einem Laufzeitfehler, wenn <em>Quelle</em> auf einen nicht vorhandenen Knoten verweist.</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenIfExists</strong></p></td>
<td><p>0x2000000</p></td>
<td><p>Ändert die Erstellungskennzeichen <strong></strong>addcreatecollection, <strong>adCreateNonCollection</strong>und <strong>adCreateStructDoc</strong>. Wenn oder mit diesem Wert und einem der Werte für die Erstellungs Kennzeichnung verwendet wird, wenn die Quell-URL auf ein vorhandenes Node-oder <strong>Record</strong> -Objekt verweist, muss der Anbieter den vorhandenen <strong>Datensatz</strong> öffnen, statt eine neue zu erstellen. Dieser Wert kann nicht zusammen mit <strong>adCreateOverwrite</strong>verwendet werden.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC-Äquivalent

Diese Konstanten haben keine ADO/WFC-Entsprechungen.

