---
title: Gruppieren-Makroanweisung
TOCTitle: Group macro statement
ms:assetid: 42aa4afa-ab5d-9dcc-2182-786f025e316d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192918(v=office.15)
ms:contentKeyID: 48544481
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 4c2504e30445b78d04e55bd5e8cab0ed0fd551eb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59581147"
---
# <a name="group-macro-statement"></a>Gruppieren-Makroanweisung


**Gilt für**: Access 2013, Office 2013

Mit der **Group-Anweisung** können Sie einen Aktionsblock innerhalb eines Makros angeben, den Sie erweitern oder reduzieren können.

## <a name="setting"></a>Einstellung

Die **Gruppieren**-Aktion kann mit den folgenden Argumenten verwendet werden.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument</p></th>
<th><p>Erforderlich</p></th>
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


## <a name="remarks"></a>HinwBemerkungeneise

Mit der **Gruppieren** -Anweisung wird kein Bereich eines Makros definiert, der einzeln ausgeführt werden kann. Verwenden Sie die **[Untermakro](submacro-macro-statement.md)** -Anweisung im **Makro-Designer**-Fenster, um eine Reihe von Aktionen zu definieren, die einzeln ausgeführt werden können.

