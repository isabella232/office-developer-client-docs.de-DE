---
title: ITableDataHrEnumRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrEnumRow
api_type:
- COM
ms.assetid: b25d9f2b-9454-4983-98f7-6a051a3b8a04
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 50fd96acd0989459c9887770ec5a3a236f182da5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418372"
---
# <a name="itabledatahrenumrow"></a><span data-ttu-id="0b3de-103">ITableData::HrEnumRow</span><span class="sxs-lookup"><span data-stu-id="0b3de-103">ITableData::HrEnumRow</span></span>

  
  
<span data-ttu-id="0b3de-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0b3de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0b3de-105">Ruft eine Zeile basierend auf ihrer Position in der Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="0b3de-105">Retrieves a row based on its position in the table.</span></span> 
  
```cpp
HRESULT HrEnumRow(
  ULONG ulRowNumber,
  LPSRow FAR * lppSRow
);
```

## <a name="parameters"></a><span data-ttu-id="0b3de-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b3de-106">Parameters</span></span>

 <span data-ttu-id="0b3de-107">_ulRowNumber_</span><span class="sxs-lookup"><span data-stu-id="0b3de-107">_ulRowNumber_</span></span>
  
> <span data-ttu-id="0b3de-108">[in] Die Nummer der Zeile, für die Eigenschaften zurückgeben werden.</span><span class="sxs-lookup"><span data-stu-id="0b3de-108">[in] The number of the row for which to return properties.</span></span> <span data-ttu-id="0b3de-109">Der Wert im  _ulRowNumber-Parameter_ kann ein beliebiger Wert von 0 sein, der die erste Zeile in der Tabelle bis n - 1 angibt, was die letzte Zeile in der Tabelle angibt.</span><span class="sxs-lookup"><span data-stu-id="0b3de-109">The value in the  _ulRowNumber_ parameter can be any value from 0, which indicates the first row in the table, through n - 1, which indicates the last row in the table.</span></span> 
    
 <span data-ttu-id="0b3de-110">_lppSRow_</span><span class="sxs-lookup"><span data-stu-id="0b3de-110">_lppSRow_</span></span>
  
> <span data-ttu-id="0b3de-111">[out] Ein Zeiger auf einen Zeiger auf eine [SRow-Struktur,](srow.md) die die Zielzeile beschreibt.</span><span class="sxs-lookup"><span data-stu-id="0b3de-111">[out] A pointer to a pointer to an [SRow](srow.md) structure that describes the target row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0b3de-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0b3de-112">Return value</span></span>

<span data-ttu-id="0b3de-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="0b3de-113">S_OK</span></span> 
  
> <span data-ttu-id="0b3de-114">Die Zeile wurde erfolgreich abgerufen, oder eine Zeile für die durch den  _ulRowNumber-Parameter_ angegebene Zeilennummer ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="0b3de-114">The row was retrieved successfully, or a row for the row number specified by the  _ulRowNumber_ parameter does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0b3de-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0b3de-115">Remarks</span></span>

<span data-ttu-id="0b3de-116">Die **ITableData::HrEnumRow-Methode** ruft eine Zeile basierend auf einer sequenziellen Zahl ab.</span><span class="sxs-lookup"><span data-stu-id="0b3de-116">The **ITableData::HrEnumRow** method retrieves a row based on a sequential number.</span></span> <span data-ttu-id="0b3de-117">Diese Zahl stellt die Einfügereihenfolge dar (0 gibt die erste Zeile an, und die Anzahl der Zeilen minus 1 gibt die letzte Zeile an).</span><span class="sxs-lookup"><span data-stu-id="0b3de-117">This number represents the order of insertion (0 indicates the first row, and the number of rows minus 1 indicates the last row).</span></span> <span data-ttu-id="0b3de-118">MAPI behält diese chronologische Reihenfolge der Zeileneinfügung für die Lebensdauer des Tabellendatenobjekts bei.</span><span class="sxs-lookup"><span data-stu-id="0b3de-118">MAPI maintains this chronological order of row insertion for the lifetime of the table data object.</span></span> 
  
<span data-ttu-id="0b3de-119">Wenn die in  _ulRowNumber_ angegebene Zahl nicht einer Zeile in der Tabelle entspricht, gibt **HrEnumRow** S_OK zurück und legt den  _lppSRow-Parameter_ auf NULL fest.</span><span class="sxs-lookup"><span data-stu-id="0b3de-119">If the number specified in  _ulRowNumber_ does not correspond to a row in the table, **HrEnumRow** returns S_OK and sets the  _lppSRow_ parameter to NULL.</span></span> 
  
<span data-ttu-id="0b3de-120">MAPI weist speicher für die zurückgegebene **SRow-Struktur** mithilfe der [MAPIAllocateBuffer-Funktion](mapiallocatebuffer.md) zu, wenn das Tabellendatenobjekt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="0b3de-120">MAPI allocates memory for the returned **SRow** structure by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function when the table data object is created.</span></span> <span data-ttu-id="0b3de-121">Der Aufrufer muss diesen Speicher durch Aufrufen der [MAPIFreeBuffer-Funktion](mapifreebuffer.md) los.</span><span class="sxs-lookup"><span data-stu-id="0b3de-121">The caller must release this memory by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="0b3de-122">Zum Abrufen von Zeilen aus einer Tabelle in der Reihenfolge, in der sie eingefügt wurden, rufen Benutzer des Tabellendatenobjekts die **HrEnumRow-Methode** auf.</span><span class="sxs-lookup"><span data-stu-id="0b3de-122">To retrieve rows from a table in the order that they were inserted, table data object users call the **HrEnumRow** method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0b3de-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b3de-123">See also</span></span>



[<span data-ttu-id="0b3de-124">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="0b3de-124">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="0b3de-125">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="0b3de-125">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="0b3de-126">SRow</span><span class="sxs-lookup"><span data-stu-id="0b3de-126">SRow</span></span>](srow.md)
  
[<span data-ttu-id="0b3de-127">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0b3de-127">ITableData : IUnknown</span></span>](itabledataiunknown.md)

