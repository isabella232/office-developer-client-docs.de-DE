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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 5247ca71c88b9c0f8591a732746a17204265741c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792283"
---
# <a name="imapipropgetidsfromnames"></a><span data-ttu-id="387a2-103">IMAPIProp::GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="387a2-103">IMAPIProp::GetIDsFromNames</span></span>

  
  
<span data-ttu-id="387a2-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="387a2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="387a2-105">Enthält die Eigenschaftenbezeichner, die mindestens einen Eigenschaftennamen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="387a2-105">Provides the property identifiers that correspond to one or more property names.</span></span>
  
```cpp
HRESULT GetIDsFromNames(
  ULONG cPropNames,
  LPMAPINAMEID FAR * lppPropNames,
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTags
);
```

## <a name="parameters"></a><span data-ttu-id="387a2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="387a2-106">Parameters</span></span>

 <span data-ttu-id="387a2-107">_cPropNames_</span><span class="sxs-lookup"><span data-stu-id="387a2-107">_cPropNames_</span></span>
  
> <span data-ttu-id="387a2-108">[in] Die Anzahl der Eigenschaftennamen, die auf den durch den Parameter _LppPropNames_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="387a2-108">[in] The count of property names pointed to by the  _lppPropNames_ parameter.</span></span> <span data-ttu-id="387a2-109">Wenn _LppPropNames_ NULL ist, muss der Parameter _cPropNames_ 0 sein.</span><span class="sxs-lookup"><span data-stu-id="387a2-109">If  _lppPropNames_ is NULL, the  _cPropNames_ parameter must be 0.</span></span> 
    
 <span data-ttu-id="387a2-110">_lppPropNames_</span><span class="sxs-lookup"><span data-stu-id="387a2-110">_lppPropNames_</span></span>
  
> <span data-ttu-id="387a2-111">[in] Ein Zeiger auf ein Array von Eigenschaftennamen oder NULL.</span><span class="sxs-lookup"><span data-stu-id="387a2-111">[in] A pointer to an array of property names, or NULL.</span></span> <span data-ttu-id="387a2-112">Bei Übergabe von NULL fordert Eigenschaftenbezeichner für alle Eigenschaftennamen in allen, die Eigenschaftensätze, die das Objekt Informationen verfügt.</span><span class="sxs-lookup"><span data-stu-id="387a2-112">Passing NULL requests property identifiers for all property names in all property sets about which the object has information.</span></span> <span data-ttu-id="387a2-113">Der Parameter _LppPropNames_ darf nicht NULL sein, wenn das Flag MAPI_CREATE ist im _UlFlags_ -Parameter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="387a2-113">The  _lppPropNames_ parameter must not be NULL if the MAPI_CREATE flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="387a2-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="387a2-114">_ulFlags_</span></span>
  
> <span data-ttu-id="387a2-115">[in] Eine Bitmaske aus Flags, die angibt, wie die Eigenschaftenbezeichner zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="387a2-115">[in] A bitmask of flags that indicates how the property identifiers should be returned.</span></span> <span data-ttu-id="387a2-116">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="387a2-116">The following flag can be set:</span></span>
    
<span data-ttu-id="387a2-117">MAPI_CREATE IST</span><span class="sxs-lookup"><span data-stu-id="387a2-117">MAPI_CREATE</span></span> 
  
> <span data-ttu-id="387a2-118">Weist einen Eigenschaftenbezeichner an, wenn eine nicht noch, um eine oder mehrere der in der Array-Eigenschaft Name auf den _LppPropNames_enthaltenen Namen zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="387a2-118">Assigns a property identifier, if one has not yet been assigned, to one or more of the names included in the property name array pointed to by  _lppPropNames_.</span></span> <span data-ttu-id="387a2-119">Dieses Kennzeichen registriert intern den Bezeichner in der Zuordnungstabelle Namensbezeichner-an.</span><span class="sxs-lookup"><span data-stu-id="387a2-119">This flag internally registers the identifier in the name-to-identifier mapping table.</span></span>
    
 <span data-ttu-id="387a2-120">_lppPropTags_</span><span class="sxs-lookup"><span data-stu-id="387a2-120">_lppPropTags_</span></span>
  
