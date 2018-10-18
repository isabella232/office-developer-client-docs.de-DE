---
<span data-ttu-id="4eb5f-101"><<<<<<< HEAD-Titel: Kapitel-Eigenschaft (ADO) TOCTitle: Kapitel-Eigenschaft (ADO) === Titel: Chapter-Eigenschaft (ADO) TOCTitle: Chapter-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="4eb5f-101"><<<<<<< HEAD title: Chapter Property (ADO) TOCTitle: Chapter Property (ADO) ======= title: Chapter property (ADO) TOCTitle: Chapter property (ADO)</span></span>
>>>>>>> <span data-ttu-id="4eb5f-102">Master Ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e Ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15) Ms:contentKeyID: 48548014 ms.date: 09/18/2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="4eb5f-102">master ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15) ms:contentKeyID: 48548014 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="4eb5f-103"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="4eb5f-103"><<<<<<< HEAD</span></span>
# <a name="chapter-property-ado"></a><span data-ttu-id="4eb5f-104">Chapter-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="4eb5f-104">Chapter Property (ADO)</span></span>
=======
# <a name="chapter-property-ado"></a><span data-ttu-id="4eb5f-105">Chapter-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="4eb5f-105">Chapter property (ADO)</span></span>
>>>>>>> <span data-ttu-id="4eb5f-106">master</span><span class="sxs-lookup"><span data-stu-id="4eb5f-106">master</span></span>


<span data-ttu-id="4eb5f-107">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="4eb5f-107">**Applies to**: Access 2013 | Office 2013</span></span>
 

<span data-ttu-id="4eb5f-108">Ein **Chapter**-OLE DB-Objekt wird aus einem **ADORecordsetConstruction**-Objekt abgerufen oder für dieses festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4eb5f-108">Gets or sets an OLE DB **Chapter** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="4eb5f-109">Bei Verwendung **platzieren\_Kapitel** , um das **Kapitel** -Objekt festzulegen, eine Teilmenge von Zeilen in ein ADO- **Recordset** -Objekt aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="4eb5f-109">When you use **put\_Chapter** to set the **Chapter** object, a subset of rows is turned into an ADO **Recordset** object.</span></span> <span data-ttu-id="4eb5f-110">Hierdurch wird das aktuelle Kapitel des **Rowset** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="4eb5f-110">This sets the current chapter of the **Rowset** object.</span></span> <span data-ttu-id="4eb5f-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="4eb5f-111">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4eb5f-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="4eb5f-112">Syntax</span></span>

<span data-ttu-id="4eb5f-113">HRESULT Get\_Kapitel (\[out Retval\] lang\* PlChapter);</span><span class="sxs-lookup"><span data-stu-id="4eb5f-113">HRESULT get\_Chapter(\[out, retval\] long\* plChapter);</span></span>

<span data-ttu-id="4eb5f-114">Platzieren Sie HRESULT\_Kapitel (\[in\] lang lChapter);</span><span class="sxs-lookup"><span data-stu-id="4eb5f-114">HRESULT put\_Chapter(\[in\] long lChapter);</span></span>

## <a name="parameters"></a><span data-ttu-id="4eb5f-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="4eb5f-115">Parameters</span></span>

  - <span data-ttu-id="4eb5f-116">*plChapter*</span><span class="sxs-lookup"><span data-stu-id="4eb5f-116">*plChapter*</span></span>

  - <span data-ttu-id="4eb5f-117">Zeiger auf das Handle eines Kapitels.</span><span class="sxs-lookup"><span data-stu-id="4eb5f-117">Pointer to the handle of a chapter.</span></span>

  - <span data-ttu-id="4eb5f-118">*LChapter*</span><span class="sxs-lookup"><span data-stu-id="4eb5f-118">*LChapter*</span></span>

  - <span data-ttu-id="4eb5f-119">Handle eines Kapitels.</span><span class="sxs-lookup"><span data-stu-id="4eb5f-119">Handle of a chapter.</span></span>

<span data-ttu-id="4eb5f-120"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="4eb5f-120"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="4eb5f-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4eb5f-121">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="4eb5f-122">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="4eb5f-122">Return values</span></span>
>>>>>>> <span data-ttu-id="4eb5f-123">master</span><span class="sxs-lookup"><span data-stu-id="4eb5f-123">master</span></span>

<span data-ttu-id="4eb5f-124">Diese Eigenschaftsmethode gibt die HRESULT-Standardwerte, einschließlich S\_OK und E\_fehl.</span><span class="sxs-lookup"><span data-stu-id="4eb5f-124">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="4eb5f-125">Betrifft</span><span class="sxs-lookup"><span data-stu-id="4eb5f-125">Applies To</span></span>

[<span data-ttu-id="4eb5f-126">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="4eb5f-126">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

