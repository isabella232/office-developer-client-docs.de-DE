---
title: Workspace-Objekt (DAO)
TOCTitle: Workspace Object
ms:assetid: bf3ab863-5e9a-4842-1f82-2ccf958d9779
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822782(v=office.15)
ms:contentKeyID: 48547481
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 2c734d5e0f022faec4ebb9efe2dfc2f7dd7b7979
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711581"
---
# <a name="workspace-object-dao"></a><span data-ttu-id="ff759-102">Workspace-Objekt (DAO)</span><span class="sxs-lookup"><span data-stu-id="ff759-102">Workspace object (DAO)</span></span>

<span data-ttu-id="ff759-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ff759-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ff759-p101">Ein **Arbeitsbereichs** objekt definiert eine benannte Sitzung für einen Benutzer. Es enthält geöffnete Datenbanken und stellt Mechanismen für gleichzeitige Transaktionen und in Microsoft Access Arbeitsbereiche für den sicheren Arbeitsgruppen-Support bereit.</span><span class="sxs-lookup"><span data-stu-id="ff759-p101">A **Workspace** object defines a named session for a user. It contains open databases and provides mechanisms for simultaneous transactions and, in Microsoft Access workspaces, secure workgroup support.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff759-106">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ff759-106">Remarks</span></span>

<span data-ttu-id="ff759-p102">Ein **Arbeitsbereich** ist ein nicht persistentes Objekt, das definiert, wie die Anwendung mit Daten interagiert, indem es das Microsoft Access-Datenbank verwendet. Verwenden Sie ein **Arbeitsbereichs** objekt, um die aktuelle Sitzung zu verwalten oder eine zusätzliche Sitzung zu starten. In einer SItzung können Sie mehrere Datenbanken oder Verbindungen öffnen und Transaktionen verwalten. Sie können beispielsweise folgende Aktionen durchführen:</span><span class="sxs-lookup"><span data-stu-id="ff759-p102">A **Workspace** is a non-persistent object that defines how your application interacts with data by using the Microsoft Access database engine. Use the **Workspace** object to manage the current session or to start an additional session. In a session, you can open multiple databases or connections, and manage transactions. For example, you can:</span></span>

- <span data-ttu-id="ff759-p103">Verwenden Sie die **Name** -, **UserName** - und **Type** -Eigenschaften, um eine benannte Sitzung einzurichten. Die Sitzung erstellt einen Bereich, in dem Sie mehrere Datenbanken öffnen und eine Instanz verschachtelter Transaktionen durchführen.</span><span class="sxs-lookup"><span data-stu-id="ff759-p103">Use the **Name**, **UserName**, and **Type** properties to establish a named session. The session creates a scope in which you can open multiple databases and conduct one instance of nested transactions.</span></span>

- <span data-ttu-id="ff759-113">Verwenden Sie die **Close** -Methode, um eine Sitzung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="ff759-113">Use the **Close** method to terminate a session.</span></span>

- <span data-ttu-id="ff759-114">Verwenden Sie die **OpenDatabase** -Methode, um eine oder mehrere vorhandene Datenbanken eines **Arbeitsbereichs** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ff759-114">Use the **OpenDatabase** method to open one or more existing databases on a **Workspace**.</span></span>

- <span data-ttu-id="ff759-115">Verwenden Sie die **BeginTrans** -, **CommitTrans** - und **Rollback** -methoden, um das Verarbeiten von verschachtelten Transaktionen innerhalb eines **Arbeitsbereichs** und mehrere **Arbeitsbereichs** objekte zum Durchführen mehrerer gleichzeitiger sich überschneidender Transaktionen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ff759-115">Use the **BeginTrans**, **CommitTrans**, and **Rollback** methods to manage nested transaction processing within a **Workspace** and use several **Workspace** objects to conduct multiple, simultaneous, and overlapping transactions.</span></span>

<span data-ttu-id="ff759-116">Wenn Sie zuerst finden Sie unter oder ein **Workspace** -Objekt verwenden, erstellen Sie automatisch den Standard-Arbeitsbereich DBEngine.Workspaces(0).</span><span class="sxs-lookup"><span data-stu-id="ff759-116">When you first refer to or use a **Workspace** object, you automatically create the default workspace, DBEngine.Workspaces(0).</span></span> <span data-ttu-id="ff759-117">Die Einstellungen der Eigenschaften **Name** und **UserName** des Standard-Arbeitsbereich sind "\#Standard-Arbeitsbereich\#" und "Admin" fest.</span><span class="sxs-lookup"><span data-stu-id="ff759-117">The settings of the **Name** and **UserName** properties of the default workspace are "\#Default Workspace\#" and "Admin," respectively.</span></span> <span data-ttu-id="ff759-118">Wenn die Sicherheit aktiviert ist, lautet ist die **UserName** -Eigenschaftseinstellung der Name des angemeldeten Benutzers.</span><span class="sxs-lookup"><span data-stu-id="ff759-118">If security is enabled, the **UserName** property setting is the name of the user who logged on.</span></span>

