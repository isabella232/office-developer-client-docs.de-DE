---
title: FieldEnum (Access Desktop Database Reference)
TOCTitle: FieldEnum
ms:assetid: fbd415c0-d6b4-278f-318b-98432c013634
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250289(v=office.15)
ms:contentKeyID: 48548876
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e42dcfe63194364986e5b235c59b011231307a7c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292594"
---
# <a name="fieldenum"></a>FieldEnum

**Gilt für**: Access 2013, Office 2013

Gibt die speziellen Felder an, auf die in der [Fields](fields-collection-ado.md)-Auflistung eines [Record](record-object-ado.md)-Objekts verwiesen wird.

## <a name="remarks"></a>Bemerkungen

These constants provide a "shortcut" to accessing special fields associated with a **Record**. Retrieve the [Field](field-object-ado.md) object from the **Fields** collection, and then obtain its contents with the **Field** object's [Value](value-property-ado.md) property.

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
<td><p><strong>adDefaultStream</strong></p></td>
<td><p>-1</p></td>
<td><p>Verweist auf das Feld mit dem <a href="stream-object-ado.md">Stream</a> -Standardobjekt, das einem <strong>Datensatz</strong>zugeordnet ist.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecordURL</strong></p></td>
<td><p>-2</p></td>
<td><p>Verweist auf das Feld, das die absolute URL-Zeichenfolge für den aktuellen Datensatz enthält.</p></td>
</tr>
</tbody>
</table>

