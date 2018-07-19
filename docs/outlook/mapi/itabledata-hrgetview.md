---
title: ITableDataHrGetView
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrGetView
api_type:
- COM
ms.assetid: 0e2a47be-497b-4031-87ce-60b2635e25f7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a913f2f3a72a365ec7d5078eccf31c4212ca83a5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792845"
---
# <a name="itabledatahrgetview"></a><span data-ttu-id="e993f-103">ITableData::HrGetView</span><span class="sxs-lookup"><span data-stu-id="e993f-103">ITableData::HrGetView</span></span>

  
  
<span data-ttu-id="e993f-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e993f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e993f-105">Erstellt eine Tabellenansicht, einen Zeiger auf eine Implementierung [IMAPITable](imapitableiunknown.md) zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="e993f-105">Creates a table view, returning a pointer to an [IMAPITable](imapitableiunknown.md) implementation.</span></span> 
  
```cpp
HRESULT HrGetView(
  LPSSortOrderSet lpSSortOrderSet,
  CALLERRELEASE FAR * lpfCallerRelease,
  ULONG_PTR ulCallerData,
  LPMAPITABLE FAR * lppMAPITable
);
```

## <a name="parameters"></a><span data-ttu-id="e993f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e993f-106">Parameters</span></span>

 <span data-ttu-id="e993f-107">_lpSSortOrderSet_</span><span class="sxs-lookup"><span data-stu-id="e993f-107">_lpSSortOrderSet_</span></span>
  
> <span data-ttu-id="e993f-108">[in] Ein Zeiger auf eine Sortierung Reihenfolge-Struktur, die Sortierreihenfolge für die Tabellenansicht beschreibt.</span><span class="sxs-lookup"><span data-stu-id="e993f-108">[in] A pointer to a sort order structure that describes the sort order for the table view.</span></span> <span data-ttu-id="e993f-109">Wenn NULL in der _LpSSortOrderSet_ -Parameter übergeben wird, wird die Ansicht nicht sortiert.</span><span class="sxs-lookup"><span data-stu-id="e993f-109">If NULL is passed in the  _lpSSortOrderSet_ parameter, the view is not sorted.</span></span> 
    
 <span data-ttu-id="e993f-110">_lpfCallerRelease_</span><span class="sxs-lookup"><span data-stu-id="e993f-110">_lpfCallerRelease_</span></span>
  
> <span data-ttu-id="e993f-111">[in] Ein Zeiger auf eine Rückruffunktion, die basierend auf der [CALLERRELEASE](callerrelease.md) Prototyp, den MAPI-aufrufen, wenn sie die Ansicht loslässt.</span><span class="sxs-lookup"><span data-stu-id="e993f-111">[in] A pointer to a callback function based on the [CALLERRELEASE](callerrelease.md) prototype that MAPI calls when it releases the view.</span></span> <span data-ttu-id="e993f-112">Wenn NULL in der _LpfCallerRelease_ -Parameter übergeben wird, wird auf die Version der Ansicht keine Funktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="e993f-112">If NULL is passed in the  _lpfCallerRelease_ parameter, no function is called on release of the view.</span></span> 
    
 <span data-ttu-id="e993f-113">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="e993f-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="e993f-114">[in] Die Daten, die mit der neuen Ansicht gespeichert und an die Rückruffunktion übergeben werden müssen, auf die _LpfCallerRelease_.</span><span class="sxs-lookup"><span data-stu-id="e993f-114">[in] The data that must be saved with the new view and passed to the callback function pointed to by  _lpfCallerRelease_.</span></span>
    
 <span data-ttu-id="e993f-115">_lppMAPITable_</span><span class="sxs-lookup"><span data-stu-id="e993f-115">_lppMAPITable_</span></span>
  
> <span data-ttu-id="e993f-116">[out] Ein Zeiger auf einen Zeiger auf die neu erstellte Ansicht.</span><span class="sxs-lookup"><span data-stu-id="e993f-116">[out] A pointer to a pointer to the newly created view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e993f-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e993f-117">Return value</span></span>

