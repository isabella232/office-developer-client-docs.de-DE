---
title: Field.SourceField-Eigenschaft (DAO)
TOCTitle: SourceField Property
ms:assetid: e5750d6c-4078-7bbb-9356-f9207c4e8028
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835953(v=office.15)
ms:contentKeyID: 48548360
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 6a07aa5d17fe6565ae81a1d35ff2cb093964f682
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59565387"
---
# <a name="fieldsourcefield-property-dao"></a>Field.SourceField-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

Gibt einen Wert zurück, der den Namen des Felds angibt, das die ursprüngliche Quelle der Daten für ein **Field**-Objekt ist. Schreibgeschützter **String**-Wert.

## <a name="syntax"></a>Syntax

*Ausdruck* . SourceField

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


Diese Eigenschaften geben die Namen des ursprünglichen Felds und der ursprünglichen Tabelle an, die einem **Field**-Objekt zugeordnet sind. Sie können mit diesen Eigenschaften beispielsweise die ursprüngliche Quelle der Daten in einem Abfragefeld ermitteln, dessen Name in keiner Beziehung zu dem Namen des Felds der zugrunde liegenden Tabelle steht.