> <span data-ttu-id="387a2-121">[out] Ein Zeiger auf einen Zeiger auf ein Array von Eigenschaftentags, vorhandene oder neu zugewiesenen Eigenschaftenbezeichner enthält.</span><span class="sxs-lookup"><span data-stu-id="387a2-121">[out] A pointer to a pointer to an array of property tags that contains existing or newly assigned property identifiers.</span></span> <span data-ttu-id="387a2-122">Die Eigenschaftentypen für die Eigenschaftentags in diesem Array werden auf **PT_UNSPECIFIED**festgelegt.</span><span class="sxs-lookup"><span data-stu-id="387a2-122">The property types for the property tags in this array are set to **PT_UNSPECIFIED**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="387a2-123">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="387a2-123">Return value</span></span>

<span data-ttu-id="387a2-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="387a2-124">S_OK</span></span> 
  
> <span data-ttu-id="387a2-125">Der Bezeichner für die angegebene Eigenschaftennamen wurden erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="387a2-125">The identifiers for the specified property names were successfully returned.</span></span>
    
<span data-ttu-id="387a2-126">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="387a2-126">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="387a2-127">Das Objekt unterstützt keine benannte Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="387a2-127">The object does not support named properties.</span></span>
    
<span data-ttu-id="387a2-128">MAPI_E_NOT_ENOUGH_MEMORY</span><span class="sxs-lookup"><span data-stu-id="387a2-128">MAPI_E_NOT_ENOUGH_MEMORY</span></span> 
  
> <span data-ttu-id="387a2-129">War nicht genügend Arbeitsspeicher zum Abrufen der Bezeichner verfügbar.</span><span class="sxs-lookup"><span data-stu-id="387a2-129">Insufficient memory was available to retrieve the identifiers.</span></span>
    
<span data-ttu-id="387a2-130">MAPI_E_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="387a2-130">MAPI_E_TOO_BIG</span></span> 
  
> <span data-ttu-id="387a2-131">Der Vorgang kann nicht ausgeführt werden, da zu viele Eigenschaftentags zurückzugebenden erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="387a2-131">The operation cannot be performed because it requires too many property tags to be returned.</span></span>
    
