---
title: UnderlyingValue-Eigenschaft (ADO)
TOCTitle: UnderlyingValue property (ADO)
ms:assetid: f84f4c1c-2bd4-a725-3575-ed063ead13c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250262(v=office.15)
ms:contentKeyID: 48548782
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6d1618a0cb310c1e564fe18289da6a2d35e91d0b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717293"
---
# <a name="underlyingvalue-property-ado"></a><span data-ttu-id="c2d58-102">UnderlyingValue-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="c2d58-102">UnderlyingValue property (ADO)</span></span>


<span data-ttu-id="c2d58-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c2d58-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="c2d58-104">Gibt den aktuellen Wert eines [Field](field-object-ado.md)-Objekts in der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="c2d58-104">Indicates a [Field](field-object-ado.md) object's current value in the database.</span></span>

## <a name="return-value"></a><span data-ttu-id="c2d58-105">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c2d58-105">Return value</span></span>

<span data-ttu-id="c2d58-106">Gibt einen **Variant** -Wert zurück, der den Wert eines **Field** -Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="c2d58-106">Returns a **Variant** value that indicates the value of the **Field**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2d58-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c2d58-107">Remarks</span></span>

<span data-ttu-id="c2d58-p101">Verwenden Sie die **UnderlyingValue** -Eigenschaft, um den aktuellen Feldwert aus der Datenbank zu ermitteln. Der Feldwert in der **UnderlyingValue** -Eigenschaft ist der Wert, der für Ihre Transaktion zu sehen ist. Er ist möglicherweise das Ergebnis einer kürzlichen Aktualisierung durch eine andere Transaktion. Dieser Wert kann sich von der [OriginalValue](originalvalue-property-ado.md)-Eigenschaft unterscheiden, die den ursprünglich an das [Recordset](recordset-object-ado.md)-Objekt zurückgegebenen Wert wiedergibt.</span><span class="sxs-lookup"><span data-stu-id="c2d58-p101">Use the **UnderlyingValue** property to return the current field value from the database. The field value in the **UnderlyingValue** property is the value that is visible to your transaction and may be the result of a recent update by another transaction. This may differ from the [OriginalValue](originalvalue-property-ado.md) property, which reflects the value that was originally returned to the [Recordset](recordset-object-ado.md).</span></span>

<span data-ttu-id="c2d58-p102">Dieses Verhalten ähnelt der [Resync](resync-method-ado.md)-Methode. Jedoch gibt die **UnderlyingValue** -Eigenschaft nur den Wert für ein bestimmtes Feld aus dem aktuellen Datensatz zurück. Dabei handelt es sich um denselben Wert, der bei der [Resync](resync-method-ado.md)-Methode zum Ersetzen der [Value](value-property-ado.md)-Eigenschaft verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c2d58-p102">This is similar to using the [Resync](resync-method-ado.md) method, but the **UnderlyingValue** property returns only the value for a specific field from the current record. This is the same value that the [Resync](resync-method-ado.md) method uses to replace the [Value](value-property-ado.md) property.</span></span>

<span data-ttu-id="c2d58-113">Wenn Sie diese Eigenschaft in Verbindung mit der **UnderlyingValue** -Eigenschaft verwenden, können Sie Konflikte lösen, die durch Batchaktualisierungen auftreten.</span><span class="sxs-lookup"><span data-stu-id="c2d58-113">When you use this property with the **OriginalValue** property, you can resolve conflicts that arise from batch updates.</span></span>

## <a name="record"></a><span data-ttu-id="c2d58-114">Record</span><span class="sxs-lookup"><span data-stu-id="c2d58-114">Record</span></span>

<span data-ttu-id="c2d58-115">Bei [Record](record-object-ado.md)-Objekten ist diese Eigenschaft für Felder leer, die vor dem Aufruf der [Update](update-method-ado.md)-Methode hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="c2d58-115">For [Record](record-object-ado.md) objects, this property will be empty for fields added before [Update](update-method-ado.md) is called.</span></span>

