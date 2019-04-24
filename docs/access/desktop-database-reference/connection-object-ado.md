---
title: Connection-Objekt (ADO)
TOCTitle: Connection object (ADO)
ms:assetid: c16023aa-0321-2513-ee71-255d6ffba03d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249940(v=office.15)
ms:contentKeyID: 48547528
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231105
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: ed736a0e52ff45cd0fed63f1ba5bd7060d7a2380
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295877"
---
# <a name="connection-object-ado"></a><span data-ttu-id="f2264-102">Connection-Objekt (ADO)</span><span class="sxs-lookup"><span data-stu-id="f2264-102">Connection object (ADO)</span></span>

<span data-ttu-id="f2264-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f2264-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f2264-104">Stellt eine offene Verbindung zu einer Datenquelle dar.</span><span class="sxs-lookup"><span data-stu-id="f2264-104">Represents an open connection to a data source.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2264-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f2264-105">Remarks</span></span>

<span data-ttu-id="f2264-p101">Ein **Connection** -Objekt stellt eine eindeutige Sitzung mit einer Datenquelle dar. Bei einem Client-/Server-Datenbanksystem kann es einer tatsächlichen Netzwerkverbindung mit dem Server entsprechen. Abhängig von der vom Anbieter unterstützten Funktionalität sind bestimmte Auflistungen, Methoden oder Eigenschaften eines **Connection** -Objekts möglicherweise nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f2264-p101">A **Connection** object represents a unique session with a data source. In the case of a client/server database system, it may be equivalent to an actual network connection to the server. Depending on the functionality supported by the provider, some collections, methods, or properties of a **Connection** object may not be available.</span></span>

