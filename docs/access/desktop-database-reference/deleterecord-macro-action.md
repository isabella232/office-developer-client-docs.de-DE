---
title: DeleteRecord-Makroaktion
TOCTitle: DeleteRecord macro action
ms:assetid: c656a72c-c037-76a5-dc07-f6eccb6590dd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823132(v=office.15)
ms:contentKeyID: 48547624
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8fb20068052972696b09ea0d2165b344e97ea922
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28725952"
---
# <a name="deleterecord-macro-action"></a>DeleteRecord-Makroaktion

**Betrifft**: Access 2013, Office 2013

Mit der **DatensatzLöschen** -Aktion können Sie einen Datensatz löschen.

## <a name="setting"></a>Einstellung

Der **DatensatzLöschen** -Datenblock kann mit den folgenden Argumenten verwendet werden.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Datensatzalias</strong></p></td>
<td><p>Eine Zeichenfolge, mit der der zu löschende Datensatz gekennzeichnet wird. Wenn das <em>Alias</em>-Argument nicht angegeben ist, wird der aktuelle Datensatz gelöscht.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Hinweise

Über die lokale Variable **LetztesErstellenDatensatzID** in einem **DatensatzErstellen** -Datenblock können Sie mit dem zuletzt erstellten Datensatz arbeiten. Beispielsweise verwenden Sie die folgende Syntax, um auf die zuletzt erstellte Datensatz zu verweisen:

`[LastCreateRecordIdentity]`

