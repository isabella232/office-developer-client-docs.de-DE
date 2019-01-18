---
title: Recordset.UpdateOptions-Eigenschaft (DAO)
TOCTitle: UpdateOptions Property
ms:assetid: 14ab955d-1c5a-dc76-8dbf-dbca49816bc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845468(v=office.15)
ms:contentKeyID: 48543391
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101185
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: ced8fc78729924ce271aa0fe38d77d287a131f13
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705939"
---
# <a name="recordsetupdateoptions-property-dao"></a><span data-ttu-id="2ef69-102">Recordset.UpdateOptions-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="2ef69-102">Recordset.UpdateOptions property (DAO)</span></span>


<span data-ttu-id="2ef69-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2ef69-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="2ef69-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ef69-104">Syntax</span></span>

<span data-ttu-id="2ef69-105">*Ausdruck* . UpdateOptions</span><span class="sxs-lookup"><span data-stu-id="2ef69-105">*expression* .UpdateOptions</span></span>

<span data-ttu-id="2ef69-106">*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="2ef69-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ef69-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2ef69-107">Remarks</span></span>

<span data-ttu-id="2ef69-108">Wenn eine **[Update](recordset-update-method-dao.md)** -Anweisung im Batchmodus ausgeführt wird, erstellen DAO und die Client-Batchcursorbibliothek eine Reihe von SQL UPDATE-Anweisungen, um die erforderlichen Änderungen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="2ef69-108">When a batch-mode **[Update](recordset-update-method-dao.md)** is executed, DAO and the client batch cursor library create a series of SQL UPDATE statements to make the needed changes.</span></span> <span data-ttu-id="2ef69-109">Für jede Aktualisierung wird eine SQL WHERE-Klausel erstellt, um die Datensätze zu isolieren, die von der **[RecordStatus](recordset-recordstatus-property-dao.md)** -Eigenschaft als geändert markiert wurden.</span><span class="sxs-lookup"><span data-stu-id="2ef69-109">An SQL WHERE clause is created for each update to isolate the records that are marked as changed by the **[RecordStatus](recordset-recordstatus-property-dao.md)** property.</span></span> <span data-ttu-id="2ef69-110">Da einige Remoteserver Trigger oder andere Wege verwenden, um die referenzielle Integrität zu erzwingen, müssen häufig die zu aktualisierenden Felder auf die Felder beschränkt werden, die von der Änderung betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="2ef69-110">Because some remote servers use triggers or other ways to enforce referential integrity, is it often important to limit the fields being updated to just those affected by the change.</span></span> 

<span data-ttu-id="2ef69-111">Hierzu legen Sie die **UpdateOptions**-Eigenschaft auf eine der Konstanten **dbCriteriaKey**, **dbCriteriaModValues**, **dbCriteriaAllCols** oder **dbCriteriaTimeStamp** fest.</span><span class="sxs-lookup"><span data-stu-id="2ef69-111">To do this, set the **UpdateOptions** property to one of the constants **dbCriteriaKey**, **dbCriteriaModValues**, **dbCriteriaAllCols**, or **dbCriteriaTimeStamp**.</span></span> <span data-ttu-id="2ef69-112">Auf diese Weise wird nur der absolut notwendige Triggercode ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2ef69-112">This way, only the absolute minimum amount of trigger code is executed.</span></span> <span data-ttu-id="2ef69-113">Als Ergebnis wird der Aktualisierungsvorgang schneller und mit weniger potenziellen Fehlern ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2ef69-113">As a result, the update operation is executed more quickly, and with fewer potential errors.</span></span>

<span data-ttu-id="2ef69-p103">Sie können auch die Konstanten **dbCriteriaDeleteInsert** und **dbCriteriaUpdate** verketten, um festzustellen, ob für jede Aktualisierung eine Gruppe von SQL DELETE- und INSERT-Anweisungen oder eine SQL UPDATE-Anweisung verwendet werden sollen, wenn Änderungen in einem Batch an den Server zurückgesendet werden. Im ersten Fall sind zwei separate Vorgänge erforderlich, um den Datensatz zu aktualisieren. In einigen Fällen, v. a. wenn das Remotesystem DELETE-, INSERT- und UPDATE-Trigger implementiert, kann die Wahl der richtigen **UpdateOptions**-Eigenschaft erheblichen Einfluss auf die Leistung haben.</span><span class="sxs-lookup"><span data-stu-id="2ef69-p103">You can also concatenate either of the constants **dbCriteriaDeleteInsert** or **dbCriteriaUpdate** to determine whether to use a set of SQL DELETE and INSERT statements or an SQL UPDATE statement for each update when sending batched modifications back to the server. In the former case, two separate operations are required to update the record. In some cases, especially where the remote system implements DELETE, INSERT, and UPDATE triggers, choosing the correct **UpdateOptions** property setting can significantly impact performance.</span></span>

<span data-ttu-id="2ef69-117">Wenn Sie keine Konstanten angeben, werden **dbCriteriaUpdate** und **dbCriteriaKey** verwendet.</span><span class="sxs-lookup"><span data-stu-id="2ef69-117">If you don't specify any constants, **dbCriteriaUpdate** and **dbCriteriaKey** will be used.</span></span>

<span data-ttu-id="2ef69-118">Neu hinzugefügte Datensätze generieren immer INSERT-Anweisungen, und gelöschte Datensätze generieren immer DELETE-Anweisungen, sodass diese Eigenschaft nur angibt, wie die Cursorbibliothek geänderte Datensätze aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="2ef69-118">Newly added records will always generate INSERT statements and deleted records will always generate DELETE statements, so this property only applies to how the cursor library updates modified records.</span></span>

## <a name="example"></a><span data-ttu-id="2ef69-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2ef69-119">Example</span></span>

<span data-ttu-id="2ef69-120">In diesem Beispiel werden die Eigenschaften **BatchSize** und **UpdateOptions** verwendet, um Aspekte von Batchaktualisierungen für das angegebene **Recordset**-Objekt zu steuern.</span><span class="sxs-lookup"><span data-stu-id="2ef69-120">This example uses the **BatchSize** and **UpdateOptions** properties to control aspects of any batch updating for the specified **Recordset** object.</span></span>

```vb 
Sub BatchSizeX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset 
 
 Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 ' This DefaultCursorDriver setting is required for 
 ' batch updating. 
 wrkMain.DefaultCursorDriver = dbUseClientBatchCursor 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conMain = wrkMain.OpenConnection("Publishers", _ 
 dbDriverNoPrompt, False, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' The following locking argument is required for 
 ' batch updating. 
 Set rstTemp = conMain.OpenRecordset( _ 
 "SELECT * FROM roysched", dbOpenDynaset, 0, _ 
 dbOptimisticBatch) 
 
 With rstTemp 
 ' Increase the number of statements sent to the server 
 ' during a single batch update, thereby reducing the 
 ' number of times an update would have to access the 
 ' server. 
 .BatchSize = 25 
 
 ' Change the UpdateOptions property so that the WHERE 
 ' clause of any batched statements going to the server 
 ' will include any updated columns in addition to the 
 ' key column(s). Also, any modifications to records 
 ' will be made by deleting the original record 
 ' and adding a modified version rather than just 
 ' modifying the original record. 
 .UpdateOptions = dbCriteriaModValues + _ 
 dbCriteriaDeleteInsert 
 
 ' Engage in batch updating using the new settings 
 ' above. 
 ' ... 
 
 .Close 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
```

