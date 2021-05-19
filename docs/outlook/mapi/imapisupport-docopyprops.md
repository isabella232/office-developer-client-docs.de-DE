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
ms.openlocfilehash: 24107ae1926c8590da6a823a354eeae72d72f248
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405583"
---
# <a name="imapisupportdocopyprops"></a><span data-ttu-id="9c78c-103">IMAPISupport::DoCopyProps</span><span class="sxs-lookup"><span data-stu-id="9c78c-103">IMAPISupport::DoCopyProps</span></span>

  
  
<span data-ttu-id="9c78c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9c78c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9c78c-105">Kopiert oder verschiebt eine oder mehrere Eigenschaften eines Objekts in ein anderes Objekt.</span><span class="sxs-lookup"><span data-stu-id="9c78c-105">Copies or moves one or more properties of an object to another object.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="9c78c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c78c-106">Parameters</span></span>

 <span data-ttu-id="9c78c-107">_lpSrcInterface_</span><span class="sxs-lookup"><span data-stu-id="9c78c-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="9c78c-108">[in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID), die die Schnittstelle darstellt, die für den Zugriff auf das Objekt mit den Eigenschaften verwendet werden soll, die kopiert oder verschoben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9c78c-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object with the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="9c78c-109">_lpSrcObj_</span><span class="sxs-lookup"><span data-stu-id="9c78c-109">_lpSrcObj_</span></span>
  
> <span data-ttu-id="9c78c-110">[in] Ein Zeiger auf das Objekt, das die eigenschaften enthält, die kopiert oder verschoben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9c78c-110">[in] A pointer to the object that contains the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="9c78c-111">_lpIncludeProps_</span><span class="sxs-lookup"><span data-stu-id="9c78c-111">_lpIncludeProps_</span></span>
  
> <span data-ttu-id="9c78c-112">[in] Ein Zeiger auf eine [SPropTagArray-Struktur,](sproptagarray.md) die ein gezähltes Array von Eigenschaftstags enthält, die die Zu kopierenden oder verschiebenden Eigenschaften angeben.</span><span class="sxs-lookup"><span data-stu-id="9c78c-112">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains a counted array of property tags that indicate the properties to copy or move.</span></span> <span data-ttu-id="9c78c-113">Der  _lpIncludeProps-Parameter_ darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="9c78c-113">The  _lpIncludeProps_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="9c78c-114">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="9c78c-114">_ulUIParam_</span></span>
  
> <span data-ttu-id="9c78c-115">[in] Ein Handle zum übergeordneten Fenster des Statusindikators.</span><span class="sxs-lookup"><span data-stu-id="9c78c-115">[in] A handle to the parent window of the progress indicator.</span></span>
    
 <span data-ttu-id="9c78c-116">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="9c78c-116">_lpProgress_</span></span>
  
> <span data-ttu-id="9c78c-117">[in] Ein Zeiger auf eine Implementierung eines Fortschrittsindikators.</span><span class="sxs-lookup"><span data-stu-id="9c78c-117">[in] A pointer to an implementation of a progress indicator.</span></span> <span data-ttu-id="9c78c-118">Wenn NULL im  _lpProgress-Parameter_ übergeben wird, wird die Statusanzeige mithilfe der MAPI-Implementierung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9c78c-118">If NULL is passed in the  _lpProgress_ parameter, the progress indicator is displayed by using the MAPI implementation.</span></span> <span data-ttu-id="9c78c-119">Der  _lpProgress-Parameter_ wird ignoriert, es sei denn, das MAPI_DIALOG wird im  _ulFlags-Parameter_ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9c78c-119">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="9c78c-120">_lpDestInterface_</span><span class="sxs-lookup"><span data-stu-id="9c78c-120">_lpDestInterface_</span></span>
  
> <span data-ttu-id="9c78c-121">[in] Ein Zeiger auf die Schnittstellen-ID, die die Schnittstelle darstellt, die für den Zugriff auf das Objekt verwendet werden soll, um die Eigenschaften zu empfangen, die kopiert oder verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="9c78c-121">[in] A pointer to the interface identifier that represents the interface to be used to access the object to receive the properties that are copied or moved.</span></span>
    
 <span data-ttu-id="9c78c-122">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="9c78c-122">_lpDestObj_</span></span>
  
