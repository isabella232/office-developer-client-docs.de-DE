---
title: Gruppieren-Makroanweisung
TOCTitle: Group macro statement
ms:assetid: 42aa4afa-ab5d-9dcc-2182-786f025e316d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192918(v=office.15)
ms:contentKeyID: 48544481
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2dc25621a49d8fd23078a926d6ec6c5de54e54d9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292111"
---
# <a name="group-macro-statement"></a>Gruppieren-Makroanweisung


**Gilt für**: Access 2013, Office 2013

Mit der **Group** -Anweisung können Sie einen Block von Aktionen innerhalb eines Makros angeben, den Sie erweitern oder reduzieren möchten.

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


## <a name="remarks"></a>Bemerkungen

Mit der **Gruppieren** -Anweisung wird kein Bereich eines Makros definiert, der einzeln ausgeführt werden kann. Verwenden Sie die **[Untermakro](submacro-macro-statement.md)** -Anweisung im **Makro-Designer**-Fenster, um eine Reihe von Aktionen zu definieren, die einzeln ausgeführt werden können.

