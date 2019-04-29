---
title: IMAPIPropGetIDsFromNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetIDsFromNames
api_type:
- COM
ms.assetid: e3f501a4-a8ee-43d7-bd83-c94e7980c398
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 28880b818bc80e31cae0c695d4aac92eb9555cac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433584"
---
# <a name="imapipropgetidsfromnames"></a><span data-ttu-id="02871-103">IMAPIProp::GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="02871-103">IMAPIProp::GetIDsFromNames</span></span>

  
  
<span data-ttu-id="02871-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="02871-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="02871-105">Stellt die Eigenschaftenbezeichner bereit, die einem oder mehreren Eigenschaftsnamen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="02871-105">Provides the property identifiers that correspond to one or more property names.</span></span>
  
```cpp
HRESULT GetIDsFromNames(
  ULONG cPropNames,
  LPMAPINAMEID FAR * lppPropNames,
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTags
);
```

## <a name="parameters"></a><span data-ttu-id="02871-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="02871-106">Parameters</span></span>

 <span data-ttu-id="02871-107">_cPropNames_</span><span class="sxs-lookup"><span data-stu-id="02871-107">_cPropNames_</span></span>
  
> <span data-ttu-id="02871-108">in Die Anzahl der Eigenschaftennamen, auf die durch den _lppPropNames_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="02871-108">[in] The count of property names pointed to by the  _lppPropNames_ parameter.</span></span> <span data-ttu-id="02871-109">Wenn _lppPropNames_ ist, muss der Parameter _cPropNames_ 0 sein.</span><span class="sxs-lookup"><span data-stu-id="02871-109">If  _lppPropNames_ is NULL, the  _cPropNames_ parameter must be 0.</span></span> 
    
 <span data-ttu-id="02871-110">_lppPropNames_</span><span class="sxs-lookup"><span data-stu-id="02871-110">_lppPropNames_</span></span>
  
> <span data-ttu-id="02871-111">in Ein Zeiger auf ein Array von Eigenschaftennamen oder NULL.</span><span class="sxs-lookup"><span data-stu-id="02871-111">[in] A pointer to an array of property names, or NULL.</span></span> <span data-ttu-id="02871-112">Beim Übergeben von NULL werden Eigenschaftenbezeichner für alle Eigenschaftennamen in allen Eigenschaftensätzen angefordert, über die das Objektinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="02871-112">Passing NULL requests property identifiers for all property names in all property sets about which the object has information.</span></span> <span data-ttu-id="02871-113">Der _lppPropNames_ -Parameter darf nicht NULL sein, wenn das MAPI_CREATE-Flag im _ulFlags_ -Parameter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="02871-113">The  _lppPropNames_ parameter must not be NULL if the MAPI_CREATE flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="02871-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="02871-114">_ulFlags_</span></span>
  
> <span data-ttu-id="02871-115">in Eine Bitmaske von Flags, die angibt, wie die Eigenschaftenbezeichner zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="02871-115">[in] A bitmask of flags that indicates how the property identifiers should be returned.</span></span> <span data-ttu-id="02871-116">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="02871-116">The following flag can be set:</span></span>
    
<span data-ttu-id="02871-117">MAPI_CREATE</span><span class="sxs-lookup"><span data-stu-id="02871-117">MAPI_CREATE</span></span> 
  
> <span data-ttu-id="02871-118">Weist einem oder mehreren Namen, die im Array der Eigenschaftennamen enthalten sind, auf die von _lppPropNames_verwiesen wurde, einen Eigenschaftenbezeichner zu, sofern noch keiner zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="02871-118">Assigns a property identifier, if one has not yet been assigned, to one or more of the names included in the property name array pointed to by  _lppPropNames_.</span></span> <span data-ttu-id="02871-119">Dieses Flag registriert den Bezeichner intern in der Zuordnungstabelle Name-to-Identifier.</span><span class="sxs-lookup"><span data-stu-id="02871-119">This flag internally registers the identifier in the name-to-identifier mapping table.</span></span>
    
 <span data-ttu-id="02871-120">_lppPropTags_</span><span class="sxs-lookup"><span data-stu-id="02871-120">_lppPropTags_</span></span>
  