> <span data-ttu-id="9c78c-123">[in] Ein Zeiger auf das Objekt, um die kopierten oder verschobenen Eigenschaften zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="9c78c-123">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="9c78c-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9c78c-124">_ulFlags_</span></span>
  
> <span data-ttu-id="9c78c-125">[in] Eine Bitmaske mit Flags, die steuert, wie der Kopier- oder Verschiebevorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9c78c-125">[in] A bitmask of flags that controls how the copy or move operation is performed.</span></span> <span data-ttu-id="9c78c-126">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="9c78c-126">The following flags can be set:</span></span>
    
<span data-ttu-id="9c78c-127">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="9c78c-127">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="9c78c-128">Zeigt eine Statusanzeige an.</span><span class="sxs-lookup"><span data-stu-id="9c78c-128">Displays a progress indicator.</span></span>
    
<span data-ttu-id="9c78c-129">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="9c78c-129">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="9c78c-130">**DoCopyProps** sollte einen Verschiebevorgang anstelle eines Kopiervorgangs ausführen.</span><span class="sxs-lookup"><span data-stu-id="9c78c-130">**DoCopyProps** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="9c78c-131">Wenn dieses Flag nicht festgelegt ist, **führt DoCopyProps** einen Kopiervorgang aus.</span><span class="sxs-lookup"><span data-stu-id="9c78c-131">When this flag is not set, **DoCopyProps** performs a copy operation.</span></span> 
    
<span data-ttu-id="9c78c-132">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="9c78c-132">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="9c78c-133">Vorhandene Eigenschaften im Zielobjekt sollten nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="9c78c-133">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="9c78c-134">Wenn dieses Flag nicht festgelegt ist, **überschreibt DoCopyProps** vorhandene Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9c78c-134">When this flag is not set, **DoCopyProps** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="9c78c-135">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="9c78c-135">_lppProblems_</span></span>
  
> <span data-ttu-id="9c78c-136">[in, out] Bei der Eingabe ein Zeiger auf einen Zeiger auf eine [SPropProblemArray-Struktur;](spropproblemarray.md) andernfalls NULL, was angibt, dass keine Fehlerinformationen benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="9c78c-136">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, which indicates no need for error information.</span></span> <span data-ttu-id="9c78c-137">Wenn  _lppProblems_ ein gültiger Zeiger für die Eingabe ist, gibt **DoCopyProps** detaillierte Informationen zu Fehlern beim Kopieren einer oder mehreren Eigenschaften zurück.</span><span class="sxs-lookup"><span data-stu-id="9c78c-137">If  _lppProblems_ is a valid pointer on input, **DoCopyProps** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9c78c-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9c78c-138">Return value</span></span>

<span data-ttu-id="9c78c-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="9c78c-139">S_OK</span></span> 
  
> <span data-ttu-id="9c78c-140">Eigenschaften wurden erfolgreich kopiert oder verschoben.</span><span class="sxs-lookup"><span data-stu-id="9c78c-140">Properties were successfully copied or moved.</span></span>
    
<span data-ttu-id="9c78c-141">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="9c78c-141">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="9c78c-142">Eine zu kopierende oder zu verschobene Eigenschaft ist bereits im Zielobjekt vorhanden, und das MAPI_NOREPLACE ist festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9c78c-142">A property to be copied or moved already exists in the destination object and the MAPI_NOREPLACE flag is set.</span></span> 
    
