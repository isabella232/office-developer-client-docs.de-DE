---
<span data-ttu-id="2458f-101">Titel: Row-Eigenschaft - ActiveX Data Objects (ADO) <<<<<<< HEAD TOCTitle: Zeile-Eigenschaft (ADO) === TOCTitle: Zeile-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="2458f-101">title: Row Property - ActiveX Data Objects (ADO) <<<<<<< HEAD TOCTitle: Row Property (ADO) ======= TOCTitle: Row property (ADO)</span></span>
>>>>>>> <span data-ttu-id="2458f-102">Master Ms:assetid: 1c2b0e27-7232-4b1c-826c-9dc15d758851 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15) Ms:contentKeyID: 48543562 ms.date: 09/18/2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="2458f-102">master ms:assetid: 1c2b0e27-7232-4b1c-826c-9dc15d758851 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15) ms:contentKeyID: 48543562 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="2458f-103"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="2458f-103"><<<<<<< HEAD</span></span>
# <a name="row-property-ado"></a><span data-ttu-id="2458f-104">Row-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="2458f-104">Row Property (ADO)</span></span>
=======
# <a name="row-property-ado"></a><span data-ttu-id="2458f-105">Row-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="2458f-105">Row property (ADO)</span></span>
>>>>>>> <span data-ttu-id="2458f-106">master</span><span class="sxs-lookup"><span data-stu-id="2458f-106">master</span></span>


<span data-ttu-id="2458f-107">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2458f-107">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="2458f-108">Ruft ein **Row** -Objekt von OLE DB aus einem **ADORecordConstruction** -Objekt ab oder legt es dafür fest.</span><span class="sxs-lookup"><span data-stu-id="2458f-108">Gets or sets an OLE DB **Row** object from/on an **ADORecordConstruction** object.</span></span> <span data-ttu-id="2458f-109">Bei Verwendung **platzieren\_Zeile** um ein **Row** -Objekt festgelegt, wird eine Zeile in ein ADO- **Record** -Objekt umgewandelt.</span><span class="sxs-lookup"><span data-stu-id="2458f-109">When you use **put\_Row** to set a **Row** object, a row is turned into an ADO **Record** object.</span></span> <span data-ttu-id="2458f-110">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="2458f-110">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2458f-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="2458f-111">Syntax</span></span>

<span data-ttu-id="2458f-112">HRESULT Get\_Zeile (\[out Retval\] IUnknown\* \* PpRow);</span><span class="sxs-lookup"><span data-stu-id="2458f-112">HRESULT get\_Row(\[out, retval\] IUnknown\*\* ppRow);</span></span>

<span data-ttu-id="2458f-113">Platzieren Sie HRESULT\_Zeile (\[in\] IUnknown\* pRow);</span><span class="sxs-lookup"><span data-stu-id="2458f-113">HRESULT put\_Row(\[in\] IUnknown\* pRow);</span></span>

## <a name="parameters"></a><span data-ttu-id="2458f-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="2458f-114">Parameters</span></span>

  - <span data-ttu-id="2458f-115">*ppRow*</span><span class="sxs-lookup"><span data-stu-id="2458f-115">*ppRow*</span></span>

  - <span data-ttu-id="2458f-116">Zeiger auf ein OLE DB- **Row** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="2458f-116">Pointer to an OLE DB **Row** object.</span></span>

  - <span data-ttu-id="2458f-117">*PRow*</span><span class="sxs-lookup"><span data-stu-id="2458f-117">*PRow*</span></span>

  - <span data-ttu-id="2458f-118">Ein OLE DB- **Row** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="2458f-118">An OLE DB **Row** object.</span></span>

<span data-ttu-id="2458f-119"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="2458f-119"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="2458f-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2458f-120">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="2458f-121">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="2458f-121">Return values</span></span>
>>>>>>> <span data-ttu-id="2458f-122">master</span><span class="sxs-lookup"><span data-stu-id="2458f-122">master</span></span>

<span data-ttu-id="2458f-123">Diese Eigenschaftsmethode gibt die HRESULT-Standardwerte, einschließlich S\_OK und E\_fehl.</span><span class="sxs-lookup"><span data-stu-id="2458f-123">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="2458f-124">Betrifft</span><span class="sxs-lookup"><span data-stu-id="2458f-124">Applies To</span></span>

[<span data-ttu-id="2458f-125">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="2458f-125">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)

