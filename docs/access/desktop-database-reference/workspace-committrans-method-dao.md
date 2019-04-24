---
title: Workspace. CommitTrans-Methode (DAO)
TOCTitle: CommitTrans Method
ms:assetid: e6d129fb-a578-5c79-9c16-6444519f0daf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835985(v=office.15)
ms:contentKeyID: 48548391
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 52af229f03b7ea10510f3e580ba2c4e12784e461
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306034"
---
# <a name="workspacecommittrans-method-dao"></a><span data-ttu-id="d3e1c-102">Workspace. CommitTrans-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="d3e1c-102">Workspace.CommitTrans method (DAO)</span></span>

<span data-ttu-id="d3e1c-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d3e1c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d3e1c-104">Beendet die aktuelle Transaktion und speichert die Änderungen.</span><span class="sxs-lookup"><span data-stu-id="d3e1c-104">Ends the current transaction and saves the changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3e1c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3e1c-105">Syntax</span></span>

<span data-ttu-id="d3e1c-106">*Ausdruck* . CommitTrans (***Optionen***)</span><span class="sxs-lookup"><span data-stu-id="d3e1c-106">*expression* .CommitTrans(***Options***)</span></span>

<span data-ttu-id="d3e1c-107">*Ausdruck* Eine Variable, die ein **Workspace** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="d3e1c-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="d3e1c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3e1c-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d3e1c-109">Name</span><span class="sxs-lookup"><span data-stu-id="d3e1c-109">Name</span></span></p></th>
<th><p><span data-ttu-id="d3e1c-110">Erforderlich/optional</span><span class="sxs-lookup"><span data-stu-id="d3e1c-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="d3e1c-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="d3e1c-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="d3e1c-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d3e1c-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d3e1c-113"><em>Option</em></span><span class="sxs-lookup"><span data-stu-id="d3e1c-113"><em>Option</em></span></span></p></td>
<td><p><span data-ttu-id="d3e1c-114">Optional</span><span class="sxs-lookup"><span data-stu-id="d3e1c-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="d3e1c-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="d3e1c-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="d3e1c-116">In einem Microsoft Access-Arbeitsbereich können Sie die <strong>dbForceOSFlush</strong>-Konstante in <strong>CommitTrans</strong> einfügen.</span><span class="sxs-lookup"><span data-stu-id="d3e1c-116">In a Microsoft Access workspace, you can include the <strong>dbForceOSFlush</strong> constant with <strong>CommitTrans</strong>.</span></span> <span data-ttu-id="d3e1c-117">Dadurch wird das Datenbankmodul gezwungen, alle Aktualisierungen sofort auf den Datenträger zu leeren, statt sie temporär zu speichern.</span><span class="sxs-lookup"><span data-stu-id="d3e1c-117">This forces the database engine to immediately flush all updates to disk, instead of caching them temporarily.</span></span> <span data-ttu-id="d3e1c-118">Ohne diese Option besteht die Gefahr, dass ein Benutzer direkt nach dem Aufrufen von <strong>CommitTrans</strong> durch das Anwendungsprogramm die Kontrolle übernimmt und den Computer ausschaltet, ohne dass die Daten auf einen Datenträger geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="d3e1c-118">Without using this option, a user could get control back immediately after the application program calls <strong>CommitTrans</strong>, turn the computer off, and not have the data written to disk.</span></span> <span data-ttu-id="d3e1c-119">Diese Option kann zwar die Anwendungsleistung beeinträchtigen, ist aber dennoch nützlich in Situationen, in denen der Computer heruntergefahren werden könnte, bevor zwischengespeicherte Aktualisierungen auf einem Datenträger gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="d3e1c-119">While using this option may affect your application's performance, it is useful in situations where the computer could be shut off before cached updates are saved to disk.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d3e1c-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d3e1c-120">Remarks</span></span>

