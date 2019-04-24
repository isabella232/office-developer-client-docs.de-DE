---
title: Database. QueryTimeout-Eigenschaft (DAO)
TOCTitle: QueryTimeout Property
ms:assetid: c83ca852-715a-c853-429b-80a15c3fc39b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823170(v=office.15)
ms:contentKeyID: 48547648
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f47d6c51079bf36cb7e1ca596a3476f1a7219c5d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294738"
---
# <a name="databasequerytimeout-property-dao"></a><span data-ttu-id="10b33-102">Database. QueryTimeout-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="10b33-102">Database.QueryTimeout property (DAO)</span></span>


<span data-ttu-id="10b33-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="10b33-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="10b33-104">Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der angibt, wie viele Sekunden beim Ausführen einer Abfrage zu einer ODBC-Datenquelle gewartet wird, bevor ein Timeoutfehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="10b33-104">Sets or returns a value that specifies the number of seconds to wait before a timeout error occurs when a query is executed on an ODBC data source.</span></span>

## <a name="syntax"></a><span data-ttu-id="10b33-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="10b33-105">Syntax</span></span>

<span data-ttu-id="10b33-106">*Ausdruck* . QueryTimeout</span><span class="sxs-lookup"><span data-stu-id="10b33-106">*expression* .QueryTimeout</span></span>

<span data-ttu-id="10b33-107">*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="10b33-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="10b33-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="10b33-108">Remarks</span></span>

<span data-ttu-id="10b33-109">Der Standardwert beträgt 60.</span><span class="sxs-lookup"><span data-stu-id="10b33-109">The default value is 60.</span></span>

<span data-ttu-id="10b33-p101">Bei einer ODBC-Datenbank, wie z. B. Microsoft SQL Server, können aufgrund des Netzwerkverkehrs oder einer hohen Belastung des ODBC-Servers Verzögerungen auftreten. Um eine unbegrenzte Wartezeit zu vermeiden, können Sie die Zeit festlegen.</span><span class="sxs-lookup"><span data-stu-id="10b33-p101">When you're using an ODBC database, such as Microsoft SQL Server, there may be delays due to network traffic or heavy use of the ODBC server. Rather than waiting indefinitely, you can specify how long to wait.</span></span>

<span data-ttu-id="10b33-p102">Wenn Sie die **QueryTimeout**-Eigenschaft bei einem **[Connection](connection-object-dao.md)** - oder **[Database](database-object-dao.md)** -Objekt verwenden, gibt sie den globalen Wert für alle Abfragen an, die der Datenbank zugeordnet sind. Sie können diesen Wert für eine bestimmte Abfrage außer Kraft setzen, indem Sie die **ODBCTimeout**-Eigenschaft des speziellen **[QueryDef](querydef-object-dao.md)** -Objekts festlegen.</span><span class="sxs-lookup"><span data-stu-id="10b33-p102">When you use **QueryTimeout** with a **[Connection](connection-object-dao.md)** or **[Database](database-object-dao.md)** object, it specifies a global value for all queries associated with the database. You can override this value for a specific query by setting the **ODBCTimeout** property of the particular **[QueryDef](querydef-object-dao.md)** object.</span></span>

## <a name="example"></a><span data-ttu-id="10b33-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="10b33-114">Example</span></span>

<span data-ttu-id="10b33-115">In diesem Beispiel werden die Eigenschaften **ODBCTimeout** und **QueryTimeout** verwendet, um zu zeigen, wie die **QueryTimeout**-Einstellung eines **Database**-Objekts die Standardeinstellung von **ODBCTimeout** für ein beliebiges **QueryDef**-Objekt festlegt, das anhand des **Database**-Objekts erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="10b33-115">This example uses the **ODBCTimeout** and **QueryTimeout** properties to show how the **QueryTimeout** setting on a **Database** object sets the default **ODBCTimeout** setting on any **QueryDef** objects created from the **Database** object.</span></span>

```vb 
Sub ODBCTimeoutX() 
 
 Dim dbsCurrent As Database 
 Dim qdfStores As QueryDef 
 Dim rstStores As Recordset 
 
 Set dbsCurrent = OpenDatabase("Northwind.mdb") 
 
 ' Change the default QueryTimeout of the Northwind 
 ' database. 
 Debug.Print "Default QueryTimeout of Database: " & _ 
 dbsCurrent.QueryTimeout 
 dbsCurrent.QueryTimeout = 30 
 Debug.Print "New QueryTimeout of Database: " & _ 
 dbsCurrent.QueryTimeout 
 
 ' Create a new QueryDef object. 
 Set qdfStores = dbsCurrent.CreateQueryDef("Stores", _ 
 "SELECT * FROM stores") 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the SQL Server. 
 qdfStores.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=Publishers" 
 
 ' Change the ODBCTimeout setting of the new QueryDef 
 ' object from its default setting. 
 Debug.Print "Default ODBCTimeout of QueryDef: " & _ 
 qdfStores.ODBCTimeout 
 qdfStores.ODBCTimeout = 0 
 Debug.Print "New ODBCTimeout of QueryDef: " & _ 
 qdfStores.ODBCTimeout 
 
 ' Execute the query and display the results. 
 Set rstStores = qdfStores.OpenRecordset() 
 
 Debug.Print "Contents of recordset:" 
 With rstStores 
 Do While Not .EOF 
 Debug.Print , .Fields(0), .Fields(1) 
 .MoveNext 
 Loop 
 .Close 
 End With 
 
 ' Delete new QueryDef because this is a demonstration. 
 dbsCurrent.QueryDefs.Delete qdfStores.Name 
 dbsCurrent.Close 
 
End Sub 
 
```

