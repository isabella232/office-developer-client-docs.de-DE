---
title: Update-Methode (ADO)
TOCTitle: Update Method (ADO)
ms:assetid: fc88cab6-c379-bb4f-530c-da08107924e0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250294(v=office.15)
ms:contentKeyID: 48548893
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9c7ca5e1f1d055c8a651b69f7c76ab4b918c1147
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474232"
---
# <a name="update-method-ado"></a><span data-ttu-id="cdaca-102">Update-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="cdaca-102">Update Method (ADO)</span></span>


<span data-ttu-id="cdaca-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="cdaca-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="cdaca-104">Speichert alle Änderungen, die Sie an der aktuellen Zeile eines [Recordset](recordset-object-ado.md)-Objekts oder der [Fields](fields-collection-ado.md)-Auflistung eines [Record](record-object-ado.md)-Objekts vornehmen.</span><span class="sxs-lookup"><span data-stu-id="cdaca-104">Saves any changes you make to the current row of a [Recordset](recordset-object-ado.md) object, or the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdaca-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cdaca-105">Syntax</span></span>

<span data-ttu-id="cdaca-106">*Recordset-Objekt*. Aktualisieren der*Felder*, *Werte*</span><span class="sxs-lookup"><span data-stu-id="cdaca-106">*recordset*.Update*Fields*, *Values*</span></span>

<span data-ttu-id="cdaca-107">*Datensatz*.</span><span class="sxs-lookup"><span data-stu-id="cdaca-107">*record*.</span></span> <span data-ttu-id="cdaca-108">*Felder*. Update</span><span class="sxs-lookup"><span data-stu-id="cdaca-108">*Fields*.Update</span></span>

## <a name="parameters"></a><span data-ttu-id="cdaca-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="cdaca-109">Parameters</span></span>

  - <span data-ttu-id="cdaca-110">*Fields*</span><span class="sxs-lookup"><span data-stu-id="cdaca-110">*Fields*</span></span>

  - <span data-ttu-id="cdaca-p102">Optional. Ein Wert vom Datentyp **Variant**, der einen einzelnen Namen darstellt, oder ein Array vom Datentyp **Variant**, das Namen oder Positionen des Felds oder der Felder darstellt, das bzw. die Sie ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="cdaca-p102">Optional. A **Variant** that represents a single name, or a **Variant** array that represents names or ordinal positions of the field or fields you wish to modify.</span></span>

  - <span data-ttu-id="cdaca-113">*Values*</span><span class="sxs-lookup"><span data-stu-id="cdaca-113">*Values*</span></span>

  - <span data-ttu-id="cdaca-p103">Optional. Ein Wert vom Datentyp **Variant**, der einen einzelnen Wert darstellt, oder ein Array vom Datentyp **Variant**, das Werte für das Feld oder die Felder im neuen Datensatz darstellt.</span><span class="sxs-lookup"><span data-stu-id="cdaca-p103">Optional. A **Variant** that represents a single value, or a **Variant** array that represents values for the field or fields in the new record.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdaca-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cdaca-116">Remarks</span></span>

<span data-ttu-id="cdaca-117">**Recordset**</span><span class="sxs-lookup"><span data-stu-id="cdaca-117">**Recordset**</span></span>

<span data-ttu-id="cdaca-p104">Verwenden Sie die **Update** -Methode, um Änderungen am aktuellen Datensatz eines **Recordset** -Objekts seit dem Aufrufen der [AddNew](addnew-method-ado.md)-Methode oder seit dem Ändern von Feldwerten in einem vorhandenen Datensatz zu speichern. Das **Recordset** -Objekt muss Aktualisierungen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="cdaca-p104">Use the **Update** method to save any changes you make to the current record of a **Recordset** object since calling the [AddNew](addnew-method-ado.md) method or since changing any field values in an existing record. The **Recordset** object must support updates.</span></span>

