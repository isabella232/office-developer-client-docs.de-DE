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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1040a0730c4b26b51d3c2b7763488502b2c5323c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792377"
---
# <a name="imapisupportdocopyto"></a><span data-ttu-id="b61c4-103">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="b61c4-103">IMAPISupport::DoCopyTo</span></span>

  
  
<span data-ttu-id="b61c4-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b61c4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b61c4-105">Kopiert oder verschiebt alle Eigenschaften eines Objekts, mit Ausnahme von speziell Ausgeschlossene Eigenschaften in ein anderes Objekt.</span><span class="sxs-lookup"><span data-stu-id="b61c4-105">Copies or moves all properties of one object, except for specifically excluded properties, to another object.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="b61c4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b61c4-106">Parameters</span></span>

 <span data-ttu-id="b61c4-107">_lpSrcInterface_</span><span class="sxs-lookup"><span data-stu-id="b61c4-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="b61c4-108">[in] Ein Zeiger auf die Schnittstelle-ID (IID), die stellt die Schnittstelle dar, die verwendet werden, um das Objekt zuzugreifen, die über die Eigenschaften, kopiert oder verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="b61c4-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object that has the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="b61c4-109">_lpSrcObj_</span><span class="sxs-lookup"><span data-stu-id="b61c4-109">_lpSrcObj_</span></span>
  
> <span data-ttu-id="b61c4-110">[in] Ein Zeiger auf das Objekt, das die Eigenschaften kopiert oder verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="b61c4-110">[in] A pointer to the object that has the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="b61c4-111">_ciidExclude_</span><span class="sxs-lookup"><span data-stu-id="b61c4-111">_ciidExclude_</span></span>
  
> <span data-ttu-id="b61c4-112">[in] Die Anzahl der Schnittstellen zum ausschließen, wenn Sie kopieren oder verschieben Sie Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b61c4-112">[in] The count of interfaces to exclude when you copy or move properties.</span></span>
    
 <span data-ttu-id="b61c4-113">_rgiidExclude_</span><span class="sxs-lookup"><span data-stu-id="b61c4-113">_rgiidExclude_</span></span>
  
> <span data-ttu-id="b61c4-114">[in] Ein Array mit den IDs der Schnittstelle, Schnittstellen angibt, die beim Kopieren oder verschieben zusätzliche Informationen zum Zielobjekt nicht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b61c4-114">[in] An array of interface identifiers that indicates interfaces that should not be used when you copy or move supplemental information to the destination object.</span></span>
    
 <span data-ttu-id="b61c4-115">_lpExcludeProps_</span><span class="sxs-lookup"><span data-stu-id="b61c4-115">_lpExcludeProps_</span></span>
  
> <span data-ttu-id="b61c4-116">[in] Ein Zeiger auf einen Tag Array-Eigenschaft, die die Eigenschaftentags identifiziert, die von der Kopie ausgeschlossen werden soll oder verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="b61c4-116">[in] A pointer to a property tag array that identifies the property tags that should be excluded from the copy or move operation.</span></span> <span data-ttu-id="b61c4-117">Übergeben von NULL in der _LpExcludeProps_ -Parameter gibt an, dass alle Eigenschaften des Objekts kopiert oder verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="b61c4-117">Passing NULL in the  _lpExcludeProps_ parameter indicates that all of the object's properties should be copied or moved.</span></span> <span data-ttu-id="b61c4-118">**DoCopyTo** zurückgegeben, dass MAPI_E_INVALID_PARAMETER, wenn das **cValues** Mitglied der [SPropTagArray](sproptagarray.md) -Struktur mit _LpExcludeProps_ gezeigt auf 0 gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="b61c4-118">**DoCopyTo** returns MAPI_E_INVALID_PARAMETER when the **cValues** member of the [SPropTagArray](sproptagarray.md) structure pointed to by  _lpExcludeProps_ is set to 0.</span></span> 
    
 <span data-ttu-id="b61c4-119">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="b61c4-119">_ulUIParam_</span></span>
  
> <span data-ttu-id="b61c4-120">[in] Ein Handle für das übergeordnete Fenster der Statusanzeige.</span><span class="sxs-lookup"><span data-stu-id="b61c4-120">[in] A handle to the parent window of the progress indicator.</span></span> 
    
 <span data-ttu-id="b61c4-121">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="b61c4-121">_lpProgress_</span></span>
  
