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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f6688afde9b36a7722eaaf768f091481c15b7308
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423573"
---
# <a name="imapipropgetnamesfromids"></a><span data-ttu-id="cf378-103">IMAPIProp::GetNamesFromIDs</span><span class="sxs-lookup"><span data-stu-id="cf378-103">IMAPIProp::GetNamesFromIDs</span></span>

  
  
<span data-ttu-id="cf378-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf378-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf378-105">Stellt die Eigenschaftsnamen zur Verfügung, die einem oder mehreren Eigenschaftsbezeichnern entsprechen.</span><span class="sxs-lookup"><span data-stu-id="cf378-105">Provides the property names that correspond to one or more property identifiers.</span></span>
  
```cpp
HRESULT GetNamesFromIDs(
  LPSPropTagArray FAR * lppPropTags,
  LPGUID lpPropSetGuid,
  ULONG ulFlags,
  ULONG FAR * lpcPropNames,
  LPMAPINAMEID FAR * FAR * lpppPropNames
);
```

## <a name="parameters"></a><span data-ttu-id="cf378-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf378-106">Parameters</span></span>

 <span data-ttu-id="cf378-107">_lppPropTags_</span><span class="sxs-lookup"><span data-stu-id="cf378-107">_lppPropTags_</span></span>
  
> <span data-ttu-id="cf378-108">[in, out] Bei der Eingabe ein Zeiger auf eine [SPropTagArray-Struktur,](sproptagarray.md) die ein Array von Eigenschaftstags enthält. Andernfalls NULL, der angibt, dass alle Namen zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cf378-108">[in, out] On input, a pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags; otherwise, NULL, indicating that all names should be returned.</span></span> <span data-ttu-id="cf378-109">Das **cValues-Element** für das Eigenschaftentagarray darf nicht 0 sein.</span><span class="sxs-lookup"><span data-stu-id="cf378-109">The **cValues** member for the property tag array cannot be 0.</span></span> <span data-ttu-id="cf378-110">Wenn  _lppPropTags_ ein gültiger Zeiger für die Eingabe ist, gibt **GetNamesFromIDs** Namen für jeden Eigenschaftenbezeichner zurück, der im Array enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="cf378-110">If  _lppPropTags_ is a valid pointer on input, **GetNamesFromIDs** returns names for each property identifier included in the array.</span></span> 
    
 <span data-ttu-id="cf378-111">_lpPropSetGuid_</span><span class="sxs-lookup"><span data-stu-id="cf378-111">_lpPropSetGuid_</span></span>
  
> <span data-ttu-id="cf378-112">[in] Ein Zeiger auf eine GUID oder [GUID-Struktur,](guid.md) die einen Eigenschaftensatz identifiziert.</span><span class="sxs-lookup"><span data-stu-id="cf378-112">[in] A pointer to a GUID, or [GUID](guid.md) structure, that identifies a property set.</span></span> <span data-ttu-id="cf378-113">Der  _lpPropSetGuid-Parameter_ kann auf einen gültigen Eigenschaftensatz oder NULL verweisen.</span><span class="sxs-lookup"><span data-stu-id="cf378-113">The  _lpPropSetGuid_ parameter can point to a valid property set or can be NULL.</span></span> 
    
 <span data-ttu-id="cf378-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cf378-114">_ulFlags_</span></span>
  
> <span data-ttu-id="cf378-115">[in] Eine Bitmaske mit Flags, die den Typ der zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="cf378-115">[in] A bitmask of flags that indicates the type of names to be returned.</span></span> <span data-ttu-id="cf378-116">Die folgenden Flags können verwendet werden (wenn beide Flags festgelegt sind, werden keine Namen zurückgegeben):</span><span class="sxs-lookup"><span data-stu-id="cf378-116">The following flags can be used (if both flags are set, no names will be returned):</span></span>
    
<span data-ttu-id="cf378-117">MAPI_NO_IDS</span><span class="sxs-lookup"><span data-stu-id="cf378-117">MAPI_NO_IDS</span></span> 
  
> <span data-ttu-id="cf378-118">Anforderungen, dass nur Als Unicode-Zeichenfolgen gespeicherte Namen zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cf378-118">Requests that only names stored as Unicode strings be returned.</span></span> 
    
