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
# <a name="itabledatahrqueryrow"></a><span data-ttu-id="3de51-103">ITableData::HrQueryRow</span><span class="sxs-lookup"><span data-stu-id="3de51-103">ITableData::HrQueryRow</span></span>

  
  
<span data-ttu-id="3de51-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3de51-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3de51-105">Ruft eine Tabellenzeile ab.</span><span class="sxs-lookup"><span data-stu-id="3de51-105">Retrieves a table row.</span></span>
  
```cpp
HRESULT HrQueryRow(
  LPSPropValue lpSPropValue,
  LPSRow FAR * lppSRow,
  ULONG FAR * lpuliRow
);
```

## <a name="parameters"></a><span data-ttu-id="3de51-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3de51-106">Parameters</span></span>

 <span data-ttu-id="3de51-107">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="3de51-107">_lpSPropValue_</span></span>
  
> <span data-ttu-id="3de51-108">[in] Ein Zeiger auf eine Eigenschaftswertstruktur, die die Indexspalte für die abzurufende Zeile beschreibt.</span><span class="sxs-lookup"><span data-stu-id="3de51-108">[in] A pointer to a property value structure that describes the index column for the row to be retrieved.</span></span> <span data-ttu-id="3de51-109">Das **ulPropTag-Element** der Eigenschaftswertstruktur sollte das gleiche Eigenschaftstag wie der  _ulPropTagIndexColumn-Parameter_ aus dem Aufruf der [CreateTable-Funktion](createtable.md) enthalten, die auf die [ITableData-Implementierung](itabledataiunknown.md) zutritt.</span><span class="sxs-lookup"><span data-stu-id="3de51-109">The **ulPropTag** member of the property value structure should contain the same property tag as the  _ulPropTagIndexColumn_ parameter from the call to the [CreateTable](createtable.md) function, which accesses the [ITableData](itabledataiunknown.md) implementation.</span></span> 
    
 <span data-ttu-id="3de51-110">_lppSRow_</span><span class="sxs-lookup"><span data-stu-id="3de51-110">_lppSRow_</span></span>
  
> <span data-ttu-id="3de51-111">[out] Ein Zeiger auf einen Zeiger auf die abgerufene Zeile.</span><span class="sxs-lookup"><span data-stu-id="3de51-111">[out] A pointer to a pointer to the retrieved row.</span></span> 
    
 <span data-ttu-id="3de51-112">_lpuliRow_</span><span class="sxs-lookup"><span data-stu-id="3de51-112">_lpuliRow_</span></span>
  
> <span data-ttu-id="3de51-113">[in, out] Bei der Eingabe ein gültiger Zeiger oder NULL, der angibt, dass keine Informationen zurückgegeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="3de51-113">[in, out] On input, a valid pointer or NULL, which indicates that no information needs to be returned.</span></span> <span data-ttu-id="3de51-114">Bei der Ausgabe ein gültiger Zeiger, der auf die Zeilennummer der Zeile zeigt, eine sequenzielle Zahl, die die Position der Zeile in der Tabelle identifiziert.</span><span class="sxs-lookup"><span data-stu-id="3de51-114">On output, a valid pointer that points to the row's row number, a sequential number that identifies the row's position in the table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3de51-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3de51-115">Return value</span></span>

<span data-ttu-id="3de51-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="3de51-116">S_OK</span></span> 
  
> <span data-ttu-id="3de51-117">Die Zeile wurde erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="3de51-117">The row was successfully retrieved.</span></span>
    
<span data-ttu-id="3de51-118">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3de51-118">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="3de51-119">Die [SPropValue-Struktur,](spropvalue.md) auf die  _lpSPropValue_ verweist, enthält nicht die Indexspalteneigenschaft.</span><span class="sxs-lookup"><span data-stu-id="3de51-119">The [SPropValue](spropvalue.md) structure that  _lpSPropValue_ points to does not contain the index column property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3de51-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3de51-120">Remarks</span></span>

<span data-ttu-id="3de51-121">Die **ITableData::HrQueryRow-Methode** ruft alle Eigenschaften für die Zeile ab, die über eine Indexspalte verfügt, die dem Wert der Indexspalte entspricht, die in der Eigenschaftenstruktur enthalten ist, auf die  _von lpSPropValue_ verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="3de51-121">The **ITableData::HrQueryRow** method retrieves all of the properties for the row that has an index column that matches the value of the index column included in the property structure pointed to by  _lpSPropValue_.</span></span> <span data-ttu-id="3de51-122">**HrQueryRow** gibt auch die Zeilennummer zurück, wenn der Aufrufer sie anfordert, die die Position der Zeile in der Tabelle identifiziert.</span><span class="sxs-lookup"><span data-stu-id="3de51-122">**HrQueryRow** also returns the row number, if the caller requests it, that identifies the row's position in the table.</span></span> 
  
<span data-ttu-id="3de51-123">Da **HrQueryRow** die **SPropValue-Struktur,** auf die  _von lpSPropValue_ verwiesen wird, nicht ändert, müssen Aufrufer die Struktur frei geben, wenn **HrQueryRow** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="3de51-123">Because **HrQueryRow** does not modify the **SPropValue** structure pointed to by  _lpSPropValue_, callers must free the structure when **HrQueryRow** returns.</span></span> <span data-ttu-id="3de51-124">Anrufer müssen auch die **SRow-Struktur,** die die abgerufene Zeile enthält, frei geben.</span><span class="sxs-lookup"><span data-stu-id="3de51-124">Callers must also free the **SRow** structure that contains the retrieved row.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3de51-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3de51-125">See also</span></span>



[<span data-ttu-id="3de51-126">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="3de51-126">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="3de51-127">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="3de51-127">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="3de51-128">SPropValue</span><span class="sxs-lookup"><span data-stu-id="3de51-128">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="3de51-129">SRow</span><span class="sxs-lookup"><span data-stu-id="3de51-129">SRow</span></span>](srow.md)
  
[<span data-ttu-id="3de51-130">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3de51-130">ITableData : IUnknown</span></span>](itabledataiunknown.md)

