---
title: Recordset2.BatchCollisions Property (DAO)
TOCTitle: BatchCollisions Property
ms:assetid: 07d6c25f-baf5-f7d6-d225-0447e0f78fe6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844993(v=office.15)
ms:contentKeyID: 48543085
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101180
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ee26b84237b1bf4a8603295a6e6d66e6f30303e9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885892"
---
# <a name="recordset2batchcollisions-property-dao"></a><span data-ttu-id="9732d-102">Recordset2.BatchCollisions Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="9732d-102">Recordset2.BatchCollisions Property (DAO)</span></span>


<span data-ttu-id="9732d-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9732d-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="9732d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9732d-104">Syntax</span></span>

<span data-ttu-id="9732d-105">*Ausdruck* . BatchCollisions</span><span class="sxs-lookup"><span data-stu-id="9732d-105">*expression* .BatchCollisions</span></span>

<span data-ttu-id="9732d-106">*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="9732d-106">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9732d-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9732d-107">Remarks</span></span>

<span data-ttu-id="9732d-p101">Diese Eigenschaft enthält ein Array von Lesezeichen für Zeilen, die beim letzten Versuch einer Batchaktualisierung (Aufruf von **[Update](recordset2-update-method-dao.md)** ) einen Konflikt verursacht haben. Die **[BatchCollisionCount](recordset2-batchcollisioncount-property-dao.md)** -Eigenschaft gibt die Anzahl der Elemente im Array an.</span><span class="sxs-lookup"><span data-stu-id="9732d-p101">This property contains an array of bookmarks to rows that encountered a collision during the last attempted batch **[Update](recordset2-update-method-dao.md)** call. The **[BatchCollisionCount](recordset2-batchcollisioncount-property-dao.md)** property indicates the number of elements in the array.</span></span>

<span data-ttu-id="9732d-110">Wenn Sie die [**Bookmark**](recordset2-bookmark-property-dao.md) -Eigenschaft des **Recordset**-Objekts festlegen, um Werte im **BatchCollisions**-Array mit einem Lesezeichen zu versehen, können Sie zu jedem Datensatz navigieren, der beim letzten Batchaktualisierungsvorgang nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="9732d-110">If you set the working **Recordset** object's **[Bookmark](recordset2-bookmark-property-dao.md)** property to bookmark values in the **BatchCollisions** array, you can move to each record that failed to complete the most recent batch-mode Update operation.</span></span>

<span data-ttu-id="9732d-p102">Nachdem die Konflikte verursachenden Datensätze korrigiert wurden, kann erneut eine Update-Methode im Batchmodus aufgerufen werden. An dieser Stelle versucht DAO eine weitere Batchaktualisierung, und die BatchCollisions-Eigenschaft gibt erneut die Datensätze zurück, bei denen der zweite Versuch fehlschlug. Datensätze, bei denen der vorhergehende Versuch erfolgreich war, werden nicht erneut gesendet, da deren RecordStatus-Eigenschaft auf dbRecordUnmodified festgelegt ist. Dieser Prozess kann fortgesetzt werden, bis Sie die Aktualisierung abbrechen und das Resultset schließen.</span><span class="sxs-lookup"><span data-stu-id="9732d-p102">After the collision records are corrected, you can call the batch mode **Update** method again. At this point DAO attempts another batch update, and the **BatchCollisions** property again reflects the set of records that failed the second attempt. Any records that succeeded in the previous attempt are not sent in the current attempt, as they now have a **[RecordStatus](recordset2-recordstatus-property-dao.md)** property of dbRecordUnmodified. This process can continue as long as collisions occur, or until you abandon the updates and close the result set.</span></span>

<span data-ttu-id="9732d-115">Dieses Array wird bei jedem Ausführen einer **Update**-Methode im Batchmodus neu erstellt.</span><span class="sxs-lookup"><span data-stu-id="9732d-115">This array is re-created each time you execute a batch-mode **Update** method.</span></span>

