---
title: Index.Required Property (DAO)
TOCTitle: Required Property
ms:assetid: ec8fafc4-8155-c48e-b3c8-2d9be425175a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836310(v=office.15)
ms:contentKeyID: 48548518
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052963
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 0797ed5f930d4475d03f492109c977f8494591ce
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475165"
---
# <a name="indexrequired-property-dao"></a>Index.Required Property (DAO)


**Betrifft**: Access 2013 | Office 2013

Gibt einen Wert zurück, der angibt, ob ein **[Field](field-object-dao.md)** -Objekt einen Nicht-Null-Wert erfordert, oder legt den betreffenden Wert fest.

## <a name="syntax"></a>Syntax

*Ausdruck* . Erforderlich

*Ausdruck* Eine Variable, die ein **Index** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen


> [!NOTE]
> <P>[!HINWEIS] Wenn Sie diese Eigenschaft sowohl für ein <STRONG>Index</STRONG>- als auch für ein <STRONG>Field</STRONG>-Objekt festlegen können, sollten Sie sie für das <STRONG>Field</STRONG>-Objekt festlegen. Die Gültigkeit des Werts dieser Eigenschaft wird zuerst für das <STRONG>Field</STRONG>-Objekt und erst danach für das <STRONG>Index</STRONG>-Objekt überprüft.</P>



Die Verfügbarkeit der **Required**-Eigenschaft hängt von dem Objekt ab, das die [Fields](fields-collection-dao.md)-Auflistung enthält, wie in der folgenden Tabelle dargestellt.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Zugehörigkeit der Fields-Auflistung</p></th>
<th><p>Required-Wert</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Index</strong>-Objekt</p></td>
<td><p>Nicht unterstützt</p></td>
</tr>
<tr class="even">
<td><p><strong>QueryDef</strong>-Objekt</p></td>
<td><p>Schreibgeschützt.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Recordset</strong>-Objekt</p></td>
<td><p>Schreibgeschützt.</p></td>
</tr>
<tr class="even">
<td><p><strong>Relation</strong>-Objekt</p></td>
<td><p>Nicht unterstützt</p></td>
</tr>
<tr class="odd">
<td><p><strong>TableDef</strong>-Objekt</p></td>
<td><p>Lese-/Schreibzugriff</p></td>
</tr>
</tbody>
</table>