<span data-ttu-id="cf378-119">MAPI_NO_STRINGS</span><span class="sxs-lookup"><span data-stu-id="cf378-119">MAPI_NO_STRINGS</span></span> 
  
> <span data-ttu-id="cf378-120">Anforderungen, dass nur Namen zurückgegeben werden, die als numerische Bezeichner gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="cf378-120">Requests that only names stored as numeric identifiers be returned.</span></span> 
    
 <span data-ttu-id="cf378-121">_lpcPropNames_</span><span class="sxs-lookup"><span data-stu-id="cf378-121">_lpcPropNames_</span></span>
  
> <span data-ttu-id="cf378-122">[out] Ein Zeiger auf eine Anzahl der Eigenschaftsnamenzeiger im Array, auf die der  _lppPropNames-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="cf378-122">[out] A pointer to a count of the property name pointers in the array pointed to by the  _lppPropNames_ parameter.</span></span> 
    
 <span data-ttu-id="cf378-123">_lpppPropNames_</span><span class="sxs-lookup"><span data-stu-id="cf378-123">_lpppPropNames_</span></span>
  
> <span data-ttu-id="cf378-124">[out] Ein Zeiger auf ein Array von Zeigern auf [MAPINAMEID-Strukturen,](mapinameid.md) die Eigenschaftsnamen enthalten.</span><span class="sxs-lookup"><span data-stu-id="cf378-124">[out] A pointer to an array of pointers to [MAPINAMEID](mapinameid.md) structures that contains property names.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="cf378-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cf378-125">Return value</span></span>

<span data-ttu-id="cf378-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="cf378-126">S_OK</span></span> 
  
> <span data-ttu-id="cf378-127">Die Eigenschaftsnamen wurden erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cf378-127">The property names were successfully returned.</span></span> 
    
<span data-ttu-id="cf378-128">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="cf378-128">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="cf378-129">Das Objekt unterstützt keine benannten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cf378-129">The object does not support named properties.</span></span> 
    
<span data-ttu-id="cf378-130">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="cf378-130">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="cf378-131">Der Aufruf war insgesamt erfolgreich, namen für eine oder mehrere Eigenschaften konnten jedoch nicht zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cf378-131">The call succeeded overall, but names for one or more properties could not be returned.</span></span> <span data-ttu-id="cf378-132">Die Eigenschaftstags für die fehlerhaften Eigenschaften haben den Eigenschaftentyp **PT_ERROR**.</span><span class="sxs-lookup"><span data-stu-id="cf378-132">The property tags for the failing properties have a property type of **PT_ERROR**.</span></span> <span data-ttu-id="cf378-133">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="cf378-133">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="cf378-134">Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** Makro.</span><span class="sxs-lookup"><span data-stu-id="cf378-134">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="cf378-135">Weitere Informationen finden Sie unter [Using Macros for Error Handling](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="cf378-135">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span> 
    
<span data-ttu-id="cf378-136">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="cf378-136">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="cf378-137">Das **cValues-Element** eines oder mehreren Einträgen im Eigenschaftentagarray, auf das  _von lppPropTags_ verwiesen wird, ist auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cf378-137">The **cValues** member of one or more of the entries in the property tag array pointed to by  _lppPropTags_ is set to 0.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="cf378-138">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cf378-138">Remarks</span></span>

<span data-ttu-id="cf378-139">Während der Zugriff auf die meisten Eigenschaften über den Eigenschaftenbezeichner festgelegt ist, kann auf einige Eigenschaften über den Namen zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="cf378-139">While access to most properties is by property identifier, some properties can be accessed by name.</span></span> <span data-ttu-id="cf378-140">Die **IMAPIProp::GetNamesFromIDs-Methode** kann aufgerufen werden, um die folgenden Schritte zu tun:</span><span class="sxs-lookup"><span data-stu-id="cf378-140">The **IMAPIProp::GetNamesFromIDs** method can be called to do the following:</span></span> 
  
- <span data-ttu-id="cf378-141">Ruft Namen für bestimmte Eigenschaftenbezeichner in einem bestimmten Eigenschaftensatz ab.</span><span class="sxs-lookup"><span data-stu-id="cf378-141">Retrieve names for specific property identifiers in a specific property set.</span></span>
    