<span data-ttu-id="cdaca-120">Führen Sie eine der folgenden Aktionen aus, um Feldwerte festzulegen:</span><span class="sxs-lookup"><span data-stu-id="cdaca-120">To set field values, do one of the following:</span></span>

  - <span data-ttu-id="cdaca-121">Weisen Sie der [Value](field-object-ado.md)-Eigenschaft eines [Field](value-property-ado.md)-Objekts Werte zu, und rufen Sie die **Update** -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="cdaca-121">Assign values to a [Field](field-object-ado.md) object's [Value](value-property-ado.md) property and call the **Update** method.</span></span>

  - <span data-ttu-id="cdaca-122">Übergeben Sie mithilfe des **Update** -Aufrufs einen Feldnamen und einen Wert als Argumente.</span><span class="sxs-lookup"><span data-stu-id="cdaca-122">Pass a field name and a value as arguments with the **Update** call.</span></span>

  - <span data-ttu-id="cdaca-123">Übergeben Sie mithilfe des **Update** -Aufrufs ein Array von Feldnamen und ein Array von Werten.</span><span class="sxs-lookup"><span data-stu-id="cdaca-123">Pass an array of field names and an array of values with the **Update** call.</span></span>

<span data-ttu-id="cdaca-p105">Wenn Sie Arrays von Feldern und Werten verwenden, müssen in beiden Arrays gleich viele Elemente vorhanden sein. Die Reihenfolge der Feldnamen muss außerdem der Reihenfolge der Feldwerte entsprechen. Wenn die Anzahl und die Reihenfolge von Feldern und Werten nicht übereinstimmen, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="cdaca-p105">When you use arrays of fields and values, there must be an equal number of elements in both arrays. Also, the order of field names must match the order of field values. If the number and order of fields and values do not match, an error occurs.</span></span>

<span data-ttu-id="cdaca-p106">Wenn das **Recordset** -Objekt die Batchaktualisierung unterstützt, können Sie mehrere Änderungen an mindestens einem Datensatz bis zum Aufrufen der [UpdateBatch](updatebatch-method-ado.md)-Methode lokal speichern. Falls Sie den aktuellen Datensatz bearbeiten oder einen neuen Datensatz hinzufügen, wenn Sie die **UpdateBatch** -Methode aufrufen, ruft ADO automatisch die **Update** -Methode auf, um ausstehende Änderungen am aktuellen Datensatz zu speichern, bevor die Batchänderungen an den Anbieter übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="cdaca-p106">If the **Recordset** object supports batch updating, you can cache multiple changes to one or more records locally until you call the [UpdateBatch](updatebatch-method-ado.md) method. If you are editing the current record or adding a new record when you call the **UpdateBatch** method, ADO will automatically call the **Update** method to save any pending changes to the current record before transmitting the batched changes to the provider.</span></span>

<span data-ttu-id="cdaca-p107">Wenn Sie den Datensatz verlassen, den Sie hinzufügen oder bearbeiten, bevor Sie die **Update** -Methode aufrufen, ruft ADO zum Speichern der Änderungen automatisch **Update** auf. Sie müssen die [CancelUpdate](cancelupdate-method-ado.md)-Methode aufrufen, falls Sie Änderungen am aktuellen Datensatz abbrechen oder einen neu hinzugefügten Datensatz verwerfen möchten.</span><span class="sxs-lookup"><span data-stu-id="cdaca-p107">If you move from the record you are adding or editing before calling the **Update** method, ADO will automatically call **Update** to save the changes. You must call the [CancelUpdate](cancelupdate-method-ado.md) method if you want to cancel any changes made to the current record or discard a newly added record.</span></span>

<span data-ttu-id="cdaca-131">Der aktuelle Datensatz bleibt aktuell, nachdem Sie die **Update** -Methode aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="cdaca-131">The current record remains current after you call the **Update** method.</span></span>

<span data-ttu-id="cdaca-132">**Record**</span><span class="sxs-lookup"><span data-stu-id="cdaca-132">**Record**</span></span>

<span data-ttu-id="cdaca-133">Mit der **Update** -Methode werden Lösch- und Aktualisierungsvorgänge für Felder in der [Fields](fields-collection-ado.md)-Auflistung eines **Record** -Objekts abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="cdaca-133">The **Update** method finalizes additions, deletions, and updates to fields in the [Fields](fields-collection-ado.md) collection of a **Record** object.</span></span>

<span data-ttu-id="cdaca-p108">Beispielsweise werden mit der **Delete** -Methode gelöschte Felder sofort zum Löschen gekennzeichnet, verbleiben aber in der Auflistung. Die **Update** -Methode muss aufgerufen werden, damit diese Felder tatsächlich in der Auflistung des Anbieters gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="cdaca-p108">For example, fields deleted with the **Delete** method are marked for deletion immediately but remain in the collection. The **Update** method must be called to actually delete these fields from the provider's collection.</span></span>

