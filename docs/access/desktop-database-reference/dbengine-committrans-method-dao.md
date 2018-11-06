---
title: DBEngine.CommitTrans-Methode (DAO)
TOCTitle: CommitTrans Method
ms:assetid: 0c9d345f-13ff-7fe6-789d-fbdb43fa54b8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845171(v=office.15)
ms:contentKeyID: 48543197
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 530f638cbf996d84b476f1d9cf259f6ab444978f
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996909"
---
# <a name="dbenginecommittrans-method-dao"></a><span data-ttu-id="1b6a6-102">DBEngine.CommitTrans-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="1b6a6-102">DBEngine.CommitTrans method (DAO)</span></span>


<span data-ttu-id="1b6a6-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1b6a6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1b6a6-104">Beendet die aktuelle Transaktion und speichert die Änderungen.</span><span class="sxs-lookup"><span data-stu-id="1b6a6-104">Ends the current transaction and saves the changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b6a6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b6a6-105">Syntax</span></span>

<span data-ttu-id="1b6a6-106">*Ausdruck* . CommitTrans (***Option***)</span><span class="sxs-lookup"><span data-stu-id="1b6a6-106">*expression* .CommitTrans(***Option***)</span></span>

<span data-ttu-id="1b6a6-107">*Ausdruck* Eine Variable, die ein **DBEngine** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="1b6a6-107">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="1b6a6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b6a6-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1b6a6-109">Name</span><span class="sxs-lookup"><span data-stu-id="1b6a6-109">Name</span></span></p></th>
<th><p><span data-ttu-id="1b6a6-110">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="1b6a6-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="1b6a6-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="1b6a6-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="1b6a6-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1b6a6-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1b6a6-113"><em>Option</em></span><span class="sxs-lookup"><span data-stu-id="1b6a6-113"><em>Option</em></span></span></p></td>
<td><p><span data-ttu-id="1b6a6-114">Optional</span><span class="sxs-lookup"><span data-stu-id="1b6a6-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="1b6a6-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="1b6a6-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="1b6a6-p101">In einem Microsoft Access-Arbeitsbereich können Sie die <strong>dbForceOSFlush</strong>-Konstante in <strong>CommitTrans</strong> einfügen. Dadurch wird das Datenbankmodul gezwungen, alle Aktualisierungen sofort auf den Datenträger zu leeren, statt sie temporär zu speichern. Ohne diese Option besteht die Gefahr, dass ein Benutzer direkt nach dem Aufrufen von <strong>CommitTrans</strong> durch das Anwendungsprogramm die Kontrolle übernimmt und den Computer ausschaltet, ohne dass die Daten auf einen Datenträger geschrieben wurden. Diese Option kann zwar die Anwendungsleistung beeinträchtigen, ist aber dennoch nützlich in Situationen, in denen der Computer heruntergefahren werden könnte, bevor zwischengespeicherte Aktualisierungen auf einem Datenträger gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="1b6a6-p101">In a Microsoft Access workspace, you can include the <strong>dbForceOSFlush</strong> constant with <strong>CommitTrans</strong>. This forces the database engine to immediately flush all updates to disk, instead of caching them temporarily. Without using this option, a user could get control back immediately after the application program calls <strong>CommitTrans</strong>, turn the computer off, and not have the data written to disk. While using this option may affect your application's performance, it is useful in situations where the computer could be shut off before cached updates are saved to disk.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="1b6a6-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1b6a6-120">Remarks</span></span>

<span data-ttu-id="1b6a6-p102">Mithilfe der Transaktionsmethoden **BeginTrans**, **CommitTrans** und **Rollback** wird die Transaktionsverarbeitung während einer Sitzung verwaltet, die durch ein **Workspace**-Objekt definiert wurde. Sie verwenden diese Methoden mit einem **Workspace**-Objekt, wenn Sie eine Reihe von an den Datenbanken vorgenommenen Änderungen in einer Sitzung als eine Einheit verarbeiten möchten.</span><span class="sxs-lookup"><span data-stu-id="1b6a6-p102">The transaction methods **BeginTrans**, **CommitTrans**, and **Rollback** manage transaction processing during a session defined by a **Workspace** object. You use these methods with a **Workspace** object when you want to treat a series of changes made to the databases in a session as one unit.</span></span>

