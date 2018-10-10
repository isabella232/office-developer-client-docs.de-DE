---
title: EXECUTE-Anweisung (Microsoft Access SQL)
TOCTitle: EXECUTE Statement (Microsoft Access SQL)
ms:assetid: 9ec4d9ee-db2a-0319-3ccf-c035d67a1496
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198330(v=office.15)
ms:contentKeyID: 48546667
ms.date: 09/28/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277471
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f150a310b562f7fc014f15230bee09f8f686c61a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474490"
---
# <a name="execute-statement-microsoft-access-sql"></a><span data-ttu-id="bc2f9-102">EXECUTE-Anweisung (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="bc2f9-102">EXECUTE Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="bc2f9-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="bc2f9-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="bc2f9-104">Wird verwendet, um die Ausführung einer Prozedur aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="bc2f9-104">Used to invoke the execution of a procedure.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc2f9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc2f9-105">Syntax</span></span>

<span data-ttu-id="bc2f9-106">EXECUTE *Prozedur* \[ *param1*\[, *param2*\[,...\]\]</span><span class="sxs-lookup"><span data-stu-id="bc2f9-106">EXECUTE *procedure* \[*param1*\[, *param2*\[, …\]\]</span></span>

<span data-ttu-id="bc2f9-107">Die EXECUTE-Anweisung besteht aus folgenden Komponenten:</span><span class="sxs-lookup"><span data-stu-id="bc2f9-107">The EXECUTE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bc2f9-108">Komponente</span><span class="sxs-lookup"><span data-stu-id="bc2f9-108">Part</span></span></p></th>
<th><p><span data-ttu-id="bc2f9-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bc2f9-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bc2f9-110"><em>Prozedur</em></span><span class="sxs-lookup"><span data-stu-id="bc2f9-110"><em>procedure</em></span></span></p></td>
<td><p><span data-ttu-id="bc2f9-111">Der Name der auszuführenden Prozedur.</span><span class="sxs-lookup"><span data-stu-id="bc2f9-111">The name of the procedure that is to be executed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc2f9-112"><em>Param1, Param2, …</em></span><span class="sxs-lookup"><span data-stu-id="bc2f9-112"><em>param1, param2, …</em></span></span></p></td>
<td><p><span data-ttu-id="bc2f9-113">Die von der Prozedur definierten Werte für die Parameter.</span><span class="sxs-lookup"><span data-stu-id="bc2f9-113">Values for the parameters defined by the procedure.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="example"></a><span data-ttu-id="bc2f9-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="bc2f9-114">Example</span></span>

<span data-ttu-id="bc2f9-115">In diesem Beispiel wird die Abfrage categoryList verwendet, und es wird die EnumFields-Prozedur, die Sie in diesem Beispiel wird die SELECT-Anweisung finden.</span><span class="sxs-lookup"><span data-stu-id="bc2f9-115">This example names the query CategoryList, and calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

```vb
    Sub ProcedureX() 
     
        Dim dbs As Database, rst As Recordset 
        Dim qdf As QueryDef, strSql As String 
         
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        strSql = "PROCEDURE CategoryList; " _ 
            & "SELECT DISTINCTROW CategoryName, " _ 
            & "CategoryID FROM Categories " _ 
            & "ORDER BY CategoryName;" 
         
        ' Create a named QueryDef based on the SQL 
        ' statement. 
        Set qdf = dbs.CreateQueryDef("NewQry", strSql) 
     
        ' Create a temporary snapshot-type Recordset. 
        Set rst = qdf.OpenRecordset(dbOpenSnapshot) 
     
        ' Populate the Recordset. 
        rst.MoveLast 
                 
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        Execute EnumFields rst, 15 
         
        ' Delete the QueryDef because this is a 
        ' demonstration. 
        dbs.QueryDefs.Delete "NewQry" 
         
        dbs.Close 
     
    End Sub
```
