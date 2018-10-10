---
title: Gruppieren-Makroanweisung
TOCTitle: Group Macro Statement
ms:assetid: 42aa4afa-ab5d-9dcc-2182-786f025e316d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192918(v=office.15)
ms:contentKeyID: 48544481
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 189744d228db0dadd3260ce77457daf8724828f8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474135"
---
# <a name="group-macro-statement"></a>Gruppieren-Makroanweisung


**Betrifft**: Access 2013 | Office 2013

Die **Group** -Anweisung können Sie einen Block von Aktionen innerhalb eines Makros angeben, die Sie erweitern oder reduzieren können.

## <a name="setting"></a>Einstellung

Die **Gruppieren** -Aktion kann mit den folgenden Argumenten verwendet werden.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument</p></th>
<th><p>Eingabe erforderlich</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Beschreibung</strong></p></td>
<td><p>Nein</p></td>
<td><p>Eine Zeichenfolge, die nach dem Reduzieren als Titel einer Gruppe angezeigt wird.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Mit der **Gruppieren** -Anweisung wird kein Bereich eines Makros definiert, der einzeln ausgeführt werden kann. Verwenden Sie die **[Untermakro](submacro-macro-statement.md)** -Anweisung im **Makro-Designer**-Fenster, um eine Reihe von Aktionen zu definieren, die einzeln ausgeführt werden können.

