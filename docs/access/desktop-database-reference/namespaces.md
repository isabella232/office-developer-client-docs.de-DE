---
title: Namespaces (Access PC-Datenbank-Referenz)
TOCTitle: Namespaces
ms:assetid: e39f003c-3d16-1fae-48c5-304593c41f2f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250158(v=office.15)
ms:contentKeyID: 48548318
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 905edba502fcc2994be6f6b8e50a7200b66a82b8
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703006"
---
# <a name="namespaces"></a>Namespaces

**Betrifft**: Access 2013, Office 2013

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
<td><p>Bezieht sich auf die &quot;XML-Daten&quot; Namespace, enthält die Elemente und Attribute, die das Schema des aktuellen <strong>Recordset-Objekt</strong>zu definieren.</p></td>
</tr>
<tr class="even">
<td><p>dt</p></td>
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


Ein Client sollten nicht auf diese Namespaces eigenen Tags hinzufügen, gemäß der Spezifikation. Beispielsweise sollte ein Client nicht als einen Namespace definieren "Urn: Schemas-Microsoft-Com:rowset", und klicken Sie dann schreiben Sie etwas wie "Rs: MyOwnTag." Weitere Informationen zu Namespaces finden Sie unter [XML-Namespaces](https://www.w3.org/tr/xml-names/).

> [!NOTE]
> [!HINWEIS] Die ID für das Schematag muss "RowsetSchema" lauten, und der Namespace, mit dem auf das Schema des aktuellen Rowsets verwiesen wird, muss auf "#RowsetSchema" zeigen.

Beachten Sie, dass Sie ein beliebiges Präfix für den Namespace verwenden können, also das Element rechts vom Doppelpunkt und links vom Gleichheitszeichen.

```vb 
 
xmlns:rs="urn:schemas-microsoft-com:rowset" 
```

Der Benutzer kann hierfür einen beliebigen Namen definieren, vorausgesetzt dieser Name wird im gesamten XML-Dokument einheitlich verwendet. ADO gibt "s", "rs", "dt", und "z" immer aus, aber diese Präfixnamen sind in der ladenden Komponente nicht hartcodiert.



