---
title: Field.SourceTable-Eigenschaft (DAO)
TOCTitle: SourceTable Property
ms:assetid: 9564ea1c-eafd-0b72-fd68-d88fcc3ea189
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197694(v=office.15)
ms:contentKeyID: 48546429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052900
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: c2ddec42d2e459b49a119adf7ac9c197da69b20f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577402"
---
# <a name="fieldsourcetable-property-dao"></a>Field.SourceTable-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

Gibt einen Wert zurück, der den Namen einer Tabelle enthält, bei der es sich um die ursprüngliche Datenquelle für ein **Field**-Objekt handelt. Schreibgeschützter **String**-Wert.

## <a name="syntax"></a>Syntax

*Ausdruck* . Sourcetable

*Ausdruck* Eine Variable, die ein **Field**-Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Bei einem **Field**-Objekt hängt die Verwendung der Eigenschaften **SourceField** und **SourceTable** vom Objekt ab, das die **Fields**-Auflistung enthält, der das **Field**-Objekt angefügt wird (siehe folgende Tabelle).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Zugehörigkeit zu Objekt</p></th>
<th><p>Nutzung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Index</strong></p></td>
<td><p>Nicht unterstützt</p></td>
</tr>
<tr class="even">
<td><p><strong>QueryDef</strong></p></td>
<td><p>Schreibgeschützt</p></td>
</tr>
<tr class="odd">
<td><p><strong>Recordset</strong></p></td>
<td><p>Schreibgeschützt</p></td>
</tr>
<tr class="even">
<td><p><strong>Relation</strong></p></td>
<td><p>Nicht unterstützt</p></td>
</tr>
<tr class="odd">
<td><p><strong>TableDef</strong></p></td>
<td><p>Schreibgeschützt</p></td>
</tr>
</tbody>
</table>


Diese Eigenschaften geben das ursprüngliche Feld und die Tabellennamen an, die einem **Field**-Objekt zugeordnet sind. Sie können mit diesen Eigenschaften z. B. die ursprüngliche Quelle der Daten in einem Abfragefeld ermitteln, dessen Name keinen Bezug zum Namen in der zugrunde liegenden Tabelle hat.


> [!NOTE]
> The **SourceTable** property will not return a meaningful table name if used on a **Field** object in the **Fields** collection of a table-type **Recordset** object.


