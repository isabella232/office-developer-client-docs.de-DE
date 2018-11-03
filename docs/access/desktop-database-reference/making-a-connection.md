---
title: Herstellen einer Verbindung
TOCTitle: Making a connection
ms:assetid: 188f6794-f4ec-8e8d-5adc-bdee36f4c9ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248932(v=office.15)
ms:contentKeyID: 48543472
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0335c4bbc0d1240d6d4ca53ceacf47bf44fce67d
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945887"
---
# <a name="making-a-connection"></a><span data-ttu-id="93ae1-102">Herstellen einer Verbindung</span><span class="sxs-lookup"><span data-stu-id="93ae1-102">Making a connection</span></span>

<span data-ttu-id="93ae1-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="93ae1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="93ae1-p101">Zum Herstellen einer Verbindung mit einer Datenquelle müssen Sie eine *Verbindungszeichenfolge* angeben, deren Parameter je nach Anbieter und Datenquelle variieren können. Weitere Informationen finden Sie unter [Erstellen der Verbindungszeichenfolge](creating-the-connection-string.md).</span><span class="sxs-lookup"><span data-stu-id="93ae1-p101">To connect to a data source, you must specify a *connection string*, the parameters of which might differ for each provider and data source. For more information, see [Creating the Connection String](creating-the-connection-string.md).</span></span>

<span data-ttu-id="93ae1-p102">ADO öffnet eine Verbindung in der Regel mithilfe der **Open** -Methode des **Connection** -Objekts. Die Syntax für die **Open** -Methode ist im Folgenden dargestellt:</span><span class="sxs-lookup"><span data-stu-id="93ae1-p102">ADO most commonly opens a connection by using the **Connection** object **Open** method. The syntax for the **Open** method is shown here:</span></span>

```vb
Dim connection as New ADODB.Connection 
connection.Open ConnectionString, UserID, Password, OpenOptions
```

<span data-ttu-id="93ae1-108">Alternativ können Sie den Kurzbefehl **Recordset.Open** verwenden, um eine implizite Verbindung zu öffnen und einen Befehl für diese Verbindung in einem Schritt auszustellen.</span><span class="sxs-lookup"><span data-stu-id="93ae1-108">Alternatively, you can invoke a shortcut technique, **Recordset.Open**, to open an implicit connection and issue a command over that connection in one operation.</span></span> <span data-ttu-id="93ae1-109">Zu diesem Zweck in eine gültige Verbindungszeichenfolge als *ActiveConnection* -Argument an die **Open** -Methode übergeben.</span><span class="sxs-lookup"><span data-stu-id="93ae1-109">Do this by passing in a valid connection string as the *ActiveConnection* argument to the **Open** method.</span></span> <span data-ttu-id="93ae1-110">Es folgt die Syntax für die verschiedenen Methoden in Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="93ae1-110">Here is the syntax for each method in Visual Basic:</span></span>

```vb
Dim recordset as ADODB.Recordset 
Set recordset = New ADODB.Recordset 
recordset.Open Source, ActiveConnection, CursorType, LockType, Options
```

> [!NOTE]
> <span data-ttu-id="93ae1-p104">[!HINWEIS] Wann sollten Sie ein **Connection** -Objekt und wann den Kurzbefehl **Recordset.Open** verwenden? Verwenden Sie das **Connection** -Objekt, falls Sie mehrere **Recordset** -Objekte öffnen möchten, oder wenn Sie mehrere Befehle ausführen. Mit dem Kurzbefehl **Recordset.Open** wird von ADO weiterhin implizit eine Verbindung erstellt.</span><span class="sxs-lookup"><span data-stu-id="93ae1-p104">When should you use a **Connection** object vs. the **Recordset.Open** shortcut? Use the **Connection** object if you plan to open more than one **Recordset**, or when executing multiple commands. A connection is still created by ADO implicitly when you use the **Recordset.Open** shortcut.</span></span>