<span data-ttu-id="9c78c-143">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="9c78c-143">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="9c78c-144">Das Quellobjekt enthält direkt oder indirekt das Zielobjekt.</span><span class="sxs-lookup"><span data-stu-id="9c78c-144">The source object directly or indirectly contains the destination object.</span></span> <span data-ttu-id="9c78c-145">Bevor diese Bedingung erkannt wurde, wurden möglicherweise erhebliche Arbeiten ausgeführt, sodass die Quell- und Zielobjekte teilweise geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="9c78c-145">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="9c78c-146">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="9c78c-146">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="9c78c-147">Die durch den  _lpSrcInterface-Parameter_ identifizierte Schnittstelle wird vom Quellobjekt nicht unterstützt, oder die vom  _lpDestInterface-Parameter_ identifizierte Schnittstelle wird vom Zielobjekt nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9c78c-147">The interface identified by the  _lpSrcInterface_ parameter is not supported by the source object, or the interface identified by the  _lpDestInterface_ parameter is not supported by the destination object.</span></span> 
    
<span data-ttu-id="9c78c-148">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="9c78c-148">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="9c78c-149">Es wurde versucht, auf ein Objekt zu zugreifen, für das der Aufrufer nicht über ausreichende Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="9c78c-149">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="9c78c-150">Dieser Fehler wird zurückgegeben, wenn das Zielobjekt mit dem Quellobjekt identisch ist.</span><span class="sxs-lookup"><span data-stu-id="9c78c-150">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="9c78c-151">Die folgenden Werte können in der **SPropProblemArray-Struktur** zurückgegeben werden, jedoch nicht als Rückgabewerte für **DoCopyProps**.</span><span class="sxs-lookup"><span data-stu-id="9c78c-151">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **DoCopyProps**.</span></span> <span data-ttu-id="9c78c-152">Diese Fehler gelten für eine einzelne Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="9c78c-152">These errors apply to a single property.</span></span>
  
<span data-ttu-id="9c78c-153">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="9c78c-153">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="9c78c-154">Entweder wurde MAPI_UNICODE festgelegt, und **DoCopyProps** unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und **DoCopyProps** unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="9c78c-154">Either the MAPI_UNICODE flag was set and **DoCopyProps** does not support Unicode, or MAPI_UNICODE was not set and **DoCopyProps** supports only Unicode.</span></span> 
    
<span data-ttu-id="9c78c-155">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="9c78c-155">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="9c78c-156">Die Eigenschaft kann vom Aufrufer nicht geändert werden, da es sich um eine schreibgeschützte Eigenschaft handelt, die vom Besitzer des Zielobjekts berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="9c78c-156">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="9c78c-157">Dieser Fehler ist nicht schwerwiegender. Der Aufrufer sollte zulassen, dass der Kopiervorgang fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="9c78c-157">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="9c78c-158">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="9c78c-158">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="9c78c-159">Der Eigenschaftentyp ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="9c78c-159">The property type is invalid.</span></span>
    
<span data-ttu-id="9c78c-160">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="9c78c-160">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="9c78c-161">Der Eigenschaftstyp ist nicht der Typ, den der Aufrufer erwartet.</span><span class="sxs-lookup"><span data-stu-id="9c78c-161">The property type is not the type that the caller expects.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9c78c-162">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9c78c-162">Remarks</span></span>

<span data-ttu-id="9c78c-163">Die **IMAPISupport::D oCopyProps-Methode** wird für Unterstützungsobjekte des Nachrichtenspeicheranbieters implementiert.</span><span class="sxs-lookup"><span data-stu-id="9c78c-163">The **IMAPISupport::DoCopyProps** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="9c78c-164">Nachrichtenspeicheranbieter können **DoCopyProps aufrufen,** um die [IMAPIProp::CopyProps-Methode](imapiprop-copyprops.md) für ihre Ordner und Nachrichten zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="9c78c-164">Message store providers can call **DoCopyProps** to implement the [IMAPIProp::CopyProps](imapiprop-copyprops.md) method for their folders and messages.</span></span> <span data-ttu-id="9c78c-165">**DoCopyProps** kopiert oder verschiebt die Eigenschaften, die im Eigenschaftentagarray identifiziert werden, auf das  _lpIncludeProps_ verweist und die im Objekt vorhanden sind, auf das  _von lpSrcObj_ verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="9c78c-165">**DoCopyProps** copies or moves the properties that are identified in the property tag array pointed to by  _lpIncludeProps_ and that are present in the object pointed to by  _lpSrcObj_.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9c78c-166">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="9c78c-166">Notes to callers</span></span>

