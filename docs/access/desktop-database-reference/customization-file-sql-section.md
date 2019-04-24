---
title: Anpassungsdatei – SQL-Abschnitt
TOCTitle: Customization File SQL section
ms:assetid: 002c544f-fe1b-6aeb-ba9a-97b1e1159516
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248776(v=office.15)
ms:contentKeyID: 48542901
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8ae259589cc8d4945068901c59105425599edc64
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295135"
---
# <a name="customization-file-sql-section"></a><span data-ttu-id="fa4b0-102">Anpassungsdatei – SQL-Abschnitt</span><span class="sxs-lookup"><span data-stu-id="fa4b0-102">Customization File SQL section</span></span>


<span data-ttu-id="fa4b0-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fa4b0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fa4b0-p101">Der **sql** -Abschnitt kann eine neue SQL-Zeichenfolge enthalten, durch die die Clientbefehlszeichenfolge ersetzt wird. Wenn im Abschnitt keine SQL-Zeichenfolge vorhanden ist, wird der Abschnitt ignoriert.</span><span class="sxs-lookup"><span data-stu-id="fa4b0-p101">The **sql** section can contain a new SQL string that replaces the client command string. If there is no SQL string in the section, the section will be ignored.</span></span>

<span data-ttu-id="fa4b0-p102">Die neue SQL-Zeichenfolge kann *parametrisiert* sein. Das heißt, die Parameter in der SQL-Zeichenfolge im **sql**-Abschnitt (die durch das Zeichen "?" angegeben werden) können durch entsprechende Argumente in einem *Bezeichner* in der Clientbefehlszeichenfolge (die durch eine durch Trennzeichen getrennte Liste in Klammern angegeben wird) ersetzt werden. Das Verhalten des Bezeichners und der Argumentliste entspricht dem eines Funktionsaufrufs.</span><span class="sxs-lookup"><span data-stu-id="fa4b0-p102">The new SQL string may be *parameterized*. That is, parameters in the **sql** section SQL string (designated by the '?' character) can be replaced by corresponding arguments in an *identifier* in the client command string (designated by a comma-delimited list in parentheses). The identifier and argument list behave like a function call.</span></span>

<span data-ttu-id="fa4b0-109">Nehmen wir beispielsweise an, dass die Clientbefehlszeichenfolge "CustomerByID (4)" lautet, der SQL \[-Abschnitts\] Header SQL CUSTOMERBYID und die neue SQL-Abschnitts Zeichenfolge \* "SELECT FROM Customers WHERE CustomerID = ?" ist.</span><span class="sxs-lookup"><span data-stu-id="fa4b0-109">For example, assume the client command string is "CustomerByID(4)" , the SQL section header is \[SQL CustomerByID\] , and the new SQL section string is "SELECT \* FROM Customers WHERE CustomerID = ?".</span></span> <span data-ttu-id="fa4b0-110">Der Handler generiert, der SQL-Abschnittsheader ist \[SQL CustomerByID\] , und die neue SQL-Abschnitts Zeichenfolge lautet " \* SELECT FROM Customers WHERE CustomerID = ?".</span><span class="sxs-lookup"><span data-stu-id="fa4b0-110">The Handler will generate , the SQL section header is \[SQL CustomerByID\] , and the new SQL section string is "SELECT \* FROM Customers WHERE CustomerID = ?".</span></span> <span data-ttu-id="fa4b0-111">Der Handler generiert "SELECT \* from Customers WHERE CustomerID = 4" und verwendet diese Zeichenfolge zum Abfragen der Datenquelle.</span><span class="sxs-lookup"><span data-stu-id="fa4b0-111">The Handler will generate "SELECT \* FROM Customers WHERE CustomerID = 4" and use that string to query the data source.</span></span>

<span data-ttu-id="fa4b0-112">Wenn die neue SQL-Anweisung die leere Zeichenfolge ("") ist, wird der Abschnitt ignoriert.</span><span class="sxs-lookup"><span data-stu-id="fa4b0-112">If the new SQL statement is the null string (""), then the section is ignored.</span></span>

<span data-ttu-id="fa4b0-p104">Wenn die neue Zeichenfolge der SQL-Anweisung nicht gültig ist, schlägt die Ausführung der Anweisung fehl. Der Clientparameter wird effektiv ignoriert. Sie können auf diese Weise bewusst alle SQL-Clientbefehle "deaktivieren", indem Sie Folgendes angeben:</span><span class="sxs-lookup"><span data-stu-id="fa4b0-p104">If the new SQL statement string is not valid, then the execution of the statement will fail. The client parameter is effectively ignored. You can do this intentionally to "turn off" all client SQL commands by specifying:</span></span>

```sql 
 
[SQL default] 
SQL = " " 
```

## <a name="syntax"></a><span data-ttu-id="fa4b0-116">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa4b0-116">Syntax</span></span>

<span data-ttu-id="fa4b0-117">Ein Eintrag für eine SQL-Zeichenfolge hat folgendes Format:</span><span class="sxs-lookup"><span data-stu-id="fa4b0-117">A replacement SQL string entry is of the form:</span></span>

<span data-ttu-id="fa4b0-118">**SQL = \* sqlString**\*</span><span class="sxs-lookup"><span data-stu-id="fa4b0-118">**SQL=\*sqlString**\*</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fa4b0-119">Teil</span><span class="sxs-lookup"><span data-stu-id="fa4b0-119">Part</span></span></p></th>
<th><p><span data-ttu-id="fa4b0-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fa4b0-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fa4b0-121"><strong>SQL</strong></span><span class="sxs-lookup"><span data-stu-id="fa4b0-121"><strong>SQL</strong></span></span></p></td>
<td><p><span data-ttu-id="fa4b0-122">Eine literale Zeichenfolge, durch die angegeben wird, dass es sich um einen Eintrag in einem SQL-Abschnitt handelt.</span><span class="sxs-lookup"><span data-stu-id="fa4b0-122">A literal string that indicates this is an SQL section entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa4b0-123"><strong><em>sqlString</em></strong></span><span class="sxs-lookup"><span data-stu-id="fa4b0-123"><strong><em>sqlString</em></strong></span></span></p></td>
<td><p><span data-ttu-id="fa4b0-124">Eine SQL-Zeichenfolge, durch die die Clientzeichenfolge ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="fa4b0-124">An SQL string that replaces the client string.</span></span></p></td>
</tr>
</tbody>
</table>

