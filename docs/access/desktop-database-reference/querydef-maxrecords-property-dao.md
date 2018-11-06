---
title: QueryDef.MaxRecords-Eigenschaft (DAO)
TOCTitle: MaxRecords Property
ms:assetid: 7492cde9-be30-3473-dabc-9602465910d1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195877(v=office.15)
ms:contentKeyID: 48545664
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053583
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 0156983a455c72e4046424def188e41b94705087
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998226"
---
# <a name="querydefmaxrecords-property-dao"></a><span data-ttu-id="cd899-102">QueryDef.MaxRecords-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="cd899-102">QueryDef.MaxRecords property (DAO)</span></span>

<span data-ttu-id="cd899-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cd899-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cd899-104">Legt die maximale Anzahl von Datensätzen fest, die von einer Abfrage an eine ODBC-Datenquelle zurückgegeben werden sollen, oder gibt den betreffenden Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="cd899-104">Sets or returns the maximum number of records to return from a query against an ODBC data source.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd899-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd899-105">Syntax</span></span>

<span data-ttu-id="cd899-106">*Ausdruck* . MaxRecords</span><span class="sxs-lookup"><span data-stu-id="cd899-106">*expression* .MaxRecords</span></span>

<span data-ttu-id="cd899-107">*Ausdruck* Eine Variable, die ein **QueryDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="cd899-107">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd899-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cd899-108">Remarks</span></span>

<span data-ttu-id="cd899-109">Der Standardwert ist 0. Bei diesem Wert gibt es keine Beschränkung der Anzahl der zurückzugebenden Datensätze.</span><span class="sxs-lookup"><span data-stu-id="cd899-109">The default value is 0, indicating no limit on the number of records returned.</span></span>

<span data-ttu-id="cd899-p101">Wenn die von **MaxRecords** festgelegte Anzahl der Zeilen an die Anwendung in einem **[Recordset](recordset-object-dao.md)** -Objekt zurückgegeben wird, beendet der Abfrageprozessor die Rückgabe der Datensätze, selbst wenn noch weitere Datensätze in das **Recordset** einbezogen werden sollten. Diese Eigenschaft ist nützlich, wenn beschränkte Clientressourcen die Verarbeitung einer großen Anzahl von Datensätzen nicht zulassen.</span><span class="sxs-lookup"><span data-stu-id="cd899-p101">Once the number of rows specified by **MaxRecords** is returned to your application in a **[Recordset](recordset-object-dao.md)**, the query processor will stop returning additional records even if more records would qualify for inclusion in the **Recordset**. This property is useful in situations where limited client resources prohibit management of large numbers of records.</span></span>

> [!NOTE]
> <span data-ttu-id="cd899-112">[!HINWEIS] Die **MaxRecords**-Eigenschaft kann nur für eine ODBC-Datenquelle verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cd899-112">The **MaxRecords** property can only be used with an ODBC data source.</span></span>

## <a name="example"></a><span data-ttu-id="cd899-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="cd899-113">Example</span></span>

<span data-ttu-id="cd899-114">In diesem Beispiel wird die **MaxRecords**-Eigenschaft verwendet, um eine Beschränkung der Anzahl der Datensätze festzulegen, die von einer Abfrage einer ODBC-Datenquelle zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="cd899-114">This example uses the **MaxRecords** property to set a limit on how many records are returned by a query on an ODBC data source.</span></span>

```vb 
Sub MaxRecordsX() 
 
 Dim dbsCurrent As Database 
 Dim qdfPassThrough As QueryDef 
 Dim qdfLocal As QueryDef 
 Dim rstTemp As Recordset 
 
 ' Open a database from which QueryDef objects can be 
 ' created. 
 Set dbsCurrent = OpenDatabase("DB1.mdb") 
 
 ' Create a pass-through query to retrieve data from 
 ' a Microsoft SQL Server database. 
 Set qdfPassThrough = _ 
 dbsCurrent.CreateQueryDef("") 
 
 ' Set the properties of the new query, limiting the 
 ' number of returnable records to 20. 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 qdfPassThrough.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=Publishers" 
 qdfPassThrough.SQL = "SELECT * FROM titles" 
 qdfPassThrough.ReturnsRecords = True 
 qdfPassThrough.MaxRecords = 20 
 
 Set rstTemp = qdfPassThrough.OpenRecordset() 
 
 ' Display results of query. 
 Debug.Print "Query results:" 
 With rstTemp 
 Do While Not .EOF 
 Debug.Print , .Fields(0), .Fields(1) 
 .MoveNext 
 Loop 
 .Close 
 End With 
 
 dbsCurrent.Close 
 
End Sub 
 
```

