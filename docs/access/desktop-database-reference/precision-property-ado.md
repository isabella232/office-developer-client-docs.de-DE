---
<span data-ttu-id="cf268-101"><<<<<<< HEAD-Titel: Precision-Eigenschaft (ADO) TOCTitle: Precision-Eigenschaft (ADO) === Titel: Precision-Eigenschaft (ADO) TOCTitle: Precision-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="cf268-101"><<<<<<< HEAD title: Precision Property (ADO) TOCTitle: Precision Property (ADO) ======= title: Precision property (ADO) TOCTitle: Precision property (ADO)</span></span>
>>>>>>> <span data-ttu-id="cf268-102">Master Ms:assetid: c9d54d78-d5a5-caf8-d635-259d1fcc0595 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249983(v=office.15) Ms:contentKeyID: 48547685 ms.date: 09/18/2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="cf268-102">master ms:assetid: c9d54d78-d5a5-caf8-d635-259d1fcc0595 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249983(v=office.15) ms:contentKeyID: 48547685 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="cf268-103"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="cf268-103"><<<<<<< HEAD</span></span>
# <a name="precision-property-ado"></a><span data-ttu-id="cf268-104">Precision-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="cf268-104">Precision Property (ADO)</span></span>
=======
# <a name="precision-property-ado"></a><span data-ttu-id="cf268-105">Precision-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="cf268-105">Precision property (ADO)</span></span>
>>>>>>> <span data-ttu-id="cf268-106">master</span><span class="sxs-lookup"><span data-stu-id="cf268-106">master</span></span>


<span data-ttu-id="cf268-107">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="cf268-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="cf268-108">Gibt den Genauigkeitsgrad für numerische Werte in einem [Parameter](parameter-object-ado.md)-Objekt oder für numerische [Field](field-object-ado.md)-Objekte an.</span><span class="sxs-lookup"><span data-stu-id="cf268-108">Indicates the degree of precision for numeric values in a [Parameter](parameter-object-ado.md) object or for numeric [Field](field-object-ado.md) objects.</span></span>

<span data-ttu-id="cf268-109"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="cf268-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="cf268-110">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="cf268-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="cf268-111">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="cf268-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="cf268-112">master</span><span class="sxs-lookup"><span data-stu-id="cf268-112">master</span></span>

<span data-ttu-id="cf268-113">Legt einen **Byte** -Wert fest oder gibt den Wert zurück, der die maximale Anzahl von Stellen angibt, die zum Darstellen eines Werts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cf268-113">Sets or returns a **Byte** value that indicates the maximum number of digits used to represent values.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf268-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cf268-114">Remarks</span></span>

<span data-ttu-id="cf268-115">Bestimmen Sie mit der **Precision** -Eigenschaft die maximale Anzahl von Stellen, die zum Darstellen von Werten für ein numerisches **Parameter** - oder **Field** -Objekt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cf268-115">Use the **Precision** property to determine the maximum number of digits used to represent values for a numeric **Parameter** or **Field** object.</span></span>

<span data-ttu-id="cf268-116">Der Wert ist bei einem **Parameter** -Objekt nicht schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="cf268-116">The value is read/write on a **Parameter** object.</span></span>

<span data-ttu-id="cf268-p101">Bei einem **Field** -Objekt ist **Precision** in der Regel schreibgeschützt. Bei neuen **Field** -Objekten, die der [Fields](fields-collection-ado.md)-Auflistung eines [Record](record-object-ado.md)-Objekts angefügt wurden, ist **Precision** erst schreibgeschützt, nachdem die [Value](value-property-ado.md)-Eigenschaft für das **Field** -Objekt festgelegt wurde und der Datenprovider das neue **Field** -Objekt durch Aufrufen der [Update](update-method-ado.md)-Methode der **Fields** -Auflistung hinzugefügt hat.</span><span class="sxs-lookup"><span data-stu-id="cf268-p101">For a **Field** object, **Precision** is normally read-only. However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Precision** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