<span data-ttu-id="1b6a6-p103">In der Regel verwenden Sie Transaktionen zur Wahrung der Integrität Ihrer Daten, wenn Sie Datensätze in mindestens zwei Tabellen aktualisieren und gleichzeitig sicherstellen müssen, dass die Änderungen in allen Tabellen (Commit) oder in keiner der Tabellen (Rollback) ausgeführt wurden. Beispielsweise subtrahieren Sie zum Übertragen von Geldbeträgen zwischen Konten einen Betrag von einem Konto und addieren ihn dann zu einem anderen Konto. Wenn eine der Aktualisierungen fehlschlägt, sind die Konten nicht mehr ausgeglichen. Verwenden Sie vor dem Aktualisieren des ersten Datensatzes die **BeginTrans**-Methode. Falls nachfolgende Aktualisierungen fehlschlagen, können Sie anschließend mithilfe der **Rollback**-Methode sämtliche Aktualisierungen rückgängig machen. Verwenden Sie die **CommitTrans**-Methode, nachdem Sie den letzten Datensatz erfolgreich aktualisiert haben.</span><span class="sxs-lookup"><span data-stu-id="1b6a6-p103">Typically, you use transactions to maintain the integrity of your data when you must both update records in two or more tables and ensure changes are completed (committed) in all tables or none at all (rolled back). For example, if you transfer money from one account to another, you might subtract an amount from one and add the amount to another. If either update fails, the accounts no longer balance. Use the **BeginTrans** method before updating the first record, and then, if any subsequent update fails, you can use the **Rollback** method to undo all of the updates. Use the **CommitTrans** method after you successfully update the last record.</span></span>

> [!NOTE]
> <span data-ttu-id="1b6a6-p104">[!HINWEIS] Innerhalb eines **Workspace**-Objekts sind Transaktionen für **Workspace** immer global und nicht auf ein **Connection**- oder **Database**-Objekt beschränkt. Wenn Sie Operationen für mehrere Verbindungen oder Datenbanken innerhalb einer **Workspace**-Transaktion durchführen, wirkt sich das Auflösen der Transaktion (d. h. die Verwendung der **CommitTrans**- oder **Rollback**-Methode) auf alle Operationen für sämtliche Verbindungen und Datenbanken innerhalb dieses Arbeitsbereichs aus.</span><span class="sxs-lookup"><span data-stu-id="1b6a6-p104">Within one **Workspace** object, transactions are always global to the **Workspace** and aren't limited to only one **Connection** or **Database** object. If you perform operations on more than one connection or database within a **Workspace** transaction, resolving the transaction (that is, using the **CommitTrans** or **Rollback** method) affects all operations on all connections and databases within that workspace.</span></span>

<span data-ttu-id="1b6a6-p105">Nach Verwendung von **CommitTrans** können Sie an dieser Transaktion vorgenommene Änderungen nur dann rückgängig machen, wenn die Transaktion in einer anderen Transaktion geschachtelt ist, für die ein Rollback ausgeführt wurde. Wenn Sie Transaktionen schachteln, müssen Sie die aktuelle Transaktion auflösen, bevor Sie eine Transaktion auf einer höheren Schachtelungsebene auflösen können.</span><span class="sxs-lookup"><span data-stu-id="1b6a6-p105">After you use **CommitTrans**, you can't undo changes made during that transaction unless the transaction is nested within another transaction that is itself rolled back. If you nest transactions, you must resolve the current transaction before you can resolve a transaction at a higher level of nesting.</span></span>

<span data-ttu-id="1b6a6-132">Wenn Sie gleichzeitige Transaktionen mit überlappenden, nicht geschachtelten Bereichen wünschen, können Sie zusätzliche **Workspace**-Objekte für die gleichzeitigen Transaktionen erstellen.</span><span class="sxs-lookup"><span data-stu-id="1b6a6-132">If you want to have simultaneous transactions with overlapping, non-nested scopes, you can create additional **Workspace** objects to contain the concurrent transactions.</span></span>

<span data-ttu-id="1b6a6-133">Wenn Sie ein **Workspace**-Objekt schließen, ohne ausstehende Transaktionen aufzulösen, wird automatisch ein Rollback für die Transaktionen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1b6a6-133">If you close a **Workspace** object without resolving any pending transactions, the transactions are automatically rolled back.</span></span>

<span data-ttu-id="1b6a6-134">Wenn Sie die **CommitTrans**- oder **Rollback**-Methode verwenden, ohne vorher die **BeginTrans**-Methode verwendet zu haben, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="1b6a6-134">If you use the **CommitTrans** or **Rollback** method without first using the **BeginTrans** method, an error occurs.</span></span>

