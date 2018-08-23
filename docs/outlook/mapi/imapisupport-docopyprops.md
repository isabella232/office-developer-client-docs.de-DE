---
title: IMAPISupportDoCopyProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoCopyProps
api_type:
- COM
ms.assetid: 2446ef52-578a-4004-9719-de9b0207ccad
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a30a323874c847d9a08b00512cfd30ff3cf5c5ff
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591128"
---
# <a name="imapisupportdocopyprops"></a><span data-ttu-id="4cc5b-103">IMAPISupport::DoCopyProps</span><span class="sxs-lookup"><span data-stu-id="4cc5b-103">IMAPISupport::DoCopyProps</span></span>

  
  
<span data-ttu-id="4cc5b-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4cc5b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4cc5b-105">Kopiert oder Verschiebt einen oder mehrere Eigenschaften eines Objekts in ein anderes Objekt.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-105">Copies or moves one or more properties of an object to another object.</span></span>
  
```cpp
HRESULT DoCopyProps(
  LPCIID lpSrcInterface,
  LPVOID lpSrcObj,
  LPSPropTagArray lpIncludeProps,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  LPCIID lpDestInterface,
  LPVOID lpDestObj,
  ULONG ulFlags,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="4cc5b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4cc5b-106">Parameters</span></span>

 <span data-ttu-id="4cc5b-107">_lpSrcInterface_</span><span class="sxs-lookup"><span data-stu-id="4cc5b-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="4cc5b-108">[in] Ein Zeiger auf die Schnittstelle-ID (IID), die stellt die Schnittstelle dar, die verwendet werden, um Zugriff auf das Objekt mit den Eigenschaften, kopiert oder verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object with the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="4cc5b-109">_lpSrcObj_</span><span class="sxs-lookup"><span data-stu-id="4cc5b-109">_lpSrcObj_</span></span>
  
> <span data-ttu-id="4cc5b-110">[in] Ein Zeiger auf das Objekt, das enthält die Eigenschaften kopiert oder verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-110">[in] A pointer to the object that contains the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="4cc5b-111">_lpIncludeProps_</span><span class="sxs-lookup"><span data-stu-id="4cc5b-111">_lpIncludeProps_</span></span>
  
> <span data-ttu-id="4cc5b-112">[in] Ein Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die ein gezählte Eigenschaftentags-Array enthält, die angeben, die Eigenschaften zum Kopieren oder verschieben.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-112">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains a counted array of property tags that indicate the properties to copy or move.</span></span> <span data-ttu-id="4cc5b-113">Der Parameter _LpIncludeProps_ darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-113">The  _lpIncludeProps_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="4cc5b-114">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="4cc5b-114">_ulUIParam_</span></span>
  
> <span data-ttu-id="4cc5b-115">[in] Ein Handle für das übergeordnete Fenster der Statusanzeige.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-115">[in] A handle to the parent window of the progress indicator.</span></span>
    
 <span data-ttu-id="4cc5b-116">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="4cc5b-116">_lpProgress_</span></span>
  
> <span data-ttu-id="4cc5b-117">[in] Ein Zeiger auf eine Implementierung der eine Statusanzeige.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-117">[in] A pointer to an implementation of a progress indicator.</span></span> <span data-ttu-id="4cc5b-118">Wenn NULL in der _LpProgress_ -Parameter übergeben wird, wird die Statusanzeige mithilfe der MAPI-Implementierung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-118">If NULL is passed in the  _lpProgress_ parameter, the progress indicator is displayed by using the MAPI implementation.</span></span> <span data-ttu-id="4cc5b-119">Der Parameter _LpProgress_ wird ignoriert, es sei denn, das Flag MAPI_DIALOG im _UlFlags_ -Parameter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-119">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="4cc5b-120">_lpDestInterface_</span><span class="sxs-lookup"><span data-stu-id="4cc5b-120">_lpDestInterface_</span></span>
  
> <span data-ttu-id="4cc5b-121">[in] Ein Zeiger auf die Schnittstellenbezeichner, der stellt die Schnittstelle dar, die verwendet werden, um Zugriff auf das Objekt, um die Eigenschaften zu erhalten, die kopiert oder verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-121">[in] A pointer to the interface identifier that represents the interface to be used to access the object to receive the properties that are copied or moved.</span></span>
    
 <span data-ttu-id="4cc5b-122">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="4cc5b-122">_lpDestObj_</span></span>
  
> <span data-ttu-id="4cc5b-123">[in] Ein Zeiger auf das Objekt, das die Eigenschaften kopierten oder verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-123">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="4cc5b-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4cc5b-124">_ulFlags_</span></span>
  
> <span data-ttu-id="4cc5b-125">[in] Eine Bitmaske aus Flags, die steuert, wie der kopieren oder verschieben-Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-125">[in] A bitmask of flags that controls how the copy or move operation is performed.</span></span> <span data-ttu-id="4cc5b-126">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="4cc5b-126">The following flags can be set:</span></span>
    
<span data-ttu-id="4cc5b-127">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="4cc5b-127">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="4cc5b-128">Eine Statusanzeige angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-128">Displays a progress indicator.</span></span>
    
<span data-ttu-id="4cc5b-129">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="4cc5b-129">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="4cc5b-130">**DoCopyProps** sollte einen Verschiebevorgang anstatt einen Kopiervorgang ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-130">**DoCopyProps** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="4cc5b-131">Wenn dieses Flag nicht festgelegt ist, führt **DoCopyProps** durch einen Kopiervorgang.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-131">When this flag is not set, **DoCopyProps** performs a copy operation.</span></span> 
    
<span data-ttu-id="4cc5b-132">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="4cc5b-132">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="4cc5b-133">Vorhandene Eigenschaften im Zielobjekt sollte nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-133">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="4cc5b-134">Wenn dieses Flag nicht festgelegt ist, überschreibt **DoCopyProps** vorhandene Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-134">When this flag is not set, **DoCopyProps** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="4cc5b-135">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="4cc5b-135">_lppProblems_</span></span>
  
> <span data-ttu-id="4cc5b-136">[in, out] Bei Eingabe einen Zeiger auf einen Zeiger auf eine [SPropProblemArray](spropproblemarray.md) -Struktur. andernfalls NULL, gibt keine Notwendigkeit zur Fehlerinformationen an.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-136">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, which indicates no need for error information.</span></span> <span data-ttu-id="4cc5b-137">Wenn _LppProblems_ einen gültigen Zeiger für die Eingabe ist, gibt **DoCopyProps** ausführliche Informationen zu Fehlern in eine oder mehrere Eigenschaften kopieren.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-137">If  _lppProblems_ is a valid pointer on input, **DoCopyProps** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4cc5b-138">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="4cc5b-138">Return value</span></span>

<span data-ttu-id="4cc5b-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="4cc5b-139">S_OK</span></span> 
  
> <span data-ttu-id="4cc5b-140">Eigenschaften wurden erfolgreich kopiert oder verschoben.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-140">Properties were successfully copied or moved.</span></span>
    
<span data-ttu-id="4cc5b-141">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="4cc5b-141">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="4cc5b-142">Eine Eigenschaft, die kopiert oder verschoben bereits vorhanden ist, im Zielobjekt, und das Flag MAPI_NOREPLACE festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-142">A property to be copied or moved already exists in the destination object and the MAPI_NOREPLACE flag is set.</span></span> 
    
<span data-ttu-id="4cc5b-143">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="4cc5b-143">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="4cc5b-144">Das Source-Objekt enthält direkt oder indirekt Zielobjekt.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-144">The source object directly or indirectly contains the destination object.</span></span> <span data-ttu-id="4cc5b-145">Erhebliche Arbeit möglicherweise durchgeführt wurden, bevor diese Bedingung ermittelt wurde, damit die Quell- und Ziel-Objekte teilweise geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-145">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="4cc5b-146">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="4cc5b-146">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="4cc5b-147">Die Schnittstelle, die vom _LpSrcInterface_ -Parameter wird von der Source-Objekt nicht unterstützt, oder die Schnittstelle, die vom _LpDestInterface_ -Parameter wird durch das Zielobjekt nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-147">The interface identified by the  _lpSrcInterface_ parameter is not supported by the source object, or the interface identified by the  _lpDestInterface_ parameter is not supported by the destination object.</span></span> 
    
<span data-ttu-id="4cc5b-148">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="4cc5b-148">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="4cc5b-149">Es wurde versucht, auf ein Objekt zuzugreifen, für den der Anrufer nicht über ausreichende Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-149">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="4cc5b-150">Dieser Fehler wird zurückgegeben, wenn Zielobjekt Quellobjekt identisch ist.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-150">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="4cc5b-151">Die folgenden Werte können in der Struktur **SPropProblemArray** , aber nicht als Rückgabewerte für **DoCopyProps**zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-151">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **DoCopyProps**.</span></span> <span data-ttu-id="4cc5b-152">Diese Fehler gelten für eine einzelne Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-152">These errors apply to a single property.</span></span>
  
<span data-ttu-id="4cc5b-153">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="4cc5b-153">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="4cc5b-154">Entweder die Option MAPI_UNICODE festgelegt wurde und **DoCopyProps** unterstützt keine Unicode oder Parameter MAPI_UNICODE wurde nicht festgelegt und **DoCopyProps** nur Unicode unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-154">Either the MAPI_UNICODE flag was set and **DoCopyProps** does not support Unicode, or MAPI_UNICODE was not set and **DoCopyProps** supports only Unicode.</span></span> 
    
<span data-ttu-id="4cc5b-155">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="4cc5b-155">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="4cc5b-156">Die Eigenschaft kann nicht vom Anrufer geändert werden, da es eine schreibgeschützte Eigenschaft, mit der Besitzer des Zielobjekts berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-156">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="4cc5b-157">Dieser Fehler ist nicht schwerwiegend. der Aufrufer sollte den Kopiervorgang fortgesetzt zulassen.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-157">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="4cc5b-158">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="4cc5b-158">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="4cc5b-159">Der Eigenschaftstyp ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-159">The property type is invalid.</span></span>
    
<span data-ttu-id="4cc5b-160">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="4cc5b-160">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="4cc5b-161">Der Eigenschaftentyp ist nicht den Typ, den der Anrufer erwartet.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-161">The property type is not the type that the caller expects.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4cc5b-162">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="4cc5b-162">Remarks</span></span>

<span data-ttu-id="4cc5b-163">Die **IMAPISupport::DoCopyProps** -Methode wird für Message Store Anbieter Unterstützungsobjekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-163">The **IMAPISupport::DoCopyProps** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="4cc5b-164">Nachricht Anbieter können **DoCopyProps** zum Implementieren der [IMAPIProp::CopyProps](imapiprop-copyprops.md) -Methode für ihre Ordner und Nachrichten aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-164">Message store providers can call **DoCopyProps** to implement the [IMAPIProp::CopyProps](imapiprop-copyprops.md) method for their folders and messages.</span></span> <span data-ttu-id="4cc5b-165">**DoCopyProps** kopiert oder verschiebt die Eigenschaften, die die Tag-Array-Eigenschaft auf den _LpIncludeProps_ erkannt werden, und, die in das Objekt, das auf _LpSrcObj_vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-165">**DoCopyProps** copies or moves the properties that are identified in the property tag array pointed to by  _lpIncludeProps_ and that are present in the object pointed to by  _lpSrcObj_.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="4cc5b-166">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="4cc5b-166">Notes to callers</span></span>

<span data-ttu-id="4cc5b-167">Beim Kopieren von Eigenschaften zwischen Objekten des gleichen Typs, wie beispielsweise zwei Nachrichten müssen die Parameter _LpSrcInterface_ und _LpDestInterface_ enthalten die gleichen Bezeichner, und die _LpSrcObj_ und _LpDestObj_ Parameter für die Benutzeroberfläche muss auf Objekte des gleichen Typs zeigen.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-167">When you copy properties between objects of the same type, such as two messages, the  _lpSrcInterface_ and  _lpDestInterface_ parameters must contain the same interface identifier, and the  _lpSrcObj_ and  _lpDestObj_ parameters must point to objects of the same type.</span></span> <span data-ttu-id="4cc5b-168">Wenn _LpDestInterface_ auf NULL festgelegt ist, gibt **DoCopyProps** MAPI_E_INVALID_PARAMETER zurück.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-168">If  _lpDestInterface_ is set to NULL, **DoCopyProps** returns MAPI_E_INVALID_PARAMETER.</span></span> <span data-ttu-id="4cc5b-169">Wenn Sie auf eine akzeptable Schnittstellenbezeichner, aber Set _LpDestObj_ in einen ungültigen Zeiger _LpDestInterface_ festlegen, sind die Ergebnisse unvorhersehbar.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-169">If you set  _lpDestInterface_ to an acceptable interface identifier, but set  _lpDestObj_ to an invalid pointer, the results are unpredictable.</span></span> <span data-ttu-id="4cc5b-170">In den meisten Fällen wird vom Dienstanbieter fehl.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-170">Most likely your provider will fail.</span></span> 
  
<span data-ttu-id="4cc5b-171">Legen Sie das Flag MAPI_NOREPLACE, wenn Sie nicht möchten, dass alle Eigenschaften im Zielobjekt überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-171">Set the MAPI_NOREPLACE flag if you do not want any of the properties in the destination object to be overwritten.</span></span> <span data-ttu-id="4cc5b-172">Eigenschaften im Zielobjekt, die in der Source-Objekt vorhanden ist und nicht überschrieben werden werden nicht gelöscht oder geändert.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-172">Properties in the destination object that exist in the source object and are not overwritten are not deleted or modified.</span></span>
  
<span data-ttu-id="4cc5b-173">Um eine Nachricht Empfängerliste zu kopieren, fügen Sie die **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))-Eigenschaft die Tag-Array-Eigenschaft auf den durch den Parameter _LpIncludeProps_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-173">To copy a message's recipient list, include the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property in the property tag array pointed to by the  _lpIncludeProps_ parameter.</span></span> <span data-ttu-id="4cc5b-174">Um die e-Mail-Anlagen zu kopieren, umfassen Sie die **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-174">To copy the message's attachments, include the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="4cc5b-175">Um einen Ordner oder Adressbuchcontainer des Hierarchie oder Inhaltstabelle zu kopieren, schließen Sie **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) oder **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) im Array Tag-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-175">To copy a folder or address book container's hierarchy or contents table, include **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in the property tag array.</span></span> <span data-ttu-id="4cc5b-176">Einen Ordner zugeordneten Inhaltstabelle aufnehmen möchten, fügen Sie die **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))-Eigenschaft im Array.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-176">To include a folder's associated contents table, include the **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) property in the array.</span></span>
  
<span data-ttu-id="4cc5b-177">Wenn Unterordner kopiert oder verschoben werden, werden vollständig unabhängig von der Verwendung von Eigenschaften, die durch die Struktur **SPropTagArray** angegeben deren Inhalt kopiert oder verschoben.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-177">If subfolders are copied or moved, their contents are copied or moved in their entirety, regardless of the use of properties indicated by the **SPropTagArray** structure.</span></span> 
  
 <span data-ttu-id="4cc5b-178">**DoCopyProps** globale mit dem Vorgang als Ganzes auftretende Fehler und einzelne einen oder mehrere der Eigenschaften auftretenden Fehler gemeldet.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-178">**DoCopyProps** reports global errors that occur with the operation as a whole, and individual errors that occur with one or more of the properties.</span></span> <span data-ttu-id="4cc5b-179">Diese einzelnen Fehler werden in einer **SPropProblemArray** eingefügt.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-179">These individual errors are put in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="4cc5b-180">Sie können die Fehlerberichterstattung Ebene der Eigenschaft, indem Sie NULL, statt dass ein gültiger Zeiger, für den Parameter Property Problem Array Struktur übergeben unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-180">You can suppress error reporting at the property level by passing NULL, rather than a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="4cc5b-181">Wenn Sie Informationen zu Fehlern erhalten möchten, übergeben Sie einen gültigen **SPropProblemArray** Struktur Zeiger des _LppProblems_ -Parameters.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-181">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="4cc5b-182">Wenn **DoCopyProps** S_OK zurückgegeben wird, überprüfen Sie auf mögliche Fehler mit einzelnen Eigenschaften in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-182">When **DoCopyProps** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="4cc5b-183">Wenn **DoCopyProps** einen Fehler zurückgibt, wird keine Informationen in der Struktur **SPropProblemArray** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-183">When **DoCopyProps** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="4cc5b-184">Rufen Sie stattdessen die [IMAPISupport::GetLastError](imapisupport-getlasterror.md) -Methode, um ausführliche Fehlerinformationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-184">Instead, call the [IMAPISupport::GetLastError](imapisupport-getlasterror.md) method to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="4cc5b-185">Wenn **DoCopyProps** S_OK zurückgibt, frei die zurückgegebene Struktur **SPropProblemArray** durch Aufrufen der [MAPIFreeBuffer](mapifreebuffer.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-185">If **DoCopyProps** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4cc5b-186">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4cc5b-186">See also</span></span>



[<span data-ttu-id="4cc5b-187">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="4cc5b-187">IMAPIProp::CopyProps</span></span>](imapiprop-copyprops.md)
  
[<span data-ttu-id="4cc5b-188">IMAPISupport::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="4cc5b-188">IMAPISupport::CopyMessages</span></span>](imapisupport-copymessages.md)
  
[<span data-ttu-id="4cc5b-189">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="4cc5b-189">IMAPISupport::DoCopyTo</span></span>](imapisupport-docopyto.md)
  
[<span data-ttu-id="4cc5b-190">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="4cc5b-190">IMAPISupport::GetLastError</span></span>](imapisupport-getlasterror.md)
  
[<span data-ttu-id="4cc5b-191">PidTagContainerContents (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4cc5b-191">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="4cc5b-192">PidTagContainerHierarchy (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4cc5b-192">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="4cc5b-193">PidTagFolderAssociatedContents (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4cc5b-193">PidTagFolderAssociatedContents Canonical Property</span></span>](pidtagfolderassociatedcontents-canonical-property.md)
  
[<span data-ttu-id="4cc5b-194">PidTagMessageAttachments (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4cc5b-194">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="4cc5b-195">PidTagMessageRecipients (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4cc5b-195">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="4cc5b-196">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="4cc5b-196">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="4cc5b-197">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="4cc5b-197">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="4cc5b-198">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="4cc5b-198">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

