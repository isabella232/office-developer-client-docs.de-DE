---
title: OriginalValue-Eigenschaft (ADO)
TOCTitle: OriginalValue property (ADO)
ms:assetid: 02ffc728-4692-d439-e2a6-2f02cca53a71
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248798(v=office.15)
ms:contentKeyID: 48542974
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 872e7c88e5ea4e79d6bff4aa590e72743feb3893
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884912"
---
# <a name="originalvalue-property-ado"></a><span data-ttu-id="8fa60-102">OriginalValue-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="8fa60-102">OriginalValue property (ADO)</span></span>

<span data-ttu-id="8fa60-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8fa60-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8fa60-104">Gibt den Wert eines [Felds](field-object-ado.md) im Datensatz an, bevor Änderungen vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="8fa60-104">Indicates the value of a [Field](field-object-ado.md) that existed in the record before any changes were made.</span></span>

## <a name="return-value"></a><span data-ttu-id="8fa60-105">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8fa60-105">Return value</span></span>

<span data-ttu-id="8fa60-106">Gibt einen **Variant** -Wert zurück, der den Wert eines Felds vor einer Änderung darstellt.</span><span class="sxs-lookup"><span data-stu-id="8fa60-106">Returns a **Variant** value that represents the value of a field prior to any change.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fa60-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8fa60-107">Remarks</span></span>

<span data-ttu-id="8fa60-108">Verwenden Sie die **OriginalValue** -Eigenschaft, um den ursprünglichen Wert eines Felds aus dem aktuellen Datensatz zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="8fa60-108">Use the **OriginalValue** property to return the original field value for a field from the current record.</span></span>

<span data-ttu-id="8fa60-109">Im *sofortigen Aktualisierungsmodus* (in dem der Anbieter schreibt Änderungen in der zugrunde liegenden Datenquelle nach dem Aufruf der [Update](update-method-ado.md) -Methode), die **OriginalValue** -Eigenschaft gibt den Wert des Felds, das vor Änderungen vorhanden war (d. h., da die letzte Aufruf der **Update** -Methode).</span><span class="sxs-lookup"><span data-stu-id="8fa60-109">In *immediate update mode* (in which the provider writes changes to the underlying data source after you call the [Update](update-method-ado.md) method), the **OriginalValue** property returns the field value that existed prior to any changes (that is, since the last **Update** method call).</span></span> <span data-ttu-id="8fa60-110">Dies ist der gleichen Wert, den die [CancelUpdate](cancelupdate-method-ado.md) -Methode verwendet, um die [Value](value-property-ado.md) -Eigenschaft ersetzen.</span><span class="sxs-lookup"><span data-stu-id="8fa60-110">This is the same value that the [CancelUpdate](cancelupdate-method-ado.md) method uses to replace the [Value](value-property-ado.md) property.</span></span>

<span data-ttu-id="8fa60-111">Im *Batchaktualisierungsmodus* (in dem der Anbieter mehrere Änderungen zwischenspeichert und schreibt sie in der zugrunde liegenden Datenquelle nur, wenn Sie die [UpdateBatch](updatebatch-method-ado.md) -Methode aufrufen), die **OriginalValue** -Eigenschaft gibt den Wert des Felds, das vorhanden, bevor Sie eine war ändert (d. h., seit die letzte **UpdateBatch** -Methode aufrufen).</span><span class="sxs-lookup"><span data-stu-id="8fa60-111">In *batch update mode* (in which the provider caches multiple changes and writes them to the underlying data source only when you call the [UpdateBatch](updatebatch-method-ado.md) method), the **OriginalValue** property returns the field value that existed prior to any changes (that is, since the last **UpdateBatch** method call).</span></span> <span data-ttu-id="8fa60-112">Dies ist der gleiche Wert, den die [CancelBatch](cancelbatch-method-ado.md) -Methode verwendet, um die **Value** -Eigenschaft ersetzen.</span><span class="sxs-lookup"><span data-stu-id="8fa60-112">This is the same value that the [CancelBatch](cancelbatch-method-ado.md) method uses to replace the **Value** property.</span></span> <span data-ttu-id="8fa60-113">Wenn Sie diese Eigenschaft mit der [UnderlyingValue](underlyingvalue-property-ado.md) -Eigenschaft verwenden, können Sie Konflikte lösen, die durch Batchaktualisierungen auftreten.</span><span class="sxs-lookup"><span data-stu-id="8fa60-113">When you use this property with the [UnderlyingValue](underlyingvalue-property-ado.md) property, you can resolve conflicts that arise from batch updates.</span></span>

## <a name="record"></a><span data-ttu-id="8fa60-114">Record</span><span class="sxs-lookup"><span data-stu-id="8fa60-114">Record</span></span>

<span data-ttu-id="8fa60-115">Bei [Record](record-object-ado.md)-Objekten ist die **OriginalValue** -Eigenschaft für Felder leer, die vor dem Aufruf der [Update](update-method-ado.md)-Methode hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="8fa60-115">For [Record](record-object-ado.md) objects, the **OriginalValue** property will be empty for fields added before [Update](update-method-ado.md) is called.</span></span>

