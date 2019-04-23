---
title: OriginalValue-Eigenschaft (ADO)
TOCTitle: OriginalValue property (ADO)
ms:assetid: 02ffc728-4692-d439-e2a6-2f02cca53a71
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248798(v=office.15)
ms:contentKeyID: 48542974
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0724320e1aaa1e7bfd3ceab8cf54afd5921c7425
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288182"
---
# <a name="originalvalue-property-ado"></a><span data-ttu-id="8b15e-102">OriginalValue-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="8b15e-102">OriginalValue property (ADO)</span></span>

<span data-ttu-id="8b15e-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8b15e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8b15e-104">Gibt den Wert eines [Felds](field-object-ado.md) im Datensatz an, bevor Änderungen vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="8b15e-104">Indicates the value of a [Field](field-object-ado.md) that existed in the record before any changes were made.</span></span>

## <a name="return-value"></a><span data-ttu-id="8b15e-105">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8b15e-105">Return value</span></span>

<span data-ttu-id="8b15e-106">Gibt einen **Variant**-Wert zurück, der den Wert eines Felds vor einer Änderung darstellt.</span><span class="sxs-lookup"><span data-stu-id="8b15e-106">Returns a **Variant** value that represents the value of a field prior to any change.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b15e-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8b15e-107">Remarks</span></span>

<span data-ttu-id="8b15e-108">Verwenden Sie die **OriginalValue**-Eigenschaft, um den ursprünglichen Wert eines Felds aus dem aktuellen Datensatz zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="8b15e-108">Use the **OriginalValue** property to return the original field value for a field from the current record.</span></span>

<span data-ttu-id="8b15e-109">Im *sofortigen Aktualisierungsmodus* (in dem der Anbieter Änderungen an der zugrunde liegenden Datenquelle schreibt, nachdem Sie die [Update](update-method-ado.md) -Methode aufgerufen haben), gibt die **OriginalValue** -Eigenschaft den Feldwert zurück, der vor Änderungen vorhanden war (das heißt, da der Aufruf der letzten **Update** -Methode).</span><span class="sxs-lookup"><span data-stu-id="8b15e-109">In *immediate update mode* (in which the provider writes changes to the underlying data source after you call the [Update](update-method-ado.md) method), the **OriginalValue** property returns the field value that existed prior to any changes (that is, since the last **Update** method call).</span></span> <span data-ttu-id="8b15e-110">Dabei handelt es sich um denselben Wert, der in der [CancelUpdate](cancelupdate-method-ado.md)-Methode dazu verwendet wird, den Wert der [Value](value-property-ado.md)-Eigenschaft zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="8b15e-110">This is the same value that the [CancelUpdate](cancelupdate-method-ado.md) method uses to replace the [Value](value-property-ado.md) property.</span></span>

<span data-ttu-id="8b15e-p102">Im *Batchaktualisierungsmodus* (in dem der Anbieter mehrere Änderungen zwischenspeichert und erst in die zugrunde liegende Datenquelle schreibt, wenn Sie die [UpdateBatch](updatebatch-method-ado.md)-Methode aufrufen) gibt die **OriginalValue**-Eigenschaft den Feldwert zurück, der vor Änderungen vorhanden war (d. h. seit dem letzten Aufruf der **UpdateBatch**-Methode). Dabei handelt es sich um denselben Wert, der bei der [CancelBatch](cancelbatch-method-ado.md)-Methode zum Ersetzen der **Value**-Eigenschaft verwendet wird. Wenn Sie diese Eigenschaft in Verbindung mit der [OriginalValue](underlyingvalue-property-ado.md)-Eigenschaft verwenden, können Sie Konflikte lösen, die durch Batchaktualisierungen auftreten.</span><span class="sxs-lookup"><span data-stu-id="8b15e-p102">In *batch update mode* (in which the provider caches multiple changes and writes them to the underlying data source only when you call the [UpdateBatch](updatebatch-method-ado.md) method), the **OriginalValue** property returns the field value that existed prior to any changes (that is, since the last **UpdateBatch** method call). This is the same value that the [CancelBatch](cancelbatch-method-ado.md) method uses to replace the **Value** property. When you use this property with the [UnderlyingValue](underlyingvalue-property-ado.md) property, you can resolve conflicts that arise from batch updates.</span></span>

## <a name="record"></a><span data-ttu-id="8b15e-114">Aufzeichnen</span><span class="sxs-lookup"><span data-stu-id="8b15e-114">Record</span></span>

<span data-ttu-id="8b15e-115">Bei [Record](record-object-ado.md)-Objekten ist die **OriginalValue**-Eigenschaft für Felder leer, die vor dem Aufruf der [Update](update-method-ado.md)-Methode hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="8b15e-115">For [Record](record-object-ado.md) objects, the **OriginalValue** property will be empty for fields added before [Update](update-method-ado.md) is called.</span></span>