<span data-ttu-id="387a2-132">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="387a2-132">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="387a2-133">Der Aufruf war insgesamt erfolgreich, aber eine oder mehrere Eigenschaftenbezeichner konnte nicht zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="387a2-133">The call succeeded overall, but one or more property identifiers could not be returned.</span></span> <span data-ttu-id="387a2-134">Der entsprechende Eigenschaftentyp für jede Eigenschaft nicht verfügbar ist **PT_ERROR** und des Bezeichners auf NULL gesetzt.</span><span class="sxs-lookup"><span data-stu-id="387a2-134">The corresponding property type for each unavailable property is set to **PT_ERROR** and its identifier to zero.</span></span> <span data-ttu-id="387a2-135">Wenn diese Warnung zurückgegeben wird, bearbeiten Sie den Anruf als erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="387a2-135">When this warning is returned, handle the call as successful.</span></span> <span data-ttu-id="387a2-136">Verwenden Sie das Makro **HR_FAILED** , um für diese Warnung zu testen.</span><span class="sxs-lookup"><span data-stu-id="387a2-136">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="387a2-137">Finden Sie unter [Verwendung von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="387a2-137">See [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="387a2-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="387a2-138">Remarks</span></span>

<span data-ttu-id="387a2-139">Die **IMAPIProp::GetIDsFromNames** -Methode ruft ein Array von Eigenschaftentags, die die als Eigenschaftenbezeichner für eine oder mehrere benannte Eigenschaften enthalten.</span><span class="sxs-lookup"><span data-stu-id="387a2-139">The **IMAPIProp::GetIDsFromNames** method retrieves an array of property tags that hold the property identifiers for one or more named properties.</span></span> <span data-ttu-id="387a2-140">**IMAPIProp::GetIDsFromNames** kann aufgerufen werden, um Folgendes auszuführen:</span><span class="sxs-lookup"><span data-stu-id="387a2-140">**IMAPIProp::GetIDsFromNames** can be called to do the following:</span></span> 
  
- <span data-ttu-id="387a2-141">Bezeichner für den neuen Namen erstellt.</span><span class="sxs-lookup"><span data-stu-id="387a2-141">Create identifiers for new names.</span></span>
    
- <span data-ttu-id="387a2-142">Rufen Sie IDs für bestimmte Namen ab.</span><span class="sxs-lookup"><span data-stu-id="387a2-142">Retrieve identifiers for specific names.</span></span>
    
- <span data-ttu-id="387a2-143">Abrufen von Bezeichnern für alle benannten Eigenschaften, die in das Objekt Zuordnung enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="387a2-143">Retrieve identifiers for all named properties that are included in the object's mapping.</span></span>
    
<span data-ttu-id="387a2-144">Benannte Eigenschaften werden in der Regel Zeichenfolgeneigenschaften Nachricht für Ordner und Nachrichten verwendet.</span><span class="sxs-lookup"><span data-stu-id="387a2-144">Named properties are typically used by message store providers for folders and messages.</span></span> <span data-ttu-id="387a2-145">Andere Objekte, wie messaging Profil Bereichen und Benutzer möglicherweise keine Unterstützung für die Zuordnung von Namen zu eigenschaftskennungen und zurückgeben MAPI_E_NO_SUPPORT vom **GetIDsFromNames**.</span><span class="sxs-lookup"><span data-stu-id="387a2-145">Other objects, such as messaging users and profile sections, might not support the association of names to property identifiers and might return MAPI_E_NO_SUPPORT from **GetIDsFromNames**.</span></span>
  
<span data-ttu-id="387a2-146">Ist ein Fehler, der einen Bezeichner für einen bestimmten Namen zurückgibt, **GetIDsFromNames** gibt MAPI_W_ERRORS_RETURNED zurück und legt den Eigenschaftstyp in der Eigenschaft Tag Array-Eintrag, der den Namen **PT_ERROR** und die ID 0 (null) entspricht.</span><span class="sxs-lookup"><span data-stu-id="387a2-146">If there is an error that returns an identifier for a particular name, **GetIDsFromNames** returns MAPI_W_ERRORS_RETURNED and sets the property type in the property tag array entry that corresponds to the name to **PT_ERROR** and the identifier to zero.</span></span> 
  
<span data-ttu-id="387a2-147">Namensbezeichner-Zuordnung wird durch ein Objekt **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md))-Eigenschaft dargestellt.</span><span class="sxs-lookup"><span data-stu-id="387a2-147">Name-to-identifier mapping is represented by an object's **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) property.</span></span> <span data-ttu-id="387a2-148">**PR_MAPPING_SIGNATURE** enthält eine [MAPIUID](mapiuid.md) -Struktur, die den Dienstanbieter verantwortlich für das Objekt angibt.</span><span class="sxs-lookup"><span data-stu-id="387a2-148">**PR_MAPPING_SIGNATURE** contains a [MAPIUID](mapiuid.md) structure that indicates the service provider responsible for the object.</span></span> <span data-ttu-id="387a2-149">Wenn die **PR_MAPPING_SIGNATURE** -Eigenschaft für zwei Objekte übereinstimmt, wird davon ausgegangen Sie, dass diese Objekte die Namensbezeichner-Zuordnung verwenden.</span><span class="sxs-lookup"><span data-stu-id="387a2-149">If the **PR_MAPPING_SIGNATURE** property is the same for two objects, assume that these objects use the same name-to-identifier mapping.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="387a2-150">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="387a2-150">Notes to implementers</span></span>

<span data-ttu-id="387a2-151">Die Bezeichner, die Sie wieder in die Array-Tag-Eigenschaft auf das durch den Parameter _LppPropNames_ übergeben, muss im Bereich von 0 x 8000 zu 0xFFFE.</span><span class="sxs-lookup"><span data-stu-id="387a2-151">The identifiers that you pass back in the property tag array pointed to by the  _lppPropNames_ parameter must be in the 0x8000 to 0xFFFE range.</span></span> <span data-ttu-id="387a2-152">Die Einträge in diesem Array müssen in der gleichen Reihenfolge die Namen übergebenen Arrays der Name-Eigenschaft mit _LppPropNames_gezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="387a2-152">The entries in this array must be in the same order as the names passed in the property name array pointed to by  _lppPropNames_.</span></span> 
  
<span data-ttu-id="387a2-153">Wenn Sie benannte Eigenschaften für einen Container unterstützen, verwenden Sie die Namensbezeichner-Zuordnung für alle Objekte in den Container (d. h., verwenden Sie keine andere Zuordnung für jeden Ordner in Ihrem Nachrichtenspeicher oder jede Nachricht im Ordner).</span><span class="sxs-lookup"><span data-stu-id="387a2-153">If you support named properties on a container, use the same name-to-identifier mapping for all objects in your container (that is, do not use a different mapping for each folder in your message store or each message in your folder).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="387a2-154">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="387a2-154">Notes to callers</span></span>

