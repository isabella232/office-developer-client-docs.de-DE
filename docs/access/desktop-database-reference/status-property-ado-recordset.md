---
title: Status-Eigenschaft (ADO-Recordset)
TOCTitle: Status property (ADO Recordset)
ms:assetid: bf3ccb36-c985-5fae-4f76-c48a0e20e6f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249930(v=office.15)
ms:contentKeyID: 48547482
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4017ff216c17479a69d6d07d0abe51b30fd5e680
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308519"
---
# <a name="status-property-ado-recordset"></a><span data-ttu-id="24026-102">Status-Eigenschaft (ADO-Recordset)</span><span class="sxs-lookup"><span data-stu-id="24026-102">Status property (ADO Recordset)</span></span>


<span data-ttu-id="24026-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="24026-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="24026-104">Gibt den Status des aktuellen Datensatzes in Bezug auf Batchaktualisierungen oder andere Massenvorgänge an.</span><span class="sxs-lookup"><span data-stu-id="24026-104">Indicates the status of the current record with respect to batch updates or other bulk operations.</span></span>

## <a name="return-value"></a><span data-ttu-id="24026-105">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="24026-105">Return value</span></span>

<span data-ttu-id="24026-106">Gibt eine Summe aus einem oder mehreren [RecordStatusEnum](recordstatusenum.md)-Werten zurück.</span><span class="sxs-lookup"><span data-stu-id="24026-106">Returns a sum of one or more [RecordStatusEnum](recordstatusenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="24026-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="24026-107">Remarks</span></span>

<span data-ttu-id="24026-p101">Verwenden Sie die **Status**-Eigenschaft, um die ausstehende Änderungen für Datensätze zu ermitteln, die während einer Batchaktualisierung geändert werden. Sie können mit der **Status**-Eigenschaft auch den Status der Datensätze anzeigen, die beispielsweise bei folgenden Massenvorgängen zu Fehlern führen: wenn Sie die Methoden [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) oder [CancelBatch](cancelbatch-method-ado.md) für ein [Recordset](recordset-object-ado.md)-Objekt aufrufen oder wenn Sie die [Filter](filter-property-ado.md)-Eigenschaft für ein **Recordset**-Objekt auf ein Textmarkenarray festlegen. Mit dieser Eigenschaft können Sie den Fehler eines bestimmten Datensatzes ermitteln und beheben.</span><span class="sxs-lookup"><span data-stu-id="24026-p101">Use the **Status** property to see what changes are pending for records modified during batch updating. You can also use the **Status** property to view the status of records that fail during bulk operations, such as when you call the [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), or [CancelBatch](cancelbatch-method-ado.md) methods on a [Recordset](recordset-object-ado.md) object, or set the [Filter](filter-property-ado.md) property on a **Recordset** object to an array of bookmarks. With this property, you can determine how a given record failed and resolve it accordingly.</span></span>

