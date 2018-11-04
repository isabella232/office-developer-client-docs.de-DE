---
title: Delete-Methode (ADO-Recordset)
TOCTitle: Delete method (ADO Recordset)
ms:assetid: 62c39b4d-223e-7b48-6780-6cd272e3114e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249374(v=office.15)
ms:contentKeyID: 48545246
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3a7ab998052cc08aa57320d05e46542b84282e6c
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949509"
---
# <a name="delete-method-ado-recordset"></a><span data-ttu-id="50b72-102">Delete-Methode (ADO-Recordset)</span><span class="sxs-lookup"><span data-stu-id="50b72-102">Delete method (ADO Recordset)</span></span>

<span data-ttu-id="50b72-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="50b72-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="50b72-104">Löscht den aktuellen Datensatz oder eine Gruppe von Datensätzen.</span><span class="sxs-lookup"><span data-stu-id="50b72-104">Deletes the current record or a group of records.</span></span>

## <a name="syntax"></a><span data-ttu-id="50b72-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="50b72-105">Syntax</span></span>

<span data-ttu-id="50b72-106">*Recordset-Objekt*. *AffectRecords* löschen</span><span class="sxs-lookup"><span data-stu-id="50b72-106">*recordset*.Delete *AffectRecords*</span></span>

## <a name="parameters"></a><span data-ttu-id="50b72-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="50b72-107">Parameters</span></span>

|<span data-ttu-id="50b72-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="50b72-108">Parameter</span></span>|<span data-ttu-id="50b72-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="50b72-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="50b72-110">*AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="50b72-110">*AffectRecords*</span></span> |<span data-ttu-id="50b72-p101">Ein [AffectEnum](affectenum.md)-Wert, der bestimmt, wie viele Datensätze die **Delete** -Methode beeinflusst. Der Standardwert lautet **adAffectCurrent**.</span><span class="sxs-lookup"><span data-stu-id="50b72-p101">An [AffectEnum](affectenum.md) value that determines how many records the **Delete** method will affect. The default value is **adAffectCurrent**.</span></span>|

> [!NOTE]
> <span data-ttu-id="50b72-113">[!HINWEIS] **adAffectAll** und **adAffectAllChapters** sind keine gültigen Argumente für **Delete**.</span><span class="sxs-lookup"><span data-stu-id="50b72-113">**adAffectAll** and **adAffectAllChapters** are not valid arguments to **Delete**.</span></span>

## <a name="remarks"></a><span data-ttu-id="50b72-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="50b72-114">Remarks</span></span>

<span data-ttu-id="50b72-p102">Mithilfe der **Delete** -Methode kann der aktuelle Datensatz oder eine Gruppe von Datensätzen in einem [Recordset](recordset-object-ado.md)-Objekt zum Löschen markiert werden. Lässt das **Recordset** -Objekt das Löschen von Datensätzen nicht zu, tritt ein Fehler auf. Wenn Sie sich im Modus der unmittelbaren Aktualisierung befinden, werden die Löschvorgänge unmittelbar in der Datenbank angezeigt. Kann ein Datensatz nicht gelöscht werden (z. B. aufgrund von Verletzungen der Datenbankintegrität), verbleibt der Datensatz nach dem Aufrufen von **Update** im Bearbeitungsmodus. Folglich müssen Sie die Aktualisierung mithilfe von [CancelUpdate](cancelupdate-method-ado.md) abbrechen, bevor Sie den aktuellen Datensatz verlassen können (z. B. mithilfe von [Close](close-method-ado.md), [Move](move-method-ado.md) oder [NextRecordset](nextrecordset-method-ado.md)).</span><span class="sxs-lookup"><span data-stu-id="50b72-p102">Using the **Delete** method marks the current record or a group of records in a [Recordset](recordset-object-ado.md) object for deletion. If the **Recordset** object doesn't allow record deletion, an error occurs. If you are in immediate update mode, deletions occur in the database immediately. If a record cannot be successfully deleted (due to database integrity violations, for example), the record will remain in edit mode after the call to **Update**. This means that you must cancel the update with [CancelUpdate](cancelupdate-method-ado.md) before moving off the current record (for example, with [Close](close-method-ado.md), [Move](move-method-ado.md), or [NextRecordset](nextrecordset-method-ado.md)).</span></span>

