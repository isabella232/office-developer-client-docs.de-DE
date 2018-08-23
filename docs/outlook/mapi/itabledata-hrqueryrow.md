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
ms.openlocfilehash: ef0dc212a6a6f761cd8dd0cae5312c548c02ae50
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583820"
---
# <a name="itabledatahrqueryrow"></a><span data-ttu-id="c758d-103">ITableData::HrQueryRow</span><span class="sxs-lookup"><span data-stu-id="c758d-103">ITableData::HrQueryRow</span></span>

  
  
<span data-ttu-id="c758d-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c758d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c758d-105">Ruft eine Tabellenzeile.</span><span class="sxs-lookup"><span data-stu-id="c758d-105">Retrieves a table row.</span></span>
  
```cpp
HRESULT HrQueryRow(
  LPSPropValue lpSPropValue,
  LPSRow FAR * lppSRow,
  ULONG FAR * lpuliRow
);
```

## <a name="parameters"></a><span data-ttu-id="c758d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c758d-106">Parameters</span></span>

 <span data-ttu-id="c758d-107">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="c758d-107">_lpSPropValue_</span></span>
  
> <span data-ttu-id="c758d-108">[in] Ein Zeiger auf eine Eigenschaft-Wert-Struktur, die beschreibt die Indexspalte der Zeile abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c758d-108">[in] A pointer to a property value structure that describes the index column for the row to be retrieved.</span></span> <span data-ttu-id="c758d-109">Der **UlPropTag** Member der Eigenschaft Wert Struktur sollte das gleiche Eigenschafts-Tag als _UlPropTagIndexColumn_ -Parameter aus dem Aufruf der Funktion [CreateTable](createtable.md) enthalten, die greift auf die [ITableData](itabledataiunknown.md) Implementierung.</span><span class="sxs-lookup"><span data-stu-id="c758d-109">The **ulPropTag** member of the property value structure should contain the same property tag as the  _ulPropTagIndexColumn_ parameter from the call to the [CreateTable](createtable.md) function, which accesses the [ITableData](itabledataiunknown.md) implementation.</span></span> 
    
 <span data-ttu-id="c758d-110">_lppSRow_</span><span class="sxs-lookup"><span data-stu-id="c758d-110">_lppSRow_</span></span>
  
> <span data-ttu-id="c758d-111">[out] Ein Zeiger auf einen Zeiger auf die abgerufenen Zeile.</span><span class="sxs-lookup"><span data-stu-id="c758d-111">[out] A pointer to a pointer to the retrieved row.</span></span> 
    
 <span data-ttu-id="c758d-112">_lpuliRow_</span><span class="sxs-lookup"><span data-stu-id="c758d-112">_lpuliRow_</span></span>
  
> <span data-ttu-id="c758d-113">[in, out] Auf Eingabe, ein gültiger Zeiger oder NULL der angibt, dass keine Informationen zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="c758d-113">[in, out] On input, a valid pointer or NULL, which indicates that no information needs to be returned.</span></span> <span data-ttu-id="c758d-114">Bei der Ausgabe zeigt, die ein gültiger Zeiger auf die Zeile Zeilennummer, eine fortlaufende Zahl, die die Zeilenposition in der Tabelle identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c758d-114">On output, a valid pointer that points to the row's row number, a sequential number that identifies the row's position in the table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c758d-115">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="c758d-115">Return value</span></span>

<span data-ttu-id="c758d-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="c758d-116">S_OK</span></span> 
  
> <span data-ttu-id="c758d-117">Die Zeile wurde erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c758d-117">The row was successfully retrieved.</span></span>
    
<span data-ttu-id="c758d-118">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c758d-118">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="c758d-119">Die [SPropValue](spropvalue.md) -Struktur, _LpSPropValue_ verweist, enthält nicht die Index-Spalte-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c758d-119">The [SPropValue](spropvalue.md) structure that  _lpSPropValue_ points to does not contain the index column property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c758d-120">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="c758d-120">Remarks</span></span>

<span data-ttu-id="c758d-121">Die **ITableData::HrQueryRow** -Methode ruft alle Eigenschaften für die Zeile, die eine Indexspalte vorhanden ist, die den Wert der Indexspalte in der Eigenschaft Struktur auf den _LpSPropValue_enthalten entspricht.</span><span class="sxs-lookup"><span data-stu-id="c758d-121">The **ITableData::HrQueryRow** method retrieves all of the properties for the row that has an index column that matches the value of the index column included in the property structure pointed to by  _lpSPropValue_.</span></span> <span data-ttu-id="c758d-122">**HrQueryRow** gibt auch die Nummer der Zeile zurück, wenn der Anrufer, anfordert, auf dem die Zeilenposition in der Tabelle identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c758d-122">**HrQueryRow** also returns the row number, if the caller requests it, that identifies the row's position in the table.</span></span> 
  
<span data-ttu-id="c758d-123">Da **HrQueryRow** nicht die **SPropValue** -Struktur, die auf den _LpSPropValue_ändert, müssen Anrufer die Struktur frei, wenn **HrQueryRow** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c758d-123">Because **HrQueryRow** does not modify the **SPropValue** structure pointed to by  _lpSPropValue_, callers must free the structure when **HrQueryRow** returns.</span></span> <span data-ttu-id="c758d-124">Anrufer müssen auch die Struktur **SRow** frei, die die abgerufene Zeile enthält.</span><span class="sxs-lookup"><span data-stu-id="c758d-124">Callers must also free the **SRow** structure that contains the retrieved row.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c758d-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c758d-125">See also</span></span>



[<span data-ttu-id="c758d-126">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="c758d-126">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="c758d-127">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="c758d-127">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="c758d-128">SPropValue</span><span class="sxs-lookup"><span data-stu-id="c758d-128">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="c758d-129">SRow</span><span class="sxs-lookup"><span data-stu-id="c758d-129">SRow</span></span>](srow.md)
  
[<span data-ttu-id="c758d-130">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c758d-130">ITableData : IUnknown</span></span>](itabledataiunknown.md)

