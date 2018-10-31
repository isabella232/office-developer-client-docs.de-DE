---
title: RecordCreateOptionsEnum
TOCTitle: RecordCreateOptionsEnum
ms:assetid: 153dc8ff-680c-1482-d386-4c4b33ffc589
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248917(v=office.15)
ms:contentKeyID: 48543405
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ff4b05f364b400c3741f690eae58d926aa9d2bad
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861514"
---
# <a name="recordcreateoptionsenum"></a>RecordCreateOptionsEnum


**Betrifft**: Access 2013 | Office 2013

Gibt an, ob ein vorhandener **Datensatz** geöffnet werden soll, oder ein neuer **Datensatz** für das [Open](open-method-ado-record.md) -Methode des [Record](record-object-ado.md) -Objekt erstellt. Die Werte können mit einem AND-Operator kombiniert werden.

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
<td><p>0 x 2000</p></td>
<td><p>Erstellt einen neuen <strong>Datensatz</strong> an dem Knoten gemäß der <em>Source</em> -Parameter zu einem vorhandenen <strong>Datensatz</strong>zu öffnen. Wenn die Quelle auf einem vorhandenen Knoten verweist, tritt ein Laufzeitfehler, es sei denn, <strong>AdCreateCollection</strong> mit <strong>AdOpenIfExists</strong> oder <strong>AdCreateOverwrite</strong>kombiniert ist.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCreateNonCollection</strong></p></td>
<td><p>0</p></td>
<td><p>Erstellt einen neuen <strong>Datensatz</strong> vom Typ <a href="recordtypeenum.md">AdSimpleRecord</a>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCreateOverwrite</strong></p></td>
<td><p>0x4000000</p></td>
<td><p>Ändert die Erstellung Flags <strong>AdCreateCollection</strong>, <strong>AdCreateNonCollection</strong>und <strong>AdCreateStructDoc</strong>. Wenn oder mit diesem Wert und einen der Werte für die Erstellung Kennzeichen verwendet wird, wenn die Quelle der URL auf einen vorhandenen Knoten oder <strong>Datensatz verweist</strong>, dann der vorhandene <strong>Datensatz</strong> überschrieben wird und an ihrer Stelle wird eine neue erstellt. Dieser Wert kann nicht zusammen mit <strong>AdOpenIfExists</strong>verwendet werden.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCreateStructDoc</strong></p></td>
<td><p>0x80000000</p></td>
<td><p>Erstellt einen neuen <strong>Datensatz</strong> vom Typ <a href="recordtypeenum.md">AdStructDoc</a>statt einen bereits vorhandenen <strong>Datensatz</strong>zu öffnen.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFailIfNotExists</strong></p></td>
<td><p>-1</p></td>
<td><p>Standardwert. Führt zu einem Laufzeitfehler, wenn <em>Quelle</em> auf einen nicht vorhandenen Knoten verweist.</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenIfExists</strong></p></td>
<td><p>0x2000000</p></td>
<td><p>Ändert die Erstellung Flags <strong>AdCreateCollection</strong>, <strong>AdCreateNonCollection</strong>und <strong>AdCreateStructDoc</strong>. Wenn oder mit diesem Wert und einen der Werte für die Erstellung Kennzeichen verwendet wird, falls die Quell-URL zu einer vorhandenen Knoten oder <strong>Record</strong> -Objekts verweist, und klicken Sie dann der Anbieter muss den vorhandenen <strong>Datensatz</strong> statt Erstellen einer neuen öffnen. Dieser Wert kann nicht zusammen mit <strong>AdCreateOverwrite</strong>verwendet werden.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC-Entsprechung

Diese Konstanten haben keine ADO/WFC-Entsprechungen.

