---
title: Anpassungsdatei – SQL-Abschnitt
TOCTitle: Customization File SQL section
ms:assetid: 002c544f-fe1b-6aeb-ba9a-97b1e1159516
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248776(v=office.15)
ms:contentKeyID: 48542901
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 629c7a5601f35253f034bb9b488aef3c8a369fc5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622480"
---
# <a name="customization-file-sql-section"></a>Anpassungsdatei – SQL-Abschnitt


**Gilt für**: Access 2013, Office 2013

Der **sql** -Abschnitt kann eine neue SQL-Zeichenfolge enthalten, durch die die Clientbefehlszeichenfolge ersetzt wird. Wenn im Abschnitt keine SQL-Zeichenfolge vorhanden ist, wird der Abschnitt ignoriert.

Die neue SQL-Zeichenfolge kann *parametrisiert* sein. Das heißt, die Parameter in der SQL-Zeichenfolge im **sql**-Abschnitt (die durch das Zeichen "?" angegeben werden) können durch entsprechende Argumente in einem *Bezeichner* in der Clientbefehlszeichenfolge (die durch eine durch Trennzeichen getrennte Liste in Klammern angegeben wird) ersetzt werden. Das Verhalten des Bezeichners und der Argumentliste entspricht dem eines Funktionsaufrufs.

Nehmen wir beispielsweise an, dass die Clientbefehlszeichenfolge "CustomerByID(4)" lautet, der SQL Abschnittsheader \[ SQL CustomerByID ist und die neue SQL \] Abschnittszeichenfolge "SELECT \* FROM Customers WHERE CustomerID = ?". Der Handler generiert , der SQL Abschnittsheader \[ SQL CustomerByID \] ist, und die neue SQL Abschnittszeichenfolge lautet "SELECT \* FROM Customers WHERE CustomerID = ?". Der Handler generiert "SELECT \* FROM Customers WHERE CustomerID = 4" und verwendet diese Zeichenfolge, um die Datenquelle abfragt.

Wenn die neue SQL-Anweisung die leere Zeichenfolge ("") ist, wird der Abschnitt ignoriert.

Wenn die neue Zeichenfolge der SQL-Anweisung nicht gültig ist, schlägt die Ausführung der Anweisung fehl. Der Clientparameter wird effektiv ignoriert. Sie können auf diese Weise bewusst alle SQL-Clientbefehle "deaktivieren", indem Sie Folgendes angeben:

```sql 
 
[SQL default] 
SQL = " " 
```

## <a name="syntax"></a>Syntax

Ein Eintrag für eine SQL-Zeichenfolge hat folgendes Format:

**SQL=*sqlString***

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
<td><p><strong><em>Sqlstring</em></strong></p></td>
<td><p>Eine SQL-Zeichenfolge, durch die die Clientzeichenfolge ersetzt wird.</p></td>
</tr>
</tbody>
</table>