> <span data-ttu-id="b61c4-122">[in] Ein Zeiger auf eine Implementierung der Fortschritt-Symbol.</span><span class="sxs-lookup"><span data-stu-id="b61c4-122">[in] A pointer to a progress indicator implementation.</span></span> <span data-ttu-id="b61c4-123">Wenn NULL in der _LpProgress_ -Parameter übergeben wird, wird die Implementierung des Fortschritts von MAPI bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="b61c4-123">If NULL is passed in the  _lpProgress_ parameter, MAPI provides the progress implementation.</span></span> <span data-ttu-id="b61c4-124">Der Parameter _LpProgress_ wird ignoriert, es sei denn, das Flag MAPI_DIALOG im _UlFlags_ -Parameter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b61c4-124">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="b61c4-125">_lpDestInterface_</span><span class="sxs-lookup"><span data-stu-id="b61c4-125">_lpDestInterface_</span></span>
  
> <span data-ttu-id="b61c4-126">[in] Ein Zeiger auf die Schnittstellenbezeichner, der die Schnittstelle für das Objekt, um die kopierte oder verschobenen Eigenschaften erhalten Zugriff auf verwendet werden darstellt.</span><span class="sxs-lookup"><span data-stu-id="b61c4-126">[in] A pointer to the interface identifier that represents the interface to be used to access the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="b61c4-127">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="b61c4-127">_lpDestObj_</span></span>
  
> <span data-ttu-id="b61c4-128">[in] Ein Zeiger auf das Objekt, das die Eigenschaften kopierten oder verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="b61c4-128">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="b61c4-129">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b61c4-129">_ulFlags_</span></span>
  
> <span data-ttu-id="b61c4-130">[in] Eine Bitmaske aus Flags, die den Vorgang kopieren oder verschieben steuert.</span><span class="sxs-lookup"><span data-stu-id="b61c4-130">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="b61c4-131">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="b61c4-131">The following flags can be set:</span></span>
    
<span data-ttu-id="b61c4-132">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="b61c4-132">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="b61c4-133">Eine Statusanzeige angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b61c4-133">Displays a progress indicator.</span></span> 
    
<span data-ttu-id="b61c4-134">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="b61c4-134">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="b61c4-135">**DoCopyTo** sollte einen Verschiebevorgang anstatt einen Kopiervorgang ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b61c4-135">**DoCopyTo** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="b61c4-136">Wenn dieses Flag nicht festgelegt ist, führt **DoCopyTo** durch einen Kopiervorgang.</span><span class="sxs-lookup"><span data-stu-id="b61c4-136">When this flag is not set, **DoCopyTo** performs a copy operation.</span></span> 
    
<span data-ttu-id="b61c4-137">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="b61c4-137">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="b61c4-138">Vorhandene Eigenschaften im Zielobjekt sollte nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="b61c4-138">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="b61c4-139">Wenn dieses Flag nicht festgelegt ist, überschreibt **DoCopyTo** vorhandene Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b61c4-139">When this flag is not set, **DoCopyTo** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="b61c4-140">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="b61c4-140">_lppProblems_</span></span>
  
