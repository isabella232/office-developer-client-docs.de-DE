---
title: IMAPIPropGetNamesFromIDs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetNamesFromIDs
api_type:
- COM
ms.assetid: 3efa4731-cf32-4a6c-9ba8-d059e58b0d98
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a2ec6def319b1f4686a61e9f97a936bfeba0d410
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792285"
---
# <a name="imapipropgetnamesfromids"></a><span data-ttu-id="99366-103">IMAPIProp::GetNamesFromIDs</span><span class="sxs-lookup"><span data-stu-id="99366-103">IMAPIProp::GetNamesFromIDs</span></span>

  
  
<span data-ttu-id="99366-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="99366-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="99366-105">Enthält die Eigenschaftennamen, die einen oder mehrere Eigenschaftenbezeichner entsprechen.</span><span class="sxs-lookup"><span data-stu-id="99366-105">Provides the property names that correspond to one or more property identifiers.</span></span>
  
```cpp
HRESULT GetNamesFromIDs(
  LPSPropTagArray FAR * lppPropTags,
  LPGUID lpPropSetGuid,
  ULONG ulFlags,
  ULONG FAR * lpcPropNames,
  LPMAPINAMEID FAR * FAR * lpppPropNames
);
```

## <a name="parameters"></a><span data-ttu-id="99366-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="99366-106">Parameters</span></span>

 <span data-ttu-id="99366-107">_lppPropTags_</span><span class="sxs-lookup"><span data-stu-id="99366-107">_lppPropTags_</span></span>
  
> <span data-ttu-id="99366-108">[in, out] Bei Eingabe einen Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die ein Array von Eigenschaftentags enthält. andernfalls NULL, was bedeutet, dass alle Namen zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="99366-108">[in, out] On input, a pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags; otherwise, NULL, indicating that all names should be returned.</span></span> <span data-ttu-id="99366-109">Das Element **cValues** Array der Tag-Eigenschaft kann nicht 0 sein.</span><span class="sxs-lookup"><span data-stu-id="99366-109">The **cValues** member for the property tag array cannot be 0.</span></span> <span data-ttu-id="99366-110">Wenn _LppPropTags_ einen gültigen Zeiger für die Eingabe ist, gibt **GetNamesFromIDs** Namen für jede Eigenschaft-ID in das Array aufgenommen.</span><span class="sxs-lookup"><span data-stu-id="99366-110">If  _lppPropTags_ is a valid pointer on input, **GetNamesFromIDs** returns names for each property identifier included in the array.</span></span> 
    
 <span data-ttu-id="99366-111">_lpPropSetGuid_</span><span class="sxs-lookup"><span data-stu-id="99366-111">_lpPropSetGuid_</span></span>
  
> <span data-ttu-id="99366-112">[in] Ein Zeiger auf eine GUID oder eine [GUID](guid.md) -Struktur, einen Eigenschaftensatz angibt.</span><span class="sxs-lookup"><span data-stu-id="99366-112">[in] A pointer to a GUID, or [GUID](guid.md) structure, that identifies a property set.</span></span> <span data-ttu-id="99366-113">Der Parameter _LpPropSetGuid_ kann auf einen gültigen Eigenschaftensatz oder NULL sein.</span><span class="sxs-lookup"><span data-stu-id="99366-113">The  _lpPropSetGuid_ parameter can point to a valid property set or can be NULL.</span></span> 
    
 <span data-ttu-id="99366-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="99366-114">_ulFlags_</span></span>
  
> <span data-ttu-id="99366-115">[in] Eine Bitmaske aus Flags, die den Typ des zurückzugebenden Namen angibt.</span><span class="sxs-lookup"><span data-stu-id="99366-115">[in] A bitmask of flags that indicates the type of names to be returned.</span></span> <span data-ttu-id="99366-116">Die folgenden Werte können verwendet werden (wenn beide Attribute festgelegt sind, keine Namen zurückgegeben):</span><span class="sxs-lookup"><span data-stu-id="99366-116">The following flags can be used (if both flags are set, no names will be returned):</span></span>
    
<span data-ttu-id="99366-117">MAPI_NO_IDS</span><span class="sxs-lookup"><span data-stu-id="99366-117">MAPI_NO_IDS</span></span> 
  
