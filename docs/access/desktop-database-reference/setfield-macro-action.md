---
title: FestlegenFeld-Makroaktion
TOCTitle: SetField Macro Action
ms:assetid: 66bd26e3-e8c3-b9a1-2f16-f29adc44a345
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195227(v=office.15)
ms:contentKeyID: 48545349
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1be405402c5f410c892c2dd8904133e09039351a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869505"
---
# <a name="setfield-macro-action"></a>FestlegenFeld-Makroaktion


**Betrifft**: Access 2013, Office 2013

Mit der **FestlegenFeld** -Aktion können Sie einem Feld einen Wert zuweisen.


> [!NOTE]
> <P>[!HINWEIS] Die <STRONG>FestlegenFeld</STRONG> -Aktion ist nur in Datenmakros verfügbar.</P>



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

