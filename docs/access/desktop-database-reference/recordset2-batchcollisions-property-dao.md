---
title: Recordset2. BatchCollisions-Eigenschaft (DAO)
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
localization_priority: Normal
ms.openlocfilehash: ea75da06c0db4eeb4e846bacfddc9f125c03fc84
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307490"
---
# <a name="recordset2batchcollisions-property-dao"></a><span data-ttu-id="4eb35-102">Recordset2. BatchCollisions-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="4eb35-102">Recordset2.BatchCollisions property (DAO)</span></span>


<span data-ttu-id="4eb35-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4eb35-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="4eb35-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4eb35-104">Syntax</span></span>

<span data-ttu-id="4eb35-105">*Ausdruck* . BatchCollisions</span><span class="sxs-lookup"><span data-stu-id="4eb35-105">*expression* .BatchCollisions</span></span>

<span data-ttu-id="4eb35-106">*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="4eb35-106">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4eb35-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4eb35-107">Remarks</span></span>

<span data-ttu-id="4eb35-p101">Diese Eigenschaft enthält ein Array von Lesezeichen für Zeilen, die beim letzten Versuch einer Batchaktualisierung (Aufruf von **[Update](recordset2-update-method-dao.md)** ) einen Konflikt verursacht haben. Die **[BatchCollisionCount](recordset2-batchcollisioncount-property-dao.md)** -Eigenschaft gibt die Anzahl der Elemente im Array an.</span><span class="sxs-lookup"><span data-stu-id="4eb35-p101">This property contains an array of bookmarks to rows that encountered a collision during the last attempted batch **[Update](recordset2-update-method-dao.md)** call. The **[BatchCollisionCount](recordset2-batchcollisioncount-property-dao.md)** property indicates the number of elements in the array.</span></span>

<span data-ttu-id="4eb35-110">Wenn Sie die [**Bookmark**](recordset2-bookmark-property-dao.md) -Eigenschaft des **Recordset**-Objekts festlegen, um Werte im **BatchCollisions**-Array mit einem Lesezeichen zu versehen, können Sie zu jedem Datensatz navigieren, der beim letzten Batchaktualisierungsvorgang nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="4eb35-110">If you set the working **Recordset** object's **[Bookmark](recordset2-bookmark-property-dao.md)** property to bookmark values in the **BatchCollisions** array, you can move to each record that failed to complete the most recent batch-mode Update operation.</span></span>

<span data-ttu-id="4eb35-p102">After the collision records are corrected, you can call the batch mode **Update** method again. At this point DAO attempts another batch update, and the **BatchCollisions** property again reflects the set of records that failed the second attempt. Any records that succeeded in the previous attempt are not sent in the current attempt, as they now have a **[RecordStatus](recordset2-recordstatus-property-dao.md)** property of dbRecordUnmodified. This process can continue as long as collisions occur, or until you abandon the updates and close the result set.</span><span class="sxs-lookup"><span data-stu-id="4eb35-p102">After the collision records are corrected, you can call the batch mode **Update** method again. At this point DAO attempts another batch update, and the **BatchCollisions** property again reflects the set of records that failed the second attempt. Any records that succeeded in the previous attempt are not sent in the current attempt, as they now have a **[RecordStatus](recordset2-recordstatus-property-dao.md)** property of dbRecordUnmodified. This process can continue as long as collisions occur, or until you abandon the updates and close the result set.</span></span>

<span data-ttu-id="4eb35-115">Dieses Array wird bei jeder Ausführung einer **Update**-Methode im Batchmodus neu erstellt.</span><span class="sxs-lookup"><span data-stu-id="4eb35-115">This array is re-created each time you execute a batch-mode **Update** method.</span></span>