> <span data-ttu-id="02871-121">Out Ein Zeiger auf einen Zeiger auf ein Array von Eigenschaftstags, das vorhandene oder neu zugewiesene Eigenschaftenbezeichner enthält.</span><span class="sxs-lookup"><span data-stu-id="02871-121">[out] A pointer to a pointer to an array of property tags that contains existing or newly assigned property identifiers.</span></span> <span data-ttu-id="02871-122">Die Eigenschaftentypen für die Eigenschaftstags in diesem Array sind auf **PT_UNSPECIFIED**festgelegt.</span><span class="sxs-lookup"><span data-stu-id="02871-122">The property types for the property tags in this array are set to **PT_UNSPECIFIED**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="02871-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="02871-123">Return value</span></span>

<span data-ttu-id="02871-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="02871-124">S_OK</span></span> 
  
> <span data-ttu-id="02871-125">Die Bezeichner für die angegebenen Eigenschaftennamen wurden erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="02871-125">The identifiers for the specified property names were successfully returned.</span></span>
    
<span data-ttu-id="02871-126">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="02871-126">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="02871-127">Das Objekt unterstützt keine benannten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="02871-127">The object does not support named properties.</span></span>
    
<span data-ttu-id="02871-128">MAPI_E_NOT_ENOUGH_MEMORY</span><span class="sxs-lookup"><span data-stu-id="02871-128">MAPI_E_NOT_ENOUGH_MEMORY</span></span> 
  
> <span data-ttu-id="02871-129">Es war nicht genügend Arbeitsspeicher verfügbar, um die Bezeichner abzurufen.</span><span class="sxs-lookup"><span data-stu-id="02871-129">Insufficient memory was available to retrieve the identifiers.</span></span>
    
<span data-ttu-id="02871-130">MAPI_E_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="02871-130">MAPI_E_TOO_BIG</span></span> 
  
> <span data-ttu-id="02871-131">Der Vorgang kann nicht ausgeführt werden, da zu viele Eigenschaftentags zurückgegeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="02871-131">The operation cannot be performed because it requires too many property tags to be returned.</span></span>
    
