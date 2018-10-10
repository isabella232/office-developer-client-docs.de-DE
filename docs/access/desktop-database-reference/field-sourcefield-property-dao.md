---
title: Field.SourceField Property (DAO)
TOCTitle: SourceField Property
ms:assetid: e5750d6c-4078-7bbb-9356-f9207c4e8028
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835953(v=office.15)
ms:contentKeyID: 48548360
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 729a858ae39c6403d8ccefcacaa7bade754f0484
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474062"
---
# <a name="fieldsourcefield-property-dao"></a>Field.SourceField Property (DAO)


**Betrifft**: Access 2013 | Office 2013

Gibt einen Wert zurück, der den Namen des Felds angibt, das die ursprüngliche Quelle der Daten für ein **Field**-Objekt ist. Schreibgeschützter **String**-Wert.

## <a name="syntax"></a>Syntax

*Ausdruck* . SourceField

*Ausdruck* Eine Variable, die ein **Field** -Objekt darstellt.

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
<th><p>Verwendung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Index</strong></p></td>
<td><p>Nicht unterstützt</p></td>
</tr>
<tr class="even">
<td><p><strong>QueryDef-Objekt</strong></p></td>
<td><p>Schreibgeschützt.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Recordset</strong></p></td>
<td><p>Schreibgeschützt.</p></td>
</tr>
<tr class="even">
<td><p><strong>Beziehung</strong></p></td>
<td><p>Nicht unterstützt</p></td>
</tr>
<tr class="odd">
<td><p><strong>TableDef</strong></p></td>
<td><p>Schreibgeschützt.</p></td>
</tr>
</tbody>
</table>


Diese Eigenschaften geben die Namen des ursprünglichen Felds und der ursprünglichen Tabelle an, die einem **Field**-Objekt zugeordnet sind. Sie können mit diesen Eigenschaften beispielsweise die ursprüngliche Quelle der Daten in einem Abfragefeld ermitteln, dessen Name in keiner Beziehung zu dem Namen des Felds der zugrunde liegenden Tabelle steht.

