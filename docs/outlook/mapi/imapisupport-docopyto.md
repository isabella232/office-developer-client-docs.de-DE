---
title: IMAPISupportDoCopyTo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoCopyTo
api_type:
- COM
ms.assetid: 84019475-5176-4fc5-a3ee-871095077498
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6f6c802f1d5ead1750c05fafc54533487fe3732a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331808"
---
# <a name="imapisupportdocopyto"></a><span data-ttu-id="9249e-103">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="9249e-103">IMAPISupport::DoCopyTo</span></span>

  
  
<span data-ttu-id="9249e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9249e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9249e-105">Kopiert oder verschiebt alle Eigenschaften eines Objekts, mit Ausnahme ausdrücklich ausgeschlossener Eigenschaften, in ein anderes Objekt.</span><span class="sxs-lookup"><span data-stu-id="9249e-105">Copies or moves all properties of one object, except for specifically excluded properties, to another object.</span></span>
  
```cpp
HRESULT DoCopyTo(
  LPCIID lpSrcInterface,
  LPVOID lpSrcObj,
  ULONG ciidExclude,
  LPCIID rgiidExclude,
  LPSPropTagArray lpExcludeProps,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  LPCIID lpDestInterface,
  LPVOID lpDestObj,
  ULONG ulFlags,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="9249e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9249e-106">Parameters</span></span>

 <span data-ttu-id="9249e-107">_lpSrcInterface_</span><span class="sxs-lookup"><span data-stu-id="9249e-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="9249e-108">[in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID), die die Schnittstelle darstellt, die für den Zugriff auf das Objekt verwendet werden soll, das über die Eigenschaften verfügt, die kopiert oder verschoben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9249e-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object that has the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="9249e-109">_lpSrcObj_</span><span class="sxs-lookup"><span data-stu-id="9249e-109">_lpSrcObj_</span></span>
  
> <span data-ttu-id="9249e-110">[in] Ein Zeiger auf das Objekt, das die eigenschaften enthält, die kopiert oder verschoben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9249e-110">[in] A pointer to the object that has the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="9249e-111">_ciidExclude_</span><span class="sxs-lookup"><span data-stu-id="9249e-111">_ciidExclude_</span></span>
  
> <span data-ttu-id="9249e-112">[in] Die Anzahl der Schnittstellen, die beim Kopieren oder Verschieben von Eigenschaften ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="9249e-112">[in] The count of interfaces to exclude when you copy or move properties.</span></span>
    
 <span data-ttu-id="9249e-113">_rgiidExclude_</span><span class="sxs-lookup"><span data-stu-id="9249e-113">_rgiidExclude_</span></span>
  
> <span data-ttu-id="9249e-114">[in] Ein Array von Schnittstellenbezeichnern, das Schnittstellen angibt, die nicht verwendet werden sollten, wenn Sie ergänzende Informationen kopieren oder in das Zielobjekt verschieben.</span><span class="sxs-lookup"><span data-stu-id="9249e-114">[in] An array of interface identifiers that indicates interfaces that should not be used when you copy or move supplemental information to the destination object.</span></span>
    
 <span data-ttu-id="9249e-115">_lpExcludeProps_</span><span class="sxs-lookup"><span data-stu-id="9249e-115">_lpExcludeProps_</span></span>
  
> <span data-ttu-id="9249e-116">[in] Ein Zeiger auf ein Eigenschaftentagarray, das die Eigenschaftstags identifiziert, die vom Kopier- oder Verschiebevorgang ausgeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9249e-116">[in] A pointer to a property tag array that identifies the property tags that should be excluded from the copy or move operation.</span></span> <span data-ttu-id="9249e-117">Das Übergeben von NULL im  _lpExcludeProps-Parameter_ gibt an, dass alle Eigenschaften des Objekts kopiert oder verschoben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9249e-117">Passing NULL in the  _lpExcludeProps_ parameter indicates that all of the object's properties should be copied or moved.</span></span> <span data-ttu-id="9249e-118">**DoCopyTo** gibt MAPI_E_INVALID_PARAMETER zurück, wenn **das cValues-Element** der [SPropTagArray-Struktur,](sproptagarray.md) auf die  _von lpExcludeProps_ verwiesen wird, auf 0 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9249e-118">**DoCopyTo** returns MAPI_E_INVALID_PARAMETER when the **cValues** member of the [SPropTagArray](sproptagarray.md) structure pointed to by  _lpExcludeProps_ is set to 0.</span></span> 
    
 <span data-ttu-id="9249e-119">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="9249e-119">_ulUIParam_</span></span>
  
> <span data-ttu-id="9249e-120">[in] Ein Handle zum übergeordneten Fenster des Statusindikators.</span><span class="sxs-lookup"><span data-stu-id="9249e-120">[in] A handle to the parent window of the progress indicator.</span></span> 
    
 <span data-ttu-id="9249e-121">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="9249e-121">_lpProgress_</span></span>
  
> <span data-ttu-id="9249e-122">[in] Ein Zeiger auf eine Fortschrittsindikatorimplementierung.</span><span class="sxs-lookup"><span data-stu-id="9249e-122">[in] A pointer to a progress indicator implementation.</span></span> <span data-ttu-id="9249e-123">Wenn NULL im  _lpProgress-Parameter übergeben_ wird, stellt MAPI die Fortschrittsimplementierung.</span><span class="sxs-lookup"><span data-stu-id="9249e-123">If NULL is passed in the  _lpProgress_ parameter, MAPI provides the progress implementation.</span></span> <span data-ttu-id="9249e-124">Der  _lpProgress-Parameter_ wird ignoriert, es sei denn, das MAPI_DIALOG wird im  _ulFlags-Parameter_ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9249e-124">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="9249e-125">_lpDestInterface_</span><span class="sxs-lookup"><span data-stu-id="9249e-125">_lpDestInterface_</span></span>
  
> <span data-ttu-id="9249e-126">[in] Ein Zeiger auf die Schnittstellen-ID, die die Schnittstelle darstellt, mit der auf das Objekt zugegriffen werden soll, um die kopierten oder verschobenen Eigenschaften zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="9249e-126">[in] A pointer to the interface identifier that represents the interface to be used to access the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="9249e-127">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="9249e-127">_lpDestObj_</span></span>
  
> <span data-ttu-id="9249e-128">[in] Ein Zeiger auf das Objekt, um die kopierten oder verschobenen Eigenschaften zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="9249e-128">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="9249e-129">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9249e-129">_ulFlags_</span></span>
  
> <span data-ttu-id="9249e-130">[in] Eine Bitmaske mit Flags, die den Kopier- oder Verschiebevorgang steuert.</span><span class="sxs-lookup"><span data-stu-id="9249e-130">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="9249e-131">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="9249e-131">The following flags can be set:</span></span>
    
<span data-ttu-id="9249e-132">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="9249e-132">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="9249e-133">Zeigt eine Statusanzeige an.</span><span class="sxs-lookup"><span data-stu-id="9249e-133">Displays a progress indicator.</span></span> 
    
<span data-ttu-id="9249e-134">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="9249e-134">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="9249e-135">**DoCopyTo** sollte einen Verschiebevorgang anstelle eines Kopiervorgangs ausführen.</span><span class="sxs-lookup"><span data-stu-id="9249e-135">**DoCopyTo** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="9249e-136">Wenn dieses Flag nicht festgelegt ist, **führt DoCopyTo** einen Kopiervorgang aus.</span><span class="sxs-lookup"><span data-stu-id="9249e-136">When this flag is not set, **DoCopyTo** performs a copy operation.</span></span> 
    
<span data-ttu-id="9249e-137">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="9249e-137">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="9249e-138">Vorhandene Eigenschaften im Zielobjekt sollten nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="9249e-138">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="9249e-139">Wenn dieses Kennzeichen nicht festgelegt ist, **überschreibt DoCopyTo** vorhandene Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9249e-139">When this flag is not set, **DoCopyTo** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="9249e-140">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="9249e-140">_lppProblems_</span></span>
  
> <span data-ttu-id="9249e-141">[out] Bei der Eingabe ein Zeiger auf einen Zeiger auf eine [SPropProblemArray-Struktur;](spropproblemarray.md) andernfalls NULL, was angibt, dass keine Fehlerinformationen benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="9249e-141">[out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, which indicates no need for error information.</span></span> <span data-ttu-id="9249e-142">Wenn  _lppProblems_ ein gültiger Zeiger für die Eingabe ist, gibt **DoCopyTo** detaillierte Informationen zu Fehlern beim Kopieren einer oder mehreren Eigenschaften zurück.</span><span class="sxs-lookup"><span data-stu-id="9249e-142">If  _lppProblems_ is a valid pointer on input, **DoCopyTo** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9249e-143">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9249e-143">Return value</span></span>

<span data-ttu-id="9249e-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="9249e-144">S_OK</span></span> 
  
> <span data-ttu-id="9249e-145">Die Eigenschaften wurden erfolgreich kopiert oder verschoben.</span><span class="sxs-lookup"><span data-stu-id="9249e-145">The properties have been successfully copied or moved.</span></span>
    
<span data-ttu-id="9249e-146">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="9249e-146">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="9249e-147">Eine zu kopierende oder zu verschobene Eigenschaft ist bereits im Zielobjekt vorhanden, und das MAPI_NOREPLACE ist festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9249e-147">A property to be copied or moved already exists in the destination object and the MAPI_NOREPLACE flag is set.</span></span> 
    
<span data-ttu-id="9249e-148">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="9249e-148">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="9249e-149">Das Quellobjekt enthält direkt oder indirekt das Zielobjekt.</span><span class="sxs-lookup"><span data-stu-id="9249e-149">The source object directly or indirectly contains the destination object.</span></span> <span data-ttu-id="9249e-150">Bevor diese Bedingung erkannt wurde, wurden möglicherweise erhebliche Arbeiten ausgeführt, sodass die Quell- und Zielobjekte teilweise geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="9249e-150">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="9249e-151">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="9249e-151">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="9249e-152">Die durch den  _lpSrcInterface-Parameter_ identifizierte Schnittstelle wird vom objekt, auf das  _von lpSrcObj_ verwiesen wird, nicht unterstützt, oder die durch den  _lpDestInterface-Parameter_ identifizierte Schnittstelle wird vom Objekt, auf das von  _lpDestObj_ verwiesen wird, nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9249e-152">The interface identified by the  _lpSrcInterface_ parameter is not supported by the object pointed to by  _lpSrcObj_, or the interface identified by the  _lpDestInterface_ parameter is not supported by the object pointed to by  _lpDestObj_.</span></span> 
    
<span data-ttu-id="9249e-153">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="9249e-153">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="9249e-154">Es wurde versucht, auf ein Objekt zu zugreifen, für das der Aufrufer nicht über ausreichende Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="9249e-154">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="9249e-155">Dieser Fehler wird zurückgegeben, wenn das Zielobjekt mit dem Quellobjekt identisch ist.</span><span class="sxs-lookup"><span data-stu-id="9249e-155">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="9249e-156">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9249e-156">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="9249e-157">Der  _lpSrcInterface-Parameter_ ist NULL.</span><span class="sxs-lookup"><span data-stu-id="9249e-157">The  _lpSrcInterface_ parameter is NULL.</span></span> 
    
<span data-ttu-id="9249e-158">Die folgenden Werte können in der **SPropProblemArray-Struktur** zurückgegeben werden, jedoch nicht als Rückgabewerte für **DoCopyTo**.</span><span class="sxs-lookup"><span data-stu-id="9249e-158">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **DoCopyTo**.</span></span> <span data-ttu-id="9249e-159">Diese Fehler gelten für eine einzelne Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="9249e-159">These errors apply to a single property.</span></span>
  
<span data-ttu-id="9249e-160">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="9249e-160">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="9249e-161">Entweder wurde das MAPI_UNICODE festgelegt, und **DoCopyTo** unterstützt unicode nicht, oder MAPI_UNICODE nicht festgelegt, und **DoCopyTo** unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="9249e-161">Either the MAPI_UNICODE flag was set and **DoCopyTo** does not support Unicode, or MAPI_UNICODE was not set and **DoCopyTo** supports only Unicode.</span></span> 
    
<span data-ttu-id="9249e-162">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="9249e-162">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="9249e-163">Die Eigenschaft kann vom Aufrufer nicht geändert werden, da es sich um eine schreibgeschützte Eigenschaft handelt, die vom Besitzer des Zielobjekts berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="9249e-163">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="9249e-164">Dieser Fehler ist nicht schwerwiegender. Der Aufrufer sollte zulassen, dass der Kopiervorgang fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="9249e-164">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="9249e-165">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="9249e-165">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="9249e-166">Der Eigenschaftentyp ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="9249e-166">The property type is invalid.</span></span>
    
<span data-ttu-id="9249e-167">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="9249e-167">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="9249e-168">Der Eigenschaftstyp ist nicht der typ, der vom Aufrufer erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="9249e-168">The property type is not the type expected by the caller.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9249e-169">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9249e-169">Remarks</span></span>

<span data-ttu-id="9249e-170">Die **IMAPISupport::D oCopyTo-Methode** wird für Unterstützungsobjekte des Nachrichtenspeicheranbieters implementiert.</span><span class="sxs-lookup"><span data-stu-id="9249e-170">The **IMAPISupport::DoCopyTo** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="9249e-171">Nachrichtenspeicheranbieter können **DoCopyTo aufrufen,** um die [IMAPIProp::CopyTo-Methode](imapiprop-copyto.md) für ihre Ordner und Nachrichten zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="9249e-171">Message store providers can call **DoCopyTo** to implement the [IMAPIProp::CopyTo](imapiprop-copyto.md) method for their folders and messages.</span></span> 
  
<span data-ttu-id="9249e-172">Standardmäßig kopiert oder verschiebt **DoCopyTo** alle Eigenschaften eines Objekts in ein anderes Objekt.</span><span class="sxs-lookup"><span data-stu-id="9249e-172">By default, **DoCopyTo** copies or moves all of the properties of one object to another object.</span></span> <span data-ttu-id="9249e-173">Alle Unterobjekte im Quellobjekt werden automatisch in den Vorgang einbezogen und vollständig kopiert oder verschoben.</span><span class="sxs-lookup"><span data-stu-id="9249e-173">Any subobjects in the source object are automatically included in the operation and copied or moved in their entirety.</span></span> 
  
<span data-ttu-id="9249e-174">Wenn eine der kopierten oder verschobenen Eigenschaften bereits im Zielobjekt vorhanden ist, werden die vorhandenen Eigenschaften von den neuen Eigenschaften überschrieben, es sei denn, das flag MAPI_NOREPLACE wird im  _ulFlags-Parameter_ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9249e-174">If any of the copied or moved properties already exist in the destination object, the existing properties are overwritten by the new properties, unless the MAPI_NOREPLACE flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="9249e-175">Vorhandene Informationen im Zielobjekt, die nicht überschrieben werden, bleiben unverändert.</span><span class="sxs-lookup"><span data-stu-id="9249e-175">Existing information in the destination object that is not overwritten is left untouched.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9249e-176">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="9249e-176">Notes to callers</span></span>

<span data-ttu-id="9249e-177">Um Eigenschaften aus dem Kopier- oder Verschiebevorgang auszuschließen, schließen Sie ihre Eigenschaftstags in den  _lpExcludeProps-Parameter_ ein.</span><span class="sxs-lookup"><span data-stu-id="9249e-177">To exclude properties from the copy or move operation, include their property tags in the  _lpExcludeProps_ parameter.</span></span> <span data-ttu-id="9249e-178">Wenn Sie die Ergebnisse [](prop_tag.md) der Verwendung des PROP_TAG-Makros übergeben, um ein Eigenschaftentag aus einem bestimmten Bezeichner im Eigenschaftentagarray zu erstellen, werden alle Eigenschaften mit diesem Bezeichner ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="9249e-178">If you pass the results of using the [PROP_TAG](prop_tag.md) macro to build a property tag from a specific identifier in the property tag array, all properties with that identifier will be excluded.</span></span> <span data-ttu-id="9249e-179">Der folgende Eintrag im Eigenschaftentagarray bewirkt beispielsweise, dass alle Eigenschaften mit dem Bezeichner 0x8002 ausgeschlossen werden, unabhängig vom Typ:</span><span class="sxs-lookup"><span data-stu-id="9249e-179">For example, the following entry in the property tag array causes all properties with an identifier of 0x8002 to be excluded, regardless of type:</span></span> 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
<span data-ttu-id="9249e-180">Um zu vermeiden, dass die Zustellungszeit einer Nachricht kopiert wird, wenn Sie die Nachricht in einen anderen Ordner kopieren, geben Sie **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) im #A0 aus.</span><span class="sxs-lookup"><span data-stu-id="9249e-180">To avoid copying a message's delivery time when you copy the message to a different folder, specify **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) in the property tag exclude array.</span></span> <span data-ttu-id="9249e-181">Um die Empfängerliste einer Nachricht auszuschließen, fügen Sie **die PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) -Eigenschaft zum Exclude-Array hinzu.</span><span class="sxs-lookup"><span data-stu-id="9249e-181">To exclude a message's recipient list, add the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property to the exclude array.</span></span> <span data-ttu-id="9249e-182">Zum Ausschließen der Anlagen einer Nachricht fügen Sie **die PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) -Eigenschaft zum Array hinzu.</span><span class="sxs-lookup"><span data-stu-id="9249e-182">To exclude a message's attachments, add the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property to the array.</span></span>
  
<span data-ttu-id="9249e-183">Um das Kopieren oder Verschieben der Hierarchie oder Inhaltstabelle eines Ordners oder Adressbuchcontainers zu verhindern, schließen Sie **auch PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) oder **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in das #A0 ein.</span><span class="sxs-lookup"><span data-stu-id="9249e-183">Similarly, to prevent the copying or moving of a folder or address book container's hierarchy or contents table, include **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in the property tag exclude array.</span></span>
  
<span data-ttu-id="9249e-184">Ignorieren MAPI_E_COMPUTED Fehler, die in der **SPropProblemArray-Struktur** im  _lppProblems-Parameter zurückgegeben_ werden.</span><span class="sxs-lookup"><span data-stu-id="9249e-184">Ignore MAPI_E_COMPUTED errors returned in the **SPropProblemArray** structure in the  _lppProblems_ parameter.</span></span> 
  
<span data-ttu-id="9249e-185">Der Schnittstellenbezeichner, auf den  _lpSrcInterface_ verweist, ist in der Regel identisch mit dem Schnittstellenbezeichner, auf den  _lpDestInterface_ verweist.</span><span class="sxs-lookup"><span data-stu-id="9249e-185">The interface identifier that  _lpSrcInterface_ points to is usually the same as the interface identifier that  _lpDestInterface_ points to.</span></span> 
  
<span data-ttu-id="9249e-186">Wenn Sie einen akzeptablen Schnittstellenbezeichner in  _lpDestInterface,_ aber einen ungültigen Zeiger in  _lpDestObj_ übergeben, sind die Ergebnisse unvorhersehbar.</span><span class="sxs-lookup"><span data-stu-id="9249e-186">If you pass an acceptable interface identifier in  _lpDestInterface_ but an invalid pointer in  _lpDestObj_, the results are unpredictable.</span></span> <span data-ttu-id="9249e-187">Dies wird höchstwahrscheinlich dazu führen, dass Ihr Anbieter fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="9249e-187">Most likely this will cause your provider to fail.</span></span> 
  
<span data-ttu-id="9249e-188">Wenn Ihnen hingegen ergänzende Informationen bekannt sind, die nicht kopiert oder verschoben werden sollten, fügen Sie die Schnittstellenbezeichner für die Schnittstellen hinzu, die im Array ausgeschlossen werden sollen, das im  _rgiidExclude-Parameter_ übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="9249e-188">Conversely, if you are aware of supplemental information that should not be copied or moved, add the interface identifiers for the interfaces to be excluded in the array passed in the  _rgiidExclude_ parameter.</span></span> <span data-ttu-id="9249e-189">Wenn Sie z. B. Nachrichten kopieren, aber keine ihrer Nachrichtenanlagen, übergeben Sie IID_IMessage im _rgiidExclude-Array._</span><span class="sxs-lookup"><span data-stu-id="9249e-189">For example, if you are copying messages, but not any of their message attachments, pass IID_IMessage in the  _rgiidExclude_ array.</span></span> <span data-ttu-id="9249e-190">**DoCopyTo** ignoriert alle in  _rgiidExclude_ aufgeführten Schnittstellen, die nicht erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="9249e-190">**DoCopyTo** ignores any interfaces listed in  _rgiidExclude_ that it does not recognize.</span></span> 
  
<span data-ttu-id="9249e-191">Wenn Sie den  _Parameter rgiidExclude_ verwenden, um eine Schnittstelle auszuschließen, werden auch alle von dieser Schnittstelle abgeleiteten Schnittstellen ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="9249e-191">When you use the  _rgiidExclude_ parameter to exclude an interface, it also excludes all interfaces derived from that interface.</span></span> <span data-ttu-id="9249e-192">Wenn Sie beispielsweise die [IMAPIContainer-Schnittstelle](imapicontainerimapiprop.md) ausschließen, werden Ordner oder Adressbuchcontainer je nach Anbietertyp ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="9249e-192">For example, excluding the [IMAPIContainer](imapicontainerimapiprop.md) interface causes folders or address book containers to be excluded, depending on the type of provider.</span></span> <span data-ttu-id="9249e-193">Schließen Sie [IMAPIProp](imapipropiunknown.md) oder [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) nicht aus, da so viele Schnittstellen von ihnen stammen.</span><span class="sxs-lookup"><span data-stu-id="9249e-193">Do not exclude [IMAPIProp](imapipropiunknown.md) or [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) because so many interfaces derive from them.</span></span> 
  
 <span data-ttu-id="9249e-194">**DoCopyTo** meldet globale Fehler, die für den gesamten Vorgang gelten, und einzelne Fehler, die für einzelne Eigenschaften gelten.</span><span class="sxs-lookup"><span data-stu-id="9249e-194">**DoCopyTo** reports global errors that apply to the operation as a whole, and individual errors that apply to individual properties.</span></span> <span data-ttu-id="9249e-195">Diese einzelnen Fehler werden in einer **SPropProblemArray-Struktur** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9249e-195">These individual errors are put in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="9249e-196">Sie können die Fehlerberichterstellung auf Eigenschaftsebene unterdrücken, indem Sie NULL anstelle eines gültigen Zeigers für den Parameter für die Arraystruktur des Eigenschaftsproblems übergeben.</span><span class="sxs-lookup"><span data-stu-id="9249e-196">You can suppress error reporting at the property level by passing NULL, rather than a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="9249e-197">Wenn Sie Informationen zu Fehlern erhalten möchten, übergeben Sie einen gültigen **SPropProblemArray-Strukturzeiger** im _lppProblems-Parameter._</span><span class="sxs-lookup"><span data-stu-id="9249e-197">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="9249e-198">Wenn **DoCopyTo** S_OK, suchen Sie nach möglichen Fehlern mit einzelnen Eigenschaften in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="9249e-198">When **DoCopyTo** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="9249e-199">Wenn **DoCopyTo** einen Fehler zurückgibt, werden keine Informationen in der **SPropProblemArray-Struktur** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9249e-199">When **DoCopyTo** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="9249e-200">Rufen Sie stattdessen die [IMAPISupport::GetLastError-Methode](imapisupport-getlasterror.md) auf, um detaillierte Fehlerinformationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9249e-200">Instead, call the [IMAPISupport::GetLastError](imapisupport-getlasterror.md) method to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="9249e-201">Wenn **DoCopyTo** S_OK zurückgibt, geben Sie die zurückgegebene **SPropProblemArray-Struktur** frei, indem Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9249e-201">If **DoCopyTo** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="9249e-202">Wenn beim **DoCopyTo-Aufruf** ein globaler Fehler auftritt, verwenden oder geben Sie die **SPropProblemArray-Struktur nicht** frei.</span><span class="sxs-lookup"><span data-stu-id="9249e-202">If a global error occurs on the **DoCopyTo** call, do not use or free the **SPropProblemArray** structure.</span></span> <span data-ttu-id="9249e-203">Anbieter sollten das _ulIndex-Element_ in den von **DoCopyTo** zurückgegebenen **SPropProblemArray-Strukturen** ignorieren.</span><span class="sxs-lookup"><span data-stu-id="9249e-203">Providers should ignore the  _ulIndex_ member in **SPropProblemArray** structures returned by **DoCopyTo**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9249e-204">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9249e-204">See also</span></span>



[<span data-ttu-id="9249e-205">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="9249e-205">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
  
[<span data-ttu-id="9249e-206">IMAPISupport::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="9249e-206">IMAPISupport::CopyFolder</span></span>](imapisupport-copyfolder.md)
  
[<span data-ttu-id="9249e-207">IMAPISupport::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="9249e-207">IMAPISupport::CopyMessages</span></span>](imapisupport-copymessages.md)
  
[<span data-ttu-id="9249e-208">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="9249e-208">IMAPISupport::GetLastError</span></span>](imapisupport-getlasterror.md)
  
[<span data-ttu-id="9249e-209">PidTagContainerContents (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9249e-209">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="9249e-210">PidTagContainerHierarchy (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9249e-210">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="9249e-211">PidTagMessageAttachments (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9249e-211">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="9249e-212">PidTagMessageDeliveryTime (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9249e-212">PidTagMessageDeliveryTime Canonical Property</span></span>](pidtagmessagedeliverytime-canonical-property.md)
  
[<span data-ttu-id="9249e-213">PidTagMessageRecipients (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9249e-213">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="9249e-214">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="9249e-214">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="9249e-215">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="9249e-215">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="9249e-216">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="9249e-216">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

