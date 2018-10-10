---
title: DatensatzLöschen-Makroaktion
TOCTitle: DeleteRecord Macro Action
ms:assetid: c656a72c-c037-76a5-dc07-f6eccb6590dd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823132(v=office.15)
ms:contentKeyID: 48547624
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 536369082a5abb94914d78d8bc64c5f9b45e8b0d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474877"
---
# <a name="deleterecord-macro-action"></a>DatensatzLöschen-Makroaktion

**Betrifft**: Access 2013 | Office 2013

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

