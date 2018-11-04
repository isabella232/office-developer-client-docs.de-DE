---
title: UpdateBatch-Methode (ADO)
TOCTitle: UpdateBatch method (ADO)
ms:assetid: 69e72a65-b637-36fd-d09f-7f81050f71ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249416(v=office.15)
ms:contentKeyID: 48545420
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3ce946d3354f6bbf05ac3819efc5f96c436fa174
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950125"
---
# <a name="updatebatch-method-ado"></a><span data-ttu-id="a81e3-102">UpdateBatch-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="a81e3-102">UpdateBatch method (ADO)</span></span>

<span data-ttu-id="a81e3-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a81e3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a81e3-104">Schreibt alle ausstehenden Batchaktualisierungen auf einen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="a81e3-104">Writes all pending batch updates to disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="a81e3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a81e3-105">Syntax</span></span>

<span data-ttu-id="a81e3-106">*Recordset-Objekt*. UpdateBatch*AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="a81e3-106">*recordset*.UpdateBatch*AffectRecords*</span></span>

## <a name="parameters"></a><span data-ttu-id="a81e3-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a81e3-107">Parameters</span></span>

|<span data-ttu-id="a81e3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a81e3-108">Parameter</span></span>|<span data-ttu-id="a81e3-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a81e3-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="a81e3-110">*AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="a81e3-110">*AffectRecords*</span></span> |<span data-ttu-id="a81e3-p101">Optional. Ein [AffectEnum](affectenum.md)-Wert, der angibt, wie viele Datensätze von der **UpdateBatch** -Methode betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="a81e3-p101">Optional. An [AffectEnum](affectenum.md) value that indicates how many records the **UpdateBatch** method will affect.</span></span>|

## <a name="remarks"></a><span data-ttu-id="a81e3-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a81e3-113">Remarks</span></span>

<span data-ttu-id="a81e3-114">Verwenden Sie die **UpdateBatch** -Methode, wenn Sie ein **Recordset** -Objekt im Batchaktualisierungsmodus ändern, um alle in einem **Recordset** -Objekt vorgenommenen Änderungen an die zugrunde liegende Datenbank zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="a81e3-114">Use the **UpdateBatch** method when modifying a **Recordset** object in batch update mode to transmit all changes made in a **Recordset** object to the underlying database.</span></span>

<span data-ttu-id="a81e3-p102">Wenn das **Recordset** -Objekt die Batchaktualisierung unterstützt, können Sie mehrere Änderungen an mindestens einem Datensatz bis zum Aufrufen der **UpdateBatch** -Methode lokal speichern. Falls Sie den aktuellen Datensatz bearbeiten oder einen neuen Datensatz hinzufügen, wenn Sie die **UpdateBatch** -Methode aufrufen, ruft ADO automatisch die [Update](update-method-ado.md)-Methode auf, um ausstehende Änderungen am aktuellen Datensatz zu speichern, bevor die Batchänderungen an den Anbieter übertragen werden. Sie sollten die Batchaktualisierung nur mit einem Keysetcursor oder einem statischen Cursor verwenden.</span><span class="sxs-lookup"><span data-stu-id="a81e3-p102">If the **Recordset** object supports batch updating, you can cache multiple changes to one or more records locally until you call the **UpdateBatch** method. If you are editing the current record or adding a new record when you call the **UpdateBatch** method, ADO will automatically call the [Update](update-method-ado.md) method to save any pending changes to the current record before transmitting the batched changes to the provider. You should use batch updating with either a keyset or static cursor only.</span></span>

> [!NOTE]
> <span data-ttu-id="a81e3-118">[!HINWEIS] Wenn Sie **adAffectGroup** als Wert für diesen Parameter angeben, wird ein Fehler erzeugt, falls im aktuellen **Recordset** -Objekt keine Datensätze angezeigt werden (z. B. ein Filter, mit dem keine Datensätze übereinstimmen).</span><span class="sxs-lookup"><span data-stu-id="a81e3-118">Specifying **adAffectGroup** as the value for this parameter will result in an error when there are no visible records in the current **Recordset** (such as a filter for which no records match).</span></span>

<span data-ttu-id="a81e3-p103">Wenn beim Übertragen von Änderungen ein Fehler bei einem Datensatz oder allen Datensätzen aufgrund eines Konflikts mit den zugrunde liegenden Daten auftritt (z. B. wurde ein Datensatz bereits von einem anderen Benutzer gelöscht), gibt der Anbieter Warnungen an die [Errors](errors-collection-ado.md)-Auflistung zurück, und ein Laufzeitfehler wird gemeldet. Verwenden Sie die [Filter](filter-property-ado.md)-Eigenschaft (**adFilterAffectedRecords**) und die [Status](status-property-ado-recordset.md)-Eigenschaft, um nach Datensätzen mit Konflikten zu suchen.</span><span class="sxs-lookup"><span data-stu-id="a81e3-p103">If the attempt to transmit changes fails for any or all records because of a conflict with the underlying data (for example, a record has already been deleted by another user), the provider returns warnings to the [Errors](errors-collection-ado.md) collection and a run-time error occurs. Use the [Filter](filter-property-ado.md) property (**adFilterAffectedRecords**) and the [Status](status-property-ado-recordset.md) property to locate records with conflicts.</span></span>

<span data-ttu-id="a81e3-121">Mit der [CancelBatch](cancelbatch-method-ado.md)-Methode brechen Sie alle ausstehenden Batchaktualisierungen ab.</span><span class="sxs-lookup"><span data-stu-id="a81e3-121">To cancel all pending batch updates, use the [CancelBatch](cancelbatch-method-ado.md) method.</span></span>

<span data-ttu-id="a81e3-122">Wenn die dynamischen Eigenschaften [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) und [Update Resync](update-resync-property-dynamic-ado.md) festgelegt sind und das **Recordset** -Objekt das Ergebnis der Ausführung einer JOIN-Operation mit mehreren Tabellen ist, folgt je nach den Einstellungen der **Update Resync** -Eigenschaft auf die Ausführung der [UpdateBatch](resync-method-ado.md) -Methode implizit die **Resync**-Methode.</span><span class="sxs-lookup"><span data-stu-id="a81e3-122">If the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) and [Update Resync](update-resync-property-dynamic-ado.md) dynamic properties are set, and the **Recordset** is the result of executing a JOIN operation on multiple tables, then the execution of the **UpdateBatch** method is implicitly followed by the [Resync](resync-method-ado.md) method depending on the settings of the **Update Resync** property.</span></span>

<span data-ttu-id="a81e3-p104">Die Reihenfolge, in der die einzelnen Aktualisierungen eines Batches in der Datenquelle ausgeführt werden, stimmt nicht unbedingt mit der Reihenfolge überein, in der sie im lokalen **Recordset** -Objekt ausgeführt wurden. Die Aktualisierungsreihenfolge ist vom Anbieter abhängig. Berücksichtigen Sie dies beim Codieren von miteinander verknüpften Aktualisierungen, wie z. B. Fremdschlüsseleinschränkungen für eine Einfügung oder Aktualisierung.</span><span class="sxs-lookup"><span data-stu-id="a81e3-p104">The order in which the individual updates of a batch are performed on the data source is not necessarily the same as the order in which they were performed on the local **Recordset**. Update order is dependent upon the provider. Take this into account when coding updates that are related to one another, such as foreign key constraints on an insert or update.</span></span>