<span data-ttu-id="02871-132">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="02871-132">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="02871-133">Der Aufruf war insgesamt erfolgreich, aber ein oder mehrere Property Identifiers konnten nicht zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="02871-133">The call succeeded overall, but one or more property identifiers could not be returned.</span></span> <span data-ttu-id="02871-134">Der entsprechende Eigenschaftentyp für jede nicht verfügbare Eigenschaft wird auf **PT_ERROR** und dessen Bezeichner auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="02871-134">The corresponding property type for each unavailable property is set to **PT_ERROR** and its identifier to zero.</span></span> <span data-ttu-id="02871-135">Wenn diese Warnung zurückgegeben wird, behandeln Sie den Anruf als erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="02871-135">When this warning is returned, handle the call as successful.</span></span> <span data-ttu-id="02871-136">Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** -Makro.</span><span class="sxs-lookup"><span data-stu-id="02871-136">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="02871-137">Weitere Informationen finden Sie unter [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="02871-137">See [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="02871-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02871-138">Remarks</span></span>

<span data-ttu-id="02871-139">Die **IMAPIProp:: GetIDsFromNames** -Methode ruft ein Array von Property-Tags ab, die die Eigenschaftenbezeichner für eine oder mehrere benannte Eigenschaften enthalten.</span><span class="sxs-lookup"><span data-stu-id="02871-139">The **IMAPIProp::GetIDsFromNames** method retrieves an array of property tags that hold the property identifiers for one or more named properties.</span></span> <span data-ttu-id="02871-140">**IMAPIProp:: GetIDsFromNames** kann aufgerufen werden, um folgende Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="02871-140">**IMAPIProp::GetIDsFromNames** can be called to do the following:</span></span> 
  
- <span data-ttu-id="02871-141">Erstellen Sie Bezeichner für neue Namen.</span><span class="sxs-lookup"><span data-stu-id="02871-141">Create identifiers for new names.</span></span>
    
- <span data-ttu-id="02871-142">Abrufen von Bezeichnern für bestimmte Namen.</span><span class="sxs-lookup"><span data-stu-id="02871-142">Retrieve identifiers for specific names.</span></span>
    
- <span data-ttu-id="02871-143">Abrufen von Bezeichnern für alle benannten Eigenschaften, die in der Zuordnung des Objekts enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="02871-143">Retrieve identifiers for all named properties that are included in the object's mapping.</span></span>
    
<span data-ttu-id="02871-144">Benannte Eigenschaften werden in der Regel von Nachrichtenspeicher Anbietern für Ordner und Nachrichten verwendet.</span><span class="sxs-lookup"><span data-stu-id="02871-144">Named properties are typically used by message store providers for folders and messages.</span></span> <span data-ttu-id="02871-145">Andere Objekte, wie Messaging-Benutzer und Profilabschnitte, unterstützen möglicherweise nicht die Zuordnung von Namen zu Eigenschafts Bezeichnern und können MAPI_E_NO_SUPPORT von **GetIDsFromNames**zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="02871-145">Other objects, such as messaging users and profile sections, might not support the association of names to property identifiers and might return MAPI_E_NO_SUPPORT from **GetIDsFromNames**.</span></span>
  
<span data-ttu-id="02871-146">Wenn ein Fehler auftritt, der einen Bezeichner für einen bestimmten Namen zurückgibt, gibt **GETIDSFROMNAMES** MAPI_W_ERRORS_RETURNED zurück und legt den Eigenschaftentyp im Array Eintrag für das Property-Tag fest, der dem Namen **PT_ERROR** und dem Bezeichner auf Null entspricht.</span><span class="sxs-lookup"><span data-stu-id="02871-146">If there is an error that returns an identifier for a particular name, **GetIDsFromNames** returns MAPI_W_ERRORS_RETURNED and sets the property type in the property tag array entry that corresponds to the name to **PT_ERROR** and the identifier to zero.</span></span> 
  
<span data-ttu-id="02871-147">Die Zuordnung von Namen zu Bezeichnern wird durch die **PR_MAPPING_SIGNATURE** ([pidtagmappingsignature (](pidtagmappingsignature-canonical-property.md))-Eigenschaft eines Objekts dargestellt.</span><span class="sxs-lookup"><span data-stu-id="02871-147">Name-to-identifier mapping is represented by an object's **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) property.</span></span> <span data-ttu-id="02871-148">**PR_MAPPING_SIGNATURE** enthält eine [MAPIUID](mapiuid.md) -Struktur, die den für das Objektverantwortlichen Dienstanbieter angibt.</span><span class="sxs-lookup"><span data-stu-id="02871-148">**PR_MAPPING_SIGNATURE** contains a [MAPIUID](mapiuid.md) structure that indicates the service provider responsible for the object.</span></span> <span data-ttu-id="02871-149">Wenn die **PR_MAPPING_SIGNATURE** -Eigenschaft für zwei Objekte identisch ist, wird davon ausgegangen, dass diese Objekte dieselbe Name-zu-Bezeichner-Zuordnung verwenden.</span><span class="sxs-lookup"><span data-stu-id="02871-149">If the **PR_MAPPING_SIGNATURE** property is the same for two objects, assume that these objects use the same name-to-identifier mapping.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="02871-150">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="02871-150">Notes to implementers</span></span>

<span data-ttu-id="02871-151">Die Bezeichner, die Sie zurückgeben, in das Eigenschaftentag-Array, auf das durch den _lppPropNames_ -Parameter verwiesen wird, müssen sich im 0X8000-0xFFFE-Bereich befinden.</span><span class="sxs-lookup"><span data-stu-id="02871-151">The identifiers that you pass back in the property tag array pointed to by the  _lppPropNames_ parameter must be in the 0x8000 to 0xFFFE range.</span></span> <span data-ttu-id="02871-152">Die Einträge in diesem Array müssen in derselben Reihenfolge wie die Namen sein, die im Array der Eigenschaftennamen übergeben wurden, auf das durch _lppPropNames_verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="02871-152">The entries in this array must be in the same order as the names passed in the property name array pointed to by  _lppPropNames_.</span></span> 
  
<span data-ttu-id="02871-153">Wenn Sie benannte Eigenschaften in einem Container unterstützen, verwenden Sie die gleiche Zuordnung Name-zu-Bezeichner für alle Objekte in Ihrem Container (das heißt, verwenden Sie keine andere Zuordnung für jeden Ordner in Ihrem Nachrichtenspeicher oder jede Nachricht in Ihrem Ordner).</span><span class="sxs-lookup"><span data-stu-id="02871-153">If you support named properties on a container, use the same name-to-identifier mapping for all objects in your container (that is, do not use a different mapping for each folder in your message store or each message in your folder).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="02871-154">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="02871-154">Notes to callers</span></span>

<span data-ttu-id="02871-155">Da die Eigenschaftentypen für die zurückgegebenen Bezeichner im Property-Tag-Array, auf das durch _lppPropTags_ verwiesen wird, auf **PT_UNSPECIFIED**festgelegt sind, müssen Sie die [IMAPIProp::](imapiprop-setprops.md) SetProps-Methode aufrufen, um die genauen Typen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="02871-155">Because the property types for the returned identifiers in the property tag array pointed to by  _lppPropTags_ are set to **PT_UNSPECIFIED**, you will have to call the [IMAPIProp::SetProps](imapiprop-setprops.md) method to retrieve the accurate types.</span></span> 
  
<span data-ttu-id="02871-156">Wenn Sie Objekte mit benannten Eigenschaften verschieben oder kopieren und die Quell-und Zielobjekte unterschiedliche Zuordnungs Signaturen aufweisen, wie durch die Werte Ihrer **PR_MAPPING_SIGNATURE** -Eigenschaften angegeben, müssen Sie die Namen während dieser Vorgänge beibehalten.</span><span class="sxs-lookup"><span data-stu-id="02871-156">If you move or copy objects with named properties, and the source and destination objects have different mapping signatures as indicated by the values of their **PR_MAPPING_SIGNATURE** properties, you must preserve the names during these operations.</span></span> <span data-ttu-id="02871-157">Um Eigenschaftsnamen beizubehalten, passen Sie die entsprechenden Eigenschaftenbezeichner so an, dass Sie der Name-to-Identifier-Zuordnung des Zielobjekts entsprechen.</span><span class="sxs-lookup"><span data-stu-id="02871-157">To preserve property names, adjust the corresponding property identifiers to match the name-to-identifier mapping of the destination object.</span></span> 
  
<span data-ttu-id="02871-158">Einige Objekte haben einen Grenzwert für die Anzahl der Eigenschaftsbezeichner, die Sie benennen können.</span><span class="sxs-lookup"><span data-stu-id="02871-158">Some objects have a limit as to the number of property identifiers they can name.</span></span> <span data-ttu-id="02871-159">Wenn ein Aufruf von **GetIDsFromNames** bewirkt, dass dieser Grenzwert überschritten wird, gibt die Methode MAPI_E_TOO_BIG zurück.</span><span class="sxs-lookup"><span data-stu-id="02871-159">If a call to **GetIDsFromNames** causes this limit to be exceeded, the method returns MAPI_E_TOO_BIG.</span></span> <span data-ttu-id="02871-160">In diesem Fall Abfrage nach Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="02871-160">In this case, query by identifier.</span></span> 
  
<span data-ttu-id="02871-161">Weitere Informationen finden Sie unter [MAPI-benannte Eigenschaften](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="02871-161">For more information, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="02871-162">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="02871-162">MFCMAPI reference</span></span>

<span data-ttu-id="02871-163">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="02871-163">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="02871-164">**Datei**</span><span class="sxs-lookup"><span data-stu-id="02871-164">**File**</span></span>|<span data-ttu-id="02871-165">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="02871-165">**Function**</span></span>|<span data-ttu-id="02871-166">**Comment**</span><span class="sxs-lookup"><span data-stu-id="02871-166">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="02871-167">SingleMAPIPropListCtrl. cpp</span><span class="sxs-lookup"><span data-stu-id="02871-167">SingleMAPIPropListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="02871-168">CSingleMAPIPropListCtrl:: FindAllNamedPropsUsed</span><span class="sxs-lookup"><span data-stu-id="02871-168">CSingleMAPIPropListCtrl::FindAllNamedPropsUsed</span></span>  <br/> |<span data-ttu-id="02871-169">MFCMAPI verwendet die **IMAPIProp:: GetIDsFromNames** -Methode, um Eigenschaftentags für alle benannten Eigenschaften abzurufen, die zugeordnet wurden.</span><span class="sxs-lookup"><span data-stu-id="02871-169">MFCMAPI uses the **IMAPIProp::GetIDsFromNames** method to obtain property tags for all named properties that have been mapped.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="02871-170">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02871-170">See also</span></span>



[<span data-ttu-id="02871-171">IMAPIProp::GetNamesFromIDs</span><span class="sxs-lookup"><span data-stu-id="02871-171">IMAPIProp::GetNamesFromIDs</span></span>](imapiprop-getnamesfromids.md)
  
[<span data-ttu-id="02871-172">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="02871-172">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="02871-173">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="02871-173">MAPINAMEID</span></span>](mapinameid.md)
  
[<span data-ttu-id="02871-174">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="02871-174">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="02871-175">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="02871-175">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="02871-176">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="02871-176">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="02871-177">Benannte Eigenschaften MAPI</span><span class="sxs-lookup"><span data-stu-id="02871-177">MAPI Named Properties</span></span>](mapi-named-properties.md)
  
[<span data-ttu-id="02871-178">Verwenden von Makros zur Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="02871-178">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

