---
title: Update-Methode (ADO)
TOCTitle: Update method (ADO)
ms:assetid: fc88cab6-c379-bb4f-530c-da08107924e0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250294(v=office.15)
ms:contentKeyID: 48548893
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f077634abea6fadfe5c4305fc25b28e6d57bf13e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306237"
---
# <a name="update-method-ado"></a><span data-ttu-id="d2515-102">Update-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="d2515-102">Update method (ADO)</span></span>

<span data-ttu-id="d2515-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d2515-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d2515-104">Speichert alle Änderungen, die Sie an der aktuellen Zeile eines [Recordset](recordset-object-ado.md)-Objekts oder der [Fields](fields-collection-ado.md)-Auflistung eines [Record](record-object-ado.md)-Objekts vornehmen.</span><span class="sxs-lookup"><span data-stu-id="d2515-104">Saves any changes you make to the current row of a [Recordset](recordset-object-ado.md) object, or the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2515-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2515-105">Syntax</span></span>

<span data-ttu-id="d2515-106">*Recordset*. Aktualisieren von*Feldern*, *Werten*</span><span class="sxs-lookup"><span data-stu-id="d2515-106">*recordset*.Update*Fields*, *Values*</span></span>

<span data-ttu-id="d2515-107">*Record*.</span><span class="sxs-lookup"><span data-stu-id="d2515-107">*record*.</span></span> <span data-ttu-id="d2515-108">*Felder*. Update</span><span class="sxs-lookup"><span data-stu-id="d2515-108">*Fields*.Update</span></span>

## <a name="parameters"></a><span data-ttu-id="d2515-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2515-109">Parameters</span></span>

|<span data-ttu-id="d2515-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2515-110">Parameter</span></span>|<span data-ttu-id="d2515-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d2515-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="d2515-112">*Fields*</span><span class="sxs-lookup"><span data-stu-id="d2515-112">*Fields*</span></span> |<span data-ttu-id="d2515-p102">Optional. Ein Wert vom Datentyp **Variant**, der einen einzelnen Namen darstellt, oder ein Array vom Datentyp **Variant**, das Namen oder Positionen des Felds oder der Felder darstellt, das bzw. die Sie ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="d2515-p102">Optional. A **Variant** that represents a single name, or a **Variant** array that represents names or ordinal positions of the field or fields you wish to modify.</span></span>|
|<span data-ttu-id="d2515-115">*Values*</span><span class="sxs-lookup"><span data-stu-id="d2515-115">*Values*</span></span> |<span data-ttu-id="d2515-p103">Optional. Ein Wert vom Datentyp **Variant**, der einen einzelnen Wert darstellt, oder ein Array vom Datentyp **Variant**, das Werte für das Feld oder die Felder im neuen Datensatz darstellt.</span><span class="sxs-lookup"><span data-stu-id="d2515-p103">Optional. A **Variant** that represents a single value, or a **Variant** array that represents values for the field or fields in the new record.</span></span>|

## <a name="remarks"></a><span data-ttu-id="d2515-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d2515-118">Remarks</span></span>

### <a name="recordset"></a><span data-ttu-id="d2515-119">Recordset</span><span class="sxs-lookup"><span data-stu-id="d2515-119">Recordset</span></span>

<span data-ttu-id="d2515-p104">Verwenden Sie die **Update**-Methode, um Änderungen am aktuellen Datensatz eines **Recordset**-Objekts seit dem Aufrufen der [AddNew](addnew-method-ado.md)-Methode oder seit dem Ändern von Feldwerten in einem vorhandenen Datensatz zu speichern. Das **Recordset**-Objekt muss Aktualisierungen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d2515-p104">Use the **Update** method to save any changes you make to the current record of a **Recordset** object since calling the [AddNew](addnew-method-ado.md) method or since changing any field values in an existing record. The **Recordset** object must support updates.</span></span>

<span data-ttu-id="d2515-122">Führen Sie eine der folgenden Aktionen aus, um Feldwerte festzulegen:</span><span class="sxs-lookup"><span data-stu-id="d2515-122">To set field values, do one of the following:</span></span>

- <span data-ttu-id="d2515-123">Weisen Sie der [Value](value-property-ado.md)-Eigenschaft eines [Field](field-object-ado.md)-Objekts Werte zu, und rufen Sie die **Update**-Methode auf.</span><span class="sxs-lookup"><span data-stu-id="d2515-123">Assign values to a [Field](field-object-ado.md) object's [Value](value-property-ado.md) property and call the **Update** method.</span></span>

