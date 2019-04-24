---
title: Field2. ValidationText-Eigenschaft (DAO)
TOCTitle: ValidationText Property
ms:assetid: 6128f66c-3891-ae4d-d12d-354a79a9c05e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194867(v=office.15)
ms:contentKeyID: 48545202
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4d58cb6bd32bd46b0a6bcec40ff68cdc52eebc31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292622"
---
# <a name="field2validationtext-property-dao"></a>Field2. ValidationText-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der den Text oder die Meldung angibt, mit der die Anwendung anzeigt, dass der Wert eines **Field2**-Objekts nicht der in der Einstellung der **ValidationRule**-Eigenschaft angegebenen Gütigkeitsregel entspricht (gilt nur für Microsoft Access-Arbeitsbereiche). **String**-Wert mit Lese-/Schreibzugriff.

## <a name="syntax"></a>Syntax

*Ausdruck* . ValidationText

*Ausdruck* Eine Variable, die ein **Field2** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Die Einstellung oder der Rückgabewert ist vom Datentyp **String** und gibt den Text an, der angezeigt wird, wenn ein Benutzer einen ungültigen Wert für ein Feld einzugeben versucht. Bei Objekten, die noch keiner Auflistung angefügt sind, besteht für diese Eigenschaft Lese-/Schreibzugriff.

Bei einem **Field2**-Objekt hängt die Verwendung der **ValidationText**-Eigenschaft vom Objekt ab, das die **[Fields](fields-collection-dao.md)** -Auflistung enthält, der das **Field2**-Objekt angefügt wird (siehe folgende Tabelle).

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
<td><p><strong>QueryDef</strong></p></td>
<td><p>Schreibgeschützt</p></td>
</tr>
<tr class="odd">
<td><p><strong>Recordset</strong></p></td>
<td><p>Schreibgeschützt</p></td>
</tr>
<tr class="even">
<td><p><strong>Beziehung</strong></p></td>
<td><p>Nicht unterstützt</p></td>
</tr>
<tr class="odd">
<td><p><strong>TableDef</strong></p></td>
<td><p>Lesen/Schreiben</p></td>
</tr>
</tbody>
</table>

