---
title: FürJedenDatensatz-Datenblock
TOCTitle: ForEachRecord Data Block
ms:assetid: be369196-230e-1f92-e36b-667048eef2be
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822743(v=office.15)
ms:contentKeyID: 48547455
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d814c4996f7779066a4dcc4cc9cb97d5e294855b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475777"
---
# <a name="foreachrecord-data-block"></a>FürJedenDatensatz-Datenblock


**Betrifft**: Access 2013 | Office 2013

Mit einem **FürJedenDatensatz** -Datenblock wird eine Reihe von Anweisungen für jeden Datensatz in einer Domäne wiederholt.


> [!NOTE]
> <P>[!HINWEIS] Der <STRONG>FürJedenDatensatz</STRONG> -Datenblock ist nur in Datenmakros verfügbar.</P>



## <a name="setting"></a>Einstellung

Die **FürJedenDatensatz** -Aktion kann mit den folgenden Argumenten verwendet werden.

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
<td><p><strong>In</strong></p></td>
<td><p>Ja</p></td>
<td><p>Eine Zeichenfolge zur Identifizierung von Datensätzen für den Betrieb die Domäne. Das <em>im</em> Argument kann der Name der Tabelle, einer select-Abfrage oder eine SQL-Anweisung enthalten.</p>

> [!NOTE]
> <P>Die angegebene Domäne darf keine Daten enthalten, die in einer verknüpften Tabelle oder einer ODBC-Datenquelle gespeichert sind.</P>


<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Where Condition</strong></p></td>
<td><p>Nein</p></td>
<td><p>Ein Zeichenfolgenausdruck, der zum Einschränken des Bereichs der Daten auf dem des <strong>FürJedenDatensatz</strong> -Datenblocks wird ausgeführt. Häufig wird beispielsweise Kriterien entspricht der WHERE-Klausel in einem SQL-Ausdruck ohne das Wort, in dem. Kriterien nicht angegeben, wirkt sich auf die gesamte Domäne angegeben, die durch das Argument <em>In</em> das <strong>FürJedenDatensatz</strong> -Datenblock. Jedes Feld, das im Argument Kriterien enthalten ist, muss auch ein Feld in <em>In</em>sein.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Alias</strong></p></td>
<td><p>Nein</p></td>
<td><p>Eine Zeichenfolge, die einen alternativen Namen für die Domäne, die durch das Argument <em>im</em> angegebenen bereitstellt. Häufig verwendet, um den Tabellennamen für nachfolgende Verweise zu verhindern, dass mögliche mehrdeutige Verweise zu verkürzen. Wenn <em>Alias</em> nicht angegeben ist, wird den Namen der Tabelle oder Abfrage als Alias verwendet werden.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Mit der **[BeendenFürJedenDatensatz](exitforeachrecord-macro-action.md)** -Aktion beenden Sie einen **FürJedenDatensatz** -Datenblock sofort.

