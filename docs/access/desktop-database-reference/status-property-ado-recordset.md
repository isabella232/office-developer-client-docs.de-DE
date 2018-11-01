---
title: Status-Eigenschaft (ADO-Recordset)
TOCTitle: Status Property (ADO Recordset)
ms:assetid: bf3ccb36-c985-5fae-4f76-c48a0e20e6f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249930(v=office.15)
ms:contentKeyID: 48547482
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c053ec9f84de4aa56513081144e23f044c72effc
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876631"
---
# <a name="status-property-ado-recordset"></a><span data-ttu-id="a95bb-102">Status-Eigenschaft (ADO-Recordset)</span><span class="sxs-lookup"><span data-stu-id="a95bb-102">Status Property (ADO Recordset)</span></span>


<span data-ttu-id="a95bb-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a95bb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a95bb-104">Gibt den Status des aktuellen Datensatzes in Bezug auf Batchaktualisierungen oder andere Massenvorgänge an.</span><span class="sxs-lookup"><span data-stu-id="a95bb-104">Indicates the status of the current record with respect to batch updates or other bulk operations.</span></span>

## <a name="return-value"></a><span data-ttu-id="a95bb-105">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a95bb-105">Return value</span></span>

<span data-ttu-id="a95bb-106">Gibt eine Summe aus einem oder mehreren [RecordStatusEnum](recordstatusenum.md)-Werten zurück.</span><span class="sxs-lookup"><span data-stu-id="a95bb-106">Returns a sum of one or more [RecordStatusEnum](recordstatusenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="a95bb-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a95bb-107">Remarks</span></span>

<span data-ttu-id="a95bb-p101">Verwenden Sie die **Status** -Eigenschaft, um die ausstehende Änderungen für Datensätze zu ermitteln, die während einer Batchaktualisierung geändert werden. Sie können mit der **Status** -Eigenschaft auch den Status der Datensätze anzeigen, die beispielsweise bei folgenden Massenvorgängen zu Fehlern führen: wenn Sie die Methoden [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) oder [CancelBatch](cancelbatch-method-ado.md) für ein [Recordset](recordset-object-ado.md)-Objekt aufrufen oder wenn Sie die [Filter](filter-property-ado.md)-Eigenschaft für ein **Recordset** -Objekt auf ein Textmarkenarray festlegen. Mit dieser Eigenschaft können Sie den Fehler eines bestimmten Datensatzes ermitteln und beheben.</span><span class="sxs-lookup"><span data-stu-id="a95bb-p101">Use the **Status** property to see what changes are pending for records modified during batch updating. You can also use the **Status** property to view the status of records that fail during bulk operations, such as when you call the [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), or [CancelBatch](cancelbatch-method-ado.md) methods on a [Recordset](recordset-object-ado.md) object, or set the [Filter](filter-property-ado.md) property on a **Recordset** object to an array of bookmarks. With this property, you can determine how a given record failed and resolve it accordingly.</span></span>

