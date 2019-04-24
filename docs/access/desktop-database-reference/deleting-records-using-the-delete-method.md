---
title: Löschen von Datensätzen mit der Delete-Methode
TOCTitle: Deleting records using the Delete method
ms:assetid: 22917c33-4d14-ebab-d85c-2cbe7f68c560
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249003(v=office.15)
ms:contentKeyID: 48543708
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a476e9bc57224b0e46afb31bf092450c26de0a17
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293966"
---
# <a name="deleting-records-using-the-delete-method"></a><span data-ttu-id="47dcf-102">Löschen von Datensätzen mit der Delete-Methode</span><span class="sxs-lookup"><span data-stu-id="47dcf-102">Deleting records using the Delete method</span></span>


<span data-ttu-id="47dcf-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="47dcf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="47dcf-p101">Mit der **Delete** -Methode wird der aktuelle Datensatz oder eine Gruppe von Datensätzen in einem **Recordset** -Objekt zum Löschen markiert. Ein Fehler tritt auf, falls das **Recordset** -Objekt das Löschen von Datensätzen nicht zulässt. Wenn der sofortige Aktualisierungsmodus aktiviert ist, werden Löschvorgänge sofort in der Datenbank ausgeführt. Wenn ein Datensatz nicht erfolgreich gelöscht werden kann (z. B. aufgrund von Verletzungen der Datenbankintegrität), verbleibt der Datensatz nach dem Aufrufen von **Update** im Bearbeitungsmodus. Dies bedeutet, dass Sie die Aktualisierung mithilfe von [CancelUpdate](cancelupdate-method-ado.md) abbrechen müssen, bevor Sie den aktuellen Datensatz verlassen (z. B. mit [Close](close-method-ado.md), [Move](move-method-ado.md) oder [NextRecordset](nextrecordset-method-ado.md)).</span><span class="sxs-lookup"><span data-stu-id="47dcf-p101">Using the **Delete** method marks the current record or a group of records in a **Recordset** object for deletion. If the **Recordset** object does not allow record deletion, an error occurs. If you are in immediate update mode, deletions occur in the database immediately. If a record cannot be successfully deleted (due to database integrity violations, for example), the record will remain in edit mode after the call to **Update**. This means that you must cancel the update using [CancelUpdate](cancelupdate-method-ado.md) before moving off the current record (for example, using [Close](close-method-ado.md), [Move](move-method-ado.md), or [NextRecordset](nextrecordset-method-ado.md)).</span></span>

<span data-ttu-id="47dcf-p102">Wenn der Batchaktualisierungsmodus aktiviert ist, werden die Datensätze im Cache zum Löschen markiert, und der eigentliche Löschvorgang wird ausgeführt, wenn Sie die **UpdateBatch** -Methode aufrufen. (Zum Anzeigen der gelöschten Datensätze legen Sie die **Filter** -Eigenschaft auf **adFilterAffectedRecords** fest, nachdem **Delete** aufgerufen wurde.)</span><span class="sxs-lookup"><span data-stu-id="47dcf-p102">If you are in batch update mode, the records are marked for deletion from the cache and the actual deletion happens when you call the **UpdateBatch** method. (To view the deleted records, set the **Filter** property to **adFilterAffectedRecords** after **Delete** is called.)</span></span>

<span data-ttu-id="47dcf-p103">Beim Abrufen von Feldwerten aus dem gelöschten Datensatz wird ein Fehler generiert. Nach dem Löschen des aktuellen Datensatzes bleibt der gelöschte Datensatz aktiv, bis Sie zu einem anderen Datensatz navigieren. Sobald Sie den gelöschten Datensatz verlassen, ist der Zugriff darauf nicht mehr möglich.</span><span class="sxs-lookup"><span data-stu-id="47dcf-p103">Attempting to retrieve field values from the deleted record generates an error. After deleting the current record, the deleted record remains current until you move to a different record. Once you move away from the deleted record, it is no longer accessible.</span></span>

<span data-ttu-id="47dcf-p104">Wenn Sie Löschvorgänge in einer Transaktion schachteln, können Sie gelöschte Datensätze mithilfe der **RollbackTrans** -Methode wiederherstellen. Falls der Batchaktualisierungsmodus aktiviert ist, können Sie einen ausstehenden Löschvorgang oder eine Gruppe von ausstehenden Löschvorgängen mithilfe der **CancelBatch** -Methode abbrechen.</span><span class="sxs-lookup"><span data-stu-id="47dcf-p104">If you nest deletions in a transaction, you can recover deleted records by using the **RollbackTrans** method. If you are in batch update mode, you can cancel a pending deletion or group of pending deletions by using the **CancelBatch** method.</span></span>

