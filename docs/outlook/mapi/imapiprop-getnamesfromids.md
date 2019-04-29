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
# <a name="imapipropgetnamesfromids"></a><span data-ttu-id="413f9-103">IMAPIProp::GetNamesFromIDs</span><span class="sxs-lookup"><span data-stu-id="413f9-103">IMAPIProp::GetNamesFromIDs</span></span>

  
  
<span data-ttu-id="413f9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="413f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="413f9-105">Stellt die Eigenschaftennamen bereit, die einem oder mehreren Eigenschafts Bezeichnern entsprechen.</span><span class="sxs-lookup"><span data-stu-id="413f9-105">Provides the property names that correspond to one or more property identifiers.</span></span>
  
```cpp
HRESULT GetNamesFromIDs(
  LPSPropTagArray FAR * lppPropTags,
  LPGUID lpPropSetGuid,
  ULONG ulFlags,
  ULONG FAR * lpcPropNames,
  LPMAPINAMEID FAR * FAR * lpppPropNames
);
```

## <a name="parameters"></a><span data-ttu-id="413f9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="413f9-106">Parameters</span></span>

 <span data-ttu-id="413f9-107">_lppPropTags_</span><span class="sxs-lookup"><span data-stu-id="413f9-107">_lppPropTags_</span></span>
  
> <span data-ttu-id="413f9-108">[in, out] Bei der Eingabe ein Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die ein Array von Property-Tags enthält; andernfalls NULL, wodurch angegeben wird, dass alle Namen zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="413f9-108">[in, out] On input, a pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags; otherwise, NULL, indicating that all names should be returned.</span></span> <span data-ttu-id="413f9-109">Das **cValues** -Element für das Property-Tag-Array kann nicht 0 sein.</span><span class="sxs-lookup"><span data-stu-id="413f9-109">The **cValues** member for the property tag array cannot be 0.</span></span> <span data-ttu-id="413f9-110">Wenn _lppPropTags_ ein gültiger Zeiger auf der Eingabe ist, gibt **GetNamesFromIDs** die Namen der einzelnen Eigenschaftenbezeichner zurück, die im Array enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="413f9-110">If  _lppPropTags_ is a valid pointer on input, **GetNamesFromIDs** returns names for each property identifier included in the array.</span></span> 
    
 <span data-ttu-id="413f9-111">_lpPropSetGuid_</span><span class="sxs-lookup"><span data-stu-id="413f9-111">_lpPropSetGuid_</span></span>
  
> <span data-ttu-id="413f9-112">in Ein Zeiger auf eine GUID oder eine [GUID](guid.md) -Struktur, die einen Eigenschaftensatz identifiziert.</span><span class="sxs-lookup"><span data-stu-id="413f9-112">[in] A pointer to a GUID, or [GUID](guid.md) structure, that identifies a property set.</span></span> <span data-ttu-id="413f9-113">Der _lpPropSetGuid_ -Parameter kann auf einen gültigen Eigenschaftensatz verweisen oder NULL sein.</span><span class="sxs-lookup"><span data-stu-id="413f9-113">The  _lpPropSetGuid_ parameter can point to a valid property set or can be NULL.</span></span> 
    
 <span data-ttu-id="413f9-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="413f9-114">_ulFlags_</span></span>
  
> <span data-ttu-id="413f9-115">in Eine Bitmaske von Flags, die den Typ der zurückzugebenden Namen angibt.</span><span class="sxs-lookup"><span data-stu-id="413f9-115">[in] A bitmask of flags that indicates the type of names to be returned.</span></span> <span data-ttu-id="413f9-116">Die folgenden Flags können verwendet werden (wenn beide Flags festgelegt sind, werden keine Namen zurückgegeben):</span><span class="sxs-lookup"><span data-stu-id="413f9-116">The following flags can be used (if both flags are set, no names will be returned):</span></span>
    
<span data-ttu-id="413f9-117">MAPI_NO_IDS</span><span class="sxs-lookup"><span data-stu-id="413f9-117">MAPI_NO_IDS</span></span> 
  