> <span data-ttu-id="99366-118">Anforderungen, die nur als Unicode-Zeichenfolgen gespeicherte Namen zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="99366-118">Requests that only names stored as Unicode strings be returned.</span></span> 
    
<span data-ttu-id="99366-119">MAPI_NO_STRINGS</span><span class="sxs-lookup"><span data-stu-id="99366-119">MAPI_NO_STRINGS</span></span> 
  
> <span data-ttu-id="99366-120">Anforderungen, die nur als numerischen Bezeichner gespeicherte Namen zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="99366-120">Requests that only names stored as numeric identifiers be returned.</span></span> 
    
 <span data-ttu-id="99366-121">_lpcPropNames_</span><span class="sxs-lookup"><span data-stu-id="99366-121">_lpcPropNames_</span></span>
  
> <span data-ttu-id="99366-122">[out] Ein Zeiger auf eine Anzahl von der Eigenschaft Name Zeigern im Array auf den durch den Parameter _LppPropNames_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="99366-122">[out] A pointer to a count of the property name pointers in the array pointed to by the  _lppPropNames_ parameter.</span></span> 
    
 <span data-ttu-id="99366-123">_lpppPropNames_</span><span class="sxs-lookup"><span data-stu-id="99366-123">_lpppPropNames_</span></span>
  
> <span data-ttu-id="99366-124">[out] Ein Zeiger auf ein Array von Zeigern für [MAPINAMEID](mapinameid.md) Strukturen, Eigenschaftennamen enthält.</span><span class="sxs-lookup"><span data-stu-id="99366-124">[out] A pointer to an array of pointers to [MAPINAMEID](mapinameid.md) structures that contains property names.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="99366-125">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="99366-125">Return value</span></span>

<span data-ttu-id="99366-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="99366-126">S_OK</span></span> 
  
> <span data-ttu-id="99366-127">Die Eigenschaftennamen wurden erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="99366-127">The property names were successfully returned.</span></span> 
    
<span data-ttu-id="99366-128">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="99366-128">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="99366-129">Das Objekt unterstützt keine benannte Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="99366-129">The object does not support named properties.</span></span> 
    
