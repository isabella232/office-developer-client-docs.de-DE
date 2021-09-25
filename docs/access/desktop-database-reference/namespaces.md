---
title: Namespaces (Access-Desktopdatenbankreferenz)
TOCTitle: Namespaces
ms:assetid: e39f003c-3d16-1fae-48c5-304593c41f2f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250158(v=office.15)
ms:contentKeyID: 48548318
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f380ea60ea9d4676f1174884ef8331c0fef0462c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602108"
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
<td><p>Bezieht sich auf den &quot; XML-Data-Namespace, &quot; der die Elemente und Attribute enthält, die das Schema des aktuellen <strong>Recordset</strong>definieren.</p></td>
</tr>
<tr class="even">
<td><p>Dt</p></td>
<td><p>Die Spezifikation für die Datentypdefinitionen.</p></td>
</tr>
<tr class="odd">
<td><p>rs</p></td>
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



