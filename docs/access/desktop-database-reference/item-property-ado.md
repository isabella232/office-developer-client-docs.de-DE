---
<span data-ttu-id="0e072-101"><<<<<<< HEAD-Titel: Item-Eigenschaft (ADO) TOCTitle: Item-Eigenschaft (ADO) === Titel: Item-Eigenschaft (ADO) TOCTitle: Item-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="0e072-101"><<<<<<< HEAD title: Item Property (ADO) TOCTitle: Item Property (ADO) ======= title: Item property (ADO) TOCTitle: Item property (ADO)</span></span>
>>>>>>> <span data-ttu-id="0e072-102">Master Ms:assetid: 793c305f-0e5b-a529-e21f-b7ab0843ed49 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249499(v=office.15) Ms:contentKeyID: 48545767 ms.date: 09/18/2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="0e072-102">master ms:assetid: 793c305f-0e5b-a529-e21f-b7ab0843ed49 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249499(v=office.15) ms:contentKeyID: 48545767 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="0e072-103"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="0e072-103"><<<<<<< HEAD</span></span>
# <a name="item-property-ado"></a><span data-ttu-id="0e072-104">Item-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="0e072-104">Item Property (ADO)</span></span>
=======
# <a name="item-property-ado"></a><span data-ttu-id="0e072-105">Item-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="0e072-105">Item property (ADO)</span></span>
>>>>>>> <span data-ttu-id="0e072-106">master</span><span class="sxs-lookup"><span data-stu-id="0e072-106">master</span></span>

<span data-ttu-id="0e072-107">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0e072-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0e072-108">Gibt ein bestimmtes Element einer Auflistung nach Name oder Ordnungszahl an.</span><span class="sxs-lookup"><span data-stu-id="0e072-108">Indicates a specific member of a collection, by name or ordinal number.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e072-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e072-109">Syntax</span></span>

<span data-ttu-id="0e072-110">Legen Sie*Objekt* = *Auflistung*. Item (Index)</span><span class="sxs-lookup"><span data-stu-id="0e072-110">Set*object* = *collection*.Item ( Index )</span></span>

<span data-ttu-id="0e072-111"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="0e072-111"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="0e072-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0e072-112">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="0e072-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0e072-113">Return value</span></span>
>>>>>>> <span data-ttu-id="0e072-114">master</span><span class="sxs-lookup"><span data-stu-id="0e072-114">master</span></span>

<span data-ttu-id="0e072-115">Gibt einen Objektverweis zurück.</span><span class="sxs-lookup"><span data-stu-id="0e072-115">Returns an object reference.</span></span>

## <a name="parameters"></a><span data-ttu-id="0e072-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e072-116">Parameters</span></span>

- <span data-ttu-id="0e072-117">*Index*</span><span class="sxs-lookup"><span data-stu-id="0e072-117">*Index*</span></span>

- <span data-ttu-id="0e072-118">Ein **Variant** -Ausdruck, der als Name oder Ordnungszahl eines Objekts in einer Auflistung ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="0e072-118">A **Variant** expression that evaluates either to the name or to the ordinal number of an object in a collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e072-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0e072-119">Remarks</span></span>

<span data-ttu-id="0e072-120">Verwenden Sie die **Item** -Eigenschaft, um ein bestimmtes Objekt in einer Auflistung zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="0e072-120">Use the **Item** property to return a specific object in a collection.</span></span> <span data-ttu-id="0e072-121">Wenn das **Element** ein Objekt in der Auflistung entspricht dem *Index* -Argument nicht finden kann, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="0e072-121">If **Item** cannot find an object in the collection corresponding to the *Index* argument, an error occurs.</span></span> <span data-ttu-id="0e072-122">Darüber hinaus unterstützen einige Sammlungen nicht benannte Objekte; für diese Auflistungen müssen Sie die Ordnungszahl Verweise verwenden.</span><span class="sxs-lookup"><span data-stu-id="0e072-122">Also, some collections don't support named objects; for these collections, you must use ordinal number references.</span></span>

<span data-ttu-id="0e072-123">Die **Item** -Eigenschaft ist die Standardeigenschaft für alle Auflistungen. Die folgenden Syntaxformen sind deshalb austauschbar:</span><span class="sxs-lookup"><span data-stu-id="0e072-123">The **Item** property is the default property for all collections; therefore, the following syntax forms are interchangeable:</span></span>

```vb
    collection.Item (Index)
    collection (Index)
```
