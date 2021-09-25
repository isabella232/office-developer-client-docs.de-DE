---
title: RecordCreateOptionsEnum
TOCTitle: RecordCreateOptionsEnum
ms:assetid: 153dc8ff-680c-1482-d386-4c4b33ffc589
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248917(v=office.15)
ms:contentKeyID: 48543405
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 6fa9193c8ff1110fb132051d5a373948d99c0892
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593782"
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
<td><p>Erstellt einen neuen <strong>Datensatz</strong> an dem durch den <em>Parameter Source</em> angegebenen Knoten, anstatt einen vorhandenen <strong>Datensatz</strong>zu öffnen. Wenn die Quelle auf einen vorhandenen Knoten zeigt, tritt ein Laufzeitfehler auf, es sei denn, <strong>adCreateCollection</strong> wird mit <strong>adOpenIfExists</strong> oder <strong>adCreateOverwrite</strong>kombiniert.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCreateNonCollection</strong></p></td>
<td><p>0</p></td>
<td><p>Erstellt einen neuen <strong>Datensatz</strong> vom Typ <a href="recordtypeenum.md">adSimpleRecord</a>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCreateOverwrite</strong></p></td>
<td><p>0x4000000</p></td>
<td><p>Ändert die Erstellungsflags <strong>"adCreateCollection",</strong> <strong>"adCreateNonCollection"</strong>und <strong>"adCreateStructDoc".</strong> Wenn OR mit diesem Wert und einem der Erstellungskennzeichenwerte verwendet wird, wenn die Quell-URL auf einen vorhandenen Knoten oder <strong>Datensatz</strong>zeigt, wird der vorhandene <strong>Datensatz</strong> überschrieben, und an seiner Stelle wird ein neuer erstellt. Dieser Wert kann nicht zusammen mit <strong>adOpenIfExists</strong>verwendet werden.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCreateStructDoc</strong></p></td>
<td><p>0x80000000</p></td>
<td><p>Erstellt einen neuen <strong>Datensatz</strong> vom Typ <a href="recordtypeenum.md">"adStructDoc",</a>anstatt einen vorhandenen <strong>Datensatz</strong>zu öffnen.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFailIfNotExists</strong></p></td>
<td><p>-1</p></td>
<td><p>Standardwert. Führt zu einem Laufzeitfehler, wenn <em>Quelle</em> auf einen nicht vorhandenen Knoten verweist.</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenIfExists</strong></p></td>
<td><p>0x2000000</p></td>
<td><p>Ändert die Erstellungsflags <strong>"adCreateCollection",</strong> <strong>"adCreateNonCollection"</strong>und <strong>"adCreateStructDoc".</strong> Wenn OR mit diesem Wert und einem der Erstellungsflagswerte verwendet wird und die Quell-URL auf einen vorhandenen Knoten oder ein <strong>Record-Objekt</strong> zeigt, muss der Anbieter den vorhandenen <strong>Datensatz</strong> öffnen, anstatt einen neuen zu erstellen. Dieser Wert kann nicht zusammen mit <strong>adCreateOverwrite</strong>verwendet werden.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC-Entsprechung

Diese Konstanten haben keine ADO/WFC-Entsprechungen.

