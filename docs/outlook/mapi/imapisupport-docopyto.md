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
# <a name="imapisupportdocopyto"></a><span data-ttu-id="cac51-103">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="cac51-103">IMAPISupport::DoCopyTo</span></span>

  
  
<span data-ttu-id="cac51-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cac51-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cac51-105">Kopiert oder verschiebt alle Eigenschaften eines Objekts, mit Ausnahme der explizit ausgeschlossenen Eigenschaften, in ein anderes Objekt.</span><span class="sxs-lookup"><span data-stu-id="cac51-105">Copies or moves all properties of one object, except for specifically excluded properties, to another object.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="cac51-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cac51-106">Parameters</span></span>

 <span data-ttu-id="cac51-107">_lpSrcInterface_</span><span class="sxs-lookup"><span data-stu-id="cac51-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="cac51-108">in Ein Zeiger auf die Schnittstellen-ID (IID), die die Schnittstelle darstellt, die für den Zugriff auf das Objekt verwendet werden soll, das über die Eigenschaften verfügt, die kopiert oder verschoben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cac51-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object that has the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="cac51-109">_lpSrcObj_</span><span class="sxs-lookup"><span data-stu-id="cac51-109">_lpSrcObj_</span></span>
  
> <span data-ttu-id="cac51-110">in Ein Zeiger auf das Objekt, das die Eigenschaften enthält, die kopiert oder verschoben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cac51-110">[in] A pointer to the object that has the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="cac51-111">_ciidExclude_</span><span class="sxs-lookup"><span data-stu-id="cac51-111">_ciidExclude_</span></span>
  
> <span data-ttu-id="cac51-112">in Die Anzahl von Schnittstellen, die beim Kopieren oder Verschieben von Eigenschaften ausgeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cac51-112">[in] The count of interfaces to exclude when you copy or move properties.</span></span>
    
 <span data-ttu-id="cac51-113">_rgiidExclude_</span><span class="sxs-lookup"><span data-stu-id="cac51-113">_rgiidExclude_</span></span>
  
> <span data-ttu-id="cac51-114">in Ein Array von Schnittstellen Bezeichnern, das Schnittstellen angibt, die beim Kopieren oder verschieben zusätzlicher Informationen in das Zielobjekt nicht verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cac51-114">[in] An array of interface identifiers that indicates interfaces that should not be used when you copy or move supplemental information to the destination object.</span></span>
    
 <span data-ttu-id="cac51-115">_lpExcludeProps_</span><span class="sxs-lookup"><span data-stu-id="cac51-115">_lpExcludeProps_</span></span>
  
> <span data-ttu-id="cac51-116">in Ein Zeiger auf ein Property-Tag-Array, das die Eigenschaftentags identifiziert, die vom Kopier-oder Verschiebungsvorgang ausgeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cac51-116">[in] A pointer to a property tag array that identifies the property tags that should be excluded from the copy or move operation.</span></span> <span data-ttu-id="cac51-117">Das übergeben von NULL im _lpExcludeProps_ -Parameter gibt an, dass alle Eigenschaften des Objekts kopiert oder verschoben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cac51-117">Passing NULL in the  _lpExcludeProps_ parameter indicates that all of the object's properties should be copied or moved.</span></span> <span data-ttu-id="cac51-118">**DoCopyTo** gibt MAPI_E_INVALID_PARAMETER zurück, wenn das **cValues** -Element der [SPropTagArray](sproptagarray.md) -Struktur, auf die durch _lpExcludeProps_ verwiesen wird, auf 0 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="cac51-118">**DoCopyTo** returns MAPI_E_INVALID_PARAMETER when the **cValues** member of the [SPropTagArray](sproptagarray.md) structure pointed to by  _lpExcludeProps_ is set to 0.</span></span> 
    
 <span data-ttu-id="cac51-119">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="cac51-119">_ulUIParam_</span></span>
  
> <span data-ttu-id="cac51-120">in Ein Handle für das übergeordnete Fenster der Statusanzeige.</span><span class="sxs-lookup"><span data-stu-id="cac51-120">[in] A handle to the parent window of the progress indicator.</span></span> 
    
 <span data-ttu-id="cac51-121">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="cac51-121">_lpProgress_</span></span>
  