<span data-ttu-id="1b6a6-p106">Möglicherweise werden Transaktionen nicht von allen in einem Microsoft Access-Arbeitsbereich verwendeten ISAM-Datenbanken unterstützt. In dem Fall hat die **Transactions**-Eigenschaft des **Database**-Objekts oder des **Recordset**-Objekts den Wert **False**. Überprüfen Sie vor dem Verwenden der **BeginTrans**-Methode den Wert der **Transactions**-Eigenschaft des **Database**-Objekts, um sicherzustellen, dass die Datenbank Transaktionen unterstützt. Wenn Sie ein **Recordset**-Objekt verwenden, das auf mehreren Datenbanken basiert, überprüfen Sie die **Transactions**-Eigenschaft des **Recordset**-Objekts. Basiert ein **Recordset**-Objekt vollständig auf Datenbankmodultabellen von Microsoft Access, können Sie in jedem Fall Transaktionen verwenden. Bei **Recordset**-Objekten, die auf in anderen Datenbankprogrammen erstellten Tabellen basieren, ist es möglich, dass Transaktionen nicht unterstützt werden. Sie können beispielsweise keine Transaktionen in einem **Recordset**-Objekt verwenden, das auf einer Paradox-Tabelle basiert. In diesem Fall ist die **Transactions**-Eigenschaft auf **False** festgelegt. Wenn **Database** oder **Recordset** keine Transaktionen unterstützen, werden die Methoden ignoriert, und es tritt kein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="1b6a6-p106">Some ISAM databases used in a Microsoft Access workspace may not support transactions, in which case the **Transactions** property of the **Database** object or **Recordset** object is **False**. To make sure the database supports transactions, check the value of the **Transactions** property of the **Database** object before using the **BeginTrans** method. If you are using a **Recordset** object based on more than one database, check the **Transactions** property of the **Recordset** object. If a **Recordset** is based entirely on Microsoft Access database engine tables, you can always use transactions. **Recordset** objects based on tables created by other database products, however, may not support transactions. For example, you can't use transactions in a **Recordset** based on a Paradox table. In this case, the **Transactions** property is **False**. If the **Database** or **Recordset** doesn't support transactions, the methods are ignored and no error occurs.</span></span>

<span data-ttu-id="1b6a6-143">Wenn Sie über das Microsoft Access-Datenbankmodul auf ODBC-Datenquellen zugreifen, können Sie Transaktionen nicht schachteln.</span><span class="sxs-lookup"><span data-stu-id="1b6a6-143">You can't nest transactions if you are accessing ODBC data sources through the Microsoft Access database engine.</span></span>

<span data-ttu-id="1b6a6-p107">Wenn Sie in ODBC-Arbeitsbereichen **CommitTrans** verwenden, ist der Cursor möglicherweise nicht mehr gültig. Zeigen Sie die Änderungen im **Recordset**-Objekt mithilfe der **Requery**-Methode an, oder schließen Sie das **Recordset**-Objekt, und öffnen Sie es erneut.</span><span class="sxs-lookup"><span data-stu-id="1b6a6-p107">In ODBC workspaces, when you use **CommitTrans** your cursor may no longer be valid. Use the **Requery** method to view the changes in the **Recordset**, or close and re-open the **Recordset**.</span></span>


> [!NOTE]
> - <span data-ttu-id="1b6a6-p108">Die Leistung der Anwendung lässt sich oftmals dadurch verbessern, dass Operationen unterbrochen werden, die Datenträgerzugriff auf Transaktionsblöcke erfordern. So werden die Operationen zwischengespeichert, und die Zugriffe auf den Datenträger können deutlich verringert werden.</span><span class="sxs-lookup"><span data-stu-id="1b6a6-p108">You can often improve the performance of your application by breaking operations that require disk access into transaction blocks. This buffers your operations and may significantly reduce the number of times a disk is accessed.</span></span>
> - <span data-ttu-id="1b6a6-p109">In einem Microsoft Access-Arbeitsbereich werden Transaktionen in einer Datei protokolliert, die in dem Verzeichnis gespeichert ist, das durch die Umgebungsvariable TEMP auf der Arbeitsstation festgelegt ist. Wenn der Speicherplatz des TEMP-Laufwerks für die Protokolldatei nicht ausreicht, löst das Datenbankmodul einen Laufzeitfehler aus. Wenn Sie nun **CommitTrans** verwenden, wird ein Commit für eine unbestimmte Anzahl von Operationen ausgeführt. Die übrigen Operationen gehen verloren, und die Operation muss neu gestartet werden. Bei Verwendung einer **Rollback**-Methode wird das Transaktionsprotokoll freigegeben, und für sämtliche Operationen in der Transaktion wird ein Rollback ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1b6a6-p109">In a Microsoft Access workspace, transactions are logged in a file kept in the directory specified by the TEMP environment variable on the workstation. If the transaction log file exhausts the available storage on your TEMP drive, the database engine triggers a run-time error. At this point, if you use **CommitTrans**, an indeterminate number of operations are committed, but the remaining uncompleted operations are lost, and the operation has to be restarted. Using a **Rollback** method releases the transaction log and rolls back all operations in the transaction.</span></span>
> - <span data-ttu-id="1b6a6-152">Wenn Sie den Klon eines **Recordset**-Objekts in einer ausstehenden Transaktion schließen, wird eine implizite **Rollback**-Operation verursacht.</span><span class="sxs-lookup"><span data-stu-id="1b6a6-152">Closing a clone **Recordset** within a pending transaction will cause an implicit **Rollback** operation.</span></span>