<span data-ttu-id="e993f-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="e993f-118">S_OK</span></span> 
  
> <span data-ttu-id="e993f-119">Die Ansicht wurde erfolgreich erstellt.</span><span class="sxs-lookup"><span data-stu-id="e993f-119">The view was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e993f-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e993f-120">Remarks</span></span>

<span data-ttu-id="e993f-121">Die **ITableData::HrGetView** -Methode erstellt eine schreibgeschützte Ansicht der Daten in der Tabelle, in der auf das durch den Parameter _LpSSortOrderSet_ Reihenfolge sortiert.</span><span class="sxs-lookup"><span data-stu-id="e993f-121">The **ITableData::HrGetView** method creates a read-only view of the data in the table, sorted in the order pointed to by the  _lpSSortOrderSet_ parameter.</span></span> <span data-ttu-id="e993f-122">Der Cursor befindet sich am Anfang der ersten Zeile in der Ansicht.</span><span class="sxs-lookup"><span data-stu-id="e993f-122">The cursor is placed at the beginning of the first row in the view.</span></span> <span data-ttu-id="e993f-123">Eine Implementierung von **IMAPITable** für den Zugriff auf die Ansicht wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e993f-123">An **IMAPITable** interface implementation for accessing the view is returned.</span></span> 
  
<span data-ttu-id="e993f-124">Dienstanbieter Aufrufen **HrGetView** , wenn sie eine Clientzugriff auf eine Tabelle gewähren müssen.</span><span class="sxs-lookup"><span data-stu-id="e993f-124">Service providers call **HrGetView** when they need to give a client access to a table.</span></span> <span data-ttu-id="e993f-125">**HrGetView** die Ansicht erstellt und gibt den **IMAPITable** Zeiger zurück.</span><span class="sxs-lookup"><span data-stu-id="e993f-125">**HrGetView** creates the view and returns the **IMAPITable** pointer.</span></span> <span data-ttu-id="e993f-126">Dienstanbieter übergeben wiederum den Mauszeiger an den Client.</span><span class="sxs-lookup"><span data-stu-id="e993f-126">Service providers in turn pass the pointer on to the client.</span></span> <span data-ttu-id="e993f-127">Wenn der Client mithilfe der Tabelle abgeschlossen ist und dessen [IUnknown](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) -Methode aufruft, ruft **HrGetView** die Callback-Funktion, die auf den durch den Parameter _LpfCallerRelease_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="e993f-127">When the client is finished using the table and calls its [IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method, **HrGetView** calls the callback function pointed to by the  _lpfCallerRelease_ parameter.</span></span> 
  
<span data-ttu-id="e993f-128">Wenn es sich bei ein Dienstanbieter muss eine Ansicht an einen Client zurück, die eine benutzerdefinierte Spalte festgelegt wurde, oder eine Einschränkung der Anbieter Aufrufen der Ansicht [IMAPITable::SetColumns](imapitable-setcolumns.md) [Methode IMAPITable:: Restrict](imapitable-restrict.md) Methoden und bevor die Clientzugriff.</span><span class="sxs-lookup"><span data-stu-id="e993f-128">If a service provider needs to return to a client a view that has a customized column set or a restriction, the provider can call the view's [IMAPITable::SetColumns](imapitable-setcolumns.md) and [IMAPITable::Restrict](imapitable-restrict.md) methods before allowing the client access.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e993f-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e993f-129">See also</span></span>



[<span data-ttu-id="e993f-130">CALLERRELEASE</span><span class="sxs-lookup"><span data-stu-id="e993f-130">CALLERRELEASE</span></span>](callerrelease.md)
  
[<span data-ttu-id="e993f-131">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e993f-131">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="e993f-132">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="e993f-132">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="e993f-133">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e993f-133">ITableData : IUnknown</span></span>](itabledataiunknown.md)