<span data-ttu-id="d3e1c-p102">Mithilfe der Transaktionsmethoden **BeginTrans**, **CommitTrans** und **Rollback** wird die Transaktionsverarbeitung während einer Sitzung verwaltet, die durch ein **Workspace**-Objekt definiert wurde. Sie verwenden diese Methoden mit einem **Workspace**-Objekt, wenn Sie eine Reihe von an den Datenbanken vorgenommenen Änderungen in einer Sitzung als eine Einheit verarbeiten möchten.</span><span class="sxs-lookup"><span data-stu-id="d3e1c-p102">The transaction methods **BeginTrans**, **CommitTrans**, and **Rollback** manage transaction processing during a session defined by a **Workspace** object. You use these methods with a **Workspace** object when you want to treat a series of changes made to the databases in a session as one unit.</span></span>

<span data-ttu-id="d3e1c-p103">In der Regel verwenden Sie Transaktionen zur Wahrung der Integrität Ihrer Daten, wenn Sie Datensätze in mindestens zwei Tabellen aktualisieren und gleichzeitig sicherstellen müssen, dass die Änderungen in allen Tabellen (Commit) oder in keiner der Tabellen (Rollback) ausgeführt wurden. Beispielsweise subtrahieren Sie zum Übertragen von Geldbeträgen zwischen Konten einen Betrag von einem Konto und addieren ihn dann zu einem anderen Konto. Wenn eine der Aktualisierungen fehlschlägt, sind die Konten nicht mehr ausgeglichen. Verwenden Sie vor dem Aktualisieren des ersten Datensatzes die **BeginTrans**-Methode. Falls nachfolgende Aktualisierungen fehlschlagen, können Sie anschließend mithilfe der **Rollback**-Methode sämtliche Aktualisierungen rückgängig machen. Verwenden Sie die **CommitTrans**-Methode, nachdem Sie den letzten Datensatz erfolgreich aktualisiert haben.</span><span class="sxs-lookup"><span data-stu-id="d3e1c-p103">Typically, you use transactions to maintain the integrity of your data when you must both update records in two or more tables and ensure changes are completed (committed) in all tables or none at all (rolled back). For example, if you transfer money from one account to another, you might subtract an amount from one and add the amount to another. If either update fails, the accounts no longer balance. Use the **BeginTrans** method before updating the first record, and then, if any subsequent update fails, you can use the **Rollback** method to undo all of the updates. Use the **CommitTrans** method after you successfully update the last record.</span></span>

> [!NOTE]
> <span data-ttu-id="d3e1c-p104">[!HINWEIS] Innerhalb eines **Workspace**-Objekts sind Transaktionen für **Workspace** immer global und nicht auf ein **Connection**- oder **Database**-Objekt beschränkt. Wenn Sie Operationen für mehrere Verbindungen oder Datenbanken innerhalb einer **Workspace**-Transaktion durchführen, wirkt sich das Auflösen der Transaktion (d. h. die Verwendung der **CommitTrans**- oder **Rollback**-Methode) auf alle Operationen für sämtliche Verbindungen und Datenbanken innerhalb dieses Arbeitsbereichs aus.</span><span class="sxs-lookup"><span data-stu-id="d3e1c-p104">Within one **Workspace** object, transactions are always global to the **Workspace** and aren't limited to only one **Connection** or **Database** object. If you perform operations on more than one connection or database within a **Workspace** transaction, resolving the transaction (that is, using the **CommitTrans** or **Rollback** method) affects all operations on all connections and databases within that workspace.</span></span>

<span data-ttu-id="d3e1c-p105">Nach Verwendung von **CommitTrans** können Sie an dieser Transaktion vorgenommene Änderungen nur dann rückgängig machen, wenn die Transaktion in einer anderen Transaktion geschachtelt ist, für die ein Rollback ausgeführt wurde. Wenn Sie Transaktionen schachteln, müssen Sie die aktuelle Transaktion auflösen, bevor Sie eine Transaktion auf einer höheren Schachtelungsebene auflösen können.</span><span class="sxs-lookup"><span data-stu-id="d3e1c-p105">After you use **CommitTrans**, you can't undo changes made during that transaction unless the transaction is nested within another transaction that is itself rolled back. If you nest transactions, you must resolve the current transaction before you can resolve a transaction at a higher level of nesting.</span></span>