<span data-ttu-id="387a2-155">Da die Eigenschaftentypen für die zurückgegebene Bezeichner in der Array-Tag-Eigenschaft auf den _LppPropTags_ auf **PT_UNSPECIFIED**festgelegt sind, müssen Sie rufen Sie die [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode, um die genauen Typen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="387a2-155">Because the property types for the returned identifiers in the property tag array pointed to by  _lppPropTags_ are set to **PT_UNSPECIFIED**, you will have to call the [IMAPIProp::SetProps](imapiprop-setprops.md) method to retrieve the accurate types.</span></span> 
  
<span data-ttu-id="387a2-156">Wenn Sie verschieben oder Objekte mit benannten Eigenschaften kopieren und die Quell- und Ziel-Objekte andere Zuordnung Signaturen, haben wie durch die Werte der Eigenschaften **PR_MAPPING_SIGNATURE** , müssen Sie die Namen während dieser Vorgänge beibehalten.</span><span class="sxs-lookup"><span data-stu-id="387a2-156">If you move or copy objects with named properties, and the source and destination objects have different mapping signatures as indicated by the values of their **PR_MAPPING_SIGNATURE** properties, you must preserve the names during these operations.</span></span> <span data-ttu-id="387a2-157">Um Eigenschaftennamen beizubehalten, passen Sie die entsprechenden Eigenschaftenbezeichner entsprechend die Namensbezeichner-Zuordnung von Zielobjekt.</span><span class="sxs-lookup"><span data-stu-id="387a2-157">To preserve property names, adjust the corresponding property identifiers to match the name-to-identifier mapping of the destination object.</span></span> 
  
<span data-ttu-id="387a2-158">Einige Objekte haben eine Obergrenze für die Anzahl der Eigenschaftenbezeichner, den, die Sie einen Namen eingeben können.</span><span class="sxs-lookup"><span data-stu-id="387a2-158">Some objects have a limit as to the number of property identifiers they can name.</span></span> <span data-ttu-id="387a2-159">Bewirkt ein Aufruf von **GetIDsFromNames** dieser Grenzwert überschritten wird, gibt die Methode MAPI_E_TOO_BIG zurück.</span><span class="sxs-lookup"><span data-stu-id="387a2-159">If a call to **GetIDsFromNames** causes this limit to be exceeded, the method returns MAPI_E_TOO_BIG.</span></span> <span data-ttu-id="387a2-160">In diesem Fall nach Bezeichnern abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="387a2-160">In this case, query by identifier.</span></span> 
  
<span data-ttu-id="387a2-161">Weitere Informationen finden Sie unter [MAPI-Eigenschaften mit dem Namen](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="387a2-161">For more information, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="387a2-162">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="387a2-162">MFCMAPI reference</span></span>

<span data-ttu-id="387a2-163">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="387a2-163">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="387a2-164">**Datei**</span><span class="sxs-lookup"><span data-stu-id="387a2-164">**File**</span></span>|<span data-ttu-id="387a2-165">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="387a2-165">**Function**</span></span>|<span data-ttu-id="387a2-166">**Comment**</span><span class="sxs-lookup"><span data-stu-id="387a2-166">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="387a2-167">SingleMAPIPropListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="387a2-167">SingleMAPIPropListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="387a2-168">CSingleMAPIPropListCtrl::FindAllNamedPropsUsed</span><span class="sxs-lookup"><span data-stu-id="387a2-168">CSingleMAPIPropListCtrl::FindAllNamedPropsUsed</span></span>  <br/> |<span data-ttu-id="387a2-169">MFCMAPI (engl.) verwendet die **IMAPIProp::GetIDsFromNames** -Methode, um Eigenschaftentags für alle benannten Eigenschaften abzurufen, die zugeordnet wurden.</span><span class="sxs-lookup"><span data-stu-id="387a2-169">MFCMAPI uses the **IMAPIProp::GetIDsFromNames** method to obtain property tags for all named properties that have been mapped.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="387a2-170">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="387a2-170">See also</span></span>



[<span data-ttu-id="387a2-171">IMAPIProp::GetNamesFromIDs</span><span class="sxs-lookup"><span data-stu-id="387a2-171">IMAPIProp::GetNamesFromIDs</span></span>](imapiprop-getnamesfromids.md)
  
[<span data-ttu-id="387a2-172">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="387a2-172">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="387a2-173">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="387a2-173">MAPINAMEID</span></span>](mapinameid.md)
  
[<span data-ttu-id="387a2-174">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="387a2-174">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="387a2-175">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="387a2-175">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="387a2-176">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="387a2-176">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="387a2-177">Benannte Eigenschaften MAPI</span><span class="sxs-lookup"><span data-stu-id="387a2-177">MAPI Named Properties</span></span>](mapi-named-properties.md)
  
[<span data-ttu-id="387a2-178">Verwenden von Makros zur Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="387a2-178">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

