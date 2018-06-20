---
title: IMAPIContainerGetHierarchyTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.GetHierarchyTable
api_type:
- COM
ms.assetid: d0c54092-86a3-47e0-8133-72e119e74b65
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b30c6e9840ed5dddfd2d3a5f149a3f0f6e8da605
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792097"
---
# <a name="imapicontainergethierarchytable"></a><span data-ttu-id="f1408-103">IMAPIContainer::GetHierarchyTable</span><span class="sxs-lookup"><span data-stu-id="f1408-103">IMAPIContainer::GetHierarchyTable</span></span>

  
  
<span data-ttu-id="f1408-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f1408-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f1408-105">Gibt einen Zeiger auf den Container Hierarchietabelle.</span><span class="sxs-lookup"><span data-stu-id="f1408-105">Returns a pointer to the container's hierarchy table.</span></span>
  
```cpp
HRESULT GetHierarchyTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="f1408-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1408-106">Parameters</span></span>

 <span data-ttu-id="f1408-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f1408-107">_ulFlags_</span></span>
  
> <span data-ttu-id="f1408-108">[in] Eine Bitmaske aus Flags, die steuert, wie Informationen in der Tabelle zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f1408-108">[in] A bitmask of flags that controls how information is returned in the table.</span></span> <span data-ttu-id="f1408-109">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="f1408-109">The following flags can be set:</span></span>
    
<span data-ttu-id="f1408-110">CONVENIENT_DEPTH</span><span class="sxs-lookup"><span data-stu-id="f1408-110">CONVENIENT_DEPTH</span></span> 
  
> <span data-ttu-id="f1408-111">Füllt die Hierarchietabelle mit Container mit Daten aus mehreren Ebenen.</span><span class="sxs-lookup"><span data-stu-id="f1408-111">Fills the hierarchy table with containers from multiple levels.</span></span> <span data-ttu-id="f1408-112">Wenn CONVENIENT_DEPTH nicht festgelegt ist, enthält die Hierarchietabelle nur den Container direkt untergeordnete Container.</span><span class="sxs-lookup"><span data-stu-id="f1408-112">If CONVENIENT_DEPTH is not set, the hierarchy table contains only the container's immediate child containers.</span></span>
    
<span data-ttu-id="f1408-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="f1408-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="f1408-114">**GetHierarchyTable** können erfolgreich, möglicherweise beendet, bevor die Tabelle mit dem Anrufer verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="f1408-114">**GetHierarchyTable** can return successfully, possibly before the table is made available to the caller.</span></span> <span data-ttu-id="f1408-115">Wenn die Tabelle nicht verfügbar ist, kann die nachfolgenden Tabelle Anrufen ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="f1408-115">If the table is not available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="f1408-116">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f1408-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="f1408-117">Anforderungen, die die Spalten, die Zeichenfolgendaten enthalten im Unicode-Format zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="f1408-117">Requests that the columns that contain string data be returned in Unicode format.</span></span> <span data-ttu-id="f1408-118">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sollte die Zeichenfolgen in ANSI-Format zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f1408-118">If the MAPI_UNICODE flag is not set, the strings should be returned in ANSI format.</span></span> 
    
<span data-ttu-id="f1408-119">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="f1408-119">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="f1408-120">Zeigt Elemente, die derzeit als soft gekennzeichnet sind gelöscht – d. h., sie sind in der Aufbewahrungszeit für gelöschte Elemente Zeit Phase.</span><span class="sxs-lookup"><span data-stu-id="f1408-120">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="f1408-121">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="f1408-121">_lppTable_</span></span>
  
> <span data-ttu-id="f1408-122">[out] Ein Zeiger auf einen Zeiger auf die Hierarchietabelle.</span><span class="sxs-lookup"><span data-stu-id="f1408-122">[out] A pointer to a pointer to the hierarchy table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f1408-123">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="f1408-123">Return value</span></span>

<span data-ttu-id="f1408-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="f1408-124">S_OK</span></span> 
  
> <span data-ttu-id="f1408-125">Die Hierarchietabelle wurde erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="f1408-125">The hierarchy table was successfully retrieved.</span></span>
    
<span data-ttu-id="f1408-126">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="f1408-126">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="f1408-127">Entweder die Option MAPI_UNICODE festgelegt wurde und die Implementierung unterstützt keine Unicode oder Parameter MAPI_UNICODE nicht festgelegt wurde und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="f1408-127">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="f1408-128">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="f1408-128">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="f1408-129">Der Container hat keine untergeordnete Container und keine Hierarchietabelle bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="f1408-129">The container has no child containers and cannot provide a hierarchy table.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f1408-130">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f1408-130">Remarks</span></span>

<span data-ttu-id="f1408-131">Die **IMAPIContainer::GetHierarchyTable** -Methode gibt einen Zeiger auf die Hierarchietabelle eines Containers.</span><span class="sxs-lookup"><span data-stu-id="f1408-131">The **IMAPIContainer::GetHierarchyTable** method returns a pointer to the hierarchy table of a container.</span></span> <span data-ttu-id="f1408-132">Eine Hierarchietabelle enthält zusammenfassende Informationen zu der untergeordnete Container im Container.</span><span class="sxs-lookup"><span data-stu-id="f1408-132">A hierarchy table holds summary information about the child containers in the container.</span></span> <span data-ttu-id="f1408-133">Ordner Hierarchietabellen enthalten Informationen über Unterordner; Address Book Hierarchietabellen enthalten Informationen über untergeordnete Address Book Container und Verteilerlisten.</span><span class="sxs-lookup"><span data-stu-id="f1408-133">Folder hierarchy tables hold information about subfolders; address book hierarchy tables hold information about child address book containers and distribution lists.</span></span> 
  
<span data-ttu-id="f1408-134">Es ist möglich, dass einige Container haben keine untergeordnete Container.</span><span class="sxs-lookup"><span data-stu-id="f1408-134">It is possible for some containers to have no child containers.</span></span> <span data-ttu-id="f1408-135">Diese Container zurück MAPI_E_NO_SUPPORT aus ihrer Implementierungen von **GetHierarchyTable**.</span><span class="sxs-lookup"><span data-stu-id="f1408-135">These containers return MAPI_E_NO_SUPPORT from their implementations of **GetHierarchyTable**.</span></span>
  
<span data-ttu-id="f1408-136">Wenn das Flag CONVENIENT_DEPTH festgelegt ist, enthält jede Zeile in der Hierarchietabelle die **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))-Eigenschaft auch als Spalte.</span><span class="sxs-lookup"><span data-stu-id="f1408-136">When the CONVENIENT_DEPTH flag is set, each row in the hierarchy table also includes the **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) property as a column.</span></span> <span data-ttu-id="f1408-137">**PR_DEPTH** gibt die Ebene der einzelnen Container relativ zum Container, der die Tabelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="f1408-137">**PR_DEPTH** indicates the level of each container relative to the container that implements the table.</span></span> <span data-ttu-id="f1408-138">Implementieren des Containers direkt untergeordnetes Element, für den Container Tiefe 0 (null), untergeordnete Container in NULL Tiefe Container sind finden Sie auf eine Tiefe usw..</span><span class="sxs-lookup"><span data-stu-id="f1408-138">The implementing container's immediate child containers are at depth zero, child containers in the zero depth containers are at depth one, and so on.</span></span> <span data-ttu-id="f1408-139">Die Werte der **PR_DEPTH** sequenziell erhöht, wie die Hierarchie der Ebenen – Revcovery.</span><span class="sxs-lookup"><span data-stu-id="f1408-139">The values of **PR_DEPTH** increase sequentially as the hierarchy of levels deepens.</span></span> 
  
<span data-ttu-id="f1408-140">Eine vollständige Liste der erforderlichen und optionalen Spalten in Hierarchietabellen finden Sie unter [Hierarchietabellen](hierarchy-tables.md).</span><span class="sxs-lookup"><span data-stu-id="f1408-140">For a complete list of required and optional columns in hierarchy tables, see [Hierarchy Tables](hierarchy-tables.md).</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f1408-141">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="f1408-141">Notes to implementers</span></span>

<span data-ttu-id="f1408-142">Wenn Sie eine Hierarchietabelle für den Container unterstützen, müssen Sie auch Folgendes:</span><span class="sxs-lookup"><span data-stu-id="f1408-142">If you support a hierarchy table for your container, you must also do the following:</span></span>
  
- <span data-ttu-id="f1408-143">Unterstützung von einem Aufruf des Containers [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode zum Öffnen der **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f1408-143">Support a call to the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="f1408-144">Geben Sie einen Anruf an den Container [IMAPIProp::GetPropList](imapiprop-getproplist.md) oder [IMAPIProp::GetProps](imapiprop-getprops.md) Methoden **PR_CONTAINER_HIERARCHY** zurück.</span><span class="sxs-lookup"><span data-stu-id="f1408-144">Return **PR_CONTAINER_HIERARCHY** from a call to the container's [IMAPIProp::GetPropList](imapiprop-getproplist.md) or [IMAPIProp::GetProps](imapiprop-getprops.md) methods.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="f1408-145">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="f1408-145">Notes to callers</span></span>

<span data-ttu-id="f1408-146">Zeichenfolge und der binären Inhalt Tabellenspalten können abgeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="f1408-146">String and binary contents table columns can be truncated.</span></span> <span data-ttu-id="f1408-147">In der Regel zurückgeben Anbieter 255 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="f1408-147">Typically, providers return 255 characters.</span></span> <span data-ttu-id="f1408-148">Da Sie im Voraus wissen können nicht, ob eine Tabelle abgeschnittene Spalten enthält, wird davon ausgegangen Sie, dass eine Spalte abgeschnitten wird, wenn die Länge der Spalte 510 maximal 255 Bytes ist.</span><span class="sxs-lookup"><span data-stu-id="f1408-148">Because you cannot know beforehand whether a table includes truncated columns, assume that a column is truncated if the length of the column is either 255 or 510 bytes.</span></span> <span data-ttu-id="f1408-149">Sie können immer den vollständigen Wert der abgeschnittene Spalte an, falls erforderlich, direkt aus dem Objekt mithilfe der Eintrags-ID um zu öffnen und anschließendes Aufrufen der [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="f1408-149">You can always retrieve the full value of a truncated column, if necessary, directly from the object by using its entry identifier to open it and then calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
<span data-ttu-id="f1408-150">Je nach der Implementierung des Anbieters, Einschränkungen und Sortierung Vorgänge können auf die gesamte Zeichenfolge oder auf die abgeschnittene Version dieser Zeichenfolge anwenden.</span><span class="sxs-lookup"><span data-stu-id="f1408-150">Depending on the provider's implementation, restrictions and sorting operations can apply to the whole string or to the truncated version of that string.</span></span> <span data-ttu-id="f1408-151">Darüber hinaus sind Anbieter nicht unbedingt festgelegten Reihenfolge sortieren berücksichtigt, [SSortOrderSet](ssortorderset.md) für Hierarchietabellen angegeben.</span><span class="sxs-lookup"><span data-stu-id="f1408-151">Moreover, store providers are not guaranteed to honor the sort order set [SSortOrderSet](ssortorderset.md) specified for hierarchy tables.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f1408-152">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="f1408-152">MFCMAPI reference</span></span>

<span data-ttu-id="f1408-153">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="f1408-153">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f1408-154">**Datei**</span><span class="sxs-lookup"><span data-stu-id="f1408-154">**File**</span></span>|<span data-ttu-id="f1408-155">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="f1408-155">**Function**</span></span>|<span data-ttu-id="f1408-156">**Comment**</span><span class="sxs-lookup"><span data-stu-id="f1408-156">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f1408-157">HierarchyTableTreeCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="f1408-157">HierarchyTableTreeCtrl.cpp</span></span>  <br/> |<span data-ttu-id="f1408-158">CHierarchyTableTreeCtrl::GetHierarchyTable</span><span class="sxs-lookup"><span data-stu-id="f1408-158">CHierarchyTableTreeCtrl::GetHierarchyTable</span></span>  <br/> |<span data-ttu-id="f1408-159">Die CHierarchyTableTreeCtrl-Klasse wird mit **GetHierarchyTable** Hierarchietabellen anzeigen in einem Strukturansicht-Steuerelement abgerufen.</span><span class="sxs-lookup"><span data-stu-id="f1408-159">The CHierarchyTableTreeCtrl class uses **GetHierarchyTable** to obtain hierarchy tables to display in a tree view control.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f1408-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f1408-160">See also</span></span>



[<span data-ttu-id="f1408-161">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="f1408-161">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="f1408-162">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="f1408-162">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="f1408-163">IMAPITable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="f1408-163">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="f1408-164">Kanonische PidTagContainerHierarchy-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f1408-164">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="f1408-165">IMAPIContainer: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f1408-165">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="f1408-166">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="f1408-166">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