<span data-ttu-id="d3e1c-132">Wenn Sie gleichzeitige Transaktionen mit überlappenden, nicht geschachtelten Bereichen wünschen, können Sie zusätzliche **Workspace**-Objekte für die gleichzeitigen Transaktionen erstellen.</span><span class="sxs-lookup"><span data-stu-id="d3e1c-132">If you want to have simultaneous transactions with overlapping, non-nested scopes, you can create additional **Workspace** objects to contain the concurrent transactions.</span></span>

<span data-ttu-id="d3e1c-133">Wenn Sie ein **Workspace**-Objekt schließen, ohne ausstehende Transaktionen aufzulösen, wird automatisch ein Rollback für die Transaktionen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d3e1c-133">If you close a **Workspace** object without resolving any pending transactions, the transactions are automatically rolled back.</span></span>

<span data-ttu-id="d3e1c-134">Wenn Sie die **CommitTrans**- oder **Rollback**-Methode verwenden, ohne vorher die **BeginTrans**-Methode verwendet zu haben, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="d3e1c-134">If you use the **CommitTrans** or **Rollback** method without first using the **BeginTrans** method, an error occurs.</span></span>

<span data-ttu-id="d3e1c-135">Einige ISAM-Datenbanken, die in einem Microsoft Access-Arbeitsbereich verwendet werden, unter \*\*\*\* stützen möglicherweise keine Transaktionen, in diesem Fall ist die Transactions-Eigenschaft des **Database** -Objekts oder **Recordset** -Objekts **false**.</span><span class="sxs-lookup"><span data-stu-id="d3e1c-135">Some ISAM databases used in a Microsoft Access workspace may not support transactions, in which case the **Transactions** property of the **Database** object or **Recordset** object is **False**.</span></span> <span data-ttu-id="d3e1c-136">Um sicherzustellen, dass die Datenbank Transaktionen unterstützt, überprüfen \*\*\*\* Sie den Wert der Transactions-Eigenschaft des **Database** -Objekts, bevor Sie die BeginTrans-Methode verwenden. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="d3e1c-136">To make sure the database supports transactions, check the value of the **Transactions** property of the **Database** object before using the **BeginTrans** method.</span></span> <span data-ttu-id="d3e1c-137">Wenn Sie ein **Recordset** -Objekt basierend auf mehr als einer Datenbank verwenden, überprüfen Sie die Transactions-Eigenschaft des **Recordset** -Objekts. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="d3e1c-137">If you are using a **Recordset** object based on more than one database, check the **Transactions** property of the **Recordset** object.</span></span> 

<span data-ttu-id="d3e1c-138">Wenn ein **Recordset** -Objekt vollständig auf Tabellen des Microsoft Access-Datenbankmoduls basiert, können Sie immer Transaktionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="d3e1c-138">If a **Recordset** is based entirely on Microsoft Access database engine tables, you can always use transactions.</span></span> <span data-ttu-id="d3e1c-139">**Recordset** -Objekte, die auf Tabellen basieren, die von anderen Datenbankprodukten erstellt wurden, unterstützen jedoch möglicherweise keine Transaktionen.</span><span class="sxs-lookup"><span data-stu-id="d3e1c-139">**Recordset** objects based on tables created by other database products, however, may not support transactions.</span></span> <span data-ttu-id="d3e1c-140">Sie können beispielsweise keine Transaktionen in einem **Recordset** basierend auf einer Paradox-Tabelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="d3e1c-140">For example, you can't use transactions in a **Recordset** based on a Paradox table.</span></span> <span data-ttu-id="d3e1c-141">In diesem Fall ist die \*\*\*\* Transactions-Eigenschaft auf **false festgelegt**.</span><span class="sxs-lookup"><span data-stu-id="d3e1c-141">In this case, the **Transactions** property is **False**.</span></span> <span data-ttu-id="d3e1c-142">Wenn die **Datenbank** oder das **Recordset** -Objekt keine Transaktionen unterstützt, werden die Methoden ignoriert, und es tritt kein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="d3e1c-142">If the **Database** or **Recordset** doesn't support transactions, the methods are ignored and no error occurs.</span></span>

