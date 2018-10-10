---
title: FieldEnum (Access PC-Datenbank-Referenz)
TOCTitle: FieldEnum
ms:assetid: fbd415c0-d6b4-278f-318b-98432c013634
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250289(v=office.15)
ms:contentKeyID: 48548876
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5efcdbd9da4214d7f2b78ffbcfb81fb13265087e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472822"
---
# <a name="fieldenum"></a>FieldEnum


**Betrifft**: Access 2013 | Office 2013

Gibt die speziellen Felder an, auf die in der [Fields](record-object-ado.md)-Auflistung eines [Record](fields-collection-ado.md)-Objekts verwiesen wird.

**Hinweise**

Diese Konstanten bieten eine "Verknüpfung" für den Zugriff auf spezielle Felder, die einem **Datensatz**zugeordnet. Das [Field](field-object-ado.md) -Objekt aus der **Fields** -Auflistung abrufen, und klicken Sie dann seinen Inhalt mit der [Value](value-property-ado.md) -Eigenschaft für das **Field** -Objekt zu erhalten.

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
<td><p><strong>adDefaultStream</strong></p></td>
<td><p>-1</p></td>
<td><p>Verweist auf das Feld, das einem <strong>Datensatz</strong>zugeordnete <a href="stream-object-ado.md">Stream</a> -Standardobjekt enthält.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecordURL</strong></p></td>
<td><p>-2</p></td>
<td><p>Verweist auf das Feld, enthält die absolute URL-Zeichenfolge für den aktuellen <strong>Datensatz</strong>.</p></td>
</tr>
</tbody>
</table>

