---
title: ForEachRecord-Datenblock
TOCTitle: ForEachRecord data block
ms:assetid: be369196-230e-1f92-e36b-667048eef2be
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822743(v=office.15)
ms:contentKeyID: 48547455
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d4c451d54b5cf7f2e5d85fed2d74bec4266d5d82
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602528"
---
# <a name="foreachrecord-data-block"></a>ForEachRecord-Datenblock

**Gilt für**: Access 2013, Office 2013

Ein **ForEachRecord-Datenblock** wiederholt eine Reihe von Anweisungen für jeden Datensatz in einer Domäne.

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
<td><p>Eine Zeichenfolge, die die Domäne von Datensätzen bezeichnet, für die eine Aktion ausgeführt werden soll. Das Argument <em>"In"</em> kann den Namen der Tabelle, eine Auswahlabfrage oder eine SQL Anweisung enthalten.</p><p><strong>HINWEIS:</strong>Die angegebene Domäne kann keine Daten enthalten, die in einer verknüpften Tabelle oder ODBC-Datenquelle gespeichert sind.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bedingung</strong></p></td>
<td><p>Nein</p></td>
<td><p>Ein Zeichenfolgenausdruck, der verwendet wird, um den Datenbereich einzuschränken, für den der <strong>ForEachRecord-Datenblock</strong> ausgeführt wird. Beispielsweise ist criteria oft äquivalent mit der WHERE-Klausel in einem SQL-Ausdruck, ohne das Wort WHERE. Wenn Kriterien nicht angegeben werden, wird der <strong>ForEachRecord-Datenblock</strong> für die gesamte durch das <em>Argument "In"</em> angegebene Domäne ausgeführt. Jedes Feld, das in Kriterien enthalten ist, muss auch ein Feld in <em>In</em>sein.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Alias</strong></p></td>
<td><p>Nein</p></td>
<td><p>Eine Zeichenfolge, die einen alternativen Namen für die durch das <em>Argument "In"</em> angegebene Domäne bereitstellt. Wird häufig verwendet, um den Tabellennamen für nachfolgende Verweise zu kürzen, um mögliche mehrdeutige Verweise zu verhindern. Wenn <em>alias</em> nicht angegeben ist, wird der Tabellen- oder Abfragename als Alias verwendet.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>HinwBemerkungeneise

Mit der **[BeendenFürJedenDatensatz](exitforeachrecord-macro-action.md)** -Aktion beenden Sie einen **FürJedenDatensatz** -Datenblock sofort.

