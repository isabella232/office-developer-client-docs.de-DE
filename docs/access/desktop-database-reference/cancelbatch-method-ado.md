---
title: CancelBatch-Methode (ADO)
TOCTitle: CancelBatch method (ADO)
ms:assetid: be7bf073-ed0b-e24c-7ec0-b7379236782a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249925(v=office.15)
ms:contentKeyID: 48547463
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 832b367824fd8043486ff85f63739c3288696774
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702985"
---
# <a name="cancelbatch-method-ado"></a><span data-ttu-id="22c10-102">CancelBatch-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="22c10-102">CancelBatch method (ADO)</span></span>

<span data-ttu-id="22c10-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="22c10-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="22c10-104">Eine ausstehende Batchaktualisierung wird abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="22c10-104">Cancels a pending batch update.</span></span>

## <a name="syntax"></a><span data-ttu-id="22c10-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="22c10-105">Syntax</span></span>

<span data-ttu-id="22c10-106">*Recordset-Objekt*. CancelBatch *AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="22c10-106">*recordset*.CancelBatch *AffectRecords*</span></span>

## <a name="parameters"></a><span data-ttu-id="22c10-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="22c10-107">Parameters</span></span>

|<span data-ttu-id="22c10-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="22c10-108">Parameter</span></span>|<span data-ttu-id="22c10-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="22c10-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="22c10-110">*AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="22c10-110">*AffectRecords*</span></span> |<span data-ttu-id="22c10-p101">Optional. Ein [AffectEnum](affectenum.md)-Wert, durch den angegeben wird, auf wie viele Datensätze sich die **CancelBatch** -Methode auswirkt.</span><span class="sxs-lookup"><span data-stu-id="22c10-p101">Optional. An [AffectEnum](affectenum.md) value that indicates how many records the **CancelBatch** method will affect.</span></span> |

## <a name="remarks"></a><span data-ttu-id="22c10-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="22c10-113">Remarks</span></span>

<span data-ttu-id="22c10-p102">Verwenden Sie die **CancelBatch** -Methode, um alle ausstehenden Aktualisierungen in einem [Recordset](recordset-object-ado.md) im Batchaktualisierungsmodus abzubrechen. Wenn sich das **Recordset** im Modus für sofortige Aktualisierungen befindet, wird durch Aufrufen von **CancelBatch** ohne **adAffectCurrent** ein Fehler generiert.</span><span class="sxs-lookup"><span data-stu-id="22c10-p102">Use the **CancelBatch** method to cancel any pending updates in a [Recordset](recordset-object-ado.md) in batch update mode. If the **Recordset** is in immediate update mode, calling **CancelBatch** without **adAffectCurrent** generates an error.</span></span>

<span data-ttu-id="22c10-p103">Wenn Sie den aktuellen Datensatz bearbeiten oder einen neuen Datensatz hinzufügen, wenn Sie **CancelBatch** aufrufen, wird von ADO zuerst die [CancelUpdate](cancelupdate-method-ado.md)-Methode aufgerufen, um alle zwischengespeicherten Änderungen abzubrechen. Danach werden alle ausstehenden Änderungen im **Recordset** abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="22c10-p103">If you are editing the current record or are adding a new record when you call **CancelBatch**, ADO first calls the [CancelUpdate](cancelupdate-method-ado.md) method to cancel any cached changes. After that, all pending changes in the **Recordset** are canceled.</span></span>

<span data-ttu-id="22c10-p104">Es ist möglich, dass nach einem **CancelBatch** -Aufruf der aktuelle Datensatz nicht ermittelt werden kann, insbesondere, wenn Sie dabei waren, einen neuen Datensatz hinzuzufügen. Aus diesem Grund ist es ratsam, nach dem **CancelBatch** -Aufruf die aktuelle Datensatzposition auf eine bekannte Stelle im **Recordset** festzulegen. Rufen Sie z. B. die [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)-Methode auf.</span><span class="sxs-lookup"><span data-stu-id="22c10-p104">It's possible that the current record will be indeterminable after a **CancelBatch** call, especially if you were in the process of adding a new record. For this reason, it is prudent to set the current record position to a known location in the **Recordset** after the **CancelBatch** call. For example, call the [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) method.</span></span>

<span data-ttu-id="22c10-p105">Wenn der Versuch, die ausstehenden Aktualisierungen abzubrechen, aufgrund eines Konflikts mit den zugrunde liegenden Daten fehlschlägt (z. B. weil ein Datensatz von einem anderen Benutzer gelöscht wurde), werden vom Anbieter Warnungen an die [Errors](errors-collection-ado.md)-Auflistung zurückgegeben, die Programmausführung wird jedoch nicht angehalten. Verwenden Sie die [Filter](filter-property-ado.md)-Eigenschaft (**adFilterAffectedRecord**) und die [Status](status-property-ado-recordset.md)-Eigenschaft, um Datensätze mit Konflikten zu suchen.</span><span class="sxs-lookup"><span data-stu-id="22c10-p105">If the attempt to cancel the pending updates fails because of a conflict with the underlying data (for example, a record has been deleted by another user), the provider returns warnings to the [Errors](errors-collection-ado.md) collection but does not halt program execution. A run-time error occurs only if there are conflicts on all the requested records. Use the [Filter](filter-property-ado.md) property (**adFilterAffectedRecords**) and the [Status](status-property-ado-recordset.md) property to locate records with conflicts.</span></span>

