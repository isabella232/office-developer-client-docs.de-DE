---
title: 'Alternativen: Verwenden von SQL-Anweisungen'
TOCTitle: 'Alternatives: Using SQL statements'
ms:assetid: 9ed787da-7099-2ef5-b2c6-c4f6bce5ddfe
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249727(v=office.15)
ms:contentKeyID: 48546668
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4bcda13d8b785f1048890d1ed9492f5da3e7288b
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945558"
---
# <a name="alternatives-using-sql-statements"></a><span data-ttu-id="d12f5-102">Alternativen: Verwenden von SQL-Anweisungen</span><span class="sxs-lookup"><span data-stu-id="d12f5-102">Alternatives: Using SQL statements</span></span>


<span data-ttu-id="d12f5-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d12f5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d12f5-p101">ADO ermöglicht alternativ zu den integrierten Eigenschaften und Methoden auch die Verwendung von Befehlen zum Bearbeiten von Daten. In Abhängigkeit von Ihrem Anbieter könnten alle in diesem Kapitel beschriebenen Vorgänge auch durch Übergeben von Befehlen an die Datenquelle ausgeführt werden. Beispielsweise können mit UPDATE-SQL-Anweisungen Daten geändert werden, ohne dass die **Value** -Eigenschaft eines **Field** -Objekts verwendet wird. Anstelle der **AddNew** -Methode von ADO können einer Datenquelle mit INSERT-SQL-Anweisungen neue Datensätze hinzugefügt werden. Weitere Informationen zu SQL oder zur Datenbearbeitungssprache Ihres Anbieters finden Sie in der Dokumentation Ihrer Datenquelle.</span><span class="sxs-lookup"><span data-stu-id="d12f5-p101">ADO also allows using commands as alternatives to its built-in properties and methods for editing data. Depending upon your provider, all operations mentioned in this chapter could also be accomplished by passing commands to your data source. For example, SQL UPDATE statements can be used to modify data without using the **Value** property of a **Field**. SQL INSERT statements can be used to add new records to a data source, rather than the ADO method **AddNew**. For more information about SQL or the data-manipulation language of your provider, see the documentation of your data source.</span></span>

<span data-ttu-id="d12f5-109">Beispielsweise können Sie wie im folgenden Code veranschaulicht eine SQL-Zeichenfolge, die eine DELETE-Anweisung enthält, an eine Datenbank übergeben:</span><span class="sxs-lookup"><span data-stu-id="d12f5-109">For example, you can pass a SQL string containing a DELETE statement to a database, as shown in the following code:</span></span>

```vb 
'BeginSQLDelete 
strSQL = "DELETE FROM Shippers WHERE ShipperID = " & intId 
objConn.Execute strSQL, , adCmdText + adExecuteNoRecords 
'EndSQLDelete 
```

