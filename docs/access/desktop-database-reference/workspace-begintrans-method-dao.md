---
title: Workspace.BeginTrans-Methode (DAO)
TOCTitle: BeginTrans Method
ms:assetid: aa7c3bf8-fb08-9360-5998-4bf3f721ecbb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821457(v=office.15)
ms:contentKeyID: 48546948
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 80ac6232c8fcb634882e04ee53cfd548131c20e4
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927711"
---
# <a name="workspacebegintrans-method-dao"></a><span data-ttu-id="a1ba6-102">Workspace.BeginTrans-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="a1ba6-102">Workspace.BeginTrans method (DAO)</span></span>

<span data-ttu-id="a1ba6-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a1ba6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a1ba6-p101">Startet eine neue Transaktion. **Database** -Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a1ba6-p101">Begins a new transaction. Read/write **Database**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1ba6-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1ba6-106">Syntax</span></span>

<span data-ttu-id="a1ba6-107">*Ausdruck* . BeginTrans</span><span class="sxs-lookup"><span data-stu-id="a1ba6-107">*expression* .BeginTrans</span></span>

<span data-ttu-id="a1ba6-108">*Ausdruck* Eine Variable, die ein **Workspace** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="a1ba6-108">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1ba6-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a1ba6-109">Remarks</span></span>

<span data-ttu-id="a1ba6-p102">Mithilfe der Transaktionsmethoden **BeginTrans**, **CommitTrans** und **Rollback** wird die Transaktionsverarbeitung während einer Sitzung verwaltet, die durch ein **Workspace**-Objekt definiert wurde. Sie verwenden diese Methoden mit einem **Workspace**-Objekt, wenn Sie eine Reihe von an den Datenbanken vorgenommenen Änderungen in einer Sitzung als eine Einheit verarbeiten möchten.</span><span class="sxs-lookup"><span data-stu-id="a1ba6-p102">The transaction methods **BeginTrans**, **CommitTrans**, and **Rollback** manage transaction processing during a session defined by a **Workspace** object. You use these methods with a **Workspace** object when you want to treat a series of changes made to the databases in a session as one unit.</span></span>

<span data-ttu-id="a1ba6-p103">In der Regel verwenden Sie Transaktionen zur Wahrung der Integrität Ihrer Daten, wenn Sie Datensätze in mindestens zwei Tabellen aktualisieren und gleichzeitig sicherstellen müssen, dass die Änderungen in allen Tabellen (Commit) oder in keiner der Tabellen (Rollback) ausgeführt wurden. Beispielsweise subtrahieren Sie zum Übertragen von Geldbeträgen zwischen Konten einen Betrag von einem Konto und addieren ihn dann zu einem anderen Konto. Wenn eine der Aktualisierungen fehlschlägt, sind die Konten nicht mehr ausgeglichen. Verwenden Sie vor dem Aktualisieren des ersten Datensatzes die **BeginTrans**-Methode. Falls nachfolgende Aktualisierungen fehlschlagen, können Sie anschließend mithilfe der **Rollback**-Methode sämtliche Aktualisierungen rückgängig machen. Verwenden Sie die **CommitTrans**-Methode, nachdem Sie den letzten Datensatz erfolgreich aktualisiert haben.</span><span class="sxs-lookup"><span data-stu-id="a1ba6-p103">Typically, you use transactions to maintain the integrity of your data when you must both update records in two or more tables and ensure changes are completed (committed) in all tables or none at all (rolled back). For example, if you transfer money from one account to another, you might subtract an amount from one and add the amount to another. If either update fails, the accounts no longer balance. Use the **BeginTrans** method before updating the first record, and then, if any subsequent update fails, you can use the **Rollback** method to undo all of the updates. Use the **CommitTrans** method after you successfully update the last record.</span></span>

> [!NOTE]
> <span data-ttu-id="a1ba6-p104">[!HINWEIS] Innerhalb eines **Workspace**-Objekts sind Transaktionen für **Workspace** immer global und nicht auf ein **Connection**- oder **Database**-Objekt beschränkt. Wenn Sie Operationen für mehrere Verbindungen oder Datenbanken innerhalb einer **Workspace**-Transaktion durchführen, wirkt sich das Auflösen der Transaktion (d. h. die Verwendung der **CommitTrans**- oder **Rollback**-Methode) auf alle Operationen für sämtliche Verbindungen und Datenbanken innerhalb dieses Arbeitsbereichs aus.</span><span class="sxs-lookup"><span data-stu-id="a1ba6-p104">Within one **Workspace** object, transactions are always global to the **Workspace** and aren't limited to only one **Connection** or **Database** object. If you perform operations on more than one connection or database within a **Workspace** transaction, resolving the transaction (that is, using the **CommitTrans** or **Rollback** method) affects all operations on all connections and databases within that workspace.</span></span>