<span data-ttu-id="9c78c-167">Wenn Sie Eigenschaften zwischen Objekten desselben Typs kopieren, z. B. zwei Nachrichten, müssen die  _Parameter lpSrcInterface_ und  _lpDestInterface_ denselben Schnittstellenbezeichner enthalten, und die  _Parameter lpSrcObj_ und  _lpDestObj_ müssen auf Objekte desselben Typs verweisen.</span><span class="sxs-lookup"><span data-stu-id="9c78c-167">When you copy properties between objects of the same type, such as two messages, the  _lpSrcInterface_ and  _lpDestInterface_ parameters must contain the same interface identifier, and the  _lpSrcObj_ and  _lpDestObj_ parameters must point to objects of the same type.</span></span> <span data-ttu-id="9c78c-168">Wenn  _lpDestInterface_ auf NULL festgelegt ist, gibt **DoCopyProps** MAPI_E_INVALID_PARAMETER.</span><span class="sxs-lookup"><span data-stu-id="9c78c-168">If  _lpDestInterface_ is set to NULL, **DoCopyProps** returns MAPI_E_INVALID_PARAMETER.</span></span> <span data-ttu-id="9c78c-169">Wenn Sie  _lpDestInterface_ auf einen akzeptablen Schnittstellenbezeichner festlegen,  _aber lpDestObj_ auf einen ungültigen Zeiger festlegen, sind die Ergebnisse unvorhersehbar.</span><span class="sxs-lookup"><span data-stu-id="9c78c-169">If you set  _lpDestInterface_ to an acceptable interface identifier, but set  _lpDestObj_ to an invalid pointer, the results are unpredictable.</span></span> <span data-ttu-id="9c78c-170">Höchstwahrscheinlich wird Ihr Anbieter fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="9c78c-170">Most likely your provider will fail.</span></span> 
  
<span data-ttu-id="9c78c-171">Legen Sie MAPI_NOREPLACE, wenn keine der Eigenschaften im Zielobjekt überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="9c78c-171">Set the MAPI_NOREPLACE flag if you do not want any of the properties in the destination object to be overwritten.</span></span> <span data-ttu-id="9c78c-172">Eigenschaften im Zielobjekt, die im Quellobjekt vorhanden sind und nicht überschrieben werden, werden nicht gelöscht oder geändert.</span><span class="sxs-lookup"><span data-stu-id="9c78c-172">Properties in the destination object that exist in the source object and are not overwritten are not deleted or modified.</span></span>
  
<span data-ttu-id="9c78c-173">Um die Empfängerliste einer Nachricht **zu** kopieren, schließen Sie die PR_MESSAGE_RECIPIENTS ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) -Eigenschaft in das Eigenschaftentagarray ein, auf das der  _lpIncludeProps-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="9c78c-173">To copy a message's recipient list, include the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property in the property tag array pointed to by the  _lpIncludeProps_ parameter.</span></span> <span data-ttu-id="9c78c-174">Um die Anlagen der Nachricht zu kopieren, schließen Sie die **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) -Eigenschaft ein.</span><span class="sxs-lookup"><span data-stu-id="9c78c-174">To copy the message's attachments, include the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="9c78c-175">Um die Hierarchie oder Inhaltstabelle eines Ordners oder Adressbuchcontainers zu kopieren, fügen Sie **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) oder **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in das Eigenschaftentagarray ein.</span><span class="sxs-lookup"><span data-stu-id="9c78c-175">To copy a folder or address book container's hierarchy or contents table, include **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in the property tag array.</span></span> <span data-ttu-id="9c78c-176">Um die zugeordnete Inhaltstabelle eines Ordners zu enthalten, schließen Sie **die PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) -Eigenschaft in das Array ein.</span><span class="sxs-lookup"><span data-stu-id="9c78c-176">To include a folder's associated contents table, include the **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) property in the array.</span></span>
  
