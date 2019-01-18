---
title: Recordset.BatchCollisions-Eigenschaft (DAO)
TOCTitle: BatchCollisions Property
ms:assetid: 53e5572b-770c-9ea5-31a5-984abdf66faa
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194079(v=office.15)
ms:contentKeyID: 48544881
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 61f60567ac170a0ecde2d4bd46589d2308b7788f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700372"
---
# <a name="recordsetbatchcollisions-property-dao"></a><span data-ttu-id="7cf59-102">Recordset.BatchCollisions-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="7cf59-102">Recordset.BatchCollisions property (DAO)</span></span>


<span data-ttu-id="7cf59-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7cf59-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="7cf59-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7cf59-104">Syntax</span></span>

<span data-ttu-id="7cf59-105">*Ausdruck* . BatchCollisions</span><span class="sxs-lookup"><span data-stu-id="7cf59-105">*expression* .BatchCollisions</span></span>

<span data-ttu-id="7cf59-106">*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="7cf59-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cf59-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7cf59-107">Remarks</span></span>

<span data-ttu-id="7cf59-p101">Diese Eigenschaft enthält ein Array der Textmarken für Zeilen, die beim letzten Versuch eines **[Update](recordset-update-method-dao.md)** -Batchaufrufs Konflikte verursacht haben. Die **[BatchCollisionCount](recordset-batchcollisioncount-property-dao.md)** -Eigenschaft gibt die Anzahl von Elementen im Array an.</span><span class="sxs-lookup"><span data-stu-id="7cf59-p101">This property contains an array of bookmarks to rows that encountered a collision during the last attempted batch **[Update](recordset-update-method-dao.md)** call. The **[BatchCollisionCount](recordset-batchcollisioncount-property-dao.md)** property indicates the number of elements in the array.</span></span>

<span data-ttu-id="7cf59-110">Wenn Sie die **[Bookmark](recordset-object-dao.md)** -Eigenschaft des aktiven **[Recordset](recordset-bookmark-property-dao.md)** -Objekts auf Textmarkenwerte im **BatchCollisions**-Array festlegen, können Sie zu jedem Datensatz wechseln, bei dem die letzte Batchaktualisierungsoperation nicht abgeschlossen werden konnte.</span><span class="sxs-lookup"><span data-stu-id="7cf59-110">If you set the working **[Recordset](recordset-object-dao.md)** object's **[Bookmark](recordset-bookmark-property-dao.md)** property to bookmark values in the **BatchCollisions** array, you can move to each record that failed to complete the most recent batch-mode Update operation.</span></span>

<span data-ttu-id="7cf59-p102">Nachdem die Konflikte verursachenden Datensätze korrigiert wurden, kann erneut eine Update-Methode im Batchmodus aufgerufen werden. An dieser Stelle versucht DAO eine weitere Batchaktualisierung, und die BatchCollisions-Eigenschaft gibt erneut die Datensätze zurück, bei denen der zweite Versuch fehlschlug. Datensätze, bei denen der vorhergehende Versuch erfolgreich war, werden nicht erneut gesendet, da deren RecordStatus-Eigenschaft auf dbRecordUnmodified festgelegt ist. Dieser Prozess kann fortgesetzt werden, bis Sie die Aktualisierung abbrechen und das Resultset schließen.</span><span class="sxs-lookup"><span data-stu-id="7cf59-p102">After the collision records are corrected, you can call the batch mode **Update** method again. At this point DAO attempts another batch update, and the **BatchCollisions** property again reflects the set of records that failed the second attempt. Any records that succeeded in the previous attempt are not sent in the current attempt, as they now have a **[RecordStatus](recordset-recordstatus-property-dao.md)** property of dbRecordUnmodified. This process can continue as long as collisions occur, or until you abandon the updates and close the result set.</span></span>

<span data-ttu-id="7cf59-115">Dieses Array wird bei jedem Ausführen einer **Update**-Methode im Batchmodus neu erstellt.</span><span class="sxs-lookup"><span data-stu-id="7cf59-115">This array is re-created each time you execute a batch-mode **Update** method.</span></span>