> <span data-ttu-id="413f9-118">Fordert an, dass nur als Unicode-Zeichenfolgen gespeicherte Namen zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="413f9-118">Requests that only names stored as Unicode strings be returned.</span></span> 
    
<span data-ttu-id="413f9-119">MAPI_NO_STRINGS</span><span class="sxs-lookup"><span data-stu-id="413f9-119">MAPI_NO_STRINGS</span></span> 
  
> <span data-ttu-id="413f9-120">Fordert an, dass nur als numerische Bezeichner gespeicherte Namen zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="413f9-120">Requests that only names stored as numeric identifiers be returned.</span></span> 
    
 <span data-ttu-id="413f9-121">_lpcPropNames_</span><span class="sxs-lookup"><span data-stu-id="413f9-121">_lpcPropNames_</span></span>
  
> <span data-ttu-id="413f9-122">Out Ein Zeiger auf die Anzahl der Eigenschaftennamen Zeiger im Array, auf das durch den _lppPropNames_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="413f9-122">[out] A pointer to a count of the property name pointers in the array pointed to by the  _lppPropNames_ parameter.</span></span> 
    
 <span data-ttu-id="413f9-123">_lpppPropNames_</span><span class="sxs-lookup"><span data-stu-id="413f9-123">_lpppPropNames_</span></span>
  
> <span data-ttu-id="413f9-124">Out Ein Zeiger auf ein Array von Zeigern auf [MAPINAMEID](mapinameid.md) -Strukturen, die Eigenschaftsnamen enthalten.</span><span class="sxs-lookup"><span data-stu-id="413f9-124">[out] A pointer to an array of pointers to [MAPINAMEID](mapinameid.md) structures that contains property names.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="413f9-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="413f9-125">Return value</span></span>

<span data-ttu-id="413f9-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="413f9-126">S_OK</span></span> 
  
> <span data-ttu-id="413f9-127">Die Eigenschaftennamen wurden erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="413f9-127">The property names were successfully returned.</span></span> 
    
<span data-ttu-id="413f9-128">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="413f9-128">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="413f9-129">Das Objekt unterstützt keine benannten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="413f9-129">The object does not support named properties.</span></span> 
    
