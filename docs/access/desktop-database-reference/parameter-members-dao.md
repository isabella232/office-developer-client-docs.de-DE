---
title: Parameter-Member (DAO)
TOCTitle: Parameter Members
ms:assetid: 38e19de8-5318-6077-13b1-10653069aaeb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192517(v=office.15)
ms:contentKeyID: 48544228
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e62125ee61598d6be125f9edb01f2aa4531043b9
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026071"
---
# <a name="parameter-members-dao"></a>Parameter-Member (DAO)

**Betrifft**: Access 2013, Office 2013

Ein Parameter-Objekt stellt einen Wert für eine Abfrage dar. Der Parameter wird einem QueryDef-Objekt zugeordnet, das aus einer Parameterabfrage erstellt wird.

## <a name="properties"></a>Eigenschaften

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="parameter-direction-property-dao.md"><ui>Direction</ui></a></strong></p></td>
<td><p><strong>Hinweis</strong>: für ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</p>
<p>Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der angibt, ob ein <strong><a href="parameter-object-dao.md">Parameter</a></strong> -Objekt einen Eingabeparameter und/oder einen Ausgabeparameter oder den Rückgabewert der Prozedur darstellt (gilt nur für ODBCDirect-Arbeitsbereiche).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="parameter-name-property-dao.md">Name</a></strong></p></td>
<td><p>Gibt den Namen des angegebenen Objekts zurück. Schreibgeschützter <strong>String</strong>-Wert.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="parameter-properties-property-dao.md">Eigenschaften</a></strong></p></td>
<td><p>Gibt die <strong><a href="properties-collection-dao.md">Properties</a></strong> -Auflistung des angegebenen Objekts zurück. Schreibgeschützt.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="parameter-type-property-dao.md">Typ</a></strong></p></td>
<td><p>Legt einen Wert fest, der den Funktions- oder Datentyp eines Objekts angibt, oder gibt einen solchen Wert zurück. Lese-/Schreibzugriff <strong>Integer</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="parameter-value-property-dao.md">Wert</a></strong></p></td>
<td><p>Legt den Wert eines Objekts fest oder gibt ihn zurück. <strong>Variant</strong>-Wert mit Lese-/Schreibzugriff.</p></td>
</tr>
</tbody>
</table>