<span data-ttu-id="47dcf-p105">Wenn beim Löschen von Datensätzen ein Fehler aufgrund eines Konflikts mit den zugrunde liegenden Daten erzeugt wird (z. B. wurde ein Datensatz bereits von einem anderen Benutzer gelöscht), gibt der Anbieter Warnungen an die **Errors** -Auflistung zurück, aber die Ausführung des Programms wird nicht unterbrochen. Ein Laufzeitfehler tritt nur auf, wenn für alle angeforderten Datensätze Konflikte vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="47dcf-p105">If the attempt to delete records fails because of a conflict with the underlying data (for example, a record has already been deleted by another user), the provider returns warnings to the **Errors** collection but does not halt program execution. A run-time error occurs only if there are conflicts on all the requested records.</span></span>

<span data-ttu-id="47dcf-118">Wenn die dynamische Eigenschaft **Unique Table** festgelegt ist und das **Recordset** -Objekt das Ergebnis der Ausführung einer JOIN-Operation in mehreren Tabellen ist, löscht die **Delete** -Methode nur Zeilen in der in der **Unique Table** -Eigenschaft angegebenen Tabelle.</span><span class="sxs-lookup"><span data-stu-id="47dcf-118">If the **Unique Table** dynamic property is set and the **Recordset** is the result of executing a JOIN operation on multiple tables, the **Delete** method will delete rows only from the table named in the **Unique Table** property.</span></span>

<span data-ttu-id="47dcf-p106">Die **Delete** -Methode verwendet ein optionales Argument, mit dem Sie angeben können, welche Datensätze von dem **Delete** -Vorgang betroffen sind. Für dieses Argument sind nur die folgenden aufgezählten **AffectEnum** -Konstanten von ADO zulässig:</span><span class="sxs-lookup"><span data-stu-id="47dcf-p106">The **Delete** method takes an optional argument that allows you to specify which records are affected by the **Delete** operation. The only valid values for this argument are either of the following ADO **AffectEnum** enumerated constants:</span></span>

  - <span data-ttu-id="47dcf-121">**adAffectCurrent** Betrifft nur den aktuellen Datensatz.</span><span class="sxs-lookup"><span data-stu-id="47dcf-121">**adAffectCurrent**Affects only the current record.</span></span>

  - <span data-ttu-id="47dcf-122">**affectgroup** Betrifft nur Datensätze, die die aktuelle Einstellung der **Filter** -Eigenschaft erfüllen.</span><span class="sxs-lookup"><span data-stu-id="47dcf-122">**adAffectGroup**Affects only records that satisfy the current **Filter** property setting.</span></span> <span data-ttu-id="47dcf-123">Die **Filter** -Eigenschaft muss auf einen **FilterGroupEnum** -Wert oder ein Array von **Bookmarks** festgelegt werden, damit diese Option verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="47dcf-123">The **Filter** property must be set to a **FilterGroupEnum** value or an array of **Bookmarks** to use this option.</span></span>

<span data-ttu-id="47dcf-p108">Der folgende Beispielcode veranschaulicht, wie Sie **adAffectGroup** angeben, wenn die **Delete** -Methode aufgerufen wird. In diesem Beispiel werden dem **Recordset** -Beispielobjekt Datensätze hinzugefügt und die Datenbank wird aktualisiert. Anschließend wird das **Recordset** -Objekt mithilfe der aufgezählten Filterkonstante **adFilterAffectedRecords** gefiltert, womit nur die neu hinzugefügten Datensätze im **Recordset** -Objekt angezeigt werden. Schließlich wird die **Delete** -Methode aufgerufen und angegeben, dass alle Datensätze, die die aktuelle Einstellung der **Filter** -Eigenschaft erfüllen (die neuen Datensätze), gelöscht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="47dcf-p108">The following code shows an example of specifying **adAffectGroup** when calling the **Delete** method. This example adds some records to the sample **Recordset** and updates the database. Then it filters the **Recordset** using the **adFilterAffectedRecords** filter enumerated constant, which leaves only the newly added records visible in the **Recordset**. Finally, it calls the **Delete** method and specifies that all of the records that satisfy the current **Filter** property setting (the new records) should be deleted.</span></span>

```vb 
 
'BeginDeleteGroup 
 'add some bogus records 
 With objRs1 
 For i = 0 To 8 
 .AddNew 
 .Fields("CompanyName") = "Shipper Number " & i + 1 
 .Fields("Phone") = "(425) 555-000" & (i + 1) 
 .Update 
 Next i 
 
 're-connect & update 
 .ActiveConnection = GetNewConnection 
 .UpdateBatch 
 
 'filter on newly added records 
 .Filter = adFilterAffectedRecords 
 Debug.Print "Deleting the " & .RecordCount & _ 
 " records you just added." 
 
 'delete the newly added bogus records 
 .Delete adAffectGroup 
 .Filter = adFilterNone 
 Debug.Print .RecordCount & " records remain." 
 
 .Close 
 End With 
'EndDeleteGroup 
```