<span data-ttu-id="9c78c-177">Wenn Unterordner kopiert oder verschoben werden, werden deren Inhalte vollständig kopiert oder verschoben, unabhängig von der Verwendung von Eigenschaften, die von der **SPropTagArray-Struktur angegeben** werden.</span><span class="sxs-lookup"><span data-stu-id="9c78c-177">If subfolders are copied or moved, their contents are copied or moved in their entirety, regardless of the use of properties indicated by the **SPropTagArray** structure.</span></span> 
  
 <span data-ttu-id="9c78c-178">**DoCopyProps** meldet globale Fehler, die mit dem Gesamten des Vorgangs auftreten, und einzelne Fehler, die bei einer oder mehreren der Eigenschaften auftreten.</span><span class="sxs-lookup"><span data-stu-id="9c78c-178">**DoCopyProps** reports global errors that occur with the operation as a whole, and individual errors that occur with one or more of the properties.</span></span> <span data-ttu-id="9c78c-179">Diese einzelnen Fehler werden in einer **SPropProblemArray-Struktur** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9c78c-179">These individual errors are put in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="9c78c-180">Sie können die Fehlerberichterstellung auf Eigenschaftsebene unterdrücken, indem Sie NULL anstelle eines gültigen Zeigers für den Parameter für die Arraystruktur des Eigenschaftsproblems übergeben.</span><span class="sxs-lookup"><span data-stu-id="9c78c-180">You can suppress error reporting at the property level by passing NULL, rather than a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="9c78c-181">Wenn Sie Informationen zu Fehlern erhalten möchten, übergeben Sie einen gültigen **SPropProblemArray-Strukturzeiger** im _lppProblems-Parameter._</span><span class="sxs-lookup"><span data-stu-id="9c78c-181">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="9c78c-182">Wenn **DoCopyProps** S_OK, überprüfen Sie nach möglichen Fehlern mit einzelnen Eigenschaften in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="9c78c-182">When **DoCopyProps** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="9c78c-183">Wenn **DoCopyProps** einen Fehler zurückgibt, werden keine Informationen in der **SPropProblemArray-Struktur** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9c78c-183">When **DoCopyProps** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="9c78c-184">Rufen Sie stattdessen die [IMAPISupport::GetLastError-Methode](imapisupport-getlasterror.md) auf, um detaillierte Fehlerinformationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9c78c-184">Instead, call the [IMAPISupport::GetLastError](imapisupport-getlasterror.md) method to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="9c78c-185">Wenn **DoCopyProps** S_OK, geben Sie die zurückgegebene **SPropProblemArray-Struktur** frei, indem Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9c78c-185">If **DoCopyProps** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9c78c-186">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c78c-186">See also</span></span>



[<span data-ttu-id="9c78c-187">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="9c78c-187">IMAPIProp::CopyProps</span></span>](imapiprop-copyprops.md)
  
[<span data-ttu-id="9c78c-188">IMAPISupport::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="9c78c-188">IMAPISupport::CopyMessages</span></span>](imapisupport-copymessages.md)
  
[<span data-ttu-id="9c78c-189">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="9c78c-189">IMAPISupport::DoCopyTo</span></span>](imapisupport-docopyto.md)
  
[<span data-ttu-id="9c78c-190">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="9c78c-190">IMAPISupport::GetLastError</span></span>](imapisupport-getlasterror.md)
  
[<span data-ttu-id="9c78c-191">PidTagContainerContents (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9c78c-191">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="9c78c-192">PidTagContainerHierarchy (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9c78c-192">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="9c78c-193">PidTagFolderAssociatedContents (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9c78c-193">PidTagFolderAssociatedContents Canonical Property</span></span>](pidtagfolderassociatedcontents-canonical-property.md)
  
[<span data-ttu-id="9c78c-194">PidTagMessageAttachments (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9c78c-194">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="9c78c-195">PidTagMessageRecipients (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9c78c-195">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="9c78c-196">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="9c78c-196">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="9c78c-197">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="9c78c-197">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="9c78c-198">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="9c78c-198">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

