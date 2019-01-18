---
title: SetField-Makroaktion
TOCTitle: SetField macro action
ms:assetid: 66bd26e3-e8c3-b9a1-2f16-f29adc44a345
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195227(v=office.15)
ms:contentKeyID: 48545349
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4fbf7252729c7b376da6ebe67f59941c1caf924d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722319"
---
# <a name="setfield-macro-action"></a>SetField-Makroaktion

**Betrifft**: Access 2013, Office 2013

Mit der **FestlegenFeld** -Aktion können Sie einem Feld einen Wert zuweisen.

> [!NOTE]
> [!HINWEIS] Die **FestlegenFeld** -Aktion ist nur in Datenmakros verfügbar.

## <a name="setting"></a>Einstellung

Die **FestlegenFeld** -Aktion kann mit den in der folgenden Tabelle aufgeführten Argumenten verwendet werden.

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
<td><p>Ein Ausdruck, der angibt, den Wert in das Feld zugewiesen.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Die **FestlegenFeld** -Aktion kann nicht außerhalb eines **[DatensatzErstellen](createrecord-data-block.md)** - oder **[BearbeitenDatensatz](editrecord-data-block.md)** -Datenblocks verwendet werden.

