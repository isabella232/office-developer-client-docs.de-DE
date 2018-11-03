---
title: 'Schritt 2: Aufrufen des Serverprogramms (RDS-Lernprogramm)'
TOCTitle: 'Step 2: Invoke the Server Program (RDS Tutorial)'
ms:assetid: 45429faa-c1e2-d448-a5b4-b2d77cb94377
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249211(v=office.15)
ms:contentKeyID: 48544549
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3d3264c58434bf7af6ae4e75c249a7009f39b7d4
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947231"
---
# <a name="step-2-invoke-the-server-program-rds-tutorial"></a><span data-ttu-id="5028f-102">Schritt 2: Aufrufen des Serverprogramms (RDS-Lernprogramm)</span><span class="sxs-lookup"><span data-stu-id="5028f-102">Step 2: Invoke the server program (RDS Tutorial)</span></span>

<span data-ttu-id="5028f-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5028f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5028f-p101">Wenn Sie auf dem Client*proxy* eine Methode aufrufen, wird die Methode vom tatsächlichen Programm auf dem Server ausgeführt. In diesem Schritt führen Sie eine Abfrage auf dem Server durch.</span><span class="sxs-lookup"><span data-stu-id="5028f-p101">When you invoke a method on the client *proxy*, the actual program on the server executes the method. In this step, you'll execute a query on the server.</span></span>

<span data-ttu-id="5028f-106">**Teil A** Wenn Sie in diesem Lernprogramm [RDSServer.DataFactory](datafactory-object-rdsserver.md) verwendet haben, wäre Weise zum Ausführen dieses Schritts, verwenden Sie die [RDS. DataControl](datacontrol-object-rds.md) Objekt.</span><span class="sxs-lookup"><span data-stu-id="5028f-106">**Part A**If you weren't using [RDSServer.DataFactory](datafactory-object-rdsserver.md) in this tutorial, the most convenient way to perform this step would be to use the [RDS.DataControl](datacontrol-object-rds.md) object.</span></span> <span data-ttu-id="5028f-107">Das **RDS.DataControl** -Objekt verbindet den vorherigen Schritt des Erstellens eines Proxys mit diesem Schritt des Erstellens einer Abfrage.</span><span class="sxs-lookup"><span data-stu-id="5028f-107">The **RDS.DataControl** combines the previous step of creating a proxy, with this step, issuing the query.</span></span>

<span data-ttu-id="5028f-p103">Geben Sie anhand der **Server**-Eigenschaft des [RDS.DataControl](server-property-rds.md) -Objekts an, wo das Serverprogramm instanziiert werden soll. Geben Sie mit der [Connect](connect-property-rds.md)-Eigenschaft die Verbindungszeichenfolge für den Zugriff auf die Datenquelle an, und geben Sie mit der [SQL](https://msdn.microsoft.com/library/jj248989\(v=office.15\))-Eigenschaft den Text des Abfragebefehls an. Rufen Sie dann die [Refresh](refresh-method-rds.md)-Methode auf, sodass das Serverprogramm die Verbindung mit der Datenquelle herstellt, die in der Abfrage angegebenen Zeilen abruft und ein **Recordset** -Objekt an den Client zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="5028f-p103">Set the **RDS.DataControl** object [Server](server-property-rds.md) property to identify where the server program should be instantiated; the [Connect](connect-property-rds.md) property to specify the connect string to access the data source; and the [SQL](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) property to specify the query command text. Then issue the [Refresh](refresh-method-rds.md) method to cause the server program to connect to the data source, retrieve rows specified by the query, and return a **Recordset** object to the client.</span></span>

<span data-ttu-id="5028f-110">In diesem Lernprogramm wird zwar kein **RDS.DataControl** -Objekt verwendet, es würde jedoch folgendermaßen auftreten:</span><span class="sxs-lookup"><span data-stu-id="5028f-110">This tutorial does not use the **RDS.DataControl**, but this is how it would look if it did:</span></span>

```vb 
 
Sub RDSTutorial2A() 
 Dim DC as New RDS.DataControl 
 DC.Server = "https://yourServer" 
 DC.Connect = "DSN=Pubs" 
 DC.SQL = "SELECT * FROM Authors" 
 DC.Refresh 
... 
```

<span data-ttu-id="5028f-111">In diesem Lernprogramm wird RDS auch nicht mit ADO-Objekten aufgerufen, was folgendermaßen aussehen würde:</span><span class="sxs-lookup"><span data-stu-id="5028f-111">Nor does the tutorial invoke RDS with ADO objects, but this is how it would look if it did:</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
"Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
```

<span data-ttu-id="5028f-112">**Teil B** Die allgemeine-Methode des für diesen Schritt ist das **RDSServer.DataFactory** -Objekt, [Query](query-method-rds.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5028f-112">**Part B**The general method of performing this step is to invoke the **RDSServer.DataFactory** object [Query](query-method-rds.md) method.</span></span> <span data-ttu-id="5028f-113">In diese Methode wird anhand einer Verbindungszeichenfolge eine Verbindung mit der Datenquelle hergestellt, und mit einem Befehlstext werden die Zeilen angegeben, die aus der Datenquelle zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5028f-113">That method takes a connect string, which is used to connect to a data source, and a command text, which is used to specify the rows to be returned from the data source.</span></span>

<span data-ttu-id="5028f-114">In diesem Lernprogramm wird die **Query** -Methode des **DataFactory** -Objekts verwendet:</span><span class="sxs-lookup"><span data-stu-id="5028f-114">This tutorial uses the **DataFactory** object **Query** method:</span></span>

```vb 
 
Sub RDSTutorial2B() 
 Dim DS as New RDS.DataSpace 
 Dim DF 
 Dim RS as ADODB.Recordset 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