<span data-ttu-id="f2264-109">Die Auflistungen, Methoden und Eigenschaften eines **Connection** -Objekts ermöglichen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="f2264-109">With the collections, methods, and properties of a **Connection** object, you can do the following:</span></span>

  - <span data-ttu-id="f2264-p102">Konfigurieren der Verbindung vor dem Öffnen mit den Eigenschaften [ConnectionString](connectionstring-property-ado.md), [ConnectionTimeout](connectiontimeout-property-ado.md) und [Mode](mode-property-ado.md). **ConnectionString** ist die Standardeigenschaft des **Connection** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="f2264-p102">Configure the connection before opening it with the [ConnectionString](connectionstring-property-ado.md), [ConnectionTimeout](connectiontimeout-property-ado.md), and [Mode](mode-property-ado.md) properties. **ConnectionString** is the default property of the **Connection** object.</span></span>

  - <span data-ttu-id="f2264-112">Festlegen der [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft auf den Client, der den [Microsoft Cursor Service für OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md), der Batchaktualisierungen unterstützt, aufrufen soll.</span><span class="sxs-lookup"><span data-stu-id="f2264-112">Set the [CursorLocation](cursorlocation-property-ado.md) property to client to invoke the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md), which supports batch updates.</span></span>

  - <span data-ttu-id="f2264-113">Festlegen der Standarddatenbank für die Verbindung mit der [DefaultDatabase](defaultdatabase-property-ado.md)-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f2264-113">Set the default database for the connection with the [DefaultDatabase](defaultdatabase-property-ado.md) property.</span></span>

  - <span data-ttu-id="f2264-114">Festlegen der Isolationsebene für die Transaktionen, die auf der Verbindung geöffnet wurden, mit der [IsolationLevel](isolationlevel-property-ado.md)-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f2264-114">Set the level of isolation for the transactions opened on the connection with the [IsolationLevel](isolationlevel-property-ado.md) property.</span></span>

  - <span data-ttu-id="f2264-115">Festlegen eines OLE DB-Anbieters mit der [Provider](provider-property-ado.md)-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f2264-115">Specify an OLE DB provider with the [Provider](provider-property-ado.md) property.</span></span>

  - <span data-ttu-id="f2264-116">Einrichten und nachfolgendes Beenden der physikalischen Verbindung mit der Datenquelle mit den Methoden [Open](open-method-ado-connection.md) und [Close](close-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="f2264-116">Establish, and later break, the physical connection to the data source with the [Open](open-method-ado-connection.md) and [Close](close-method-ado.md) methods.</span></span>

  - <span data-ttu-id="f2264-117">Ausführen eines Befehls auf der Verbindung mit der [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection)-Methode und Konfigurieren der Ausführung mit der [CommandTimeout](commandtimeout-property-ado.md)-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f2264-117">Execute a command on the connection with the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) method and configure the execution with the [CommandTimeout](commandtimeout-property-ado.md) property.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="f2264-p103">To execute a query without using a Command object, pass a query string to the **Execute** method of a **Connection** object. However, a [Command](command-object-ado.md) object is required when you want to persist the command text and re-execute it, or use query parameters.</span><span class="sxs-lookup"><span data-stu-id="f2264-p103">To execute a query without using a Command object, pass a query string to the **Execute** method of a **Connection** object. However, a [Command](command-object-ado.md) object is required when you want to persist the command text and re-execute it, or use query parameters.</span></span>

  - <span data-ttu-id="f2264-120">Verwalten der Transaktionen auf der offenen Verbindung, einschließlich geschachtelter Transaktionen, sofern sie vom Anbieter unterstützt werden, mit den Methoden [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md), [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) und [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) und der [Attributes](attributes-property-ado.md)-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f2264-120">Manage transactions on the open connection, including nested transactions if the provider supports them, with the [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md), [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md), and [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) methods and the [Attributes](attributes-property-ado.md) property.</span></span>

  - <span data-ttu-id="f2264-121">Untersuchen der von der Datenquelle zurückgegebenen Fehler mit der [Errors](errors-collection-ado.md)-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="f2264-121">Examine errors returned from the data source with the [Errors](errors-collection-ado.md) collection.</span></span>

  - <span data-ttu-id="f2264-122">Lesen der Version der ADO-Implementierung mit der [Version](version-property-ado.md)-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f2264-122">Read the version from the ADO implementation used with the [Version](version-property-ado.md) property.</span></span>

  - <span data-ttu-id="f2264-123">Erhalten von Schemainformationen über die Datenbank mit der [OpenSchema](openschema-method-ado.md)-Methode.</span><span class="sxs-lookup"><span data-stu-id="f2264-123">Obtain schema information about your database with the [OpenSchema](openschema-method-ado.md) method.</span></span>

<span data-ttu-id="f2264-124">Sie können **Connection** -Objekte unabhängig von allen zuvor definierten Objekten erstellen.</span><span class="sxs-lookup"><span data-stu-id="f2264-124">You can create **Connection** objects independently of any other previously defined object.</span></span>

<span data-ttu-id="f2264-125">Sie können Befehle oder gespeicherte Prozeduren wie systemeigene Methoden des **Connection** -Objekts verwenden, wie im Folgenden beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f2264-125">You can execute commands or stored procedures as if they were native methods on the **Connection** object, as illustrated below.</span></span>

### <a name="execute-a-command-as-a-native-method-of-a-connection-object"></a><span data-ttu-id="f2264-126">Ausführen eines Befehls als systemeigene Methode eines Connection-Objekts</span><span class="sxs-lookup"><span data-stu-id="f2264-126">Execute a command as a native method of a Connection object</span></span>

<span data-ttu-id="f2264-p104">Zum Ausführen eines Befehls geben Sie ihm zunächst mithilfe der [Name](name-property-ado.md)-Eigenschaft des **Command**-Objekts einen Namen. Geben Sie für die **ActiveConnection**-Eigenschaft des **Command**-Objekts die entsprechende Verbindung an. Verwenden Sie anschließend eine Anweisung, in der Sie den Befehlsnamen wie eine Methode des **Connection**-Objekts verwenden, gefolgt von beliebigen Parametern und einem **Recordset**-Objekt, sofern Zeilen zurückgegeben werden. Legen Sie die **Recordset**-Eigenschaften fest, um das resultierende **Recordset**-Objekt anzupassen. Beispiel:</span><span class="sxs-lookup"><span data-stu-id="f2264-p104">To execute a command, give the command a name using the **Command** object [Name](name-property-ado.md) property. Set the **Command** object's **ActiveConnection** property to the connection. Then issue a statement where the command name is used as if it were a method on the **Connection** object, followed by any parameters, then followed by a **Recordset** object if any rows are returned. Set the **Recordset** properties to customize the resulting **Recordset**. For example:</span></span>

```vb
    Dim cnn As New ADODB.Connection
    Dim cmd As New ADODB.Command
    Dim rst As New ADODB.Recordset
    ...
    cnn.Open "..."
    cmd.Name = "yourCommandName"
    cmd.ActiveConnection = cnn
    ...
    'Your command name, any parameters, and an optional Recordset.
    cnn.yourCommandName "parameter", rst
```

### <a name="execute-a-stored-procedure-as-a-native-method-of-a-connection-object"></a><span data-ttu-id="f2264-132">Ausführen einer gespeicherten Prozedur als systemeigene Methode eines Connection-Objekts</span><span class="sxs-lookup"><span data-stu-id="f2264-132">Execute a stored procedure as a native method of a Connection object</span></span>

<span data-ttu-id="f2264-p105">Verwenden Sie zum Ausführen einer gespeicherten Prozedur eine Anweisung, in der Sie den Namen der gespeicherten Prozedur wie eine Methode des **Connection**-Objekts und gefolgt von beliebigen Parametern angeben. ADO verwendet geeignet erscheinende Parametertypen. Beispiel:</span><span class="sxs-lookup"><span data-stu-id="f2264-p105">To execute a stored procedure, issue a statement where the stored procedure name is used as if it were a method on the **Connection** object, followed by any parameters. ADO will make a "best guess" of parameter types. For example:</span></span>

```vb
    Dim cnn As New ADODB.Connection
    ...
    'Your stored procedure name and any parameters.
    cnn.sp_yourStoredProcedureName "parameter"
```
