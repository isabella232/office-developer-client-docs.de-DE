---
title: SetField-Makroaktion
TOCTitle: SetField macro action
ms:assetid: 66bd26e3-e8c3-b9a1-2f16-f29adc44a345
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195227(v=office.15)
ms:contentKeyID: 48545349
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 693a81a26aea22e934046c221ade55810287da95
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572690"
---
# <a name="setfield-macro-action"></a>SetField-Makroaktion

**Gilt für**: Access 2013, Office 2013

Mit der **FestlegenFeld** -Aktion können Sie einem Feld einen Wert zuweisen.

> [!NOTE]
> Die **FestlegenFeld**-Aktion ist nur in Datenmakros verfügbar.

## <a name="setting"></a>Einstellung

Die **FestlegenFeld**-Aktion kann mit den in der folgenden Tabelle aufgeführten Argumenten verwendet werden.

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
<td><p><strong>Name</strong></p></td>
<td><p>Eine Zeichenfolge, die das Feld bezeichnet.</p></td>
</tr>
<tr class="even">
<td><p><strong>Wert</strong></p></td>
<td><p>Ein Ausdruck, der den Wert angibt, der dem Feld zugewiesen werden soll.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>HinwBemerkungeneise

Die **FestlegenFeld** -Aktion kann nicht außerhalb eines **[DatensatzErstellen](createrecord-data-block.md)** - oder **[BearbeitenDatensatz](editrecord-data-block.md)** -Datenblocks verwendet werden.

