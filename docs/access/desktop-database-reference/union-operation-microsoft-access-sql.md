---
title: UNION-Operation (Microsoft Access SQL)
TOCTitle: UNION operation (Microsoft Access SQL)
ms:assetid: a5139921-51e5-7d96-74e3-11c3fd5f7eaa
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821131(v=office.15)
ms:contentKeyID: 48546826
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277582
dev_langs:
- sql
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: f842e662f2576d8aab5f3857877f45e380d3d3b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314700"
---
# <a name="union-operation-microsoft-access-sql"></a><span data-ttu-id="fa254-102">UNION-Operation (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="fa254-102">UNION Operation (Microsoft Access SQL)</span></span>

<span data-ttu-id="fa254-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fa254-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fa254-104">Erstellt eine Union-Abfrage, in der die Ergebnisse von mindestens zwei unabhängigen Abfragen oder Tabellen miteinander kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="fa254-104">Creates a union query, which combines the results of two or more independent queries or tables.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa254-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa254-105">Syntax</span></span>

<span data-ttu-id="fa254-106">\[TABLE\] *query1* UNION \[ALL\] \[TABLE\] *query2* \[UNION \[ALL\] \[TABLE\] *queryn* \[ …</span><span class="sxs-lookup"><span data-stu-id="fa254-106">\[TABLE\] *query1* UNION \[ALL\] \[TABLE\] *query2* \[UNION \[ALL\] \[TABLE\] *queryn* \[ …</span></span> <span data-ttu-id="fa254-107">\]\]</span><span class="sxs-lookup"><span data-stu-id="fa254-107"></span></span>

<span data-ttu-id="fa254-108">Der UNION-Vorgang besteht aus den folgenden Teilen:</span><span class="sxs-lookup"><span data-stu-id="fa254-108">The UNION operation has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fa254-109">Part</span><span class="sxs-lookup"><span data-stu-id="fa254-109">Part</span></span></p></th>
<th><p><span data-ttu-id="fa254-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fa254-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fa254-111"><em>Abfrage1-n</em></span><span class="sxs-lookup"><span data-stu-id="fa254-111"><em>query1-n</em></span></span></p></td>
<td><p><span data-ttu-id="fa254-112">Eine SELECT-Anweisung, der Name einer gespeicherten Abfrage oder der Name einer gespeicherten Tabelle, der das Schlüsselwort TABLE vorangestellt ist.</span><span class="sxs-lookup"><span data-stu-id="fa254-112">A SELECT statement, the name of a stored query, or the name of a stored table preceded by the TABLE keyword.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="fa254-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fa254-113">Remarks</span></span>

<span data-ttu-id="fa254-p102">Sie können die Ergebnisse von mindestens zwei Abfragen, Tabellen und SELECT-Anweisungen in einer beliebigen Kombination in einem einzigen UNION-Vorgang zusammenführen. Im folgenden Beispiel werden die vorhandene Tabelle "Neue Konten" und eine SELECT-Anweisung zusammengeführt:</span><span class="sxs-lookup"><span data-stu-id="fa254-p102">You can merge the results of two or more queries, tables, and SELECT statements, in any combination, in a single UNION operation. The following example merges an existing table named New Accounts and a SELECT statement:</span></span>

```sql
TABLE [New Accounts] UNION ALL 
SELECT * 
FROM Customers 
WHERE OrderAmount > 1000;
```

<span data-ttu-id="fa254-p103">Standardmäßig werden bei Verwendung einer UNION-Operation keine duplizierten Datensätze zurückgegeben. Sie können jedoch mithilfe des Prädikats [ALL](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql) sicherstellen, dass alle Datensätze zurückgegeben werden. Außerdem wird dadurch die Ausführung der Abfrage beschleunigt.</span><span class="sxs-lookup"><span data-stu-id="fa254-p103">By default, no duplicate records are returned when you use a UNION operation; however, you can include the [ALL](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql) predicate to ensure that all records are returned. This also makes the query run faster.</span></span>

<span data-ttu-id="fa254-118">Alle Abfragen in einer UNION-Operation müssen dieselbe Anzahl von Feldern anfordern. Doch die Felder müssen nicht dieselbe Größe oder denselben Datentyp besitzen.</span><span class="sxs-lookup"><span data-stu-id="fa254-118">All queries in a UNION operation must request the same number of fields; however, the fields do not have to be of the same size or data type.</span></span>

<span data-ttu-id="fa254-p104">Verwenden Sie Aliase nur in der ersten SELECT-Anweisung, weil sie in anderen Anweisungen ignoriert werden. Verweisen Sie in der ORDER BY-Klausel so auf die Felder, wie sie in der ersten SELECT-Anweisung bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="fa254-p104">Use aliases only in the first SELECT statement because they are ignored in any others. In the ORDER BY clause, refer to fields by what they are called in the first SELECT statement.</span></span>

> [!NOTE]
> - <span data-ttu-id="fa254-121">Sie können in jedem *Abfrage*argument eine [GROUP BY](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/group-by-clause-microsoft-access-sql)- oder eine [HAVING](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/having-clause-microsoft-access-sql)-Klausel verwenden, um die zurückgegebenen Daten zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="fa254-121">You can use a [GROUP BY](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/group-by-clause-microsoft-access-sql) or [HAVING](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/having-clause-microsoft-access-sql) clause in each *query* argument to group the returned data.</span></span>
> - <span data-ttu-id="fa254-122">Sie können am Ende des letzten *Abfrage*arguments eine [ORDER BY](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/order-by-clause-microsoft-access-sql)-Klausel verwenden, um die zurückgegebenen Daten in einer bestimmten Reihenfolge anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="fa254-122">You can use an [ORDER BY](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/order-by-clause-microsoft-access-sql) clause at the end of the last *query* argument to display the returned data in a specified order.</span></span>

## <a name="example"></a><span data-ttu-id="fa254-123">Beispiel</span><span class="sxs-lookup"><span data-stu-id="fa254-123">Example</span></span>

<span data-ttu-id="fa254-124">In diesem Beispiel werden die Namen und Städte aller Händler und Kunden in Brasilien abgerufen.</span><span class="sxs-lookup"><span data-stu-id="fa254-124">This example retrieves the names and cities of all suppliers and customers in Brazil.</span></span> <span data-ttu-id="fa254-125">Dabei wird die EnumFields-Prozedur aufgerufen, die im Beispiel für die SELECT-Anweisung enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="fa254-125">It calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

```vb
    Sub UnionX() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Retrieve the names and cities of all suppliers  
        ' and customers in Brazil. 
        Set rst = dbs.OpenRecordset("SELECT CompanyName," _ 
            & " City FROM Suppliers" _ 
            & " WHERE Country = 'Brazil' UNION" _ 
            & " SELECT CompanyName, City FROM Customers" _ 
            & " WHERE Country = 'Brazil';") 
         
        ' Populate the Recordset. 
        rst.MoveLast 
         
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        EnumFields rst, 12 
     
        dbs.Close 
     
    End Sub
```