<span data-ttu-id="413f9-130">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="413f9-130">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="413f9-131">Der Aufruf war insgesamt erfolgreich, aber Namen für eine oder mehrere Eigenschaften konnten nicht zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="413f9-131">The call succeeded overall, but names for one or more properties could not be returned.</span></span> <span data-ttu-id="413f9-132">Die Eigenschaftstags für die fehlerhaften Eigenschaften haben den Eigenschaftentyp **PT_ERROR**.</span><span class="sxs-lookup"><span data-stu-id="413f9-132">The property tags for the failing properties have a property type of **PT_ERROR**.</span></span> <span data-ttu-id="413f9-133">Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="413f9-133">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="413f9-134">Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** -Makro.</span><span class="sxs-lookup"><span data-stu-id="413f9-134">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="413f9-135">Weitere Informationen finden Sie unter [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="413f9-135">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span> 
    
<span data-ttu-id="413f9-136">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="413f9-136">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="413f9-137">Das **cValues** -Element eines oder mehrerer der Einträge im Array der Eigenschaftentags, auf die von _lppPropTags_ verwiesen wird, ist auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="413f9-137">The **cValues** member of one or more of the entries in the property tag array pointed to by  _lppPropTags_ is set to 0.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="413f9-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="413f9-138">Remarks</span></span>

<span data-ttu-id="413f9-139">Während der Zugriff auf die meisten Eigenschaften durch die Eigenschaftskennung erfolgt, können auf einige Eigenschaften über den Namen zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="413f9-139">While access to most properties is by property identifier, some properties can be accessed by name.</span></span> <span data-ttu-id="413f9-140">Die **IMAPIProp:: GetNamesFromIDs** -Methode kann aufgerufen werden, um folgende Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="413f9-140">The **IMAPIProp::GetNamesFromIDs** method can be called to do the following:</span></span> 
  
- <span data-ttu-id="413f9-141">Ruft Namen für bestimmte Eigenschaftenbezeichner in einem bestimmten Eigenschaftensatz ab.</span><span class="sxs-lookup"><span data-stu-id="413f9-141">Retrieve names for specific property identifiers in a specific property set.</span></span>
    
- <span data-ttu-id="413f9-142">Ruft Namen für bestimmte Eigenschaftenbezeichner in einem beliebigen Eigenschaftensatz ab.</span><span class="sxs-lookup"><span data-stu-id="413f9-142">Retrieve names for specific property identifiers in any property set.</span></span>
    
- <span data-ttu-id="413f9-143">Ruft Namen für alle benannten Eigenschaften ab, die in der Zuordnung des Objekts enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="413f9-143">Retrieve names for all named properties that are included in the object's mapping.</span></span>
    
<span data-ttu-id="413f9-144">Wenn _lppPropTags_ auf ein gültiges Property-Tag-Array mit einem oder mehreren Property Identifiers zeigt und _lpPropSetGuid_ auf einen gültigen Eigenschaftensatz zeigt, ignoriert **GetNamesFromIDs** den Eigenschaftensatz und die Eigenschaftentypen und gibt alle Namen zurück. , die den angegebenen Bezeichnern zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="413f9-144">If  _lppPropTags_ points to a valid property tag array with one or more property identifiers, and  _lpPropSetGuid_ points to a valid property set, **GetNamesFromIDs** ignores the property set and the property types and returns all of the names that map to the specified identifiers.</span></span> 
  
<span data-ttu-id="413f9-145">Wenn _lppPropTags_ auf ein gültiges Property-Tag-Array mit einem oder mehreren Property Identifiers zeigt und _LPPROPSETGUID_ den Wert NULL hat, gibt **GetNamesFromIDs** alle Namen zurück, die den angegebenen Bezeichnern zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="413f9-145">If  _lppPropTags_ points to a valid property tag array with one or more property identifiers and  _lpPropSetGuid_ is NULL, **GetNamesFromIDs** returns all of the names that map to the specified identifiers.</span></span> 
  
<span data-ttu-id="413f9-146">Wenn ein angegebener Bezeichner keinen Namen hat, gibt **GetNamesFromIDs** in der in _lpppPropNames_ zurückgegebenen Struktur NULL an der Stelle des Bezeichners zurück und gibt auch MAPI_W_ERRORS_RETURNED zurück.</span><span class="sxs-lookup"><span data-stu-id="413f9-146">If a specified identifier does not have a name, **GetNamesFromIDs** returns NULL in that identifier's place in the structure returned in  _lpppPropNames_ and also returns MAPI_W_ERRORS_RETURNED.</span></span> 
  
<span data-ttu-id="413f9-147">Wenn sowohl _lpPropSetGuid_ als auch _lppPropTags_ NULL sind, weist **GetNamesFromIDs** ein neues Property-Tag-Array zu und gibt alle Namen für alle benannten Eigenschaften für das Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="413f9-147">If both  _lpPropSetGuid_ and  _lppPropTags_ are NULL, **GetNamesFromIDs** allocates a new property tag array and returns all of the names for all of the named properties for the object.</span></span> 
  
<span data-ttu-id="413f9-148">Wenn keine Namen zurückgegeben werden sollen, möglicherweise, da keine Eigenschaften im angeforderten Eigenschaftensatz vorhanden sind oder alle Eigenschaften einen Typ aufweisen, der durch die Flags ausgeschlossen ist, führt **GetNamesFromIDs** Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="413f9-148">When there are no names to be returned, perhaps because there are no properties in the requested property set or all of the properties are of a type excluded by the flags, **GetNamesFromIDs** does the following:</span></span> 
  
- <span data-ttu-id="413f9-149">Gibt S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="413f9-149">Returns S_OK.</span></span>
    
- <span data-ttu-id="413f9-150">Weist eine neue **SPropTagArray** -Struktur zu, wobei das **cValues** -Element auf 0 festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="413f9-150">Allocates a new **SPropTagArray** structure, setting the **cValues** member to 0.</span></span> 
    
- <span data-ttu-id="413f9-151">Legt den Inhalt von _lpcPropNames_ auf 0 fest.</span><span class="sxs-lookup"><span data-stu-id="413f9-151">Sets the contents of  _lpcPropNames_ to 0.</span></span> 
    
- <span data-ttu-id="413f9-152">Legt den Inhalt von _lpppPropNames_ auf NULL fest.</span><span class="sxs-lookup"><span data-stu-id="413f9-152">Sets the contents of  _lpppPropNames_ to NULL.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="413f9-153">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="413f9-153">Notes to implementers</span></span>

<span data-ttu-id="413f9-154">Wenn _lpPropSetGuid_ auf einen gültigen Eigenschaftensatz verweist und _LPPPROPTAGS_ den Wert NULL hat, ist das Ergebnis nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="413f9-154">If  _lpPropSetGuid_ points to a valid property set and  _lppPropTags_ is NULL, the result is undefined.</span></span> <span data-ttu-id="413f9-155">Sie können eine der folgenden Strategien verwenden:</span><span class="sxs-lookup"><span data-stu-id="413f9-155">You can use one of the following strategies:</span></span> 
  
- <span data-ttu-id="413f9-156">Ignorieren Sie den Eigenschaftensatz, und geben Sie die Namen der Bezeichner im Property-Tag-Array zurück.</span><span class="sxs-lookup"><span data-stu-id="413f9-156">Ignore the property set and return the names for the identifiers in the property tag array.</span></span>
    
- <span data-ttu-id="413f9-157">Gibt die Namen nur für die Bezeichner im Property-Tag-Array zurück, die zum angegebenen Eigenschaftensatz gehören.</span><span class="sxs-lookup"><span data-stu-id="413f9-157">Return the names for only the identifiers in the property tag array that belong to the specified property set.</span></span>
    
- <span data-ttu-id="413f9-158">Fehlschlagen des Anrufs, zurückgeben von MAPI_E_INVALID_PARAMETER.</span><span class="sxs-lookup"><span data-stu-id="413f9-158">Fail the call, returning MAPI_E_INVALID_PARAMETER.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="413f9-159">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="413f9-159">Notes to callers</span></span>

<span data-ttu-id="413f9-160">Wenn Sie alle benannten Eigenschaften für ein Objekt abrufen möchten, müssen Sie zuerst die [IMAPIProp::](imapiprop-getproplist.md) getproplist-Methode des Objekts aufrufen und dann die zurückgegebenen Bezeichner über dem 0X8000-Range an **GetNamesFromIDs**.</span><span class="sxs-lookup"><span data-stu-id="413f9-160">To retrieve all of the named properties for an object, you must first call the object's [IMAPIProp::GetPropList](imapiprop-getproplist.md) method and then pass the returned identifiers that are above the 0x8000 range to **GetNamesFromIDs**.</span></span>
  
<span data-ttu-id="413f9-161">Wenn Sie einen gültigen Eigenschaftensatz, aber keinen gültigen Property-Tag-Array, werden auf unvorhersehbare Ergebnisse vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="413f9-161">If you pass a valid property set but not a valid property tag array, be prepared for unpredictable results.</span></span> <span data-ttu-id="413f9-162">Bei einigen Implementierungen von **GetNamesFromIDs** wird der Eigenschaftensatz ignoriert und die Namen der Bezeichner im Property-Tag-Array zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="413f9-162">Some implementations of **GetNamesFromIDs** ignore the property set and return the names for the identifiers in the property tag array.</span></span> <span data-ttu-id="413f9-163">Einige Implementierungen geben MAPI_E_INVALID_PARAMETER zurück.</span><span class="sxs-lookup"><span data-stu-id="413f9-163">Some implementations return MAPI_E_INVALID_PARAMETER.</span></span> <span data-ttu-id="413f9-164">Weitere Implementierungen geben Namen für Bezeichner aller Eigenschaften im Eigenschaftensatz zurück.</span><span class="sxs-lookup"><span data-stu-id="413f9-164">Still other implementations return names for identifiers of all properties in the property set.</span></span> <span data-ttu-id="413f9-165">Wenn der Eigenschaftensatz PS_PUBLIC_STRINGS ist, kann **GetNamesFromIDs** alle Namen zurückgeben, die jemals erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="413f9-165">If the property set is PS_PUBLIC_STRINGS, **GetNamesFromIDs** can return all names that were ever created.</span></span> <span data-ttu-id="413f9-166">Ob der Dienstanbieter eine Eigenschaft unter den mit den öffentlichen Zeichenfolgen verknüpften Bezeichnern speichert, ist unerheblich.</span><span class="sxs-lookup"><span data-stu-id="413f9-166">Whether the service provider stores a property under the identifiers associated with the public strings is immaterial.</span></span> 
  
<span data-ttu-id="413f9-167">Wenn Sie die Eigenschaftennamen beendet haben, überprüfen Sie den Inhalt des _lpcPropNames_ -Parameters, um zu bestimmen, ob Namen zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="413f9-167">When you are finished with the property names, check the contents of the  _lpcPropNames_ parameter to determine whether any names were returned.</span></span> <span data-ttu-id="413f9-168">Wenn dies der Fall ist, rufen Sie die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion auf, um den Arbeitsspeicher freizugeben, auf den von _lppPropTags_ und _lpppPropNames_ verwiesen wird, wenn ein erfolgreiches Ergebnis zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="413f9-168">If so, call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the memory pointed to by  _lppPropTags_ and  _lpppPropNames_ when a successful result is returned.</span></span> <span data-ttu-id="413f9-169">Ein Aufruf von **mapifreebufferfreigegeben** ist für jeden Parameter ausreichend; Sie müssen nicht das Array von Zeigern durchlaufen und jede **MAPINAMEID** -Struktur einzeln freigeben.</span><span class="sxs-lookup"><span data-stu-id="413f9-169">One call to **MAPIFreeBuffer** is sufficient for each parameter; you do not have to traverse the array of pointers and free each **MAPINAMEID** structure individually.</span></span> 
  
<span data-ttu-id="413f9-170">Weitere Informationen zu benannten Eigenschaften finden Sie unter [MAPI Named Properties](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="413f9-170">For more information about named properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="413f9-171">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="413f9-171">MFCMAPI reference</span></span>

<span data-ttu-id="413f9-172">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="413f9-172">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="413f9-173">**Datei**</span><span class="sxs-lookup"><span data-stu-id="413f9-173">**File**</span></span>|<span data-ttu-id="413f9-174">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="413f9-174">**Function**</span></span>|<span data-ttu-id="413f9-175">**Comment**</span><span class="sxs-lookup"><span data-stu-id="413f9-175">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="413f9-176">SingleMAPIPropListCtrl. cpp</span><span class="sxs-lookup"><span data-stu-id="413f9-176">SingleMAPIPropListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="413f9-177">CSingleMAPIPropListCtrl:: FindAllNamedProps</span><span class="sxs-lookup"><span data-stu-id="413f9-177">CSingleMAPIPropListCtrl::FindAllNamedProps</span></span>  <br/> |<span data-ttu-id="413f9-178">MFCMAPI verwendet die **IMAPIProp:: GetNamesFromIDs** -Methode, um benannte Eigenschaften nachzuschlagen, die zuvor zugeordnet wurden.</span><span class="sxs-lookup"><span data-stu-id="413f9-178">MFCMAPI uses the **IMAPIProp::GetNamesFromIDs** method to look up named properties that have previously been mapped.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="413f9-179">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="413f9-179">See also</span></span>



[<span data-ttu-id="413f9-180">GUID</span><span class="sxs-lookup"><span data-stu-id="413f9-180">GUID</span></span>](guid.md)
  
[<span data-ttu-id="413f9-181">IMAPIProp::GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="413f9-181">IMAPIProp::GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md)
  
[<span data-ttu-id="413f9-182">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="413f9-182">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="413f9-183">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="413f9-183">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="413f9-184">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="413f9-184">MAPINAMEID</span></span>](mapinameid.md)
  
[<span data-ttu-id="413f9-185">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="413f9-185">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="413f9-186">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="413f9-186">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="413f9-187">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="413f9-187">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="413f9-188">Benannte Eigenschaften MAPI</span><span class="sxs-lookup"><span data-stu-id="413f9-188">MAPI Named Properties</span></span>](mapi-named-properties.md)
  
[<span data-ttu-id="413f9-189">Verwenden von Makros zur Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="413f9-189">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

