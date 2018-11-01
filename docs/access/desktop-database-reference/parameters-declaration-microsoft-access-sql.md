---
title: PARAMETERS-Deklaration (Microsoft Access SQL)
TOCTitle: PARAMETERS Declaration (Microsoft Access SQL)
ms:assetid: 0dcaad68-6a5f-93dc-e62a-b82b36e1e69c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845220(v=office.15)
ms:contentKeyID: 48543230
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277577
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 24212ce3a29c0e30fae1dad7566ef93815f8a03f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876778"
---
# <a name="parameters-declaration-microsoft-access-sql"></a><span data-ttu-id="63a05-102">PARAMETERS-Deklaration (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="63a05-102">PARAMETERS Declaration (Microsoft Access SQL)</span></span>


<span data-ttu-id="63a05-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="63a05-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="63a05-104">Deklariert den Namen und Datentyp der einzelnen Parameter in einer Parameterabfrage.</span><span class="sxs-lookup"><span data-stu-id="63a05-104">Declares the name and data type of each parameter in a parameter query.</span></span>

## <a name="syntax"></a><span data-ttu-id="63a05-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="63a05-105">Syntax</span></span>

<span data-ttu-id="63a05-106">PARAMETERS *Name Datentyp* \[, *Name Datentyp* \[,...\]\]</span><span class="sxs-lookup"><span data-stu-id="63a05-106">PARAMETERS *name datatype* \[, *name datatype* \[, …\]\]</span></span>

<span data-ttu-id="63a05-107">Die PARAMETERS-Deklaration enthält die folgenden Bestandteile:</span><span class="sxs-lookup"><span data-stu-id="63a05-107">The PARAMETERS declaration has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="63a05-108">Argument</span><span class="sxs-lookup"><span data-stu-id="63a05-108">Part</span></span></p></th>
<th><p><span data-ttu-id="63a05-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="63a05-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="63a05-110"><em>name</em></span><span class="sxs-lookup"><span data-stu-id="63a05-110"><em>name</em></span></span></p></td>
<td><p><span data-ttu-id="63a05-111">Der Name des Parameters.</span><span class="sxs-lookup"><span data-stu-id="63a05-111">The name of the parameter.</span></span> <span data-ttu-id="63a05-112">Wird der <strong>Name</strong> -Eigenschaft des <strong>Parameter</strong> -Objekts zugewiesen und wird verwendet, um diesen Parameter in der <strong>Parameters</strong> -Auflistung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="63a05-112">Assigned to the <strong>Name</strong> property of the <strong>Parameter</strong> object and used to identify this parameter in the <strong>Parameters</strong> collection.</span></span> <span data-ttu-id="63a05-113">Sie können <em>Name</em> als Zeichenfolge, die in einem Dialogfeld angezeigt wird, während die Anwendung die Abfrage ausführt.</span><span class="sxs-lookup"><span data-stu-id="63a05-113">You can use <em>name</em> as a string that is displayed in a dialog box while your application runs the query.</span></span> <span data-ttu-id="63a05-114">Umgeben Sie Text, der Leerzeichen oder Satzzeichen enthält, mit Klammern ([ ]).</span><span class="sxs-lookup"><span data-stu-id="63a05-114">Use brackets ([ ]) to enclose text that contains spaces or punctuation.</span></span> <span data-ttu-id="63a05-115">Beispielsweise [Low Price] und [Bericht mit welcher Month? beginnen] sind gültigen <em>Namen</em> Argumente.</span><span class="sxs-lookup"><span data-stu-id="63a05-115">For example, [Low price] and [Begin report with which month?] are valid <em>name</em> arguments.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63a05-116"><em>Datentyp</em></span><span class="sxs-lookup"><span data-stu-id="63a05-116"><em>datatype</em></span></span></p></td>
<td><p><span data-ttu-id="63a05-117">Einer der wichtigsten <a href="sql-data-types.md">Microsoft Access SQL-Datentypen</a> oder eines der Synonyme.</span><span class="sxs-lookup"><span data-stu-id="63a05-117">One of the primary <a href="sql-data-types.md">Microsoft Access SQL data types</a> or their synonyms.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="63a05-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="63a05-118">Remarks</span></span>

<span data-ttu-id="63a05-p102">Für regelmäßig ausgeführte Abfragen können Sie zum Erstellen der Parameterabfrage eine PARAMETERS-Deklaration verwenden. Eine Parameterabfrage kann Sie dabei unterstützen, das Ändern der Abfragekriterien zu automatisieren. Bei einer Parameterabfrage müssen die Parameter jedes Mal, wenn die Abfrage ausgeführt wird, im Code angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="63a05-p102">For queries that you run regularly, you can use a PARAMETERS declaration to create a parameter query. A parameter query can help automate the process of changing query criteria. With a parameter query, your code will need to provide the parameters each time the query is run.</span></span>