- <span data-ttu-id="cf378-142">Rufen Sie Namen für bestimmte Eigenschaftenbezeichner in einem beliebigen Eigenschaftensatz ab.</span><span class="sxs-lookup"><span data-stu-id="cf378-142">Retrieve names for specific property identifiers in any property set.</span></span>
    
- <span data-ttu-id="cf378-143">Ruft Namen für alle benannten Eigenschaften ab, die in der Zuordnung des Objekts enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="cf378-143">Retrieve names for all named properties that are included in the object's mapping.</span></span>
    
<span data-ttu-id="cf378-144">Wenn  _lppPropTags_ auf ein gültiges Eigenschaftstagarray mit einem oder mehreren Eigenschaftsbezeichnern zeigt und  _lpPropSetGuid_ auf einen gültigen Eigenschaftensatz verweist, ignoriert **GetNamesFromIDs** den Eigenschaftensatz und die Eigenschaftstypen und gibt alle Namen zurück, die den angegebenen Bezeichnern zuordnungen.</span><span class="sxs-lookup"><span data-stu-id="cf378-144">If  _lppPropTags_ points to a valid property tag array with one or more property identifiers, and  _lpPropSetGuid_ points to a valid property set, **GetNamesFromIDs** ignores the property set and the property types and returns all of the names that map to the specified identifiers.</span></span> 
  
<span data-ttu-id="cf378-145">Wenn  _lppPropTags_ auf ein gültiges Eigenschaftstagarray mit mindestens einem Eigenschaftsbezeichner verweist und  _lpPropSetGuid_ NULL ist, gibt **GetNamesFromIDs** alle Namen zurück, die den angegebenen Bezeichnern zuordnungen.</span><span class="sxs-lookup"><span data-stu-id="cf378-145">If  _lppPropTags_ points to a valid property tag array with one or more property identifiers and  _lpPropSetGuid_ is NULL, **GetNamesFromIDs** returns all of the names that map to the specified identifiers.</span></span> 
  
<span data-ttu-id="cf378-146">Wenn ein angegebener Bezeichner keinen Namen hat, gibt **GetNamesFromIDs** NULL an der Stelle dieses Bezeichners in der Struktur zurück, die in  _lpppPropNames_ zurückgegeben wird, und gibt auch MAPI_W_ERRORS_RETURNED.</span><span class="sxs-lookup"><span data-stu-id="cf378-146">If a specified identifier does not have a name, **GetNamesFromIDs** returns NULL in that identifier's place in the structure returned in  _lpppPropNames_ and also returns MAPI_W_ERRORS_RETURNED.</span></span> 
  
<span data-ttu-id="cf378-147">Wenn  _lpPropSetGuid_ und  _lppPropTags_ NULL sind, weist **GetNamesFromIDs** ein neues Eigenschaftentagarray zu und gibt alle Namen für alle benannten Eigenschaften für das Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="cf378-147">If both  _lpPropSetGuid_ and  _lppPropTags_ are NULL, **GetNamesFromIDs** allocates a new property tag array and returns all of the names for all of the named properties for the object.</span></span> 
  
<span data-ttu-id="cf378-148">Wenn keine Namen zurückgegeben werden sollen, möglicherweise weil keine Eigenschaften im angeforderten Eigenschaftensatz enthalten sind oder alle Eigenschaften von einem Typ sind, der von den Flags ausgeschlossen wird, führt **GetNamesFromIDs** die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="cf378-148">When there are no names to be returned, perhaps because there are no properties in the requested property set or all of the properties are of a type excluded by the flags, **GetNamesFromIDs** does the following:</span></span> 
  
- <span data-ttu-id="cf378-149">Gibt S_OK.</span><span class="sxs-lookup"><span data-stu-id="cf378-149">Returns S_OK.</span></span>
    
- <span data-ttu-id="cf378-150">Weist eine neue **SPropTagArray-Struktur** zu, und das **cValues-Element** wird auf 0 festlegen.</span><span class="sxs-lookup"><span data-stu-id="cf378-150">Allocates a new **SPropTagArray** structure, setting the **cValues** member to 0.</span></span> 
    
