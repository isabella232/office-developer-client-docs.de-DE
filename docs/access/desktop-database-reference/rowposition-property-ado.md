---
<span data-ttu-id="77c03-101"><<<<<<< HEAD-Titel: RowPosition-Eigenschaft (ADO) TOCTitle: RowPosition-Eigenschaft (ADO) === Titel: RowPosition-Eigenschaft (ADO) TOCTitle: RowPosition-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="77c03-101"><<<<<<< HEAD title: RowPosition Property (ADO) TOCTitle: RowPosition Property (ADO) ======= title: RowPosition property (ADO) TOCTitle: RowPosition property (ADO)</span></span>
>>>>>>> <span data-ttu-id="77c03-102">Master Ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15) Ms:contentKeyID: 48547325 ms.date: 09/18/2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="77c03-102">master ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15) ms:contentKeyID: 48547325 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="77c03-103"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="77c03-103"><<<<<<< HEAD</span></span>
# <a name="rowposition-property-ado"></a><span data-ttu-id="77c03-104">RowPosition-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="77c03-104">RowPosition Property (ADO)</span></span>
=======
# <a name="rowposition-property-ado"></a><span data-ttu-id="77c03-105">RowPosition-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="77c03-105">RowPosition property (ADO)</span></span>
>>>>>>> <span data-ttu-id="77c03-106">master</span><span class="sxs-lookup"><span data-stu-id="77c03-106">master</span></span>


<span data-ttu-id="77c03-107">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="77c03-107">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="77c03-108">Ruft ein OLE DB- **RowPosition** -Objekt aus einem **ADORecordsetConstruction** -Objekt ab oder legt es dafür fest.</span><span class="sxs-lookup"><span data-stu-id="77c03-108">Gets or sets an OLE DB **RowPosition** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="77c03-109">Bei Verwendung **platzieren\_RowPosition** zur **RowPosition** -Objekt das resultierende **Recordset** -Objekt verwendet das **RowPosition** -Objekt zum Bestimmen der aktuellen Zeile.</span><span class="sxs-lookup"><span data-stu-id="77c03-109">When you use **put\_RowPosition** to set the **RowPosition** object, the resulting **Recordset** object uses the **RowPosition** object to determine the current row.</span></span>

<span data-ttu-id="77c03-110">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="77c03-110">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="77c03-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="77c03-111">Syntax</span></span>

<span data-ttu-id="77c03-112">HRESULT Get\_RowPosition (\[out Retval\] IUnknown\* \* PpRowPos);</span><span class="sxs-lookup"><span data-stu-id="77c03-112">HRESULT get\_RowPosition(\[out, retval\] IUnknown\*\* ppRowPos);</span></span>

<span data-ttu-id="77c03-113">Platzieren Sie HRESULT\_RowPosition (\[in\] IUnknown\* pRowPos);</span><span class="sxs-lookup"><span data-stu-id="77c03-113">HRESULT put\_RowPosition(\[in\] IUnknown\* pRowPos);</span></span>

## <a name="parameters"></a><span data-ttu-id="77c03-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="77c03-114">Parameters</span></span>

  - <span data-ttu-id="77c03-115">*ppRowPos*</span><span class="sxs-lookup"><span data-stu-id="77c03-115">*ppRowPos*</span></span>

  - <span data-ttu-id="77c03-116">Zeiger auf ein OLE DB- **RowPosition** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="77c03-116">Pointer to an OLE DB **RowPosition** object.</span></span>

  - <span data-ttu-id="77c03-117">*PRowPos*</span><span class="sxs-lookup"><span data-stu-id="77c03-117">*PRowPos*</span></span>

  - <span data-ttu-id="77c03-118">Ein OLE DB- **RowPosition** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="77c03-118">An OLE DB **RowPosition** object.</span></span>

<span data-ttu-id="77c03-119"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="77c03-119"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="77c03-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="77c03-120">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="77c03-121">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="77c03-121">Return values</span></span>
>>>>>>> <span data-ttu-id="77c03-122">master</span><span class="sxs-lookup"><span data-stu-id="77c03-122">master</span></span>

<span data-ttu-id="77c03-123">Diese Eigenschaftsmethode gibt die HRESULT-Standardwerte, einschließlich S\_OK und E\_fehl.</span><span class="sxs-lookup"><span data-stu-id="77c03-123">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="77c03-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="77c03-124">Remarks</span></span>

<span data-ttu-id="77c03-p102">Wenn diese Eigenschaft festgelegt ist und sich das **Rowset** -Objekt für das **RowPosition** -Objekt vom **Rowset** -Objekt für das **Recordset** -Objekt unterscheidet, wird letzteres überschrieben. Dasselbe Verhalten gilt auch für das aktuelle **Chapter** -Objekt des **RowPosition** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="77c03-p102">When this property is set, if the **Rowset** object on the **RowPosition** object is different from the **Rowset** object on the **Recordset** object, the former overrides the latter. The same behavior applies to the current **Chapter** of the **RowPosition** as well.</span></span>

## <a name="applies-to"></a><span data-ttu-id="77c03-127">Betrifft</span><span class="sxs-lookup"><span data-stu-id="77c03-127">Applies To</span></span>

[<span data-ttu-id="77c03-128">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="77c03-128">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

