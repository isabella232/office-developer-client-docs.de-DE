---
<span data-ttu-id="462d6-101"><<<<<<< HEAD-Titel: UnderlyingValue-Eigenschaft (ADO) TOCTitle: UnderlyingValue-Eigenschaft (ADO) === Titel: UnderlyingValue-Eigenschaft (ADO) TOCTitle: UnderlyingValue-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="462d6-101"><<<<<<< HEAD title: UnderlyingValue Property (ADO) TOCTitle: UnderlyingValue Property (ADO) ======= title: UnderlyingValue property (ADO) TOCTitle: UnderlyingValue property (ADO)</span></span>
>>>>>>> <span data-ttu-id="462d6-102">Master Ms:assetid: f84f4c1c-2bd4-a725-3575-ed063ead13c8 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ250262(v=office.15) Ms:contentKeyID: 48548782 ms.date: 09/18/2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="462d6-102">master ms:assetid: f84f4c1c-2bd4-a725-3575-ed063ead13c8 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250262(v=office.15) ms:contentKeyID: 48548782 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="462d6-103"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="462d6-103"><<<<<<< HEAD</span></span>
# <a name="underlyingvalue-property-ado"></a><span data-ttu-id="462d6-104">UnderlyingValue-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="462d6-104">UnderlyingValue Property (ADO)</span></span>
=======
# <a name="underlyingvalue-property-ado"></a><span data-ttu-id="462d6-105">UnderlyingValue-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="462d6-105">UnderlyingValue property (ADO)</span></span>
>>>>>>> <span data-ttu-id="462d6-106">master</span><span class="sxs-lookup"><span data-stu-id="462d6-106">master</span></span>


<span data-ttu-id="462d6-107">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="462d6-107">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="462d6-108">Gibt den aktuellen Wert eines [Field](field-object-ado.md)-Objekts in der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="462d6-108">Indicates a [Field](field-object-ado.md) object's current value in the database.</span></span>

<span data-ttu-id="462d6-109"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="462d6-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="462d6-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="462d6-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="462d6-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="462d6-111">Return value</span></span>
>>>>>>> <span data-ttu-id="462d6-112">master</span><span class="sxs-lookup"><span data-stu-id="462d6-112">master</span></span>

<span data-ttu-id="462d6-113">Gibt einen **Variant** -Wert zurück, der den Wert eines **Field** -Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="462d6-113">Returns a **Variant** value that indicates the value of the **Field**.</span></span>

## <a name="remarks"></a><span data-ttu-id="462d6-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="462d6-114">Remarks</span></span>

<span data-ttu-id="462d6-p101">Verwenden Sie die **UnderlyingValue** -Eigenschaft, um den aktuellen Feldwert aus der Datenbank zu ermitteln. Der Feldwert in der **UnderlyingValue** -Eigenschaft ist der Wert, der für Ihre Transaktion zu sehen ist. Er ist möglicherweise das Ergebnis einer kürzlichen Aktualisierung durch eine andere Transaktion. Dieser Wert kann sich von der [OriginalValue](originalvalue-property-ado.md)-Eigenschaft unterscheiden, die den ursprünglich an das [Recordset](recordset-object-ado.md)-Objekt zurückgegebenen Wert wiedergibt.</span><span class="sxs-lookup"><span data-stu-id="462d6-p101">Use the **UnderlyingValue** property to return the current field value from the database. The field value in the **UnderlyingValue** property is the value that is visible to your transaction and may be the result of a recent update by another transaction. This may differ from the [OriginalValue](originalvalue-property-ado.md) property, which reflects the value that was originally returned to the [Recordset](recordset-object-ado.md).</span></span>

<span data-ttu-id="462d6-p102">Dieses Verhalten ähnelt der [Resync](resync-method-ado.md)-Methode. Jedoch gibt die **UnderlyingValue** -Eigenschaft nur den Wert für ein bestimmtes Feld aus dem aktuellen Datensatz zurück. Dabei handelt es sich um denselben Wert, der bei der [Resync](resync-method-ado.md)-Methode zum Ersetzen der [Value](value-property-ado.md)-Eigenschaft verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="462d6-p102">This is similar to using the [Resync](resync-method-ado.md) method, but the **UnderlyingValue** property returns only the value for a specific field from the current record. This is the same value that the [Resync](resync-method-ado.md) method uses to replace the [Value](value-property-ado.md) property.</span></span>

<span data-ttu-id="462d6-120">Wenn Sie diese Eigenschaft in Verbindung mit der **UnderlyingValue** -Eigenschaft verwenden, können Sie Konflikte lösen, die durch Batchaktualisierungen auftreten.</span><span class="sxs-lookup"><span data-stu-id="462d6-120">When you use this property with the **OriginalValue** property, you can resolve conflicts that arise from batch updates.</span></span>

## <a name="record"></a><span data-ttu-id="462d6-121">Record</span><span class="sxs-lookup"><span data-stu-id="462d6-121">Record</span></span>

<span data-ttu-id="462d6-122">Bei [Record](record-object-ado.md)-Objekten ist diese Eigenschaft für Felder leer, die vor dem Aufruf der [Update](update-method-ado.md)-Methode hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="462d6-122">For [Record](record-object-ado.md) objects, this property will be empty for fields added before [Update](update-method-ado.md) is called.</span></span>