> <span data-ttu-id="b61c4-141">[out] Bei Eingabe einen Zeiger auf einen Zeiger auf eine [SPropProblemArray](spropproblemarray.md) -Struktur. andernfalls NULL, gibt keine Notwendigkeit zur Fehlerinformationen an.</span><span class="sxs-lookup"><span data-stu-id="b61c4-141">[out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, which indicates no need for error information.</span></span> <span data-ttu-id="b61c4-142">Wenn _LppProblems_ einen gültigen Zeiger für die Eingabe ist, gibt **DoCopyTo** ausführliche Informationen zu Fehlern in eine oder mehrere Eigenschaften kopieren.</span><span class="sxs-lookup"><span data-stu-id="b61c4-142">If  _lppProblems_ is a valid pointer on input, **DoCopyTo** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b61c4-143">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="b61c4-143">Return value</span></span>

<span data-ttu-id="b61c4-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="b61c4-144">S_OK</span></span> 
  
> <span data-ttu-id="b61c4-145">Die Eigenschaften haben erfolgreich kopiert oder verschoben.</span><span class="sxs-lookup"><span data-stu-id="b61c4-145">The properties have been successfully copied or moved.</span></span>
    
<span data-ttu-id="b61c4-146">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="b61c4-146">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="b61c4-147">Eine Eigenschaft, die kopiert oder verschoben bereits vorhanden ist, im Zielobjekt, und das Flag MAPI_NOREPLACE festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b61c4-147">A property to be copied or moved already exists in the destination object and the MAPI_NOREPLACE flag is set.</span></span> 
    
<span data-ttu-id="b61c4-148">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="b61c4-148">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="b61c4-149">Das Source-Objekt enthält direkt oder indirekt Zielobjekt.</span><span class="sxs-lookup"><span data-stu-id="b61c4-149">The source object directly or indirectly contains the destination object.</span></span> <span data-ttu-id="b61c4-150">Erhebliche Arbeit möglicherweise durchgeführt wurden, bevor diese Bedingung ermittelt wurde, damit die Quell- und Ziel-Objekte teilweise geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="b61c4-150">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="b61c4-151">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="b61c4-151">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="b61c4-152">Die Schnittstelle, die vom _LpSrcInterface_ -Parameter wird nicht unterstützt, durch das Objekt, auf das _LpSrcObj_oder die Schnittstelle, die vom _LpDestInterface_ -Parameter wird durch das auf den _LpDestObj-Objekt nicht unterstützt _.</span><span class="sxs-lookup"><span data-stu-id="b61c4-152">The interface identified by the  _lpSrcInterface_ parameter is not supported by the object pointed to by  _lpSrcObj_, or the interface identified by the  _lpDestInterface_ parameter is not supported by the object pointed to by  _lpDestObj_.</span></span> 
    
<span data-ttu-id="b61c4-153">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="b61c4-153">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="b61c4-154">Es wurde versucht, auf ein Objekt zuzugreifen, für den der Anrufer nicht über ausreichende Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="b61c4-154">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="b61c4-155">Dieser Fehler wird zurückgegeben, wenn Zielobjekt Quellobjekt identisch ist.</span><span class="sxs-lookup"><span data-stu-id="b61c4-155">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="b61c4-156">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b61c4-156">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="b61c4-157">Der Parameter _LpSrcInterface_ ist NULL.</span><span class="sxs-lookup"><span data-stu-id="b61c4-157">The  _lpSrcInterface_ parameter is NULL.</span></span> 
    
<span data-ttu-id="b61c4-158">Die folgenden Werte können in der Struktur **SPropProblemArray** , aber nicht als Rückgabewerte für **DoCopyTo**zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="b61c4-158">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **DoCopyTo**.</span></span> <span data-ttu-id="b61c4-159">Diese Fehler gelten für eine einzelne Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b61c4-159">These errors apply to a single property.</span></span>
  
<span data-ttu-id="b61c4-160">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="b61c4-160">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="b61c4-161">Entweder die Option MAPI_UNICODE festgelegt wurde und **DoCopyTo** unterstützt keine Unicode oder Parameter MAPI_UNICODE wurde nicht festgelegt und **DoCopyTo** nur Unicode unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b61c4-161">Either the MAPI_UNICODE flag was set and **DoCopyTo** does not support Unicode, or MAPI_UNICODE was not set and **DoCopyTo** supports only Unicode.</span></span> 
    
<span data-ttu-id="b61c4-162">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="b61c4-162">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="b61c4-163">Die Eigenschaft kann nicht vom Anrufer geändert werden, da es eine schreibgeschützte Eigenschaft, mit der Besitzer des Zielobjekts berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="b61c4-163">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="b61c4-164">Dieser Fehler ist nicht schwerwiegend. der Aufrufer sollte den Kopiervorgang fortgesetzt zulassen.</span><span class="sxs-lookup"><span data-stu-id="b61c4-164">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="b61c4-165">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="b61c4-165">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="b61c4-166">Der Eigenschaftstyp ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="b61c4-166">The property type is invalid.</span></span>
    
<span data-ttu-id="b61c4-167">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="b61c4-167">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="b61c4-168">Der Eigenschaftentyp ist nicht vom Anrufer erwartet.</span><span class="sxs-lookup"><span data-stu-id="b61c4-168">The property type is not the type expected by the caller.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b61c4-169">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b61c4-169">Remarks</span></span>

<span data-ttu-id="b61c4-170">Die **IMAPISupport::DoCopyTo** -Methode wird für Message Store Anbieter Unterstützungsobjekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="b61c4-170">The **IMAPISupport::DoCopyTo** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="b61c4-171">Nachricht Anbieter können **DoCopyTo** zum Implementieren der [IMAPIProp::CopyTo](imapiprop-copyto.md) -Methode für ihre Ordner und Nachrichten aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b61c4-171">Message store providers can call **DoCopyTo** to implement the [IMAPIProp::CopyTo](imapiprop-copyto.md) method for their folders and messages.</span></span> 
  
<span data-ttu-id="b61c4-172">In der Standardeinstellung **DoCopyTo** kopiert oder verschiebt alle Eigenschaften eines Objekts in ein anderes Objekt.</span><span class="sxs-lookup"><span data-stu-id="b61c4-172">By default, **DoCopyTo** copies or moves all of the properties of one object to another object.</span></span> <span data-ttu-id="b61c4-173">Alle Unterobjekte im Quellobjekt werden vollständig automatisch bei der Konflikte enthalten und kopiert oder verschoben.</span><span class="sxs-lookup"><span data-stu-id="b61c4-173">Any subobjects in the source object are automatically included in the operation and copied or moved in their entirety.</span></span> 
  
<span data-ttu-id="b61c4-174">Wenn die kopierte oder verschobenen Eigenschaften bereits im Zielobjekt vorhanden sind, werden die vorhandenen Eigenschaften von den Eigenschaften der neuen überschrieben, wenn das Flag MAPI_NOREPLACE im _UlFlags_ -Parameter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b61c4-174">If any of the copied or moved properties already exist in the destination object, the existing properties are overwritten by the new properties, unless the MAPI_NOREPLACE flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="b61c4-175">Vorhandene Informationen im Zielobjekt, das nicht überschrieben wird, bleibt unverändert.</span><span class="sxs-lookup"><span data-stu-id="b61c4-175">Existing information in the destination object that is not overwritten is left untouched.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b61c4-176">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="b61c4-176">Notes to callers</span></span>

<span data-ttu-id="b61c4-177">Ausschließen von Eigenschaften aus der Kopie oder Verschiebevorgang, deren Eigenschaftentags im _LpExcludeProps_ -Parameter enthalten.</span><span class="sxs-lookup"><span data-stu-id="b61c4-177">To exclude properties from the copy or move operation, include their property tags in the  _lpExcludeProps_ parameter.</span></span> <span data-ttu-id="b61c4-178">Wenn Sie die Ergebnisse der Verwendung von Makros [PROP_TAG](prop_tag.md) zum Erstellen einer Eigenschaftentag aus einem bestimmten Kennzeichen im Array Tag-Eigenschaft übergeben wird, werden alle Eigenschaften mit diesem Bezeichner ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="b61c4-178">If you pass the results of using the [PROP_TAG](prop_tag.md) macro to build a property tag from a specific identifier in the property tag array, all properties with that identifier will be excluded.</span></span> <span data-ttu-id="b61c4-179">Der folgende Eintrag im Array Tag-Eigenschaft bewirkt beispielsweise alle Eigenschaften mit der ID 0x8002, ausgeschlossen werden sollen, unabhängig vom Typ:</span><span class="sxs-lookup"><span data-stu-id="b61c4-179">For example, the following entry in the property tag array causes all properties with an identifier of 0x8002 to be excluded, regardless of type:</span></span> 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
<span data-ttu-id="b61c4-180">Geben Sie zum Vermeiden von Zeitaufwands für die Bereitstellung einer Nachricht, wenn Sie die Nachricht auf einen anderen Ordner kopieren, kopieren **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) die Array-Eigenschaft Tag ausschließen.</span><span class="sxs-lookup"><span data-stu-id="b61c4-180">To avoid copying a message's delivery time when you copy the message to a different folder, specify **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) in the property tag exclude array.</span></span> <span data-ttu-id="b61c4-181">Um eine Nachricht Empfängerliste auszuschließen, fügen Sie die **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))-Eigenschaft dem Exclude-Array.</span><span class="sxs-lookup"><span data-stu-id="b61c4-181">To exclude a message's recipient list, add the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property to the exclude array.</span></span> <span data-ttu-id="b61c4-182">Um eine e-Mail-Anlagen auszuschließen, fügen Sie die **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))-Eigenschaft dem Array hinzu.</span><span class="sxs-lookup"><span data-stu-id="b61c4-182">To exclude a message's attachments, add the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property to the array.</span></span>
  
