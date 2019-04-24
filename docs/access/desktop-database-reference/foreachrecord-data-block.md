---
title: Fürjedendatensatz-Datenblock
TOCTitle: ForEachRecord data block
ms:assetid: be369196-230e-1f92-e36b-667048eef2be
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822743(v=office.15)
ms:contentKeyID: 48547455
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 84ab685b946e390645027790e5b1402561527ab6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292328"
---
# <a name="foreachrecord-data-block"></a>Fürjedendatensatz-Datenblock

**Gilt für**: Access 2013, Office 2013

Ein **fürjedendatensatz** -Datenblock wiederholt eine Reihe von Anweisungen für jeden Datensatz in einer Domäne.

> [!NOTE]
> Der **FürJedenDatensatz**-Datenblock ist nur in Datenmakros verfügbar.

## <a name="setting"></a>Einstellung

Die **FürJedenDatensatz**-Aktion kann mit den folgenden Argumenten verwendet werden.

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
<td><p><strong>In</strong></p></td>
<td><p>Ja</p></td>
<td><p>Eine Zeichenfolge, die die Domäne von Datensätzen bezeichnet, für die eine Aktion ausgeführt werden soll. Das Argument <em>in</em> kann den Namen der Tabelle, eine Auswahlabfrage oder eine SQL-Anweisung enthalten.</p><p><strong>Hinweis</strong>: die angegebene Domäne kann Daten, die in einer verknüpften Tabelle oder ODBC-Datenquelle gespeichert sind, nicht aufnehmen.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bedingung</strong></p></td>
<td><p>Nein</p></td>
<td><p>Ein Zeichenfolgenausdruck, mit dem der Datenumfang eingeschränkt wird, auf dem der <strong>fürjedendatensatz</strong> -Datenblock ausgeführt wird. Beispielsweise ist criteria oft äquivalent mit der WHERE-Klausel in einem SQL-Ausdruck, ohne das Wort WHERE. Wenn criteria nicht angegeben wird, wird der <strong>fürjedendatensatz</strong> -Datenblock auf die gesamte Domäne angewendet, die durch das <em>in</em> -Argument angegeben wird. Jedes Feld, das in Criteria enthalten ist, muss auch ein Feld in <em>in</em>sein.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Alias</strong></p></td>
<td><p>Nein</p></td>
<td><p>Eine Zeichenfolge, die einen alternativen Namen für die durch das Argument <em>in</em> angegebene Domäne bereitstellt. Wird häufig verwendet, um den Tabellennamen für nachfolgende Verweise zu kürzen, um mögliche mehrdeutige Verweise zu verhindern. Wenn <em>Alias</em> nicht angegeben wird, wird der Tabellen-oder Abfragename als Alias verwendet.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Mit der **[BeendenFürJedenDatensatz](exitforeachrecord-macro-action.md)** -Aktion beenden Sie einen **FürJedenDatensatz** -Datenblock sofort.

