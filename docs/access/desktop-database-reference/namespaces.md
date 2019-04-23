---
title: Namespaces (Access Desktop Database Reference)
TOCTitle: Namespaces
ms:assetid: e39f003c-3d16-1fae-48c5-304593c41f2f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250158(v=office.15)
ms:contentKeyID: 48548318
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 905edba502fcc2994be6f6b8e50a7200b66a82b8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288625"
---
# <a name="namespaces"></a>Namespaces

**Gilt für**: Access 2013, Office 2013

Für das XML-Speicherformat in ADO werden die folgenden vier Namespaces verwendet.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Präfix</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>s</p></td>
<td><p>BeZieht sich &quot;auf den XML&quot; -Data-Namespace, der die Elemente und Attribute enthält, die das Schema des aktuellen <strong>Recordset-Objekts</strong>definieren.</p></td>
</tr>
<tr class="even">
<td><p>dt</p></td>
<td><p>Die Spezifikation für die Datentypdefinitionen.</p></td>
</tr>
<tr class="odd">
<td><p>RS</p></td>
<td><p>Der Namespace, der die Elemente und Attribute speziell für die ADO-Eigenschaften und -Attribute des <strong>Recordset</strong>-Objekts enthält.</p></td>
</tr>
<tr class="even">
<td><p>z</p></td>
<td><p>Das Schema des aktuellen Rowsets.</p></td>
</tr>
</tbody>
</table>


A client should not add its own tags to these namespaces, as defined by the specification. For example, a client should not define a namespace as "urn:schemas-microsoft-com:rowset" and then write out something such as "rs:MyOwnTag." To learn more about namespaces, see [XML Namespaces](https://www.w3.org/tr/xml-names/).

> [!NOTE]
> [!HINWEIS] Die ID für das Schematag muss "RowsetSchema" lauten, und der Namespace, mit dem auf das Schema des aktuellen Rowsets verwiesen wird, muss auf "#RowsetSchema" zeigen.

Beachten Sie, dass Sie ein beliebiges Präfix für den Namespace verwenden können, also das Element rechts vom Doppelpunkt und links vom Gleichheitszeichen.

```vb 
 
xmlns:rs="urn:schemas-microsoft-com:rowset" 
```

Der Benutzer kann hierfür einen beliebigen Namen definieren, vorausgesetzt dieser Name wird im gesamten XML-Dokument einheitlich verwendet. ADO gibt "s", "rs", "dt", und "z" immer aus, aber diese Präfixnamen sind in der ladenden Komponente nicht hartcodiert.



