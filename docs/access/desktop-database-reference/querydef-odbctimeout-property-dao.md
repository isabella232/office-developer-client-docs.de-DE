---
title: QueryDef.ODBCTimeout Property (DAO)
TOCTitle: ODBCTimeout Property
ms:assetid: b251c4fb-64a8-aa95-deed-64425df3e00c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822019(v=office.15)
ms:contentKeyID: 48547166
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053052
f1_categories:
- Office.Version=v15
ms.openlocfilehash: dcb15511f3052366eb3d322c26cdd31d72c9beab
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475757"
---
# <a name="querydefodbctimeout-property-dao"></a><span data-ttu-id="e1b22-102">QueryDef.ODBCTimeout Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="e1b22-102">QueryDef.ODBCTimeout Property (DAO)</span></span>


<span data-ttu-id="e1b22-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e1b22-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e1b22-104">Gibt an, wie viele Sekunden gewartet werden soll, bevor ein Timeoutfehler auftritt, wenn ein **[QueryDef](querydef-object-dao.md)** -Objekt in einer ODBC-Datenbank ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e1b22-104">Indicates the number of seconds to wait before a timeout error occurs when a **[QueryDef](querydef-object-dao.md)** is executed on an ODBC database.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1b22-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1b22-105">Syntax</span></span>

<span data-ttu-id="e1b22-106">*Ausdruck* . ODBCTimeout</span><span class="sxs-lookup"><span data-stu-id="e1b22-106">*expression* .ODBCTimeout</span></span>

<span data-ttu-id="e1b22-107">*Ausdruck* Eine Variable, die ein **QueryDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="e1b22-107">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1b22-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e1b22-108">Remarks</span></span>

<span data-ttu-id="e1b22-p101">Wenn die ODBCTimeout-Eigenschaft den Wert -1 erhält, wird für das Timeout standardmäßig die aktuelle Einstellung der QueryTimeout-Eigenschaft des Connection- oder Database-Objekts verwendet, das das QueryDef-Objekt enthält. Wenn die ODBCTimeout-Eigenschaft den Wert 0 hat, tritt kein Timeoutfehler auf.</span><span class="sxs-lookup"><span data-stu-id="e1b22-p101">When the **ODBCTimeout** property is set to -1, the timeout defaults to the current setting of the **[QueryTimeout](database-querytimeout-property-dao.md)** property of the **[Connection](connection-object-dao.md)** or **[Database](database-object-dao.md)** object that contains the **QueryDef**. When the **ODBCTimeout** property is set to 0, no timeout error occurs.</span></span>

<span data-ttu-id="e1b22-p102">Wenn Sie eine ODBC-Datenbank verwenden, wie etwa Microsoft SQL Server, kann es aufgrund einer hohen Auslastung des Netzwerks oder des ODBC-Server zu Verzögerungen kommen. Anstatt zu warten, können Sie einen Zeitraum festlegen, nach dessen Ablauf ein Fehler zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e1b22-p102">When you're using an ODBC database, such as Microsoft SQL Server, delays can occur because of network traffic or heavy use of the ODBC server. Rather than waiting indefinitely, you can specify how long to wait before returning an error.</span></span>

<span data-ttu-id="e1b22-113">Der Wert der **ODBCTimeout**-Eigenschaft eines **QueryDef**-Objekts hat Vorrang vor dem für die **QueryTimeout**-Eigenschaft angegebenen Wert des **Connection** - oder **Database**-Objekts, das das **QueryDef**-Objekt enthält. Dies gilt jedoch nur für das betreffende **QueryDef**-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e1b22-113">Setting the **ODBCTimeout** property of a **QueryDef** object overrides the value specified by the **QueryTimeout** property of the **Connection** or **Database** object containing the **QueryDef**, but only for that **QueryDef** object.</span></span>

## <a name="example"></a><span data-ttu-id="e1b22-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e1b22-114">Example</span></span>

<span data-ttu-id="e1b22-115">In diesem Beispiel werden die Eigenschaften **ODBCTimeout** und **QueryTimeout** verwendet, um zu zeigen, wie die **QueryTimeout**-Einstellung eines **Database**-Objekts die Standardeinstellung von **ODBCTimeout** für ein beliebiges **QueryDef**-Objekt festlegt, das anhand des **Database**-Objekts erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e1b22-115">This example uses the **ODBCTimeout** and **QueryTimeout** properties to show how the **QueryTimeout** setting on a **Database** object sets the default **ODBCTimeout** setting on any **QueryDef** objects created from the **Database** object.</span></span>

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

