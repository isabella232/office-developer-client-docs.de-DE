---
title: ITableDataHrQueryRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrQueryRow
api_type:
- COM
ms.assetid: 66ce8f36-2b2b-4a8e-b9b2-43782d8357a1
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: da41fadc9a71a410dd115e28ce2cf9c81442b104
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434767"
---
# <a name="itabledatahrqueryrow"></a><span data-ttu-id="d768c-103">ITableData::HrQueryRow</span><span class="sxs-lookup"><span data-stu-id="d768c-103">ITableData::HrQueryRow</span></span>

  
  
<span data-ttu-id="d768c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d768c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d768c-105">Ruft eine Tabellenzeile ab.</span><span class="sxs-lookup"><span data-stu-id="d768c-105">Retrieves a table row.</span></span>
  
```cpp
HRESULT HrQueryRow(
  LPSPropValue lpSPropValue,
  LPSRow FAR * lppSRow,
  ULONG FAR * lpuliRow
);
```

## <a name="parameters"></a><span data-ttu-id="d768c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d768c-106">Parameters</span></span>

 <span data-ttu-id="d768c-107">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="d768c-107">_lpSPropValue_</span></span>
  
> <span data-ttu-id="d768c-108">in Ein Zeiger auf eine Eigenschaftswert Struktur, die die Indexspalte für die abgerufene Zeile beschreibt.</span><span class="sxs-lookup"><span data-stu-id="d768c-108">[in] A pointer to a property value structure that describes the index column for the row to be retrieved.</span></span> <span data-ttu-id="d768c-109">Das **ulPropTag** -Element der Eigenschaftswert Struktur sollte das gleiche Property-Tag wie der _ulPropTagIndexColumn_ -Parameter aus dem Aufruf der [createable](createtable.md) -Funktion enthalten, die auf die [ITableData](itabledataiunknown.md) -Implementierung zugreift.</span><span class="sxs-lookup"><span data-stu-id="d768c-109">The **ulPropTag** member of the property value structure should contain the same property tag as the  _ulPropTagIndexColumn_ parameter from the call to the [CreateTable](createtable.md) function, which accesses the [ITableData](itabledataiunknown.md) implementation.</span></span> 
    
 <span data-ttu-id="d768c-110">_lppSRow_</span><span class="sxs-lookup"><span data-stu-id="d768c-110">_lppSRow_</span></span>
  
> <span data-ttu-id="d768c-111">Out Ein Zeiger auf einen Zeiger auf die abgerufene Zeile.</span><span class="sxs-lookup"><span data-stu-id="d768c-111">[out] A pointer to a pointer to the retrieved row.</span></span> 
    
 <span data-ttu-id="d768c-112">_lpuliRow_</span><span class="sxs-lookup"><span data-stu-id="d768c-112">_lpuliRow_</span></span>
  
> <span data-ttu-id="d768c-113">[in, out] Bei der Eingabe ein gültiger Zeiger oder NULL, der angibt, dass keine Informationen zurückgegeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="d768c-113">[in, out] On input, a valid pointer or NULL, which indicates that no information needs to be returned.</span></span> <span data-ttu-id="d768c-114">Bei der Ausgabe ein gültiger Zeiger, der auf die Zeilennummer der Zeile verweist, eine fortlaufende Nummer, die die Position der Zeile in der Tabelle identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d768c-114">On output, a valid pointer that points to the row's row number, a sequential number that identifies the row's position in the table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d768c-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d768c-115">Return value</span></span>

<span data-ttu-id="d768c-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="d768c-116">S_OK</span></span> 
  
> <span data-ttu-id="d768c-117">Die Zeile wurde erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="d768c-117">The row was successfully retrieved.</span></span>
    
<span data-ttu-id="d768c-118">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d768c-118">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="d768c-119">Die [SPropValue](spropvalue.md) -Struktur, auf die _lpSPropValue_ verweist, enthält nicht die Index Column-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="d768c-119">The [SPropValue](spropvalue.md) structure that  _lpSPropValue_ points to does not contain the index column property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d768c-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d768c-120">Remarks</span></span>

<span data-ttu-id="d768c-121">Die **ITableData:: HrQueryRow** -Methode ruft alle Eigenschaften für die Zeile mit einer Indexspalte ab, die mit dem Wert der Indexspalte übereinstimmt, die in der Eigenschaften Struktur enthalten ist, auf die von _lpSPropValue_verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="d768c-121">The **ITableData::HrQueryRow** method retrieves all of the properties for the row that has an index column that matches the value of the index column included in the property structure pointed to by  _lpSPropValue_.</span></span> <span data-ttu-id="d768c-122">**HrQueryRow** gibt auch die Zeilennummer zurück, wenn der Anrufer Sie anfordert, der die Position der Zeile in der Tabelle identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d768c-122">**HrQueryRow** also returns the row number, if the caller requests it, that identifies the row's position in the table.</span></span> 
  
<span data-ttu-id="d768c-123">Da **HrQueryRow** die **SPropValue** -Struktur, auf die durch _lpSPropValue_verwiesen wird, nicht ändert, müssen Aufrufer die Struktur freigeben, wenn **HrQueryRow** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d768c-123">Because **HrQueryRow** does not modify the **SPropValue** structure pointed to by  _lpSPropValue_, callers must free the structure when **HrQueryRow** returns.</span></span> <span data-ttu-id="d768c-124">Aufrufer müssen auch die **SRow** -Struktur freigeben, die die abgerufene Zeile enthält.</span><span class="sxs-lookup"><span data-stu-id="d768c-124">Callers must also free the **SRow** structure that contains the retrieved row.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d768c-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d768c-125">See also</span></span>



[<span data-ttu-id="d768c-126">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="d768c-126">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="d768c-127">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="d768c-127">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="d768c-128">SPropValue</span><span class="sxs-lookup"><span data-stu-id="d768c-128">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="d768c-129">SRow</span><span class="sxs-lookup"><span data-stu-id="d768c-129">SRow</span></span>](srow.md)
  
[<span data-ttu-id="d768c-130">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d768c-130">ITableData : IUnknown</span></span>](itabledataiunknown.md)