<span data-ttu-id="b61c4-183">Auf ähnliche Weise, um das Kopieren oder Verschieben eines Ordners oder Adressbuchcontainer des Hierarchie oder Inhaltstabelle zu verhindern, schließen Sie **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) oder **PR_CONTAINER_CONTENTS** ([ PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in der Eigenschaft Tag Array ausschließen.</span><span class="sxs-lookup"><span data-stu-id="b61c4-183">Similarly, to prevent the copying or moving of a folder or address book container's hierarchy or contents table, include **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in the property tag exclude array.</span></span>
  
<span data-ttu-id="b61c4-184">Ignorieren Sie MAPI_E_COMPUTED Fehler in der Struktur **SPropProblemArray** im _LppProblems_ -Parameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b61c4-184">Ignore MAPI_E_COMPUTED errors returned in the **SPropProblemArray** structure in the  _lppProblems_ parameter.</span></span> 
  
<span data-ttu-id="b61c4-185">Der Schnittstellenbezeichner, die _LpSrcInterface_ verweist, ist in der Regel identisch mit der Identifier, _LpDestInterface_ verweist.</span><span class="sxs-lookup"><span data-stu-id="b61c4-185">The interface identifier that  _lpSrcInterface_ points to is usually the same as the interface identifier that  _lpDestInterface_ points to.</span></span> 
  
<span data-ttu-id="b61c4-186">Wenn Sie einen Schnittstellenbezeichner akzeptable in _LpDestInterface_ , aber ein ungültiger Zeiger in _LpDestObj_übergeben, sind die Ergebnisse unvorhersehbar.</span><span class="sxs-lookup"><span data-stu-id="b61c4-186">If you pass an acceptable interface identifier in  _lpDestInterface_ but an invalid pointer in  _lpDestObj_, the results are unpredictable.</span></span> <span data-ttu-id="b61c4-187">In den meisten Fällen bewirkt dies vom Dienstanbieter ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="b61c4-187">Most likely this will cause your provider to fail.</span></span> 
  
<span data-ttu-id="b61c4-188">Umgekehrt, wenn Sie zusätzliche Informationen, die nicht kopiert oder verschoben werden soll kennen, fügen Sie die als Schnittstellenbezeichner für die Schnittstellen, die in der _RgiidExclude_ -Parameter übergebenen Arrays ausgeschlossen werden hinzu.</span><span class="sxs-lookup"><span data-stu-id="b61c4-188">Conversely, if you are aware of supplemental information that should not be copied or moved, add the interface identifiers for the interfaces to be excluded in the array passed in the  _rgiidExclude_ parameter.</span></span> <span data-ttu-id="b61c4-189">Wenn Sie Nachrichten, aber keine ihrer e-Mail-Anlagen kopieren, übergeben Sie IID_IMessage im Array _RgiidExclude_ fest.</span><span class="sxs-lookup"><span data-stu-id="b61c4-189">For example, if you are copying messages, but not any of their message attachments, pass IID_IMessage in the  _rgiidExclude_ array.</span></span> <span data-ttu-id="b61c4-190">**DoCopyTo** ignoriert Schnittstellen, die in _RgiidExclude_ , die es nicht erkennt aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="b61c4-190">**DoCopyTo** ignores any interfaces listed in  _rgiidExclude_ that it does not recognize.</span></span> 
  
<span data-ttu-id="b61c4-191">Wenn Sie den Parameter _RgiidExclude_ verwenden, um eine Schnittstelle auszuschließen, werden auch alle Schnittstellen, die von dieser Schnittstelle abgeleitet ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="b61c4-191">When you use the  _rgiidExclude_ parameter to exclude an interface, it also excludes all interfaces derived from that interface.</span></span> <span data-ttu-id="b61c4-192">Die Schnittstelle [IMAPIContainer](imapicontainerimapiprop.md) ausschließen bewirkt beispielsweise, dass Ordner oder Adresse Adressbuch-Container, je nach den Typ des Anbieters ausgeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b61c4-192">For example, excluding the [IMAPIContainer](imapicontainerimapiprop.md) interface causes folders or address book containers to be excluded, depending on the type of provider.</span></span> <span data-ttu-id="b61c4-193">Schließen Sie keine [IMAPIProp](imapipropiunknown.md) oder [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) , da so viele Schnittstellen, die von ihnen abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="b61c4-193">Do not exclude [IMAPIProp](imapipropiunknown.md) or [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) because so many interfaces derive from them.</span></span> 
  
 <span data-ttu-id="b61c4-194">**DoCopyTo** meldet globale Fehlern, die für den Vorgang als Ganzes gelten und einzelnen Fehler, die für die einzelnen Eigenschaften gelten.</span><span class="sxs-lookup"><span data-stu-id="b61c4-194">**DoCopyTo** reports global errors that apply to the operation as a whole, and individual errors that apply to individual properties.</span></span> <span data-ttu-id="b61c4-195">Diese einzelnen Fehler werden in einer **SPropProblemArray** eingefügt.</span><span class="sxs-lookup"><span data-stu-id="b61c4-195">These individual errors are put in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="b61c4-196">Sie können die Fehlerberichterstattung Ebene der Eigenschaft, indem Sie NULL, statt dass ein gültiger Zeiger, für den Parameter Property Problem Array Struktur übergeben unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="b61c4-196">You can suppress error reporting at the property level by passing NULL, rather than a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="b61c4-197">Wenn Sie Informationen zu Fehlern erhalten möchten, übergeben Sie einen gültigen **SPropProblemArray** Struktur Zeiger des _LppProblems_ -Parameters.</span><span class="sxs-lookup"><span data-stu-id="b61c4-197">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="b61c4-198">Wenn **DoCopyTo** S_OK zurückgegeben wird, überprüfen Sie auf mögliche Fehler mit einzelnen Eigenschaften in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="b61c4-198">When **DoCopyTo** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="b61c4-199">Wenn **DoCopyTo** einen Fehler zurückgibt, wird keine Informationen in der Struktur **SPropProblemArray** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b61c4-199">When **DoCopyTo** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="b61c4-200">Rufen Sie stattdessen die [IMAPISupport::GetLastError](imapisupport-getlasterror.md) -Methode, um ausführliche Fehlerinformationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b61c4-200">Instead, call the [IMAPISupport::GetLastError](imapisupport-getlasterror.md) method to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="b61c4-201">Wenn **DoCopyTo** S_OK zurückgibt, frei die zurückgegebene Struktur **SPropProblemArray** durch Aufrufen der [MAPIFreeBuffer](mapifreebuffer.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="b61c4-201">If **DoCopyTo** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="b61c4-202">Wenn bei der **DoCopyTo** Aufruf ein globaler Fehler auftritt, nicht verwenden oder die Struktur **SPropProblemArray** frei.</span><span class="sxs-lookup"><span data-stu-id="b61c4-202">If a global error occurs on the **DoCopyTo** call, do not use or free the **SPropProblemArray** structure.</span></span> <span data-ttu-id="b61c4-203">Anbieter sollte das _UlIndex_ -Element in **SPropProblemArray** Strukturen zurückgegebene **DoCopyTo**ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="b61c4-203">Providers should ignore the  _ulIndex_ member in **SPropProblemArray** structures returned by **DoCopyTo**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b61c4-204">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b61c4-204">See also</span></span>



[<span data-ttu-id="b61c4-205">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="b61c4-205">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
  
[<span data-ttu-id="b61c4-206">IMAPISupport::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="b61c4-206">IMAPISupport::CopyFolder</span></span>](imapisupport-copyfolder.md)
  
[<span data-ttu-id="b61c4-207">IMAPISupport::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="b61c4-207">IMAPISupport::CopyMessages</span></span>](imapisupport-copymessages.md)
  
[<span data-ttu-id="b61c4-208">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="b61c4-208">IMAPISupport::GetLastError</span></span>](imapisupport-getlasterror.md)
  
[<span data-ttu-id="b61c4-209">PidTagContainerContents (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b61c4-209">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="b61c4-210">PidTagContainerHierarchy (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b61c4-210">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="b61c4-211">PidTagMessageAttachments (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b61c4-211">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="b61c4-212">PidTagMessageDeliveryTime (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b61c4-212">PidTagMessageDeliveryTime Canonical Property</span></span>](pidtagmessagedeliverytime-canonical-property.md)
  
[<span data-ttu-id="b61c4-213">PidTagMessageRecipients (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b61c4-213">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="b61c4-214">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="b61c4-214">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="b61c4-215">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="b61c4-215">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="b61c4-216">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b61c4-216">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

