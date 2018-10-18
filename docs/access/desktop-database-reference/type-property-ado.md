---
<span data-ttu-id="aba6c-101"><<<<<<< HEAD-Titel: Type-Eigenschaft (ADO) TOCTitle: Type-Eigenschaft (ADO) === Titel: Type-Eigenschaft (ADO) TOCTitle: Type-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="aba6c-101"><<<<<<< HEAD title: Type Property (ADO) TOCTitle: Type Property (ADO) ======= title: Type property (ADO) TOCTitle: Type property (ADO)</span></span>
>>>>>>> <span data-ttu-id="aba6c-102">Master Ms:assetid: 14d99172-2145-05ae-620b-459ba097f05c Ms:mtpsurl: https://msdn.microsoft.com/library/JJ248914(v=office.15) Ms:contentKeyID: 48543397 ms.date: 09/18/2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="aba6c-102">master ms:assetid: 14d99172-2145-05ae-620b-459ba097f05c ms:mtpsurl: https://msdn.microsoft.com/library/JJ248914(v=office.15) ms:contentKeyID: 48543397 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="aba6c-103"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="aba6c-103"><<<<<<< HEAD</span></span>
# <a name="type-property-ado"></a><span data-ttu-id="aba6c-104">Type-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="aba6c-104">Type Property (ADO)</span></span>
=======
# <a name="type-property-ado"></a><span data-ttu-id="aba6c-105">Type-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="aba6c-105">Type property (ADO)</span></span>
>>>>>>> <span data-ttu-id="aba6c-106">master</span><span class="sxs-lookup"><span data-stu-id="aba6c-106">master</span></span>


<span data-ttu-id="aba6c-107">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="aba6c-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="aba6c-108">Gibt den Funktions- oder Datentyp eines [Parameter](parameter-object-ado.md)-, [Field](field-object-ado.md)- oder [Property](property-object-ado.md)-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="aba6c-108">Indicates the operational type or data type of a [Parameter](parameter-object-ado.md), [Field](field-object-ado.md), or [Property](property-object-ado.md) object.</span></span>

<span data-ttu-id="aba6c-109"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="aba6c-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="aba6c-110">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="aba6c-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="aba6c-111">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="aba6c-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="aba6c-112">master</span><span class="sxs-lookup"><span data-stu-id="aba6c-112">master</span></span>

<span data-ttu-id="aba6c-113">Legt einen [DataTypeEnum](datatypeenum.md)-Wert fest oder gibt den Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="aba6c-113">Sets or returns a [DataTypeEnum](datatypeenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="aba6c-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="aba6c-114">Remarks</span></span>

<span data-ttu-id="aba6c-p101">Bei **Parameter** -Objekten ist die **Type** -Eigenschaft nicht schreibgeschützt. Bei neuen **Field** -Objekten, die der [Fields](fields-collection-ado.md)-Auflistung eines [Record](record-object-ado.md)-Objekts angefügt wurden, ist **Type** erst schreibgeschützt, nachdem die [Value](value-property-ado.md)-Eigenschaft für das **Field** -Objekt festgelegt wurde und der Datenprovider das neue **Field** -Objekt durch Aufrufen der [Update](update-method-ado.md)-Methode der **Fields** -Auflistung hinzugefügt hat.</span><span class="sxs-lookup"><span data-stu-id="aba6c-p101">For **Parameter** objects, the **Type** property is read/write. For new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Type** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

<span data-ttu-id="aba6c-117">Bei allen anderen Objekten ist die **Type** -Eigenschaft schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="aba6c-117">For all other objects, the **Type** property is read-only.</span></span>

