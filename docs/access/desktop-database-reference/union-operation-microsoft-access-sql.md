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
ms.openlocfilehash: 1a61512c58ccbde82072fa4d8105c82b9f145ebc
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937421"
---
# <a name="union-operation-microsoft-access-sql"></a><span data-ttu-id="7cd44-102">UNION-Operation (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="7cd44-102">UNION operation (Microsoft Access SQL)</span></span>


<span data-ttu-id="7cd44-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7cd44-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7cd44-104">Erstellt eine Union-Abfrage, in der die Ergebnisse von mindestens zwei unabhängigen Abfragen oder Tabellen miteinander kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="7cd44-104">Creates a union query, which combines the results of two or more independent queries or tables.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cd44-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7cd44-105">Syntax</span></span>

<span data-ttu-id="7cd44-106">\[Tabelle\] *Abfrage1* UNION \[alle\] \[Tabelle\] *abfrage2* \[UNION \[alle\] \[Tabelle\] *Abfragen* \[ ...</span><span class="sxs-lookup"><span data-stu-id="7cd44-106">\[TABLE\] *query1* UNION \[ALL\] \[TABLE\] *query2* \[UNION \[ALL\] \[TABLE\] *queryn* \[ …</span></span> <span data-ttu-id="7cd44-107">\]\]</span><span class="sxs-lookup"><span data-stu-id="7cd44-107"></span></span>

<span data-ttu-id="7cd44-108">Die UNION-Operation enthält die folgenden Bestandteile:</span><span class="sxs-lookup"><span data-stu-id="7cd44-108">The UNION operation has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7cd44-109">Argument</span><span class="sxs-lookup"><span data-stu-id="7cd44-109">Part</span></span></p></th>
<th><p><span data-ttu-id="7cd44-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7cd44-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7cd44-111"><em>Abfrage1-N</em></span><span class="sxs-lookup"><span data-stu-id="7cd44-111"><em>query1-n</em></span></span></p></td>
<td><p><span data-ttu-id="7cd44-112">Eine SELECT-Anweisung, der Name einer gespeicherten Abfrage oder der Name einer gespeicherten Tabelle, der das Schlüsselwort TABLE vorangestellt ist.</span><span class="sxs-lookup"><span data-stu-id="7cd44-112">A SELECT statement, the name of a stored query, or the name of a stored table preceded by the TABLE keyword.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="7cd44-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7cd44-113">Remarks</span></span>

<span data-ttu-id="7cd44-p102">Sie können die Ergebnisse von zwei oder mehr Abfragen, Tabellen und SELECT-Anweisungen in jeder beliebigen Kombination in einer einzelnen UNION-Operation zusammenführen. Im folgenden Beispiel wird die vorhandene New Accounts-Tabelle mit einer SELECT-Anweisung zusammengeführt:</span><span class="sxs-lookup"><span data-stu-id="7cd44-p102">You can merge the results of two or more queries, tables, and SELECT statements, in any combination, in a single UNION operation. The following example merges an existing table named New Accounts and a SELECT statement:</span></span>

```sql
TABLE [New Accounts] UNION ALL 
SELECT * 
FROM Customers 
WHERE OrderAmount > 1000;
```

<span data-ttu-id="7cd44-p103">Standardmäßig werden bei Verwendung einer UNION-Operation keine duplizierten Datensätze zurückgegeben. Sie können jedoch mithilfe des Prädikats [ALL](https://msdn.microsoft.com/library/ff195711\(v=office.15\)) sicherstellen, dass alle Datensätze zurückgegeben werden. Außerdem wird dadurch die Ausführung der Abfrage beschleunigt.</span><span class="sxs-lookup"><span data-stu-id="7cd44-p103">By default, no duplicate records are returned when you use a UNION operation; however, you can include the [ALL](https://msdn.microsoft.com/library/ff195711\(v=office.15\)) predicate to ensure that all records are returned. This also makes the query run faster.</span></span>

<span data-ttu-id="7cd44-118">Alle Abfragen in einer UNION-Operation müssen dieselbe Anzahl von Feldern anfordern. Doch die Felder müssen nicht dieselbe Größe oder denselben Datentyp besitzen.</span><span class="sxs-lookup"><span data-stu-id="7cd44-118">All queries in a UNION operation must request the same number of fields; however, the fields do not have to be of the same size or data type.</span></span>

<span data-ttu-id="7cd44-p104">Verwenden Sie Aliase nur in der ersten SELECT-Anweisung, da sie in anderen Anweisungen ignoriert werden. In der ORDER BY-Klausel verweisen Sie auf ein Feld unter dem Namen, der in der ersten SELECT-Anweisung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7cd44-p104">Use aliases only in the first SELECT statement because they are ignored in any others. In the ORDER BY clause, refer to fields by what they are called in the first SELECT statement.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="7cd44-121">Eine <A href="https://msdn.microsoft.com/library/ff837271(v=office.15)">GROUP BY-</A> oder <A href="https://msdn.microsoft.com/library/ff193795(v=office.15)">HAVING</A> -Klausel können in <EM>jedem Abfrageargument</EM> Sie um die zurückgegebenen Daten zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="7cd44-121">You can use a <A href="https://msdn.microsoft.com/library/ff837271(v=office.15)">GROUP BY</A> or <A href="https://msdn.microsoft.com/library/ff193795(v=office.15)">HAVING</A> clause in each <EM>query</EM> argument to group the returned data.</span></span></P>
> <LI>
> <P><span data-ttu-id="7cd44-122"><A href="https://msdn.microsoft.com/library/ff198293(v=office.15)">ORDER BY</A> -Klausel können am Ende des <EM>letzten abfragearguments</EM> Sie die zurückgegebenen Daten in einer bestimmten Reihenfolge angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7cd44-122">You can use an <A href="https://msdn.microsoft.com/library/ff198293(v=office.15)">ORDER BY</A> clause at the end of the last <EM>query</EM> argument to display the returned data in a specified order.</span></span></P></LI></UL>



## <a name="example"></a><span data-ttu-id="7cd44-123">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7cd44-123">Example</span></span>

<span data-ttu-id="7cd44-124">In diesem Beispiel werden die Namen und Städte aller Lieferanten und Kunden in Brasilien abgerufen.</span><span class="sxs-lookup"><span data-stu-id="7cd44-124">This example retrieves the names and cities of all suppliers and customers in Brazil.</span></span> <span data-ttu-id="7cd44-125">Sie ruft die EnumFields-Prozedur, die Sie in diesem Beispiel wird die SELECT-Anweisung finden.</span><span class="sxs-lookup"><span data-stu-id="7cd44-125">It calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

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
