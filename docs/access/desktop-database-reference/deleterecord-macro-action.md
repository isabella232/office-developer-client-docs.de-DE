---
title: DeleteRecord-Makroaktion
TOCTitle: DeleteRecord macro action
ms:assetid: c656a72c-c037-76a5-dc07-f6eccb6590dd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823132(v=office.15)
ms:contentKeyID: 48547624
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: b6190a4fe8395901304202019b2ac0891f36fada
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577430"
---
# <a name="deleterecord-macro-action"></a>DeleteRecord-Makroaktion

**Gilt für**: Access 2013, Office 2013

Mit der **DatensatzLöschen**-Aktion können Sie einen Datensatz löschen.

## <a name="setting"></a>Einstellung

Der **DatensatzErstellen**-Datenblock kann mit den folgenden Argumenten verwendet werden.

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

## <a name="remarks"></a>HinwBemerkungeneise

Über die lokale Variable **LetztesErstellenDatensatzID** in einem **DatensatzErstellen** -Datenblock können Sie mit dem zuletzt erstellten Datensatz arbeiten. Verwenden Sie beispielsweise die folgende Syntax, um auf den zuletzt erstellten Datensatz zu verweisen:

`[LastCreateRecordIdentity]`