<span data-ttu-id="ff759-p105">Bei der Verwendung von Transaktionen sind alle im **Arbeitsbereich** angegebenen Datenbanken betroffen - sogar wenn mehrere **Datenbank** objekte im **Arbeitsbereich** geöffnet sind. Wenn Sie beispielsweise eine **BeginTrans** -Methode verwenden, aktualisieren Sie mehrere Datensätze in einer Datenbank und löschen Sie anschließend die Datensätze in einer anderen Datenbank. Wenn Sie anschließend die **Rollback** -Methode verwenden, werden die Aktualisierungs- und Löschvorgänge abgebrochen und zurückgesetzt. Sie können zusätzliche **Arbeitsbereichs** objekte erstellen, um Transaktionen unabhängig zwischen **Datenbank** objekten zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="ff759-p105">When you use transactions, all databases in the specified **Workspace** are affected— even if multiple **Database** objects are opened in the **Workspace**. For example, you use a **BeginTrans** method, update several records in a database, and then delete records in another database. If you then use the **Rollback** method, both the update and delete operations are canceled and rolled back. You can create additional **Workspace** objects to manage transactions independently across **Database** objects.</span></span>

<span data-ttu-id="ff759-p106">Sie können **Arbeitsbereichs** objekte mit der **CreateWorkspace** -Methode erstellen. Nachdem Sie ein neues **Arbeitsbereichs** objekt erstellt haben, müssen Sie es an die **Arbeitsbereichs** auflistung anhängen, wenn Sie aus der **Arbeitsbereichs** auflistung darauf verweisen müssen.</span><span class="sxs-lookup"><span data-stu-id="ff759-p106">You can create **Workspace** objects with the **CreateWorkspace** method. After you create a new **Workspace** object, you must append it to the **Workspaces** collection if you need to refer to it from the **Workspaces** collection.</span></span>

<span data-ttu-id="ff759-p107">Sie können ein neu erstelltes **Arbeitsbereichs** objekt verwenden, ohne es an die **Arbeitsbereichs** auflistung anhängen zu müssen. Sie müssen jedoch durch die Objektvariable darauf verweisen, der sie es zugewiesen haben.</span><span class="sxs-lookup"><span data-stu-id="ff759-p107">You can use a newly created **Workspace** object without appending it to the **Workspaces** collection. However, you must refer to it by the object variable to which you have assigned it.</span></span>

<span data-ttu-id="ff759-127">Um auf ein **Arbeitsbereichs** objekt in einer Auflistung durch die Ordinalzahl oder die **Name** -Eigenschaftseinstellung zu verweisen, verwenden Sie eine der folgenden Syntaxformen:</span><span class="sxs-lookup"><span data-stu-id="ff759-127">To refer to a **Workspace** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="ff759-128">**DBEngine**. **Arbeitsbereiche** (0)</span><span class="sxs-lookup"><span data-stu-id="ff759-128">**DBEngine**.**Workspaces**(0)</span></span>

<span data-ttu-id="ff759-129">**DBEngine**. **Arbeitsbereiche** ("Name")</span><span class="sxs-lookup"><span data-stu-id="ff759-129">**DBEngine**.**Workspaces**("name")</span></span>

<span data-ttu-id="ff759-130">**DBEngine**. **Arbeitsbereiche** \! \[Namen\]</span><span class="sxs-lookup"><span data-stu-id="ff759-130">**DBEngine**.**Workspaces**\!\[name\]</span></span>

> [!NOTE]
> <span data-ttu-id="ff759-p108">[!HINWEIS] ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ff759-p108">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


## <a name="example"></a><span data-ttu-id="ff759-133">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ff759-133">Example</span></span>

<span data-ttu-id="ff759-p109">In diesem Beispiel wird ein neues Microsoft Access-Arbeitsbereichsobjekt erstellt und an die **Arbeitsbereichs** auflistung angehängt. Anschließend werden die **Arbeitsbereichs** auflistungen und die **Eigenschafts** auflistung des **Arbeitsbereichs** objekts aufgezählt.</span><span class="sxs-lookup"><span data-stu-id="ff759-p109">This example creates a new Microsoft Access Workspace object and appends it to the **Workspaces** collection. It then enumerates the **Workspaces** collections and the **Properties** collection of the **Workspace** object.</span></span>

