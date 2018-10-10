---
title: SQL-Abschnitt der Anpassungsdatei
TOCTitle: Customization File SQL Section
ms:assetid: 002c544f-fe1b-6aeb-ba9a-97b1e1159516
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248776(v=office.15)
ms:contentKeyID: 48542901
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 09be671ba15727e3612ade78c5b54af12b1d1c57
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472992"
---
# <a name="customization-file-sql-section"></a>SQL-Abschnitt der Anpassungsdatei


**Betrifft**: Access 2013 | Office 2013

Der **sql** -Abschnitt kann eine neue SQL-Zeichenfolge enthalten, durch die die Clientbefehlszeichenfolge ersetzt wird. Wenn im Abschnitt keine SQL-Zeichenfolge vorhanden ist, wird der Abschnitt ignoriert.

Die neue SQL-Zeichenfolge kann *parametrisiert* sein. Das heißt, die Parameter in der SQL-Zeichenfolge im **sql**-Abschnitt (die durch das Zeichen "?" angegeben werden) können durch entsprechende Argumente in einem *Bezeichner* in der Clientbefehlszeichenfolge (die durch eine durch Trennzeichen getrennte Liste in Klammern angegeben wird) ersetzt werden. Das Verhalten des Bezeichners und der Argumentliste entspricht dem eines Funktionsaufrufs.

Nehmen wir beispielsweise an die Clientbefehlszeichenfolge ist "CustomerByID(4)", die SQL-Abschnittsheader lautet \[SQL CustomerByID\] , und die neue Zeichenfolge der SQL-Abschnitt ist "Wählen Sie \* FROM Kunden WHERE CustomerID = ?". Den Ereignishandler zu generieren, die SQL-Abschnittsheader lautet \[SQL CustomerByID\] , und die neue Zeichenfolge der SQL-Abschnitt ist "Wählen Sie \* FROM Kunden WHERE CustomerID = ?". Der Ereignishandler generiert "Wählen Sie \* FROM Kunden WHERE CustomerID = 4" generiert und zum Abfragen der Datenquelle verwendet.

Wenn die neue SQL-Anweisung die leere Zeichenfolge ("") ist, wird der Abschnitt ignoriert.

Wenn die neue Zeichenfolge der SQL-Anweisung nicht gültig ist, schlägt die Ausführung der Anweisung fehl. Der Clientparameter wird effektiv ignoriert. Sie können auf diese Weise bewusst alle SQL-Clientbefehle "deaktivieren", indem Sie Folgendes angeben:

```sql 
 
[SQL default] 
SQL = " " 
```

## <a name="syntax"></a>Syntax

Ein Eintrag für eine SQL-Zeichenfolge hat folgendes Format:

**SQL = * SqlString***

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Teil</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>SQL</strong></p></td>
<td><p>Eine literale Zeichenfolge, durch die angegeben wird, dass es sich um einen Eintrag in einem SQL-Abschnitt handelt.</p></td>
</tr>
<tr class="even">
<td><p><strong><em>sqlString</em></strong></p></td>
<td><p>Eine SQL-Zeichenfolge, durch die die Clientzeichenfolge ersetzt wird.</p></td>
</tr>
</tbody>
</table>