- <span data-ttu-id="cf378-151">Legt den Inhalt von  _lpcPropNames auf_ 0 fest.</span><span class="sxs-lookup"><span data-stu-id="cf378-151">Sets the contents of  _lpcPropNames_ to 0.</span></span> 
    
- <span data-ttu-id="cf378-152">Legt den Inhalt von  _lpppPropNames auf_ NULL fest.</span><span class="sxs-lookup"><span data-stu-id="cf378-152">Sets the contents of  _lpppPropNames_ to NULL.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="cf378-153">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="cf378-153">Notes to implementers</span></span>

<span data-ttu-id="cf378-154">Wenn  _lpPropSetGuid_ auf einen gültigen Eigenschaftensatz verweist und  _lppPropTags_ null ist, ist das Ergebnis nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="cf378-154">If  _lpPropSetGuid_ points to a valid property set and  _lppPropTags_ is NULL, the result is undefined.</span></span> <span data-ttu-id="cf378-155">Sie können eine der folgenden Strategien verwenden:</span><span class="sxs-lookup"><span data-stu-id="cf378-155">You can use one of the following strategies:</span></span> 
  
- <span data-ttu-id="cf378-156">Ignorieren Sie den Eigenschaftensatz, und geben Sie die Namen für die Bezeichner im Eigenschaftentagarray zurück.</span><span class="sxs-lookup"><span data-stu-id="cf378-156">Ignore the property set and return the names for the identifiers in the property tag array.</span></span>
    
- <span data-ttu-id="cf378-157">Geben Sie die Namen nur für die Bezeichner im Eigenschaftentagarray zurück, die zum angegebenen Eigenschaftensatz gehören.</span><span class="sxs-lookup"><span data-stu-id="cf378-157">Return the names for only the identifiers in the property tag array that belong to the specified property set.</span></span>
    
- <span data-ttu-id="cf378-158">Führen Sie einen Fehler beim Anruf aus, und MAPI_E_INVALID_PARAMETER.</span><span class="sxs-lookup"><span data-stu-id="cf378-158">Fail the call, returning MAPI_E_INVALID_PARAMETER.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="cf378-159">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="cf378-159">Notes to callers</span></span>

<span data-ttu-id="cf378-160">Zum Abrufen aller benannten Eigenschaften für ein Objekt müssen Sie zuerst die [IMAPIProp::GetPropList-Methode](imapiprop-getproplist.md) des Objekts aufrufen und dann die zurückgegebenen Bezeichner, die sich über dem 0x8000-Bereich befinden, an **GetNamesFromIDs übergeben.**</span><span class="sxs-lookup"><span data-stu-id="cf378-160">To retrieve all of the named properties for an object, you must first call the object's [IMAPIProp::GetPropList](imapiprop-getproplist.md) method and then pass the returned identifiers that are above the 0x8000 range to **GetNamesFromIDs**.</span></span>
  
<span data-ttu-id="cf378-161">Wenn Sie einen gültigen Eigenschaftensatz, aber kein gültiges Eigenschaftstagarray übergeben, sollten Sie auf unvorhersehbare Ergebnisse vorbereitet sein.</span><span class="sxs-lookup"><span data-stu-id="cf378-161">If you pass a valid property set but not a valid property tag array, be prepared for unpredictable results.</span></span> <span data-ttu-id="cf378-162">Einige Implementierungen von **GetNamesFromIDs** ignorieren den Eigenschaftensatz und geben die Namen für die Bezeichner im Eigenschaftentagarray zurück.</span><span class="sxs-lookup"><span data-stu-id="cf378-162">Some implementations of **GetNamesFromIDs** ignore the property set and return the names for the identifiers in the property tag array.</span></span> <span data-ttu-id="cf378-163">Einige Implementierungen geben MAPI_E_INVALID_PARAMETER.</span><span class="sxs-lookup"><span data-stu-id="cf378-163">Some implementations return MAPI_E_INVALID_PARAMETER.</span></span> <span data-ttu-id="cf378-164">Auch andere Implementierungen geben Namen für Bezeichner aller Eigenschaften im Eigenschaftensatz zurück.</span><span class="sxs-lookup"><span data-stu-id="cf378-164">Still other implementations return names for identifiers of all properties in the property set.</span></span> <span data-ttu-id="cf378-165">Wenn der Eigenschaftensatz PS_PUBLIC_STRINGS, **kann GetNamesFromIDs** alle Namen zurückgeben, die jemals erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="cf378-165">If the property set is PS_PUBLIC_STRINGS, **GetNamesFromIDs** can return all names that were ever created.</span></span> <span data-ttu-id="cf378-166">Ob der Dienstanbieter eine Eigenschaft unter den den öffentlichen Zeichenfolgen zugeordneten Bezeichnern speichert, ist unerheblich.</span><span class="sxs-lookup"><span data-stu-id="cf378-166">Whether the service provider stores a property under the identifiers associated with the public strings is immaterial.</span></span> 
  