```vb 
Sub WorkspaceX() 
 
   Dim wrkNewAcc As Workspace 
   Dim wrkLoop As Workspace 
   Dim prpLoop As Property 
 
   ' Create a new Microsoft Access workspace. 
   Set wrkNewAcc = CreateWorkspace("NewAccessWorkspace", _ 
      "admin", "", dbUseJet) 
   Workspaces.Append wrkNewAcc 
 
   ' Enumerate the Workspaces collection. 
   For Each wrkLoop In Workspaces 
      With wrkLoop 
         Debug.Print "Properties of " & .Name 
         ' Enumerate the Properties collection of the new 
         ' Workspace object. 
         For Each prpLoop In .Properties 
            On Error Resume Next 
            If prpLoop <> "" Then Debug.Print "  " & _ 
               prpLoop.Name & " = " & prpLoop 
            On Error GoTo 0 
         Next prpLoop 
      End With 
   Next wrkLoop 
 
   wrkNewAcc.Close 
End Sub 
```

<br/>

<span data-ttu-id="ff759-p110">In diesem Beispiel wird die **CreateWorkspace** -Methode verwendet, um einen Microsoft Access-Arbeitsbereich zu erstellen. Anschließend werden die Eigenschaften des Arbeitsbereichs aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="ff759-p110">This example uses the **CreateWorkspace** method to create a Microsoft Access workspace. It then lists the properties of theworkspace.</span></span>

```vb 
Sub CreateWorkspaceX() 
 
   Dim wrkAcc As Workspace 
   Dim wrkLoop As Workspace 
   Dim prpLoop As Property 
 
 
   DefaultType = dbUseJet 
   ' Create an unnamed Workspace object of the type  
   ' specified by the DefaultType property of DBEngine  
   ' (dbUseJet). 
   Set wrkAcc = CreateWorkspace("", "admin", "") 
 
   ' Enumerate Workspaces collection. 
   Debug.Print "Workspace objects in Workspaces collection:" 
   For Each wrkLoop In Workspaces 
      Debug.Print "  " & wrkLoop.Name 
   Next wrkLoop 
 
   With wrkAcc 
      ' Enumerate Properties collection of Microsoft Access  
      ' workspace. 
      Debug.Print _ 
         "Properties of unnamed Microsoft Access workspace" 
      On Error Resume Next 
      For Each prpLoop In .Properties 
         Debug.Print "  " & prpLoop.Name & " = " & prpLoop 
      Next prpLoop 
      On Error GoTo 0 
   End With 
 
   wrkAcc.Close 
 
End Sub 
```

<br/>

<span data-ttu-id="ff759-138">Im folgenden Beispiel wird aufgezeigt, wie eine Transaktion in einem Data Access Objects (DAO)-Arbeitsbereich verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ff759-138">The following example shows how to use a transaction in a Data Access Objects (DAO) workspace.</span></span>

<span data-ttu-id="ff759-139">**Beispielcode von** der [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="ff759-139">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>


```vb
    Public Sub TransferFunds()
        Dim wrk As DAO.Workspace
        Dim dbC As DAO.Database
        Dim dbX As DAO.Database
        
        Set wrk = DBEngine(0)
        Set dbC = CurrentDb
        Set dbX = wrk.OpenDatabase("e:\books\acc2007vba\myDB.accdb")
        
        On Error GoTo trans_Err
        
        'Begin the transaction
        
        wrk.BeginTrans
        
        'Withdraw funds from one account table
        dbC.Execute "INSERT INTO tblAccounts ( Amount, Txn, TxnDate ) SELECT -20, 'DEBIT', Date()", dbFailOnError
    
        'Deposit funds into another account table
        dbX.Execute "INSERT INTO tblAccounts ( Amount, Txn, TxnDate ) SELECT 20, 'CREDIT', Date()", dbFailOnError
        
        'Commit the transaction
        wrk.CommitTrans dbForceOSFlush
        
    trans_Exit:
        'Clean up
        wrk.Close
        Set dbC = Nothing
        Set dbX = Nothing
        Set wrk = Nothing
        Exit Sub
        
    trans_Err:
        'Roll back the transaction
        wrk.Rollback
        Resume trans_Exit
        
    End Sub
```