<span data-ttu-id="63a05-122">Die PARAMETERS-Deklaration ist optional, doch wenn sie angegeben wird, wird sie vor allen anderen Anweisungen angegeben, selbst vor einer [SELECT](select-statement-microsoft-access-sql.md)-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="63a05-122">The PARAMETERS declaration is optional but when included precedes any other statement, including [SELECT](select-statement-microsoft-access-sql.md).</span></span>

<span data-ttu-id="63a05-p103">Wenn die Deklaration mehrere Parameter einschließt, müssen diese durch Kommas getrennt werden. Im folgenden Beispiel sind zwei Parameter eingeschlossen:</span><span class="sxs-lookup"><span data-stu-id="63a05-p103">If the declaration includes more than one parameter, separate them with commas. The following example includes two parameters:</span></span>

```sql
PARAMETERS [Low price] Currency, [Beginning date] DateTime;
```

<span data-ttu-id="63a05-125">Sie können *Name* , aber nicht den *Datentyp* in einer [, in dem](https://msdn.microsoft.com/library/ff195245\(v=office.15\)) oder eine [HAVING](https://msdn.microsoft.com/library/ff193795\(v=office.15\)) -Klausel verwenden.</span><span class="sxs-lookup"><span data-stu-id="63a05-125">You can use *name* but not *datatype* in a [WHERE](https://msdn.microsoft.com/library/ff195245\(v=office.15\)) or [HAVING](https://msdn.microsoft.com/library/ff193795\(v=office.15\)) clause.</span></span> <span data-ttu-id="63a05-126">In den folgenden Beispielen wird die Angabe von zwei Parametern erwartet, anschließend werden die Kriterien auf die Datensätze in der Orders-Tabelle angewendet:</span><span class="sxs-lookup"><span data-stu-id="63a05-126">The following example expects two parameters to be provided and then applies the criteria to records in the Orders table:</span></span>

```sql
PARAMETERS [Low price] Currency, 
[Beginning date] DateTime; 
SELECT OrderID, OrderAmount
FROM Orders 
WHERE OrderAmount > [Low price] 
AND OrderDate >= [Beginning date];
```

## <a name="example"></a><span data-ttu-id="63a05-127">Beispiel</span><span class="sxs-lookup"><span data-stu-id="63a05-127">Example</span></span>

<span data-ttu-id="63a05-128">In diesem Beispiel muss der Benutzer eine Position angeben, die dann als Kriterium in der Abfrage verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="63a05-128">This example requires the user to provide a job title and then uses that job title as the criteria for the query.</span></span>

<span data-ttu-id="63a05-129">In diesem Beispiel wird die EnumFields-Prozedur aufgerufen, die im Beispiel für die [SELECT-Anweisung](select-statement-microsoft-access-sql.md) enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="63a05-129">This example calls the EnumFields procedure, which you can find in the [SELECT statement](select-statement-microsoft-access-sql.md) example.</span></span>

```vb
    Sub ParametersX() 
     
        Dim dbs As Database, qdf As QueryDef 
        Dim rst As Recordset 
        Dim strSql As String, strParm As String 
        Dim strMessage As String 
        Dim intCommand As Integer 
         
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("NorthWind.mdb") 
         
        ' Define the parameters clause. 
        strParm = "PARAMETERS [Employee Title] CHAR; " 
     
        ' Define an SQL statement with the parameters 
        ' clause. 
        strSql = strParm & "SELECT LastName, FirstName, " _ 
            & "EmployeeID " _ 
            & "FROM Employees " _ 
            & "WHERE Title =[Employee Title];" 
         
        ' Create a QueryDef object based on the  
        ' SQL statement. 
        Set qdf = dbs.CreateQueryDef _ 
            ("Find Employees", strSql) 
         
        Do While True 
            strMessage = "Find Employees by Job " _ 
                & "title:" & Chr(13) _ 
                & "  Choose Job Title:" & Chr(13) _ 
                & "   1 - Sales Manager" & Chr(13) _ 
                & "   2 - Sales Representative" & Chr(13) _ 
                & "   3 - Inside Sales Coordinator" 
             
            intCommand = Val(InputBox(strMessage)) 
             
            Select Case intCommand 
                Case 1 
                    qdf("Employee Title") = _ 
                        "Sales Manager" 
                Case 2 
                    qdf("Employee Title") = _ 
                        "Sales Representative" 
                Case 3 
                    qdf("Employee Title") = _ 
                        "Inside Sales Coordinator" 
                Case Else 
                    Exit Do 
            End Select 
             
            ' Create a temporary snapshot-type Recordset. 
            Set rst = qdf.OpenRecordset(dbOpenSnapshot) 
     
            ' Populate the Recordset. 
            rst.MoveLast 
                 
            ' Call EnumFields to print the contents of the  
            ' Recordset. Pass the Recordset object and desired 
            ' field width. 
            EnumFields rst, 12 
     
        Loop 
         
        ' Delete the QueryDef because this is a 
        ' demonstration. 
        dbs.QueryDefs.Delete "Find Employees" 
         
        dbs.Close 
     
    End Sub
```