<span data-ttu-id="cf378-167">Wenn Sie mit den Eigenschaftennamen fertig sind, überprüfen Sie den Inhalt des  _lpcPropNames-Parameters,_ um zu ermitteln, ob Namen zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="cf378-167">When you are finished with the property names, check the contents of the  _lpcPropNames_ parameter to determine whether any names were returned.</span></span> <span data-ttu-id="cf378-168">Wenn ja, rufen Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) auf, um den Arbeitsspeicher frei zu machen, auf den  _lppPropTags_ und  _lpppPropNames_ zeigen, wenn ein erfolgreiches Ergebnis zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cf378-168">If so, call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the memory pointed to by  _lppPropTags_ and  _lpppPropNames_ when a successful result is returned.</span></span> <span data-ttu-id="cf378-169">Ein Aufruf von **MAPIFreeBuffer** ist für jeden Parameter ausreichend. Sie müssen nicht das Array von Zeigern durchlaufen und jede **MAPINAMEID-Struktur** einzeln frei geben.</span><span class="sxs-lookup"><span data-stu-id="cf378-169">One call to **MAPIFreeBuffer** is sufficient for each parameter; you do not have to traverse the array of pointers and free each **MAPINAMEID** structure individually.</span></span> 
  
<span data-ttu-id="cf378-170">Weitere Informationen zu benannten Eigenschaften finden Sie unter [MAPI Named Properties](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="cf378-170">For more information about named properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="cf378-171">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="cf378-171">MFCMAPI reference</span></span>

<span data-ttu-id="cf378-172">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="cf378-172">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="cf378-173">**Datei**</span><span class="sxs-lookup"><span data-stu-id="cf378-173">**File**</span></span>|<span data-ttu-id="cf378-174">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="cf378-174">**Function**</span></span>|<span data-ttu-id="cf378-175">**Comment**</span><span class="sxs-lookup"><span data-stu-id="cf378-175">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cf378-176">SingleMAPIPropListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="cf378-176">SingleMAPIPropListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="cf378-177">CSingleMAPIPropListCtrl::FindAllNamedProps</span><span class="sxs-lookup"><span data-stu-id="cf378-177">CSingleMAPIPropListCtrl::FindAllNamedProps</span></span>  <br/> |<span data-ttu-id="cf378-178">MFCMAPI verwendet die **IMAPIProp::GetNamesFromIDs-Methode,** um benannte Eigenschaften nach zu suchen, die zuvor zugeordnet wurden.</span><span class="sxs-lookup"><span data-stu-id="cf378-178">MFCMAPI uses the **IMAPIProp::GetNamesFromIDs** method to look up named properties that have previously been mapped.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cf378-179">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf378-179">See also</span></span>



[<span data-ttu-id="cf378-180">GUID</span><span class="sxs-lookup"><span data-stu-id="cf378-180">GUID</span></span>](guid.md)
  
[<span data-ttu-id="cf378-181">IMAPIProp::GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="cf378-181">IMAPIProp::GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md)
  
[<span data-ttu-id="cf378-182">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="cf378-182">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="cf378-183">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="cf378-183">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="cf378-184">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="cf378-184">MAPINAMEID</span></span>](mapinameid.md)
  
[<span data-ttu-id="cf378-185">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="cf378-185">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="cf378-186">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cf378-186">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="cf378-187">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="cf378-187">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="cf378-188">Benannte Eigenschaften MAPI</span><span class="sxs-lookup"><span data-stu-id="cf378-188">MAPI Named Properties</span></span>](mapi-named-properties.md)
  
[<span data-ttu-id="cf378-189">Verwenden von Makros für die Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="cf378-189">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

