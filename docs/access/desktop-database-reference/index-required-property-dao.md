---
title: Index.Required-Eigenschaft (DAO)
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
ms.localizationpriority: medium
ms.openlocfilehash: 02cf71cbd5c1692fb68829902191922536061e43
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626379"
---
# <a name="indexrequired-property-dao"></a>Index.Required-Eigenschaft (DAO)

**Gilt für**: Access 2013, Office 2013

Gibt einen Wert zurück, der angibt, ob für ein **[Field](field-object-dao.md)** -Objekt ein Nicht-Null-Wert erforderlich ist, oder legt den betreffenden Wert fest.

## <a name="syntax"></a>Syntax

*Ausdruck* . Erforderlich

*Ausdruck* Eine Variable, die ein **Index-Objekt** darstellt.

## <a name="remarks"></a>Bemerkungen

> [!NOTE]
> [!HINWEIS] Wenn Sie diese Eigenschaft sowohl für ein **Index**- als auch für ein **Field**-Objekt festlegen können, sollten Sie sie für das **Field**-Objekt festlegen. Die Gültigkeit des Werts dieser Eigenschaft wird zuerst für das **Field**-Objekt und erst danach für das **Index**-Objekt überprüft.

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
<td><p>Schreibgeschützt</p></td>
</tr>
<tr class="odd">
<td><p><strong>Recordset</strong>-Objekt</p></td>
<td><p>Schreibgeschützt</p></td>
</tr>
<tr class="even">
<td><p><strong>Relation</strong>-Objekt</p></td>
<td><p>Nicht unterstützt</p></td>
</tr>
<tr class="odd">
<td><p><strong>TableDef</strong>-Objekt</p></td>
<td><p>Lesen/Schreiben</p></td>
</tr>
</tbody>
</table>

