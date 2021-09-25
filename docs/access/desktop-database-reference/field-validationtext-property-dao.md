---
title: Field.ValidationText-Eigenschaft (DAO)
TOCTitle: ValidationText Property
ms:assetid: 6d9ec790-a9d2-84d7-ccba-57d738491e36
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195540(v=office.15)
ms:contentKeyID: 48545494
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 747422ac1a3dc4ac51ed40611d1c4eee9560d07f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59581287"
---
# <a name="fieldvalidationtext-property-dao"></a>Field.ValidationText-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

Legt einen Wert fest, der den Text der Nachricht angibt, die von der Anwendung angezeigt wird, wenn der Wert eines **Field**-Objekts die von der **ValidationRule**-Eigenschaft festgelegte Gültigkeitsregel nicht unterstützt, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche). **String**-Wert mit Lese-/Schreibzugriff.

## <a name="syntax"></a>Syntax

*Ausdruck* . ValidationText

*Ausdruck* Eine Variable, die ein **Field**-Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Die Einstellung bzw. der Rückgabewert ist ein **String**-Wert des Texts, der angezeigt wird, wenn ein Benutzer versucht, einen ungültigen Wert für ein Feld einzugeben. Für ein Objekt, das noch nicht an eine Auflistung angehängt wurde, besteht Lese-/Schreibzugriff für diese Eigenschaft.

Bei einem **Field**-Objekt hängt die Verwendung der **ValidationText**-Eigenschaft von dem Objekt ab, das die **[Fields](fields-collection-dao.md)** -Auflistung enthält, an die das **Field**-Objekt angehängt wird, wie in der folgenden Tabelle angegeben.

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
<td><p>Lesen/Schreiben</p></td>
</tr>
</tbody>
</table>