> <span data-ttu-id="cac51-122">in Ein Zeiger auf eine Statusindikator-Implementierung.</span><span class="sxs-lookup"><span data-stu-id="cac51-122">[in] A pointer to a progress indicator implementation.</span></span> <span data-ttu-id="cac51-123">Wenn NULL im _lpProgress_ -Parameter übergeben wird, stellt MAPI die Status Implementierung bereit.</span><span class="sxs-lookup"><span data-stu-id="cac51-123">If NULL is passed in the  _lpProgress_ parameter, MAPI provides the progress implementation.</span></span> <span data-ttu-id="cac51-124">Der _lpProgress_ -Parameter wird ignoriert, es sei denn, das MAPI_DIALOG-Flag wird im _ulFlags_ -Parameter festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cac51-124">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="cac51-125">_lpDestInterface_</span><span class="sxs-lookup"><span data-stu-id="cac51-125">_lpDestInterface_</span></span>
  
> <span data-ttu-id="cac51-126">in Ein Zeiger auf den Schnittstellenbezeichner, der die Schnittstelle darstellt, die für den Zugriff auf das Objekt zum Abrufen der kopierten oder verschobenen Eigenschaften verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cac51-126">[in] A pointer to the interface identifier that represents the interface to be used to access the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="cac51-127">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="cac51-127">_lpDestObj_</span></span>
  
> <span data-ttu-id="cac51-128">in Ein Zeiger auf das Objekt, das die kopierten oder verschobenen Eigenschaften empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="cac51-128">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="cac51-129">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cac51-129">_ulFlags_</span></span>
  
> <span data-ttu-id="cac51-130">in Eine Bitmaske von Flags, die den Kopier-oder Verschiebungsvorgang steuert.</span><span class="sxs-lookup"><span data-stu-id="cac51-130">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="cac51-131">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="cac51-131">The following flags can be set:</span></span>
    
<span data-ttu-id="cac51-132">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="cac51-132">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="cac51-133">Zeigt eine Statusanzeige an.</span><span class="sxs-lookup"><span data-stu-id="cac51-133">Displays a progress indicator.</span></span> 
    
<span data-ttu-id="cac51-134">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="cac51-134">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="cac51-135">**DoCopyTo** sollte anstelle eines Kopiervorgangs einen Verschiebungsvorgang ausführen.</span><span class="sxs-lookup"><span data-stu-id="cac51-135">**DoCopyTo** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="cac51-136">Wenn dieses Flag nicht festgelegt ist, führt **DoCopyTo** einen Kopiervorgang aus.</span><span class="sxs-lookup"><span data-stu-id="cac51-136">When this flag is not set, **DoCopyTo** performs a copy operation.</span></span> 
    
<span data-ttu-id="cac51-137">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="cac51-137">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="cac51-138">Vorhandene Eigenschaften im Zielobjekt sollten nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="cac51-138">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="cac51-139">Wenn dieses Flag nicht festgelegt ist, überschreibt **DoCopyTo** vorhandene Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cac51-139">When this flag is not set, **DoCopyTo** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="cac51-140">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="cac51-140">_lppProblems_</span></span>
  