<span data-ttu-id="a1ba6-p105">Nach Verwendung von **CommitTrans** können Sie an dieser Transaktion vorgenommene Änderungen nur dann rückgängig machen, wenn die Transaktion in einer anderen Transaktion geschachtelt ist, für die ein Rollback ausgeführt wurde. Wenn Sie Transaktionen schachteln, müssen Sie die aktuelle Transaktion auflösen, bevor Sie eine Transaktion auf einer höheren Schachtelungsebene auflösen können.</span><span class="sxs-lookup"><span data-stu-id="a1ba6-p105">After you use **CommitTrans**, you can't undo changes made during that transaction unless the transaction is nested within another transaction that is itself rolled back. If you nest transactions, you must resolve the current transaction before you can resolve a transaction at a higher level of nesting.</span></span>

<span data-ttu-id="a1ba6-121">Wenn Sie gleichzeitige Transaktionen mit überlappenden, nicht geschachtelten Bereichen wünschen, können Sie zusätzliche **Workspace**-Objekte für die gleichzeitigen Transaktionen erstellen.</span><span class="sxs-lookup"><span data-stu-id="a1ba6-121">If you want to have simultaneous transactions with overlapping, non-nested scopes, you can create additional **Workspace** objects to contain the concurrent transactions.</span></span>

<span data-ttu-id="a1ba6-122">Wenn Sie ein **Workspace**-Objekt schließen, ohne ausstehende Transaktionen aufzulösen, wird automatisch ein Rollback für die Transaktionen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a1ba6-122">If you close a **Workspace** object without resolving any pending transactions, the transactions are automatically rolled back.</span></span>

<span data-ttu-id="a1ba6-123">Wenn Sie die **CommitTrans**- oder **Rollback**-Methode verwenden, ohne vorher die **BeginTrans**-Methode verwendet zu haben, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="a1ba6-123">If you use the **CommitTrans** or **Rollback** method without first using the **BeginTrans** method, an error occurs.</span></span>

<span data-ttu-id="a1ba6-124">Einige ISAM-Datenbanken, die in einem Microsoft Access-Arbeitsbereich verwendet unterstützen möglicherweise keine Transaktionen, in diesem Fall wird die **Transactions** -Eigenschaft des **Database** -Objekt oder **Recordset** -Objekts **False**.</span><span class="sxs-lookup"><span data-stu-id="a1ba6-124">Some ISAM databases used in a Microsoft Access workspace may not support transactions, in which case the **Transactions** property of the **Database** object or **Recordset** object is **False**.</span></span> <span data-ttu-id="a1ba6-125">Überprüfen Sie den Wert der **Transaktionen** -Eigenschaft des **Database** -Objekts, um sicherzustellen, dass die Datenbank Transaktionen unterstützt, bevor Sie die **BeginTrans** -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="a1ba6-125">To make sure the database supports transactions, check the value of the **Transactions** property of the **Database** object before using the **BeginTrans** method.</span></span> <span data-ttu-id="a1ba6-126">Wenn Sie ein **Recordset** -Objekt basierend auf mehrere Datenbanken verwenden, überprüfen Sie die **Transactions** -Eigenschaft des **Recordset** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="a1ba6-126">If you are using a **Recordset** object based on more than one database, check the **Transactions** property of the **Recordset** object.</span></span> 

<span data-ttu-id="a1ba6-127">Wenn ein **Recordset** vollständig auf Tabellen des Microsoft Access-Datenbankmoduls basiert, können Sie immer Transaktionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="a1ba6-127">If a **Recordset** is based entirely on Microsoft Access database engine tables, you can always use transactions.</span></span> <span data-ttu-id="a1ba6-128">**Recordset** -Objekte auf Tabellen, die von anderen Datenbankprodukten erstellt wurde, jedoch basieren, möglicherweise Transaktionen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a1ba6-128">**Recordset** objects based on tables created by other database products, however, may not support transactions.</span></span> <span data-ttu-id="a1ba6-129">Sie können nicht beispielsweise Transaktionen in einem **Recordset-Objekt** basierend auf einer Paradox-Tabelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="a1ba6-129">For example, you can't use transactions in a **Recordset** based on a Paradox table.</span></span> <span data-ttu-id="a1ba6-130">In diesem Fall wird die **Transactions** -Eigenschaft **False**.</span><span class="sxs-lookup"><span data-stu-id="a1ba6-130">In this case, the **Transactions** property is **False**.</span></span> <span data-ttu-id="a1ba6-131">Wenn die **Datenbank** oder **Recordset-Objekt** nicht Transaktionen unterstützt, die Methoden werden ignoriert, und tritt kein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="a1ba6-131">If the **Database** or **Recordset** doesn't support transactions, the methods are ignored and no error occurs.</span></span>