<span data-ttu-id="d3e1c-143">Wenn Sie über das Microsoft Access-Datenbankmodul auf ODBC-Datenquellen zugreifen, können Sie Transaktionen nicht schachteln.</span><span class="sxs-lookup"><span data-stu-id="d3e1c-143">You can't nest transactions if you are accessing ODBC data sources through the Microsoft Access database engine.</span></span>

<span data-ttu-id="d3e1c-p108">Wenn Sie in ODBC-Arbeitsbereichen **CommitTrans** verwenden, ist der Cursor möglicherweise nicht mehr gültig. Zeigen Sie die Änderungen im **Recordset**-Objekt mithilfe der **Requery**-Methode an, oder schließen Sie das **Recordset**-Objekt, und öffnen Sie es erneut.</span><span class="sxs-lookup"><span data-stu-id="d3e1c-p108">In ODBC workspaces, when you use **CommitTrans** your cursor may no longer be valid. Use the **Requery** method to view the changes in the **Recordset**, or close and re-open the **Recordset**.</span></span>

> [!NOTE]
> - <span data-ttu-id="d3e1c-p109">Die Leistung der Anwendung lässt sich oftmals dadurch verbessern, dass Operationen unterbrochen werden, die Datenträgerzugriff auf Transaktionsblöcke erfordern. So werden die Operationen zwischengespeichert, und die Zugriffe auf den Datenträger können deutlich verringert werden.</span><span class="sxs-lookup"><span data-stu-id="d3e1c-p109">You can often improve the performance of your application by breaking operations that require disk access into transaction blocks. This buffers your operations and may significantly reduce the number of times a disk is accessed.</span></span>
> - <span data-ttu-id="d3e1c-p110">In einem Microsoft Access-Arbeitsbereich werden Transaktionen in einer Datei protokolliert, die in dem Verzeichnis gespeichert ist, das durch die Umgebungsvariable TEMP auf der Arbeitsstation festgelegt ist. Wenn der Speicherplatz des TEMP-Laufwerks für die Protokolldatei nicht ausreicht, löst das Datenbankmodul einen Laufzeitfehler aus. Wenn Sie nun **CommitTrans** verwenden, wird ein Commit für eine unbestimmte Anzahl von Operationen ausgeführt. Die übrigen Operationen gehen verloren, und die Operation muss neu gestartet werden. Bei Verwendung einer **Rollback**-Methode wird das Transaktionsprotokoll freigegeben, und für sämtliche Operationen in der Transaktion wird ein Rollback ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d3e1c-p110">In a Microsoft Access workspace, transactions are logged in a file kept in the directory specified by the TEMP environment variable on the workstation. If the transaction log file exhausts the available storage on your TEMP drive, the database engine triggers a run-time error. At this point, if you use **CommitTrans**, an indeterminate number of operations are committed, but the remaining uncompleted operations are lost, and the operation has to be restarted. Using a **Rollback** method releases the transaction log and rolls back all operations in the transaction.</span></span>
> - <span data-ttu-id="d3e1c-152">Wenn Sie den Klon eines **Recordset**-Objekts in einer ausstehenden Transaktion schließen, wird eine implizite **Rollback**-Operation verursacht.</span><span class="sxs-lookup"><span data-stu-id="d3e1c-152">Closing a clone **Recordset** within a pending transaction will cause an implicit **Rollback** operation.</span></span>

## <a name="example"></a><span data-ttu-id="d3e1c-153">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d3e1c-153">Example</span></span>

<span data-ttu-id="d3e1c-154">Im folgenden Beispiel wird aufgezeigt, wie eine Transaktion in einem Data Access Objects (DAO)-Arbeitsbereich verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d3e1c-154">The following example shows how to use a transaction in a Data Access Objects (DAO) workspace.</span></span>

<span data-ttu-id="d3e1c-155">**Der Beispielcode stammt von:**[Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="d3e1c-155">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>


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