> <span data-ttu-id="cac51-141">Out Bei der Eingabe ein Zeiger auf einen Zeiger auf eine [SPropProblemArray](spropproblemarray.md) -Struktur; andernfalls NULL, was bedeutet, dass keine Fehlerinformationen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="cac51-141">[out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, which indicates no need for error information.</span></span> <span data-ttu-id="cac51-142">Wenn _lppProblems_ ein gültiger Zeiger auf der Eingabe ist, gibt **DoCopyTo** detaillierte Informationen zu Fehlern beim Kopieren einer oder mehrerer Eigenschaften zurück.</span><span class="sxs-lookup"><span data-stu-id="cac51-142">If  _lppProblems_ is a valid pointer on input, **DoCopyTo** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="cac51-143">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cac51-143">Return value</span></span>

<span data-ttu-id="cac51-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="cac51-144">S_OK</span></span> 
  
> <span data-ttu-id="cac51-145">Die Eigenschaften wurden erfolgreich kopiert oder verschoben.</span><span class="sxs-lookup"><span data-stu-id="cac51-145">The properties have been successfully copied or moved.</span></span>
    
<span data-ttu-id="cac51-146">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="cac51-146">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="cac51-147">Eine Eigenschaft, die kopiert oder verschoben werden soll, ist bereits im Zielobjekt vorhanden, und das MAPI_NOREPLACE-Flag wird festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cac51-147">A property to be copied or moved already exists in the destination object and the MAPI_NOREPLACE flag is set.</span></span> 
    
<span data-ttu-id="cac51-148">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="cac51-148">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="cac51-149">Das Source-Objekt enthält direkt oder indirekt das Zielobjekt.</span><span class="sxs-lookup"><span data-stu-id="cac51-149">The source object directly or indirectly contains the destination object.</span></span> <span data-ttu-id="cac51-150">Möglicherweise wurde vor dem erkennen dieser Bedingung eine beträchtliche Arbeit ausgeführt, sodass die Quell-und Zielobjekte teilweise geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="cac51-150">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="cac51-151">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="cac51-151">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="cac51-152">Die vom _lpSrcInterface_ -Parameter angegebene Schnittstelle wird von dem Objekt, auf das durch _lpSrcObj_verwiesen wird, nicht unterstützt, oder die durch den _lpDestInterface_ -Parameter angegebene Schnittstelle wird von dem Objekt, auf das durch _lpDestObj _.</span><span class="sxs-lookup"><span data-stu-id="cac51-152">The interface identified by the  _lpSrcInterface_ parameter is not supported by the object pointed to by  _lpSrcObj_, or the interface identified by the  _lpDestInterface_ parameter is not supported by the object pointed to by  _lpDestObj_.</span></span> 
    
<span data-ttu-id="cac51-153">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="cac51-153">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="cac51-154">Es wurde versucht, auf ein Objekt zuzugreifen, für das der Aufrufer nicht über ausreichende Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="cac51-154">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="cac51-155">Dieser Fehler wird zurückgegeben, wenn das Zielobjekt mit dem Quellobjekt identisch ist.</span><span class="sxs-lookup"><span data-stu-id="cac51-155">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="cac51-156">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="cac51-156">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="cac51-157">Der _lpSrcInterface_ -Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="cac51-157">The  _lpSrcInterface_ parameter is NULL.</span></span> 
    
<span data-ttu-id="cac51-158">Die folgenden Werte können in der **SPropProblemArray** -Struktur zurückgegeben werden, jedoch nicht als Rückgabewerte für **DoCopyTo**.</span><span class="sxs-lookup"><span data-stu-id="cac51-158">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **DoCopyTo**.</span></span> <span data-ttu-id="cac51-159">Diese Fehler gelten für eine einzelne Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="cac51-159">These errors apply to a single property.</span></span>
  
<span data-ttu-id="cac51-160">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="cac51-160">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="cac51-161">Entweder wurde das MAPI_UNICODE-Flag festgelegt, und **DoCopyTo** unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und **DoCopyTo** unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="cac51-161">Either the MAPI_UNICODE flag was set and **DoCopyTo** does not support Unicode, or MAPI_UNICODE was not set and **DoCopyTo** supports only Unicode.</span></span> 
    
<span data-ttu-id="cac51-162">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="cac51-162">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="cac51-163">Die Eigenschaft kann vom Aufrufer nicht geändert werden, da es sich um eine schreibgeschützte Eigenschaft handelt, die vom Besitzer des Zielobjekts berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="cac51-163">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="cac51-164">Dieser Fehler ist nicht schwerwiegend; der Aufrufer sollte den Kopiervorgang fortsetzen lassen.</span><span class="sxs-lookup"><span data-stu-id="cac51-164">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="cac51-165">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="cac51-165">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="cac51-166">Der Eigenschaftentyp ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="cac51-166">The property type is invalid.</span></span>
    
<span data-ttu-id="cac51-167">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="cac51-167">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="cac51-168">Der Eigenschaftentyp ist nicht der vom Aufrufer erwartete Typ.</span><span class="sxs-lookup"><span data-stu-id="cac51-168">The property type is not the type expected by the caller.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cac51-169">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cac51-169">Remarks</span></span>

<span data-ttu-id="cac51-170">Die **IMAPISupport::D ocopyto** -Methode wird für Support Objekte des Nachrichtenspeicher Anbieters implementiert.</span><span class="sxs-lookup"><span data-stu-id="cac51-170">The **IMAPISupport::DoCopyTo** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="cac51-171">Nachrichtenspeicher Anbieter können **DoCopyTo** aufrufen, um die [IMAPIProp:: CopyTo](imapiprop-copyto.md) -Methode für Ihre Ordner und Nachrichten zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="cac51-171">Message store providers can call **DoCopyTo** to implement the [IMAPIProp::CopyTo](imapiprop-copyto.md) method for their folders and messages.</span></span> 
  
<span data-ttu-id="cac51-172">Standardmäßig kopiert **DoCopyTo** alle Eigenschaften eines Objekts in ein anderes Objekt.</span><span class="sxs-lookup"><span data-stu-id="cac51-172">By default, **DoCopyTo** copies or moves all of the properties of one object to another object.</span></span> <span data-ttu-id="cac51-173">Alle unter Objekte im Source-Objekt werden automatisch in den Vorgang eingeschlossen und vollständig kopiert oder verschoben.</span><span class="sxs-lookup"><span data-stu-id="cac51-173">Any subobjects in the source object are automatically included in the operation and copied or moved in their entirety.</span></span> 
  
<span data-ttu-id="cac51-174">Wenn eine der kopierten oder verschobenen Eigenschaften bereits im Zielobjekt vorhanden ist, werden die vorhandenen Eigenschaften von den neuen Eigenschaften überschrieben, es sei denn, das MAPI_NOREPLACE-Flag wird im _ulFlags_ -Parameter festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cac51-174">If any of the copied or moved properties already exist in the destination object, the existing properties are overwritten by the new properties, unless the MAPI_NOREPLACE flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="cac51-175">Vorhandene Informationen im Zielobjekt, das nicht überschrieben wird, bleiben unberührt.</span><span class="sxs-lookup"><span data-stu-id="cac51-175">Existing information in the destination object that is not overwritten is left untouched.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="cac51-176">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="cac51-176">Notes to callers</span></span>

<span data-ttu-id="cac51-177">Um Eigenschaften aus dem Kopier-oder Verschiebungsvorgang auszuschließen, schließen Sie deren Eigenschaftstags in den Parameter _lpExcludeProps_ ein.</span><span class="sxs-lookup"><span data-stu-id="cac51-177">To exclude properties from the copy or move operation, include their property tags in the  _lpExcludeProps_ parameter.</span></span> <span data-ttu-id="cac51-178">Wenn Sie die Ergebnisse der Verwendung des [PROP_TAG](prop_tag.md) -Makros zum Erstellen eines Eigenschaftentags aus einem bestimmten Bezeichner im Property-Tag-Array überschreiten, werden alle Eigenschaften mit diesem Bezeichner ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="cac51-178">If you pass the results of using the [PROP_TAG](prop_tag.md) macro to build a property tag from a specific identifier in the property tag array, all properties with that identifier will be excluded.</span></span> <span data-ttu-id="cac51-179">Beispielsweise bewirkt der folgende Eintrag im Property Tag-Array, dass alle Eigenschaften mit einem Bezeichner von 0x8002 unabhängig vom Typ ausgeschlossen werden:</span><span class="sxs-lookup"><span data-stu-id="cac51-179">For example, the following entry in the property tag array causes all properties with an identifier of 0x8002 to be excluded, regardless of type:</span></span> 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
<span data-ttu-id="cac51-180">Um zu verhindern, dass die Übermittlungszeit einer Nachricht kopiert wird, wenn Sie die Nachricht in einen anderen Ordner kopieren, geben Sie **PR_MESSAGE_DELIVERY_TIME** ([pidtagmessagedeliverytime (](pidtagmessagedeliverytime-canonical-property.md)) im Property-Tag Exclude-Array an.</span><span class="sxs-lookup"><span data-stu-id="cac51-180">To avoid copying a message's delivery time when you copy the message to a different folder, specify **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) in the property tag exclude array.</span></span> <span data-ttu-id="cac51-181">Wenn Sie die Empfängerliste einer Nachricht ausschließen möchten, fügen Sie die **PR_MESSAGE_RECIPIENTS** ([pidtagmessagerecipients (](pidtagmessagerecipients-canonical-property.md))-Eigenschaft zum Exclude-Array hinzu.</span><span class="sxs-lookup"><span data-stu-id="cac51-181">To exclude a message's recipient list, add the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property to the exclude array.</span></span> <span data-ttu-id="cac51-182">Zum Ausschließen der Anlagen einer Nachricht fügen Sie die **PR_MESSAGE_ATTACHMENTS** ([pidtagmessageattachments (](pidtagmessageattachments-canonical-property.md))-Eigenschaft zum Array hinzu.</span><span class="sxs-lookup"><span data-stu-id="cac51-182">To exclude a message's attachments, add the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property to the array.</span></span>
  
<span data-ttu-id="cac51-183">Um zu verhindern, dass ein Ordner-oder Adressbuchcontainer die Hierarchie-oder Inhaltstabelle kopiert oder verschiebt, schließen Sie **PR_CONTAINER_HIERARCHY** ([Pidtagcontainerhierarchy (](pidtagcontainerhierarchy-canonical-property.md)) oder **PR_CONTAINER_CONTENTS** ([ Pidtagcontainercontents (](pidtagcontainercontents-canonical-property.md)) im Property-Tag Exclude-Array.</span><span class="sxs-lookup"><span data-stu-id="cac51-183">Similarly, to prevent the copying or moving of a folder or address book container's hierarchy or contents table, include **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in the property tag exclude array.</span></span>
  
<span data-ttu-id="cac51-184">Ignoriert MAPI_E_COMPUTED-Fehler, die in der **SPropProblemArray** -Struktur im _lppProblems_ -Parameter zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cac51-184">Ignore MAPI_E_COMPUTED errors returned in the **SPropProblemArray** structure in the  _lppProblems_ parameter.</span></span> 
  
<span data-ttu-id="cac51-185">Der Schnittstellenbezeichner, auf den _lpSrcInterface_ verweist, ist in der Regel derselbe wie der Schnittstellenbezeichner, auf den _lpDestInterface_ verweist.</span><span class="sxs-lookup"><span data-stu-id="cac51-185">The interface identifier that  _lpSrcInterface_ points to is usually the same as the interface identifier that  _lpDestInterface_ points to.</span></span> 
  
<span data-ttu-id="cac51-186">Wenn Sie einen akzeptablen Schnittstellenbezeichner in _lpDestInterface_ , jedoch einen ungültigen Zeiger in _lpDestObj_, sind die Ergebnisse unvorhersehbar.</span><span class="sxs-lookup"><span data-stu-id="cac51-186">If you pass an acceptable interface identifier in  _lpDestInterface_ but an invalid pointer in  _lpDestObj_, the results are unpredictable.</span></span> <span data-ttu-id="cac51-187">Dies führt zu einem Fehler des Anbieters.</span><span class="sxs-lookup"><span data-stu-id="cac51-187">Most likely this will cause your provider to fail.</span></span> 
  
<span data-ttu-id="cac51-188">Wenn Sie jedoch zusätzliche Informationen kennen, die nicht kopiert oder verschoben werden sollen, fügen Sie die Schnittstellenbezeichner für die Schnittstellen hinzu, die in dem im _rgiidExclude_ -Parameter übergebenen Array ausgeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cac51-188">Conversely, if you are aware of supplemental information that should not be copied or moved, add the interface identifiers for the interfaces to be excluded in the array passed in the  _rgiidExclude_ parameter.</span></span> <span data-ttu-id="cac51-189">Wenn Sie beispielsweise Nachrichten kopieren, jedoch keine Ihrer Nachrichtenanlagen, führen Sie IID_IMessage im _rgiidExclude_ -Array aus.</span><span class="sxs-lookup"><span data-stu-id="cac51-189">For example, if you are copying messages, but not any of their message attachments, pass IID_IMessage in the  _rgiidExclude_ array.</span></span> <span data-ttu-id="cac51-190">**DoCopyTo** ignoriert alle in _rgiidExclude_ aufgeführten Schnittstellen, die nicht erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="cac51-190">**DoCopyTo** ignores any interfaces listed in  _rgiidExclude_ that it does not recognize.</span></span> 
  
<span data-ttu-id="cac51-191">Wenn Sie den Parameter _rgiidExclude_ verwenden, um eine Schnittstelle auszuschließen, werden auch alle von dieser Schnittstelle abgeleiteten Schnittstellen ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="cac51-191">When you use the  _rgiidExclude_ parameter to exclude an interface, it also excludes all interfaces derived from that interface.</span></span> <span data-ttu-id="cac51-192">Wenn Sie beispielsweise die [IMAPIContainer](imapicontainerimapiprop.md) -Schnittstelle ausschließen, werden Ordner oder Adressbuchcontainer abhängig vom Anbietertyp ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="cac51-192">For example, excluding the [IMAPIContainer](imapicontainerimapiprop.md) interface causes folders or address book containers to be excluded, depending on the type of provider.</span></span> <span data-ttu-id="cac51-193">Schließen Sie [IMAPIProp](imapipropiunknown.md) oder [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) nicht aus, da so viele Schnittstellen von Ihnen abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="cac51-193">Do not exclude [IMAPIProp](imapipropiunknown.md) or [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) because so many interfaces derive from them.</span></span> 
  
 <span data-ttu-id="cac51-194">**DoCopyTo** meldet globale Fehler, die für den Vorgang als Ganzes gelten, sowie einzelne Fehler, die für einzelne Eigenschaften gelten.</span><span class="sxs-lookup"><span data-stu-id="cac51-194">**DoCopyTo** reports global errors that apply to the operation as a whole, and individual errors that apply to individual properties.</span></span> <span data-ttu-id="cac51-195">Diese einzelnen Fehler werden in eine **SPropProblemArray** -Struktur eingefügt.</span><span class="sxs-lookup"><span data-stu-id="cac51-195">These individual errors are put in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="cac51-196">Sie können die Fehlerberichterstattung auf der Eigenschaftsebene unterdrücken, indem Sie anstelle eines gültigen Zeigers für den Array Struktur Parameter der Eigenschaft "NULL" übergeben.</span><span class="sxs-lookup"><span data-stu-id="cac51-196">You can suppress error reporting at the property level by passing NULL, rather than a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="cac51-197">Wenn Sie Informationen zu Fehlern erhalten möchten, übergeben Sie einen gültigen **SPropProblemArray** -Struktur Zeiger im _lppProblems_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="cac51-197">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="cac51-198">Wenn **DOCOPYTO** S_OK zurückgibt, überprüfen Sie auf mögliche Fehler mit einzelnen Eigenschaften in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="cac51-198">When **DoCopyTo** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="cac51-199">Wenn **DoCopyTo** einen Fehler zurückgibt, werden in der **SPropProblemArray** -Struktur keine Informationen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cac51-199">When **DoCopyTo** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="cac51-200">Rufen Sie stattdessen die [IMAPISupport:: getlasterroraufzurufen](imapisupport-getlasterror.md) -Methode auf, um detaillierte Fehlerinformationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="cac51-200">Instead, call the [IMAPISupport::GetLastError](imapisupport-getlasterror.md) method to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="cac51-201">Wenn **DOCOPYTO** S_OK zurückgibt, können Sie die zurückgegebene **SPropProblemArray** -Struktur freigeben, indem Sie die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="cac51-201">If **DoCopyTo** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="cac51-202">Wenn ein globaler Fehler beim **DoCopyTo** -Aufruf auftritt, verwenden oder befreien Sie die **SPropProblemArray** -Struktur nicht.</span><span class="sxs-lookup"><span data-stu-id="cac51-202">If a global error occurs on the **DoCopyTo** call, do not use or free the **SPropProblemArray** structure.</span></span> <span data-ttu-id="cac51-203">Anbieter sollten das _ulIndex_ -Element in **SPropProblemArray** -Strukturen, die von **DoCopyTo**zurückgegeben werden, ignorieren.</span><span class="sxs-lookup"><span data-stu-id="cac51-203">Providers should ignore the  _ulIndex_ member in **SPropProblemArray** structures returned by **DoCopyTo**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cac51-204">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cac51-204">See also</span></span>



[<span data-ttu-id="cac51-205">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="cac51-205">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
  
[<span data-ttu-id="cac51-206">IMAPISupport::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="cac51-206">IMAPISupport::CopyFolder</span></span>](imapisupport-copyfolder.md)
  
[<span data-ttu-id="cac51-207">IMAPISupport::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="cac51-207">IMAPISupport::CopyMessages</span></span>](imapisupport-copymessages.md)
  
[<span data-ttu-id="cac51-208">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="cac51-208">IMAPISupport::GetLastError</span></span>](imapisupport-getlasterror.md)
  
[<span data-ttu-id="cac51-209">Kanonische Pidtagcontainercontents (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cac51-209">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="cac51-210">Kanonische Pidtagcontainerhierarchy (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cac51-210">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="cac51-211">Kanonische Pidtagmessageattachments (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cac51-211">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="cac51-212">Kanonische Pidtagmessagedeliverytime (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cac51-212">PidTagMessageDeliveryTime Canonical Property</span></span>](pidtagmessagedeliverytime-canonical-property.md)
  
[<span data-ttu-id="cac51-213">Kanonische Pidtagmessagerecipients (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cac51-213">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="cac51-214">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="cac51-214">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="cac51-215">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="cac51-215">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="cac51-216">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="cac51-216">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

