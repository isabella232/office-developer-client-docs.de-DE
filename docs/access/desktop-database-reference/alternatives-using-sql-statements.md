---
title: 'Alternativen: Verwenden von SQL-Anweisungen'
TOCTitle: 'Alternatives: Using SQL statements'
ms:assetid: 9ed787da-7099-2ef5-b2c6-c4f6bce5ddfe
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249727(v=office.15)
ms:contentKeyID: 48546668
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 185f5c1eb7e11a9425ff6cc4a16f1387424f3219
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297151"
---
# <a name="alternatives-using-sql-statements"></a><span data-ttu-id="32287-102">Alternativen: Verwenden von SQL-Anweisungen</span><span class="sxs-lookup"><span data-stu-id="32287-102">Alternatives: Using SQL statements</span></span>


<span data-ttu-id="32287-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="32287-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="32287-p101">ADO ermöglicht alternativ zu den integrierten Eigenschaften und Methoden auch die Verwendung von Befehlen zum Bearbeiten von Daten. In Abhängigkeit von Ihrem Anbieter könnten alle in diesem Kapitel beschriebenen Vorgänge auch durch Übergeben von Befehlen an die Datenquelle ausgeführt werden. Beispielsweise können mit UPDATE-SQL-Anweisungen Daten geändert werden, ohne dass die **Value** -Eigenschaft eines **Field** -Objekts verwendet wird. Anstelle der **AddNew** -Methode von ADO können einer Datenquelle mit INSERT-SQL-Anweisungen neue Datensätze hinzugefügt werden. Weitere Informationen zu SQL oder zur Datenbearbeitungssprache Ihres Anbieters finden Sie in der Dokumentation Ihrer Datenquelle.</span><span class="sxs-lookup"><span data-stu-id="32287-p101">ADO also allows using commands as alternatives to its built-in properties and methods for editing data. Depending upon your provider, all operations mentioned in this chapter could also be accomplished by passing commands to your data source. For example, SQL UPDATE statements can be used to modify data without using the **Value** property of a **Field**. SQL INSERT statements can be used to add new records to a data source, rather than the ADO method **AddNew**. For more information about SQL or the data-manipulation language of your provider, see the documentation of your data source.</span></span>

<span data-ttu-id="32287-109">Beispielsweise können Sie wie im folgenden Code veranschaulicht eine SQL-Zeichenfolge, die eine DELETE-Anweisung enthält, an eine Datenbank übergeben:</span><span class="sxs-lookup"><span data-stu-id="32287-109">For example, you can pass a SQL string containing a DELETE statement to a database, as shown in the following code:</span></span>

```vb 
'BeginSQLDelete 
strSQL = "DELETE FROM Shippers WHERE ShipperID = " & intId 
objConn.Execute strSQL, , adCmdText + adExecuteNoRecords 
'EndSQLDelete 
```

