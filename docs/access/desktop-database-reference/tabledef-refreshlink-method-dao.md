---
title: TableDef.RefreshLink-Methode (DAO)
TOCTitle: RefreshLink Method
ms:assetid: 9f0059c6-3b7b-57e3-7527-ef674ad9417d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198349(v=office.15)
ms:contentKeyID: 48546674
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052980
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 8b7fda0c095a04d2a3ab7f295497cff05a620ea6
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922538"
---
# <a name="tabledefrefreshlink-method-dao"></a><span data-ttu-id="3a6cd-102">TableDef.RefreshLink-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="3a6cd-102">TableDef.RefreshLink method (DAO)</span></span>

<span data-ttu-id="3a6cd-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3a6cd-103">**Applies to**: Access 2013, Office 2013</span></span>
 
<span data-ttu-id="3a6cd-104">Aktualisiert die Verbindungsinformation für eine verknüpfte Tabelle (gilt nur für Microsoft Access-Arbeitsbereiche ).</span><span class="sxs-lookup"><span data-stu-id="3a6cd-104">Updates the connection information for a linked table (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="3a6cd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a6cd-105">Syntax</span></span>

<span data-ttu-id="3a6cd-106">*Ausdruck* . RefreshLink</span><span class="sxs-lookup"><span data-stu-id="3a6cd-106">*expression* .RefreshLink</span></span>

<span data-ttu-id="3a6cd-107">*Ausdruck* Eine Variable, die ein **TableDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="3a6cd-107">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a6cd-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3a6cd-108">Remarks</span></span>

<span data-ttu-id="3a6cd-p101">Wenn Sie die Verbindungsinformationen für eine verknüpfte Tabelle ändern möchten, müssen Sie die **[Connect](connection-connect-property-dao.md)** -Eigenschaft des entsprechenden **TableDef**-Objekts zurücksetzen und die Informationen anschließend mit der **RefreshLink**-Methode aktualisieren. Beim Verwenden von **RefreshLink** werden keine Änderungen an den Eigenschaften der verknüpften Tabelle und an **[Relation](relation-object-dao.md)** -Objekten vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="3a6cd-p101">To change the connection information for a linked table, reset the **[Connect](connection-connect-property-dao.md)** property of the corresponding **TableDef** object and then use the **RefreshLink** method to update the information. Using **RefreshLink** method doesn't change the linked table's properties and **[Relation](relation-object-dao.md)** objects.</span></span>

<span data-ttu-id="3a6cd-111">Sie müssen für jede Auflistung die [**Refresh**](tabledefs-refresh-method-dao.md) -Methode verwenden, damit diese Verbindungsinformationen in allen Auflistungen vorhanden sind, die mit dem **TableDef**-Objekt verknüpft sind, das der verknüpften Tabelle entspricht.</span><span class="sxs-lookup"><span data-stu-id="3a6cd-111">For this connection information to exist in all collections associated with the **TableDef** object that represents the linked table, you must use the **[Refresh](tabledefs-refresh-method-dao.md)** method on each collection.</span></span>

## <a name="example"></a><span data-ttu-id="3a6cd-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3a6cd-112">Example</span></span>

<span data-ttu-id="3a6cd-p102">In diesem Beispiel wird die RefreshLink-Methode verwendet, um die Daten in einer verknüpften Tabelle zu aktualisieren, nachdem sich deren Verbindung in Bezug auf die Datenquelle geändert hat. Zum Ausführen dieses Vorgangs ist die RefreshLinkOutput-Prozedur erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3a6cd-p102">This example uses the **RefreshLink** method to refresh the data in a linked table after its connection has been changed from one data source to another. The RefreshLinkOutput procedure is required for this procedure to run.</span></span>

```vb 
Sub RefreshLinkX() 
 
 Dim dbsCurrent As Database 
 Dim tdfLinked As TableDef 
 
 ' Open a database to which a linked table can be 
 ' appended. 
 Set dbsCurrent = OpenDatabase("DB1.mdb") 
 
 ' Create a linked table that points to a Microsoft 
 ' SQL Server database. 
 Set tdfLinked = _ 
 dbsCurrent.CreateTableDef("AuthorsTable") 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 tdfLinked.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=Publishers" 
 tdfLinked.SourceTableName = "authors" 
 dbsCurrent.TableDefs.Append tdfLinked 
 
 ' Display contents of linked table. 
 Debug.Print _ 
 "Data from linked table connected to first source:" 
 RefreshLinkOutput dbsCurrent 
 
 ' Change connection information for linked table and 
 ' refresh the connection in order to make the new data 
 ' available. 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 tdfLinked.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=NewPublishers" 
 tdfLinked.RefreshLink 
 
 ' Display contents of linked table. 
 Debug.Print _ 
 "Data from linked table connected to second source:" 
 RefreshLinkOutput dbsCurrent 
 
 ' Delete linked table because this is a demonstration. 
 dbsCurrent.TableDefs.Delete tdfLinked.Name 
 
 dbsCurrent.Close 
 
End Sub 
 
Sub RefreshLinkOutput(dbsTemp As Database) 
 
 Dim rstRemote As Recordset 
 Dim intCount As Integer 
 
 ' Open linked table. 
 Set rstRemote = _ 
 dbsTemp.OpenRecordset("AuthorsTable") 
 
 intCount = 0 
 
 ' Enumerate Recordset object, but stop at 50 records. 
 With rstRemote 
 Do While Not .EOF And intCount < 50 
 Debug.Print , .Fields(0), .Fields(1) 
 intCount = intCount + 1 
 .MoveNext 
 Loop 
 If Not .EOF Then Debug.Print , "[more records]" 
 .Close 
 End With 
 
End Sub 
 
```