- <span data-ttu-id="d2515-124">Übergeben Sie mithilfe des **Update**-Aufrufs einen Feldnamen und einen Wert als Argumente.</span><span class="sxs-lookup"><span data-stu-id="d2515-124">Pass a field name and a value as arguments with the **Update** call.</span></span>

- <span data-ttu-id="d2515-125">Übergeben Sie mithilfe des **Update**-Aufrufs ein Array von Feldnamen und ein Array von Werten.</span><span class="sxs-lookup"><span data-stu-id="d2515-125">Pass an array of field names and an array of values with the **Update** call.</span></span>

<span data-ttu-id="d2515-p105">Wenn Sie Arrays von Feldern und Werten verwenden, müssen in beiden Arrays gleich viele Elemente vorhanden sein. Die Reihenfolge der Feldnamen muss außerdem der Reihenfolge der Feldwerte entsprechen. Wenn die Anzahl und die Reihenfolge von Feldern und Werten nicht übereinstimmen, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="d2515-p105">When you use arrays of fields and values, there must be an equal number of elements in both arrays. Also, the order of field names must match the order of field values. If the number and order of fields and values do not match, an error occurs.</span></span>

<span data-ttu-id="d2515-p106">Wenn das **Recordset** -Objekt die Batchaktualisierung unterstützt, können Sie mehrere Änderungen an mindestens einem Datensatz bis zum Aufrufen der [UpdateBatch](updatebatch-method-ado.md)-Methode lokal speichern. Falls Sie den aktuellen Datensatz bearbeiten oder einen neuen Datensatz hinzufügen, wenn Sie die **UpdateBatch** -Methode aufrufen, ruft ADO automatisch die **Update** -Methode auf, um ausstehende Änderungen am aktuellen Datensatz zu speichern, bevor die Batchänderungen an den Anbieter übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="d2515-p106">If the **Recordset** object supports batch updating, you can cache multiple changes to one or more records locally until you call the [UpdateBatch](updatebatch-method-ado.md) method. If you are editing the current record or adding a new record when you call the **UpdateBatch** method, ADO will automatically call the **Update** method to save any pending changes to the current record before transmitting the batched changes to the provider.</span></span>

<span data-ttu-id="d2515-p107">Wenn Sie den Datensatz verlassen, den Sie hinzufügen oder bearbeiten, bevor Sie die **Update** -Methode aufrufen, ruft ADO zum Speichern der Änderungen automatisch **Update** auf. Sie müssen die [CancelUpdate](cancelupdate-method-ado.md)-Methode aufrufen, falls Sie Änderungen am aktuellen Datensatz abbrechen oder einen neu hinzugefügten Datensatz verwerfen möchten.</span><span class="sxs-lookup"><span data-stu-id="d2515-p107">If you move from the record you are adding or editing before calling the **Update** method, ADO will automatically call **Update** to save the changes. You must call the [CancelUpdate](cancelupdate-method-ado.md) method if you want to cancel any changes made to the current record or discard a newly added record.</span></span>

<span data-ttu-id="d2515-133">Der aktuelle Datensatz bleibt aktuell, nachdem Sie die **Update** -Methode aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="d2515-133">The current record remains current after you call the **Update** method.</span></span>

### <a name="record"></a><span data-ttu-id="d2515-134">Aufzeichnen</span><span class="sxs-lookup"><span data-stu-id="d2515-134">Record</span></span>

<span data-ttu-id="d2515-135">Mit der **Update**-Methode werden Lösch- und Aktualisierungsvorgänge für Felder in der [Fields](fields-collection-ado.md)-Auflistung eines **Record**-Objekts abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="d2515-135">The **Update** method finalizes additions, deletions, and updates to fields in the [Fields](fields-collection-ado.md) collection of a **Record** object.</span></span>

<span data-ttu-id="d2515-p108">Beispielsweise werden mit der **Delete**-Methode gelöschte Felder sofort zum Löschen gekennzeichnet, verbleiben aber in der Auflistung. Die **Update**-Methode muss aufgerufen werden, damit diese Felder tatsächlich in der Auflistung des Anbieters gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="d2515-p108">For example, fields deleted with the **Delete** method are marked for deletion immediately but remain in the collection. The **Update** method must be called to actually delete these fields from the provider's collection.</span></span>

