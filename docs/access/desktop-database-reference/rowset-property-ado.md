---
<span data-ttu-id="8cba4-101"><<<<<<< HEAD-Titel: Rowset-Eigenschaft (ADO) TOCTitle: Rowset-Eigenschaft (ADO) === Titel: Rowset-Eigenschaft (ADO) TOCTitle: Rowset-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="8cba4-101"><<<<<<< HEAD title: Rowset Property (ADO) TOCTitle: Rowset Property (ADO) ======= title: Rowset property (ADO) TOCTitle: Rowset property (ADO)</span></span>
>>>>>>> <span data-ttu-id="8cba4-102">Master Ms:assetid: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15) Ms:contentKeyID: 48543515 ms.date: 09/18/2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="8cba4-102">master ms:assetid: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15) ms:contentKeyID: 48543515 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="8cba4-103"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="8cba4-103"><<<<<<< HEAD</span></span>
# <a name="rowset-property-ado"></a><span data-ttu-id="8cba4-104">Rowset-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="8cba4-104">Rowset Property (ADO)</span></span>
=======
# <a name="rowset-property-ado"></a><span data-ttu-id="8cba4-105">Rowset-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="8cba4-105">Rowset property (ADO)</span></span>
>>>>>>> <span data-ttu-id="8cba4-106">master</span><span class="sxs-lookup"><span data-stu-id="8cba4-106">master</span></span>


<span data-ttu-id="8cba4-107">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8cba4-107">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="8cba4-108">Ein **Rowset**-OLE DB-Objekt wird aus einem **ADORecordsetConstruction**-Objekt abgerufen oder für dieses festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8cba4-108">Gets or sets an OLE DB **Rowset** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="8cba4-109">Bei Verwendung der Put\_Rowset, das Rowset in ein ADO- **Recordset** -Objekt aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="8cba4-109">When you use put\_Rowset, the rowset is turned into an ADO **Recordset** object.</span></span>

<span data-ttu-id="8cba4-110">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="8cba4-110">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cba4-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="8cba4-111">Syntax</span></span>

<span data-ttu-id="8cba4-112">HRESULT Get\_Rowset (\[out Retval\] IUnknown\* \* PpRowset);</span><span class="sxs-lookup"><span data-stu-id="8cba4-112">HRESULT get\_Rowset(\[out, retval\] IUnknown\*\* ppRowset);</span></span>

<span data-ttu-id="8cba4-113">Platzieren Sie HRESULT\_Rowset (\[in\] IUnknown\* pRowset);</span><span class="sxs-lookup"><span data-stu-id="8cba4-113">HRESULT put\_Rowset(\[in\] IUnknown\* pRowset);</span></span>

## <a name="parameters"></a><span data-ttu-id="8cba4-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cba4-114">Parameters</span></span>

  - <span data-ttu-id="8cba4-115">*ppRowset*</span><span class="sxs-lookup"><span data-stu-id="8cba4-115">*ppRowset*</span></span>

  - <span data-ttu-id="8cba4-116">Zeiger auf ein OLE DB- **Rowset** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="8cba4-116">Pointer to an OLE DB **Rowset** object.</span></span>

  - <span data-ttu-id="8cba4-117">*PRowset*</span><span class="sxs-lookup"><span data-stu-id="8cba4-117">*PRowset*</span></span>

  - <span data-ttu-id="8cba4-118">Ein OLE DB- **Rowset** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="8cba4-118">An OLE DB **Rowset** object.</span></span>

<span data-ttu-id="8cba4-119"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="8cba4-119"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="8cba4-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8cba4-120">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="8cba4-121">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8cba4-121">Return values</span></span>
>>>>>>> <span data-ttu-id="8cba4-122">master</span><span class="sxs-lookup"><span data-stu-id="8cba4-122">master</span></span>

<span data-ttu-id="8cba4-123">Diese Eigenschaftsmethode gibt die HRESULT-Standardwerte, einschließlich S\_OK und E\_fehl.</span><span class="sxs-lookup"><span data-stu-id="8cba4-123">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="8cba4-124">Betrifft</span><span class="sxs-lookup"><span data-stu-id="8cba4-124">Applies To</span></span>

[<span data-ttu-id="8cba4-125">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="8cba4-125">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

