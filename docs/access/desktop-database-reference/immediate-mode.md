---
title: Sofortiger Aktualisierungsmodus (Access PC-Datenbank-Referenz)
TOCTitle: Immediate mode
ms:assetid: 61bd3645-6e84-2e3a-7814-37d8c1247df0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249362(v=office.15)
ms:contentKeyID: 48545220
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b6401e7954325eded85b70b9edb5d164e857d113
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947861"
---
# <a name="immediate-mode"></a><span data-ttu-id="5733a-102">Sofortiger Aktualisierungsmodus</span><span class="sxs-lookup"><span data-stu-id="5733a-102">Immediate mode</span></span>


<span data-ttu-id="5733a-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5733a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5733a-p101">Der sofortige Aktualisierungsmodus ist aktiviert, wenn die **LockType** -Eigenschaft auf **adLockOptimistic** oder **adLockPessimistic** festgelegt ist. Im sofortigen Aktualisierungsmodus werden Änderungen an einem Datensatz an die Datenquelle weitergegeben, sobald Sie die Bearbeitung einer Zeile als abgeschlossen deklarieren, indem Sie die **Update** -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5733a-p101">Immediate mode is in effect when the **LockType** property is set to **adLockOptimistic** or **adLockPessimistic**. In immediate mode, changes to a record are propagated to the data source as soon as you declare the work on a row complete by calling the **Update** method.</span></span>

## <a name="calling-update"></a><span data-ttu-id="5733a-106">Aufrufen der Update-Methode</span><span class="sxs-lookup"><span data-stu-id="5733a-106">Calling Update</span></span>

<span data-ttu-id="5733a-p102">Wenn Sie den Datensatz verlassen, den Sie hinzufügen oder bearbeiten, bevor Sie die **Update** -Methode aufrufen, ruft ADO zum Speichern der Änderungen automatisch **Update** auf. Sie müssen vor der Navigation die **CancelUpdate** -Methode aufrufen, falls Sie Änderungen am aktuellen Datensatz abbrechen oder einen neu hinzugefügten Datensatz verwerfen möchten.</span><span class="sxs-lookup"><span data-stu-id="5733a-p102">If you move from the record you are adding or editing before calling the **Update** method, ADO will automatically call **Update** to save the changes. You must call the **CancelUpdate** method before navigation if you want to cancel any changes made to the current record or discard a newly added record.</span></span>

<span data-ttu-id="5733a-109">Der aktuelle Datensatz bleibt aktuell, nachdem Sie die **Update** -Methode aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="5733a-109">The current record remains current after you call the **Update** method.</span></span>

## <a name="cancelupdate"></a><span data-ttu-id="5733a-110">CancelUpdate</span><span class="sxs-lookup"><span data-stu-id="5733a-110">CancelUpdate</span></span>

<span data-ttu-id="5733a-p103">Verwenden Sie die **CancelUpdate** -Methode, um Änderungen an der aktuellen Zeile abzubrechen oder um eine neu hinzugefügte Zeile zu verwerfen. Änderungen an der aktuellen Zeile oder eine neue Zeile können nicht abgebrochen werden, nachdem Sie die **Update** -Methode aufgerufen haben, außer die Änderungen sind Teil einer Transaktion, für die Sie ein Rollback mit der **RollbackTrans** -Methode ausführen können, oder Teil einer Batchaktualisierung. Bei einer Batchaktualisierung können Sie **Update** mit der **CancelUpdate** - oder **CancelBatch** -Methode abbrechen.</span><span class="sxs-lookup"><span data-stu-id="5733a-p103">Use the **CancelUpdate** method to cancel any changes made to the current row or to discard a newly added row. You cannot cancel changes to the current row or a new row after you call the **Update** method, unless the changes are either part of a transaction that you can roll back with the **RollbackTrans** method or part of a batch update. In the case of a batch update, you can cancel the **Update** with the **CancelUpdate** or **CancelBatch** method.</span></span>

<span data-ttu-id="5733a-114">Wenn Sie beim Aufrufen der **CancelUpdate** -Methode eine neue Zeile hinzufügen, wird die Zeile, die vor dem Aufruf von **AddNew** die aktuelle Zeile war, zur aktuellen Zeile.</span><span class="sxs-lookup"><span data-stu-id="5733a-114">If you are adding a new row when you call the **CancelUpdate** method, the current row becomes the row that was current before the **AddNew** call.</span></span>

<span data-ttu-id="5733a-115">Wenn Sie die aktuelle Zeile nicht geändert haben oder keine neue Zeile hinzugefügt haben, wird durch Aufrufen der **CancelUpdate** -Methode ein Fehler generiert.</span><span class="sxs-lookup"><span data-stu-id="5733a-115">If you have not changed the current row or added a new row, calling the **CancelUpdate** method generates an error.</span></span>

