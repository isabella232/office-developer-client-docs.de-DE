---
<span data-ttu-id="8e07b-101"><<<<<<< HEAD-Titel: NumericScale-Eigenschaft (ADO) TOCTitle: NumericScale-Eigenschaft (ADO) === Titel: NumericScale-Eigenschaft (ADO) TOCTitle: NumericScale-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="8e07b-101"><<<<<<< HEAD title: NumericScale Property (ADO) TOCTitle: NumericScale Property (ADO) ======= title: NumericScale property (ADO) TOCTitle: NumericScale property (ADO)</span></span>
>>>>>>> <span data-ttu-id="8e07b-102">Master Ms:assetid: 51b232d2-5bfd-521c-f4e9-65655ecc7c70 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249263(v=office.15) Ms:contentKeyID: 48544824 ms.date: 09/18/2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="8e07b-102">master ms:assetid: 51b232d2-5bfd-521c-f4e9-65655ecc7c70 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249263(v=office.15) ms:contentKeyID: 48544824 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="8e07b-103"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="8e07b-103"><<<<<<< HEAD</span></span>
# <a name="numericscale-property-ado"></a><span data-ttu-id="8e07b-104">NumericScale-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="8e07b-104">NumericScale Property (ADO)</span></span>
=======
# <a name="numericscale-property-ado"></a><span data-ttu-id="8e07b-105">NumericScale-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="8e07b-105">NumericScale property (ADO)</span></span>
>>>>>>> <span data-ttu-id="8e07b-106">master</span><span class="sxs-lookup"><span data-stu-id="8e07b-106">master</span></span>


<span data-ttu-id="8e07b-107">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8e07b-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8e07b-108">Gibt die Dezimalstellen numerischer Werte in einem [Parameter](parameter-object-ado.md)- oder [Field](field-object-ado.md)-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="8e07b-108">Indicates the scale of numeric values in a [Parameter](parameter-object-ado.md) or [Field](field-object-ado.md) object.</span></span>

<span data-ttu-id="8e07b-109"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="8e07b-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="8e07b-110">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8e07b-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="8e07b-111">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8e07b-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="8e07b-112">master</span><span class="sxs-lookup"><span data-stu-id="8e07b-112">master</span></span>

<span data-ttu-id="8e07b-113">Legt einen **Byte** -Wert fest, der die Anzahl von Dezimalstellen angibt, in die numerische Werte aufgelöst werden, oder gibt den Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="8e07b-113">Sets or returns a **Byte** value that indicates the number of decimal places to which numeric values will be resolved.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e07b-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8e07b-114">Remarks</span></span>

<span data-ttu-id="8e07b-115">Bestimmen Sie mit der **NumericScale** -Eigenschaft die Anzahl von Stellen rechts vom Dezimalkomma, die zur Darstellung von Werten für ein numerisches **Parameter** - oder **Field** -Objekt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8e07b-115">Use the **NumericScale** property to determine how many digits to the right of the decimal point will be used to represent values for a numeric **Parameter** or **Field** object.</span></span>

<span data-ttu-id="8e07b-116">Bei **Parameter** -Objekten ist die **NumericScale** -Eigenschaft nicht schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="8e07b-116">For **Parameter** objects, the **NumericScale** property is read/write.</span></span>

<span data-ttu-id="8e07b-p101">Bei einem **Field** -Objekt ist **NumericScale** in der Regel schreibgeschützt. Bei neuen **Field** -Objekten, die der [Fields](fields-collection-ado.md)-Auflistung eines [Record](record-object-ado.md)-Objekts angefügt wurden, ist **NumericScale** erst schreibgeschützt, nachdem die [Value](value-property-ado.md)-Eigenschaft für das **Field** -Objekt festgelegt wurde und der Datenprovider das neue **Field** -Objekt durch Aufrufen der [Update](update-method-ado.md)-Methode der **Fields** -Auflistung hinzugefügt hat.</span><span class="sxs-lookup"><span data-stu-id="8e07b-p101">For a **Field** object, **NumericScale** is normally read-only. However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **NumericScale** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