<span data-ttu-id="a1ba6-132">Wenn Sie über das Microsoft Access-Datenbankmodul auf ODBC-Datenquellen zugreifen, können Sie Transaktionen nicht schachteln.</span><span class="sxs-lookup"><span data-stu-id="a1ba6-132">You can't nest transactions if you are accessing ODBC data sources through the Microsoft Access database engine.</span></span>

<span data-ttu-id="a1ba6-p108">Wenn Sie in ODBC-Arbeitsbereichen **CommitTrans** verwenden, ist der Cursor möglicherweise nicht mehr gültig. Zeigen Sie die Änderungen im **Recordset**-Objekt mithilfe der **Requery**-Methode an, oder schließen Sie das **Recordset**-Objekt, und öffnen Sie es erneut.</span><span class="sxs-lookup"><span data-stu-id="a1ba6-p108">In ODBC workspaces, when you use **CommitTrans** your cursor may no longer be valid. Use the **Requery** method to view the changes in the **Recordset**, or close and re-open the **Recordset**.</span></span>

> [!NOTE]
> - <span data-ttu-id="a1ba6-p109">Die Leistung der Anwendung lässt sich oftmals dadurch verbessern, dass Operationen unterbrochen werden, die Datenträgerzugriff auf Transaktionsblöcke erfordern. So werden die Operationen zwischengespeichert, und die Zugriffe auf den Datenträger können deutlich verringert werden.</span><span class="sxs-lookup"><span data-stu-id="a1ba6-p109">You can often improve the performance of your application by breaking operations that require disk access into transaction blocks. This buffers your operations and may significantly reduce the number of times a disk is accessed.</span></span>
> - <span data-ttu-id="a1ba6-p110">In einem Microsoft Access-Arbeitsbereich werden Transaktionen in einer Datei protokolliert, die in dem Verzeichnis gespeichert ist, das durch die Umgebungsvariable TEMP auf der Arbeitsstation festgelegt ist. Wenn der Speicherplatz des TEMP-Laufwerks für die Protokolldatei nicht ausreicht, löst das Datenbankmodul einen Laufzeitfehler aus. Wenn Sie nun **CommitTrans** verwenden, wird ein Commit für eine unbestimmte Anzahl von Operationen ausgeführt. Die übrigen Operationen gehen verloren, und die Operation muss neu gestartet werden. Bei Verwendung einer **Rollback**-Methode wird das Transaktionsprotokoll freigegeben, und für sämtliche Operationen in der Transaktion wird ein Rollback ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a1ba6-p110">In a Microsoft Access workspace, transactions are logged in a file kept in the directory specified by the TEMP environment variable on the workstation. If the transaction log file exhausts the available storage on your TEMP drive, the database engine triggers a run-time error. At this point, if you use **CommitTrans**, an indeterminate number of operations are committed, but the remaining uncompleted operations are lost, and the operation has to be restarted. Using a **Rollback** method releases the transaction log and rolls back all operations in the transaction.</span></span>
> - <span data-ttu-id="a1ba6-141">Wenn Sie den Klon eines **Recordset**-Objekts in einer ausstehenden Transaktion schließen, wird eine implizite **Rollback**-Operation verursacht.</span><span class="sxs-lookup"><span data-stu-id="a1ba6-141">Closing a clone **Recordset** within a pending transaction will cause an implicit **Rollback** operation.</span></span>

## <a name="example"></a><span data-ttu-id="a1ba6-142">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a1ba6-142">Example</span></span>

<span data-ttu-id="a1ba6-143">Im folgenden Beispiel wird aufgezeigt, wie eine Transaktion in einem Data Access Objects (DAO)-Arbeitsbereich verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a1ba6-143">The following example shows how to use a transaction in a Data Access Objects (DAO) workspace.</span></span>

<span data-ttu-id="a1ba6-144">**Beispielcode von** der [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="a1ba6-144">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
