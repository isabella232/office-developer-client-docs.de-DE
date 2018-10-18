---
<span data-ttu-id="136be-101"><<<<<<< HEAD-Titel: Name-Eigenschaft (ADO) TOCTitle: Name-Eigenschaft (ADO) === Titel: Name-Eigenschaft (ADO) TOCTitle: Name-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="136be-101"><<<<<<< HEAD title: Name Property (ADO) TOCTitle: Name Property (ADO) ======= title: Name property (ADO) TOCTitle: Name property (ADO)</span></span>
>>>>>>> <span data-ttu-id="136be-102">Master Ms:assetid: 4b19bd08-ac3c-86f0-471d-06a37a0d4f89 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249234(v=office.15) Ms:contentKeyID: 48544683 ms.date: 09/18/2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="136be-102">master ms:assetid: 4b19bd08-ac3c-86f0-471d-06a37a0d4f89 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249234(v=office.15) ms:contentKeyID: 48544683 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="136be-103"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="136be-103"><<<<<<< HEAD</span></span>
# <a name="name-property-ado"></a><span data-ttu-id="136be-104">Name-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="136be-104">Name Property (ADO)</span></span>
=======
# <a name="name-property-ado"></a><span data-ttu-id="136be-105">Name-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="136be-105">Name property (ADO)</span></span>
>>>>>>> <span data-ttu-id="136be-106">master</span><span class="sxs-lookup"><span data-stu-id="136be-106">master</span></span>


<span data-ttu-id="136be-107">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="136be-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="136be-108">Gibt den Namen eines Objekts an.</span><span class="sxs-lookup"><span data-stu-id="136be-108">Indicates the name of an object.</span></span>

<span data-ttu-id="136be-109"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="136be-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="136be-110">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="136be-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="136be-111">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="136be-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="136be-112">master</span><span class="sxs-lookup"><span data-stu-id="136be-112">master</span></span>

<span data-ttu-id="136be-113">Legt einen **String** -Wert fest, der den Namen eines Objekts oder einer Anwendung angibt, oder gibt den Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="136be-113">Sets or returns a **String** value that indicates the name of an object.</span></span>

## <a name="remarks"></a><span data-ttu-id="136be-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="136be-114">Remarks</span></span>

<span data-ttu-id="136be-115">Verwenden Sie die **Name** -Eigenschaft, um den Namen eines **Command** -, **Property** -, **Field** - oder **Parameter** -Objekts zuzuweisen oder abzurufen.</span><span class="sxs-lookup"><span data-stu-id="136be-115">Use the **Name** property to assign a name to or retrieve the name of a **Command**, **Property**, **Field**, or **Parameter** object.</span></span>

<span data-ttu-id="136be-116">Der Wert ist bei einem **Command** -Objekt nicht schreibgeschützt. Bei einem **Property** -Objekt ist der Wert schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="136be-116">The value is read/write on a **Command** object and read-only on a **Property** object.</span></span>

<span data-ttu-id="136be-p101">Bei einem **Field** -Objekt ist **Name** in der Regel schreibgeschützt. Bei neuen **Field** -Objekten, die der [Fields](fields-collection-ado.md)-Auflistung eines [Record](record-object-ado.md)-Objekts angefügt wurden, ist **Name** erst schreibgeschützt, nachdem die [Value](value-property-ado.md)-Eigenschaft für das **Field** -Objekt festgelegt wurde und der Datenprovider das neue **Field** -Objekt durch Aufrufen der [Update](update-method-ado.md)-Methode der **Fields** -Auflistung hinzugefügt hat.</span><span class="sxs-lookup"><span data-stu-id="136be-p101">For a **Field** object, **Name** is normally read-only. However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Name** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

<span data-ttu-id="136be-p102">Bei **Parameter** -Objekten, die der [Parameters](parameters-collection-ado.md)-Auflistung noch nicht angefügt wurden, ist die **Name** -Eigenschaft nicht schreibgeschützt. Bei angefügten **Parameter** -Objekten und allen sonstigen Objekten ist die **Name** -Eigenschaft schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="136be-p102">For **Parameter** objects not yet appended to the [Parameters](parameters-collection-ado.md) collection, the **Name** property is read/write. For appended **Parameter** objects and all other objects, the **Name** property is read-only. Names do not have to be unique within a collection.</span></span>

<span data-ttu-id="136be-122">Sie können die **Name** -Eigenschaft eines Objekts ordinal Bezugnahme abrufen, nach denen Sie auf das Objekt direkt nach Namen verweisen können.</span><span class="sxs-lookup"><span data-stu-id="136be-122">You can retrieve the **Name** property of an object by an ordinal reference, after which you can refer to the object directly by name.</span></span> <span data-ttu-id="136be-123">Beispielsweise wenn rstMain.Properties(20). Name ergibt Updatability, Sie können später auf diese Eigenschaft, wenn Updatability liefert verweisen, Sie können später auf diese Eigenschaft als rstMain.Properties("Updatability") verweisen.</span><span class="sxs-lookup"><span data-stu-id="136be-123">For example, if rstMain.Properties(20).Name yields Updatability , you can subsequently refer to this property as yields Updatability , you can subsequently refer to this property as rstMain.Properties("Updatability") .</span></span>