<span data-ttu-id="99366-130">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="99366-130">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="99366-131">Der Aufruf war insgesamt erfolgreich, aber Namen für eine oder mehrere Eigenschaften konnte nicht zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="99366-131">The call succeeded overall, but names for one or more properties could not be returned.</span></span> <span data-ttu-id="99366-132">Die Eigenschaftentags für die fehlerhafte Eigenschaften haben einen Eigenschaftentyp des **PT_ERROR**.</span><span class="sxs-lookup"><span data-stu-id="99366-132">The property tags for the failing properties have a property type of **PT_ERROR**.</span></span> <span data-ttu-id="99366-133">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="99366-133">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="99366-134">Verwenden Sie das Makro **HR_FAILED** , um für diese Warnung zu testen.</span><span class="sxs-lookup"><span data-stu-id="99366-134">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="99366-135">Weitere Informationen finden Sie unter [Verwendung von Makros Fehlerbehandlung](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="99366-135">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span> 
    
<span data-ttu-id="99366-136">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="99366-136">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="99366-137">Das **cValues** -Element aus einem oder mehreren der Einträge in der Array-Tag-Eigenschaft auf den _LppPropTags_ ist auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="99366-137">The **cValues** member of one or more of the entries in the property tag array pointed to by  _lppPropTags_ is set to 0.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="99366-138">Hinweise</span><span class="sxs-lookup"><span data-stu-id="99366-138">Remarks</span></span>

<span data-ttu-id="99366-139">Während der Zugriff auf die meisten Eigenschaften vom Eigenschaftenbezeichner ist, können einige Eigenschaften namentlich zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="99366-139">While access to most properties is by property identifier, some properties can be accessed by name.</span></span> <span data-ttu-id="99366-140">Die **IMAPIProp::GetNamesFromIDs** -Methode kann aufgerufen werden, um Folgendes auszuführen:</span><span class="sxs-lookup"><span data-stu-id="99366-140">The **IMAPIProp::GetNamesFromIDs** method can be called to do the following:</span></span> 
  
- <span data-ttu-id="99366-141">Namen für bestimmte Eigenschaftenbezeichner in einer bestimmten Eigenschaft abrufen.</span><span class="sxs-lookup"><span data-stu-id="99366-141">Retrieve names for specific property identifiers in a specific property set.</span></span>
    
- <span data-ttu-id="99366-142">Namen für bestimmte Eigenschaftenbezeichner in einer Reihe Eigenschaft abrufen.</span><span class="sxs-lookup"><span data-stu-id="99366-142">Retrieve names for specific property identifiers in any property set.</span></span>
    
- <span data-ttu-id="99366-143">Abrufen von Namen für alle benannten Eigenschaften, die in das Objekt Zuordnung enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="99366-143">Retrieve names for all named properties that are included in the object's mapping.</span></span>
    
<span data-ttu-id="99366-144">Wenn _LppPropTags_ verweist auf eine gültige Eigenschaft Tag-Array mit mindestens einen Eigenschaftenbezeichner und _LpPropSetGuid_ verweist auf eine gültige Eigenschaft festlegen, ignoriert die Eigenschaft festgelegt und die Eigenschaftentypen und gibt die Namen aller **GetNamesFromIDs** die auf die angegebene Bezeichner zuordnen.</span><span class="sxs-lookup"><span data-stu-id="99366-144">If  _lppPropTags_ points to a valid property tag array with one or more property identifiers, and  _lpPropSetGuid_ points to a valid property set, **GetNamesFromIDs** ignores the property set and the property types and returns all of the names that map to the specified identifiers.</span></span> 
  
<span data-ttu-id="99366-145">Wenn _LppPropTags_ verweist auf eine gültige Eigenschaft Tag Array mit einem oder mehreren Eigenschaftenbezeichner und _LpPropSetGuid_ ist NULL, **GetNamesFromIDs** gibt alle Namen, die dem angegebenen Bezeichner zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="99366-145">If  _lppPropTags_ points to a valid property tag array with one or more property identifiers and  _lpPropSetGuid_ is NULL, **GetNamesFromIDs** returns all of the names that map to the specified identifiers.</span></span> 
  
<span data-ttu-id="99366-146">Wenn ein angegebenen Bezeichner keinen Namen, **GetNamesFromIDs** gibt NULL zurück, in diesem Bezeichner Stelle in der Struktur in _LpppPropNames_ zurückgegeben und gibt auch MAPI_W_ERRORS_RETURNED zurück.</span><span class="sxs-lookup"><span data-stu-id="99366-146">If a specified identifier does not have a name, **GetNamesFromIDs** returns NULL in that identifier's place in the structure returned in  _lpppPropNames_ and also returns MAPI_W_ERRORS_RETURNED.</span></span> 
  
<span data-ttu-id="99366-147">Wenn _LpPropSetGuid_ und _LppPropTags_ NULL sind, **GetNamesFromIDs** ordnet ein neues Eigenschaft Tag Array und gibt die Namen aller benannten Eigenschaften für das Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="99366-147">If both  _lpPropSetGuid_ and  _lppPropTags_ are NULL, **GetNamesFromIDs** allocates a new property tag array and returns all of the names for all of the named properties for the object.</span></span> 
  
<span data-ttu-id="99366-148">Wenn es keine Namen sind zurückgegeben werden soll, führt möglicherweise, weil keine Eigenschaften vorhanden, in dem angeforderten Eigenschaftensatz sind oder alle Eigenschaften eines Typs werden durch die Kennzeichen ausgeschlossen werden **GetNamesFromIDs** Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="99366-148">When there are no names to be returned, perhaps because there are no properties in the requested property set or all of the properties are of a type excluded by the flags, **GetNamesFromIDs** does the following:</span></span> 
  
- <span data-ttu-id="99366-149">Gibt S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="99366-149">Returns S_OK.</span></span>
    
- <span data-ttu-id="99366-150">Ordnet eine neue **SPropTagArray** -Struktur, wenn das Element **cValues** auf 0 festlegen.</span><span class="sxs-lookup"><span data-stu-id="99366-150">Allocates a new **SPropTagArray** structure, setting the **cValues** member to 0.</span></span> 
    
- <span data-ttu-id="99366-151">Der Inhalt des _LpcPropNames_ festgelegt auf 0.</span><span class="sxs-lookup"><span data-stu-id="99366-151">Sets the contents of  _lpcPropNames_ to 0.</span></span> 
    
- <span data-ttu-id="99366-152">Legt den Inhalt der _LpppPropNames_ auf NULL fest.</span><span class="sxs-lookup"><span data-stu-id="99366-152">Sets the contents of  _lpppPropNames_ to NULL.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="99366-153">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="99366-153">Notes to implementers</span></span>

<span data-ttu-id="99366-154">Wenn _LpPropSetGuid_ verweist auf einen gültigen Eigenschaftensatz und _LppPropTags_ NULL ist, ist das Ergebnis nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="99366-154">If  _lpPropSetGuid_ points to a valid property set and  _lppPropTags_ is NULL, the result is undefined.</span></span> <span data-ttu-id="99366-155">Sie können eine der folgenden Strategien verwenden:</span><span class="sxs-lookup"><span data-stu-id="99366-155">You can use one of the following strategies:</span></span> 
  
- <span data-ttu-id="99366-156">Ignorieren Sie die Eigenschaft festgelegt, und zurückgegeben Sie die Namen für den Bezeichner in Array der Tag-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="99366-156">Ignore the property set and return the names for the identifiers in the property tag array.</span></span>
    
- <span data-ttu-id="99366-157">Die Namen für die nur die Bezeichner in der Tag Array-Eigenschaft, die zu dem angegebenen Eigenschaftensatz gehören zurück.</span><span class="sxs-lookup"><span data-stu-id="99366-157">Return the names for only the identifiers in the property tag array that belong to the specified property set.</span></span>
    
- <span data-ttu-id="99366-158">Ein Fehler auf den Anruf MAPI_E_INVALID_PARAMETER zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="99366-158">Fail the call, returning MAPI_E_INVALID_PARAMETER.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="99366-159">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="99366-159">Notes to callers</span></span>

<span data-ttu-id="99366-160">Um alle benannten Eigenschaften für ein Objekt abzurufen, müssen Sie zunächst das Objekt [IMAPIProp::GetPropList](imapiprop-getproplist.md) -Methode aufrufen, und übergeben Sie den zurückgegebenen IDs, die über dem Bereich 0 x 8000 zu **GetNamesFromIDs**sind.</span><span class="sxs-lookup"><span data-stu-id="99366-160">To retrieve all of the named properties for an object, you must first call the object's [IMAPIProp::GetPropList](imapiprop-getproplist.md) method and then pass the returned identifiers that are above the 0x8000 range to **GetNamesFromIDs**.</span></span>
  
<span data-ttu-id="99366-161">Wenn Sie eine gültige Eigenschaft fest, jedoch keine gültige Eigenschaft Tag-Array übergeben, bereiten Sie für zu unvorhersehbaren Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="99366-161">If you pass a valid property set but not a valid property tag array, be prepared for unpredictable results.</span></span> <span data-ttu-id="99366-162">Einige Implementierungen von **GetNamesFromIDs** ignorieren die Eigenschaft festgelegt und die Namen für den Bezeichner in Array der Tag-Eigenschaft zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="99366-162">Some implementations of **GetNamesFromIDs** ignore the property set and return the names for the identifiers in the property tag array.</span></span> <span data-ttu-id="99366-163">Einige Implementierungen zurückgeben MAPI_E_INVALID_PARAMETER.</span><span class="sxs-lookup"><span data-stu-id="99366-163">Some implementations return MAPI_E_INVALID_PARAMETER.</span></span> <span data-ttu-id="99366-164">Implementierungen wird weiterhin Namen für die IDs aller Eigenschaften im Eigenschaftensatz zurück.</span><span class="sxs-lookup"><span data-stu-id="99366-164">Still other implementations return names for identifiers of all properties in the property set.</span></span> <span data-ttu-id="99366-165">Wenn der Eigenschaftensatz PS_PUBLIC_STRINGS ist, können **GetNamesFromIDs** alle Namen zurück, die jemals erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="99366-165">If the property set is PS_PUBLIC_STRINGS, **GetNamesFromIDs** can return all names that were ever created.</span></span> <span data-ttu-id="99366-166">Es ist, ob der Dienstanbieter, eine Eigenschaft unter den IDs der öffentlichen Zeichenfolgen zugeordnet speichert irrelevant.</span><span class="sxs-lookup"><span data-stu-id="99366-166">Whether the service provider stores a property under the identifiers associated with the public strings is immaterial.</span></span> 
  
<span data-ttu-id="99366-167">Wenn Sie mit den Eigenschaftennamen fertig sind, überprüfen Sie den Inhalt des Parameters _LpcPropNames_ , um zu bestimmen, ob alle Namen zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="99366-167">When you are finished with the property names, check the contents of the  _lpcPropNames_ parameter to determine whether any names were returned.</span></span> <span data-ttu-id="99366-168">Wenn dies der Fall ist, auf die Aufruf der [MAPIFreeBuffer](mapifreebuffer.md) -Funktion, um den Arbeitsspeicher freizugeben _LppPropTags_ und _LpppPropNames_ soll, wenn ein erfolgreiches Ergebnis zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="99366-168">If so, call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the memory pointed to by  _lppPropTags_ and  _lpppPropNames_ when a successful result is returned.</span></span> <span data-ttu-id="99366-169">Durch Aufrufen von **MAPIFreeBuffer** ist ausreichend für jeden Parameter. Sie müssen nicht das Array von Zeigern zu durchlaufen und jede **MAPINAMEID** Struktur einzeln frei.</span><span class="sxs-lookup"><span data-stu-id="99366-169">One call to **MAPIFreeBuffer** is sufficient for each parameter; you do not have to traverse the array of pointers and free each **MAPINAMEID** structure individually.</span></span> 
  
<span data-ttu-id="99366-170">Weitere Informationen zu benannten Eigenschaften finden Sie unter [MAPI-Eigenschaften mit dem Namen](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="99366-170">For more information about named properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="99366-171">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="99366-171">MFCMAPI reference</span></span>

<span data-ttu-id="99366-172">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="99366-172">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="99366-173">**Datei**</span><span class="sxs-lookup"><span data-stu-id="99366-173">**File**</span></span>|<span data-ttu-id="99366-174">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="99366-174">**Function**</span></span>|<span data-ttu-id="99366-175">**Comment**</span><span class="sxs-lookup"><span data-stu-id="99366-175">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="99366-176">SingleMAPIPropListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="99366-176">SingleMAPIPropListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="99366-177">CSingleMAPIPropListCtrl::FindAllNamedProps</span><span class="sxs-lookup"><span data-stu-id="99366-177">CSingleMAPIPropListCtrl::FindAllNamedProps</span></span>  <br/> |<span data-ttu-id="99366-178">MFCMAPI (engl.) verwendet die **IMAPIProp::GetNamesFromIDs** -Methode zum Nachschlagen von benannten Eigenschaften, die zuvor zugeordnet wurden.</span><span class="sxs-lookup"><span data-stu-id="99366-178">MFCMAPI uses the **IMAPIProp::GetNamesFromIDs** method to look up named properties that have previously been mapped.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="99366-179">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99366-179">See also</span></span>



[<span data-ttu-id="99366-180">GUID</span><span class="sxs-lookup"><span data-stu-id="99366-180">GUID</span></span>](guid.md)
  
[<span data-ttu-id="99366-181">IMAPIProp::GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="99366-181">IMAPIProp::GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md)
  
[<span data-ttu-id="99366-182">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="99366-182">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="99366-183">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="99366-183">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="99366-184">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="99366-184">MAPINAMEID</span></span>](mapinameid.md)
  
[<span data-ttu-id="99366-185">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="99366-185">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="99366-186">IMAPIProp: IUnknown</span><span class="sxs-lookup"><span data-stu-id="99366-186">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="99366-187">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="99366-187">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="99366-188">Benannte Eigenschaften MAPI</span><span class="sxs-lookup"><span data-stu-id="99366-188">MAPI Named Properties</span></span>](mapi-named-properties.md)
  
[<span data-ttu-id="99366-189">Verwenden von Makros zur Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="99366-189">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