<span data-ttu-id="50b72-p103">Wenn Sie sich im Batchaktualisierungsmodus befinden, werden die Datensätze zum Löschen aus dem Cache markiert, und der eigentliche Löschvorgang wird ausgeführt, sobald Sie die [UpdateBatch](updatebatch-method-ado.md)-Methode aufgerufen haben. (Verwenden Sie die [Filter](filter-property-ado.md)-Eigenschaft, um die gelöschten Datensätze anzuzeigen.)</span><span class="sxs-lookup"><span data-stu-id="50b72-p103">If you are in batch update mode, the records are marked for deletion from the cache and the actual deletion happens when you call the [UpdateBatch](updatebatch-method-ado.md) method. (Use the [Filter](filter-property-ado.md) property to view the deleted records.)</span></span>

<span data-ttu-id="50b72-p104">Beim Abrufen von Feldwerten aus den gelöschten Datensätzen wird ein Fehler generiert. Nach dem Löschen des aktuellen Datensatzes bleibt der gelöschte Datensatz der aktuelle Datensatz, bis Sie zu einem anderen Datensatz wechseln. Sobald Sie einen gelöschten Datensatz verlassen, können Sie nicht mehr auf diesen Datensatz zugreifen.</span><span class="sxs-lookup"><span data-stu-id="50b72-p104">Retrieving field values from the deleted record generates an error. After deleting the current record, the deleted record remains current until you move to a different record. Once you move away from the deleted record, it is no longer accessible.</span></span>

<span data-ttu-id="50b72-p105">Wenn Sie Löschvorgänge in eine Transaktion schachteln, können Sie gelöschte Datensätze mithilfe der [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md)-Methode wiederherstellen. Wenn Sie sich im Batchaktualisierungsmodus befinden, können Sie mithilfe der [CancelBatch](cancelbatch-method-ado.md)-Methode einen ausstehenden Löschvorgang oder eine Gruppe von ausstehenden Löschvorgängen abbrechen.</span><span class="sxs-lookup"><span data-stu-id="50b72-p105">If you nest deletions in a transaction, you can recover deleted records with the [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) method. If you are in batch update mode, you can cancel a pending deletion or group of pending deletions with the [CancelBatch](cancelbatch-method-ado.md) method.</span></span>

<span data-ttu-id="50b72-p106">Schlägt das Löschen eines Datensatzes aufgrund eines Konflikts mit den zugrunde liegenden Daten fehl (z. B. wenn ein Datensatz bereits von einem anderen Benutzer gelöscht wurde), gibt der Anbieter Warnungen an die [Errors](errors-collection-ado.md)-Auflistung zurück, beendet aber nicht die Ausführung des Programms. Ein Laufzeitfehler tritt nur dann auf, wenn bei allen angeforderten Datensätzen Konflikte bestehen.</span><span class="sxs-lookup"><span data-stu-id="50b72-p106">If the attempt to delete records fails because of a conflict with the underlying data (for example, a record has already been deleted by another user), the provider returns warnings to the [Errors](errors-collection-ado.md) collection but does not halt program execution. A run-time error occurs only if there are conflicts on all the requested records.</span></span>

<span data-ttu-id="50b72-129">Ist die dynamische Eigenschaft [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) festgelegt und handelt es sich beim **Recordset** -Objekt um das Ergebnis der Ausführung eines JOIN-Vorgangs für mehrere Tabellen, löscht die **Delete** -Methode nur Zeilen aus der Tabelle, die in der [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md)-Eigenschaft angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="50b72-129">If the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) dynamic property is set, and the **Recordset** is the result of executing a JOIN operation on multiple tables, then the **Delete** method will only delete rows from the table named in the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) property.</span></span>

