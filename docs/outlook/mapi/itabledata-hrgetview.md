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
ms.openlocfilehash: 375a0f1d39b09b7ad453120f20752e00ffda0e15
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278715"
---
# <a name="itabledatahrgetview"></a><span data-ttu-id="23354-103">ITableData::HrGetView</span><span class="sxs-lookup"><span data-stu-id="23354-103">ITableData::HrGetView</span></span>

  
  
<span data-ttu-id="23354-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="23354-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="23354-105">Erstellt eine Tabellenansicht und gibt einen Zeiger auf eine [IMAPITable-Implementierung](imapitableiunknown.md) zurück.</span><span class="sxs-lookup"><span data-stu-id="23354-105">Creates a table view, returning a pointer to an [IMAPITable](imapitableiunknown.md) implementation.</span></span> 
  
```cpp
HRESULT HrGetView(
  LPSSortOrderSet lpSSortOrderSet,
  CALLERRELEASE FAR * lpfCallerRelease,
  ULONG_PTR ulCallerData,
  LPMAPITABLE FAR * lppMAPITable
);
```

## <a name="parameters"></a><span data-ttu-id="23354-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="23354-106">Parameters</span></span>

 <span data-ttu-id="23354-107">_lpSSortOrderSet_</span><span class="sxs-lookup"><span data-stu-id="23354-107">_lpSSortOrderSet_</span></span>
  
> <span data-ttu-id="23354-108">[in] Ein Zeiger auf eine Sortierreihenfolgenstruktur, die die Sortierreihenfolge für die Tabellenansicht beschreibt.</span><span class="sxs-lookup"><span data-stu-id="23354-108">[in] A pointer to a sort order structure that describes the sort order for the table view.</span></span> <span data-ttu-id="23354-109">Wenn NULL im  _lpSSortOrderSet-Parameter übergeben_ wird, wird die Ansicht nicht sortiert.</span><span class="sxs-lookup"><span data-stu-id="23354-109">If NULL is passed in the  _lpSSortOrderSet_ parameter, the view is not sorted.</span></span> 
    
 <span data-ttu-id="23354-110">_lpfCallerRelease_</span><span class="sxs-lookup"><span data-stu-id="23354-110">_lpfCallerRelease_</span></span>
  
> <span data-ttu-id="23354-111">[in] Ein Zeiger auf eine Rückruffunktion basierend auf dem [CALLERRELEASE-Prototyp,](callerrelease.md) den MAPI aufruft, wenn die Ansicht veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="23354-111">[in] A pointer to a callback function based on the [CALLERRELEASE](callerrelease.md) prototype that MAPI calls when it releases the view.</span></span> <span data-ttu-id="23354-112">Wenn NULL im  _lpfCallerRelease-Parameter übergeben_ wird, wird bei der Freigabe der Ansicht keine Funktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="23354-112">If NULL is passed in the  _lpfCallerRelease_ parameter, no function is called on release of the view.</span></span> 
    
 <span data-ttu-id="23354-113">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="23354-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="23354-114">[in] Die Daten, die mit der neuen Ansicht gespeichert und an die Rückruffunktion übergeben werden müssen, auf die von _lpfCallerRelease verwiesen wird._</span><span class="sxs-lookup"><span data-stu-id="23354-114">[in] The data that must be saved with the new view and passed to the callback function pointed to by  _lpfCallerRelease_.</span></span>
    
 <span data-ttu-id="23354-115">_lppMAPITable_</span><span class="sxs-lookup"><span data-stu-id="23354-115">_lppMAPITable_</span></span>
  
> <span data-ttu-id="23354-116">[out] Ein Zeiger auf einen Zeiger auf die neu erstellte Ansicht.</span><span class="sxs-lookup"><span data-stu-id="23354-116">[out] A pointer to a pointer to the newly created view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="23354-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="23354-117">Return value</span></span>

<span data-ttu-id="23354-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="23354-118">S_OK</span></span> 
  
> <span data-ttu-id="23354-119">Die Ansicht wurde erfolgreich erstellt.</span><span class="sxs-lookup"><span data-stu-id="23354-119">The view was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="23354-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="23354-120">Remarks</span></span>

<span data-ttu-id="23354-121">Die **ITableData::HrGetView-Methode** erstellt eine schreibgeschützte Ansicht der Daten in der Tabelle, sortiert in der Reihenfolge, auf die der  _lpSSortOrderSet-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="23354-121">The **ITableData::HrGetView** method creates a read-only view of the data in the table, sorted in the order pointed to by the  _lpSSortOrderSet_ parameter.</span></span> <span data-ttu-id="23354-122">Der Cursor wird am Anfang der ersten Zeile in der Ansicht platziert.</span><span class="sxs-lookup"><span data-stu-id="23354-122">The cursor is placed at the beginning of the first row in the view.</span></span> <span data-ttu-id="23354-123">Eine **IMAPITable-Schnittstellenimplementierung** für den Zugriff auf die Ansicht wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="23354-123">An **IMAPITable** interface implementation for accessing the view is returned.</span></span> 
  
<span data-ttu-id="23354-124">Dienstanbieter rufen **HrGetView auf,** wenn sie einem Client Zugriff auf eine Tabelle geben müssen.</span><span class="sxs-lookup"><span data-stu-id="23354-124">Service providers call **HrGetView** when they need to give a client access to a table.</span></span> <span data-ttu-id="23354-125">**HrGetView** erstellt die Ansicht und gibt den **IMAPITable-Zeiger** zurück.</span><span class="sxs-lookup"><span data-stu-id="23354-125">**HrGetView** creates the view and returns the **IMAPITable** pointer.</span></span> <span data-ttu-id="23354-126">Dienstanbieter geben den Zeiger wiederum an den Client weiter.</span><span class="sxs-lookup"><span data-stu-id="23354-126">Service providers in turn pass the pointer on to the client.</span></span> <span data-ttu-id="23354-127">Wenn der Client mit der Tabelle fertig ist und seine [IUnknown::Release-Methode](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) aufruft, ruft **HrGetView** die Rückruffunktion auf, auf die der  _lpfCallerRelease-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="23354-127">When the client is finished using the table and calls its [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method, **HrGetView** calls the callback function pointed to by the  _lpfCallerRelease_ parameter.</span></span> 
  
<span data-ttu-id="23354-128">Wenn ein Dienstanbieter eine Ansicht mit einem angepassten Spaltensatz oder einer Einschränkung an einen Client zurückgeben muss, kann der Anbieter die [Methoden IMAPITable::SetColumns](imapitable-setcolumns.md) und [IMAPITable::Restrict](imapitable-restrict.md) der Ansicht aufrufen, bevor der Clientzugriff ermöglicht wird.</span><span class="sxs-lookup"><span data-stu-id="23354-128">If a service provider needs to return to a client a view that has a customized column set or a restriction, the provider can call the view's [IMAPITable::SetColumns](imapitable-setcolumns.md) and [IMAPITable::Restrict](imapitable-restrict.md) methods before allowing the client access.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="23354-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="23354-129">See also</span></span>



[<span data-ttu-id="23354-130">CALLERRELEASE</span><span class="sxs-lookup"><span data-stu-id="23354-130">CALLERRELEASE</span></span>](callerrelease.md)
  
[<span data-ttu-id="23354-131">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="23354-131">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="23354-132">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="23354-132">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="23354-133">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="23354-133">ITableData : IUnknown</span></span>](itabledataiunknown.md)

