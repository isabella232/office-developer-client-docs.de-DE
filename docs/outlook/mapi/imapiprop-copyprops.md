---
title: IMAPIPropCopyProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.CopyProps
api_type:
- COM
ms.assetid: f65da1c8-d49b-44e8-8c66-9c53d088d334
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7319f1abb4a74ee17b0a4a1220215c29434d256b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345507"
---
# <a name="imapipropcopyprops"></a><span data-ttu-id="f6223-103">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="f6223-103">IMAPIProp::CopyProps</span></span>

  
  
<span data-ttu-id="f6223-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f6223-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f6223-105">Kopiert oder verschiebt ausgewählte Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f6223-105">Copies or moves selected properties.</span></span> 
  
```cpp
HRESULT CopyProps(
  LPSPropTagArray lpIncludeProps,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  LPCIID lpInterface,
  LPVOID lpDestObj,
  ULONG ulFlags,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="f6223-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6223-106">Parameters</span></span>

 <span data-ttu-id="f6223-107">_lpIncludeProps_</span><span class="sxs-lookup"><span data-stu-id="f6223-107">_lpIncludeProps_</span></span>
  
> <span data-ttu-id="f6223-108">in Ein Zeiger auf ein Property-Tag-Array, das die Eigenschaften angibt, die kopiert oder verschoben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f6223-108">[in] A pointer to a property tag array that specifies the properties to copy or move.</span></span> <span data-ttu-id="f6223-109">**PR_NULL** ([Pidtagnull (](pidtagnull-canonical-property.md)) kann nicht im Array enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="f6223-109">**PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) cannot be included in the array.</span></span> <span data-ttu-id="f6223-110">Der _lpIncludeProps_ -Parameter darf nicht **null**sein.</span><span class="sxs-lookup"><span data-stu-id="f6223-110">The  _lpIncludeProps_ parameter cannot be **null**.</span></span>
    
 <span data-ttu-id="f6223-111">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="f6223-111">_ulUIParam_</span></span>
  
> <span data-ttu-id="f6223-112">in Ein Handle für das übergeordnete Fenster der Statusanzeige.</span><span class="sxs-lookup"><span data-stu-id="f6223-112">[in] A handle to the parent window of the progress indicator.</span></span> 
    
 <span data-ttu-id="f6223-113">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="f6223-113">_lpProgress_</span></span>
  
> <span data-ttu-id="f6223-114">in Ein Zeiger auf eine Implementierung einer Statusanzeige.</span><span class="sxs-lookup"><span data-stu-id="f6223-114">[in] A pointer to an implementation of a progress indicator.</span></span> <span data-ttu-id="f6223-115">Wenn **null** im _lpProgress_ -Parameter übergeben wird, wird die STATUSanzeige mithilfe der MAPI-Implementierung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f6223-115">If **null** is passed in the  _lpProgress_ parameter, the progress indicator is displayed by using the MAPI implementation.</span></span> <span data-ttu-id="f6223-116">Der _lpProgress_ -Parameter wird ignoriert, es sei denn, das MAPI_DIALOG-Flag wird im _ulFlags_ -Parameter festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f6223-116">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="f6223-117">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="f6223-117">_lpInterface_</span></span>
  
> <span data-ttu-id="f6223-118">in Ein Zeiger auf die Schnittstellen-ID (IID), die die Schnittstelle darstellt, die für den Zugriff auf das Objekt verwendet werden muss, auf das durch den _lpDestObj_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="f6223-118">[in] A pointer to the interface identifier (IID) that represents the interface that must be used to access the object pointed to by the  _lpDestObj_ parameter.</span></span> <span data-ttu-id="f6223-119">Der _lpInterface_ -Parameter darf nicht **null**sein.</span><span class="sxs-lookup"><span data-stu-id="f6223-119">The  _lpInterface_ parameter must not be **null**.</span></span>
    
 <span data-ttu-id="f6223-120">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="f6223-120">_lpDestObj_</span></span>
  
> <span data-ttu-id="f6223-121">in Ein Zeiger auf das Objekt, das die kopierten oder verschobenen Eigenschaften empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="f6223-121">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="f6223-122">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f6223-122">_ulFlags_</span></span>
  
> <span data-ttu-id="f6223-123">in Eine Bitmaske von Flags, die den Kopier-oder Verschiebungsvorgang steuert.</span><span class="sxs-lookup"><span data-stu-id="f6223-123">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="f6223-124">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="f6223-124">The following flags can be set:</span></span>
    
<span data-ttu-id="f6223-125">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="f6223-125">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="f6223-126">Wenn **CopyProps** die [IMAPISupport::D-ocopyprops](imapisupport-docopyprops.md) -Methode zum Verarbeiten des Kopier-oder Verschiebungsvorgangs aufruft, sollte stattdessen sofort mit dem Fehlerwert MAPI_E_DECLINE_COPY zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f6223-126">If **CopyProps** calls the [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) method to handle the copy or move operation, it should instead return immediately with the error value MAPI_E_DECLINE_COPY.</span></span> <span data-ttu-id="f6223-127">Das MAPI_DECLINE_OK-Flag wird durch MAPI festgelegt, um die Rekursion einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="f6223-127">The MAPI_DECLINE_OK flag is set by MAPI to limit recursion.</span></span> <span data-ttu-id="f6223-128">Clients legen dieses Flag nicht fest.</span><span class="sxs-lookup"><span data-stu-id="f6223-128">Clients do not set this flag.</span></span> 
    
<span data-ttu-id="f6223-129">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="f6223-129">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="f6223-130">Zeigt eine Statusanzeige an.</span><span class="sxs-lookup"><span data-stu-id="f6223-130">Displays a progress indicator.</span></span>
    
<span data-ttu-id="f6223-131">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="f6223-131">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="f6223-132">**CopyProps** sollte anstelle eines Kopiervorgangs einen Verschiebungsvorgang ausführen.</span><span class="sxs-lookup"><span data-stu-id="f6223-132">**CopyProps** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="f6223-133">Wenn dieses Flag nicht festgelegt ist, führt **CopyProps** einen Kopiervorgang aus.</span><span class="sxs-lookup"><span data-stu-id="f6223-133">When this flag is not set, **CopyProps** performs a copy operation.</span></span> 
    
<span data-ttu-id="f6223-134">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="f6223-134">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="f6223-135">Vorhandene Eigenschaften im Zielobjekt sollten nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="f6223-135">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="f6223-136">Wenn dieses Flag nicht festgelegt ist, überschreibt **CopyProps** vorhandene Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f6223-136">When this flag is not set, **CopyProps** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="f6223-137">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="f6223-137">_lppProblems_</span></span>
  
> <span data-ttu-id="f6223-138">[in, out] Bei der Eingabe ein Zeiger auf einen Zeiger auf eine [SPropProblemArray](spropproblemarray.md) -Struktur; andernfalls **null**, was darauf hinweist, dass keine Fehlerinformationen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="f6223-138">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, **null**, indicating that there is no need for error information.</span></span> <span data-ttu-id="f6223-139">Wenn _lppProblems_ ein gültiger Zeiger auf der Eingabe ist, gibt **CopyProps** detaillierte Informationen zu Fehlern beim Kopieren einer oder mehrerer Eigenschaften zurück.</span><span class="sxs-lookup"><span data-stu-id="f6223-139">If  _lppProblems_ is a valid pointer on input, **CopyProps** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f6223-140">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f6223-140">Return value</span></span>

<span data-ttu-id="f6223-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="f6223-141">S_OK</span></span> 
  
> <span data-ttu-id="f6223-142">Eigenschaften wurden erfolgreich kopiert oder verschoben.</span><span class="sxs-lookup"><span data-stu-id="f6223-142">Properties have been successfully copied or moved.</span></span>
    
<span data-ttu-id="f6223-143">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="f6223-143">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="f6223-144">Ein Subobjekt kann nicht kopiert werden, da ein Unterobjekt mit demselben Anzeigenamen, der durch die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft definiert ist, bereits im Zielobjekt vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="f6223-144">A subobject cannot be copied because a subobject with the same display name, defined by the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, already exists in the destination object.</span></span> 
    
<span data-ttu-id="f6223-145">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="f6223-145">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="f6223-146">Der Dienstanbieter implementiert den Kopiervorgang nicht.</span><span class="sxs-lookup"><span data-stu-id="f6223-146">The service provider does not implement the copy operation.</span></span>
    
<span data-ttu-id="f6223-147">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="f6223-147">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="f6223-148">Das Source-Objekt, das den Kopier-oder Verschiebungsvorgang ausführt, enthält direkt oder indirekt das Zielobjekt.</span><span class="sxs-lookup"><span data-stu-id="f6223-148">The source object performing the copy or move operation directly or indirectly contains the destination object.</span></span> <span data-ttu-id="f6223-149">Möglicherweise wurde vor dem erkennen dieser Bedingung eine beträchtliche Arbeit ausgeführt, sodass die Quell-und Zielobjekte teilweise geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="f6223-149">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="f6223-150">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="f6223-150">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="f6223-151">Die vom _lpInterface_ -Parameter angegebene Schnittstelle wird vom Zielobjekt nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f6223-151">The interface identified by the  _lpInterface_ parameter is not supported by the destination object.</span></span> 
    
<span data-ttu-id="f6223-152">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="f6223-152">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="f6223-153">Es wurde versucht, auf ein Objekt zuzugreifen, für das der Aufrufer nicht über ausreichende Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="f6223-153">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="f6223-154">Dieser Fehler wird zurückgegeben, wenn das Zielobjekt mit dem Quellobjekt identisch ist.</span><span class="sxs-lookup"><span data-stu-id="f6223-154">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="f6223-155">Die folgenden Werte können in der **SPropProblemArray** -Struktur zurückgegeben werden, jedoch nicht als Rückgabewerte für **CopyProps**.</span><span class="sxs-lookup"><span data-stu-id="f6223-155">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **CopyProps**.</span></span> <span data-ttu-id="f6223-156">Diese Fehler gelten für eine einzelne Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f6223-156">These errors apply to a single property.</span></span>
  
<span data-ttu-id="f6223-157">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="f6223-157">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="f6223-158">Entweder wurde das MAPI_UNICODE-Flag festgelegt, und **CopyProps** unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und **CopyProps** unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="f6223-158">Either the MAPI_UNICODE flag was set and **CopyProps** does not support Unicode, or MAPI_UNICODE was not set and **CopyProps** supports only Unicode.</span></span> 
    
<span data-ttu-id="f6223-159">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="f6223-159">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="f6223-160">Die Eigenschaft kann vom Aufrufer nicht geändert werden, da es sich um eine schreibgeschützte Eigenschaft handelt, die vom Besitzer des Zielobjekts berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="f6223-160">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="f6223-161">Dieser Fehler ist nicht schwerwiegend; der Aufrufer sollte den Kopiervorgang fortsetzen lassen.</span><span class="sxs-lookup"><span data-stu-id="f6223-161">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="f6223-162">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="f6223-162">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="f6223-163">Der Eigenschaftentyp ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="f6223-163">The property type is invalid.</span></span>
    
<span data-ttu-id="f6223-164">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="f6223-164">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="f6223-165">Der Eigenschaftentyp ist nicht der vom Aufrufer erwartete Typ.</span><span class="sxs-lookup"><span data-stu-id="f6223-165">The property type is not the type expected by the caller.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f6223-166">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f6223-166">Remarks</span></span>

<span data-ttu-id="f6223-167">Die **IMAPIProp:: CopyProps** -Methode kopiert oder verschiebt ausgewählte Eigenschaften aus dem aktuellen Objekt in ein Zielobjekt.</span><span class="sxs-lookup"><span data-stu-id="f6223-167">The **IMAPIProp::CopyProps** method copies or moves selected properties from the current object to a destination object.</span></span> <span data-ttu-id="f6223-168">**CopyProps** wird hauptsächlich zum beantworten und Weiterleiten von Nachrichten verwendet, wobei nur einige der Eigenschaften der ursprünglichen Nachricht mit der Antwort oder der weitergeleiteten Kopie Reisen.</span><span class="sxs-lookup"><span data-stu-id="f6223-168">**CopyProps** is used mainly for replying to and forwarding messages, where only some of the properties from the original message travel with the reply or forwarded copy.</span></span> 
  
<span data-ttu-id="f6223-169">Alle unter Objekte im Source-Objekt werden automatisch in den Vorgang eingeschlossen und vollständig kopiert oder verschoben, unabhängig von der Verwendung von Eigenschaften, die in der [SPropTagArray](sproptagarray.md) -Struktur angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="f6223-169">Any subobjects in the source object are automatically included in the operation and copied or moved in their entirety, regardless of the use of properties indicated by the [SPropTagArray](sproptagarray.md) structure.</span></span> <span data-ttu-id="f6223-170">Standardmäßig überschreibt **CopyProps** alle Eigenschaften im Zielobjekt, die Eigenschaften des Source-Objekts erfüllen.</span><span class="sxs-lookup"><span data-stu-id="f6223-170">By default, **CopyProps** overwrites any properties in the destination object that match properties from the source object.</span></span> <span data-ttu-id="f6223-171">Wenn eine der kopierten oder verschobenen Eigenschaften bereits im Zielobjekt vorhanden ist, werden die vorhandenen Eigenschaften von den neuen Eigenschaften überschrieben, es sei denn, das MAPI_NOREPLACE-Flag wird im _ulFlags_ -Parameter festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f6223-171">If any of the copied or moved properties already exist in the destination object, the existing properties are overwritten by the new properties, unless the MAPI_NOREPLACE flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="f6223-172">Vorhandene Informationen im Zielobjekt, das nicht überschrieben wird, bleiben unberührt.</span><span class="sxs-lookup"><span data-stu-id="f6223-172">Existing information in the destination object that is not overwritten is left untouched.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f6223-173">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="f6223-173">Notes to implementers</span></span>

<span data-ttu-id="f6223-174">Sie können eine vollständige Implementierung von **CopyProps** bereitstellen oder sich auf die Implementierung verlassen, die MAPI im Unterstützungsobjekt bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="f6223-174">You can provide a full implementation of **CopyProps** or rely on the implementation that MAPI provides in its support object.</span></span> <span data-ttu-id="f6223-175">Wenn Sie die MAPI-Implementierung verwenden möchten, rufen Sie die **IMAPISupport::D ocopyprops** -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="f6223-175">If you want to use the MAPI implementation, call the **IMAPISupport::DoCopyProps** method.</span></span> <span data-ttu-id="f6223-176">Wenn Sie jedoch die Verarbeitung an **DoCopyProps** delegieren und das MAPI_DECLINE_OK-Flag übergeben werden, vermeiden Sie den Support Aufruf, und geben Sie stattdessen MAPI_E_DECLINE_COPY zurück.</span><span class="sxs-lookup"><span data-stu-id="f6223-176">However, if you do delegate processing to **DoCopyProps** and you are passed the MAPI_DECLINE_OK flag, avoid the support call and return MAPI_E_DECLINE_COPY instead.</span></span> <span data-ttu-id="f6223-177">Sie werden mit dieser Kennzeichnung von MAPI aufgerufen, um eine mögliche Rekursion zu vermeiden, die beim Kopieren von Ordnern auftreten kann.</span><span class="sxs-lookup"><span data-stu-id="f6223-177">You will be called with this flag by MAPI to avoid the possible recursion that can occur when you copy folders.</span></span> 
  
<span data-ttu-id="f6223-178">Da der Kopiervorgang langwierig sein kann, sollten Sie eine Statusanzeige anzeigen.</span><span class="sxs-lookup"><span data-stu-id="f6223-178">Because the copy operation can be lengthy, you should display a progress indicator.</span></span> <span data-ttu-id="f6223-179">Verwenden Sie die [IMAPIProgress](imapiprogressiunknown.md) -Implementierung, die im _lpProgress_ -Parameter übergeben wird, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="f6223-179">Use the [IMAPIProgress](imapiprogressiunknown.md) implementation that is passed in the  _lpProgress_ parameter, if there is one.</span></span> <span data-ttu-id="f6223-180">Wenn _lpProgress_ ist \*\*\*\*, rufen sie die [IMAPISupport::D oprogressdialog](imapisupport-doprogressdialog.md) -Methode auf, um die MAPI-Implementierung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="f6223-180">If  _lpProgress_ is **null**, call the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method to use the MAPI implementation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f6223-181">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="f6223-181">Notes to callers</span></span>

<span data-ttu-id="f6223-182">Legen Sie das MAPI_DECLINE_OK-Flag nicht fest; Sie wird von MAPI in ihren Aufrufen von **CopyProps** -Implementierungen des Nachrichtenspeicher Anbieters verwendet.</span><span class="sxs-lookup"><span data-stu-id="f6223-182">Do not set the MAPI_DECLINE_OK flag; it is used by MAPI in its calls to message store provider **CopyProps** implementations.</span></span> 
  
<span data-ttu-id="f6223-183">Da Kopier-und Verschiebungsvorgänge Zeit in Anspruch nehmen können, ist es ratsam, eine Statusanzeige anzufordern, indem Sie das MAPI_DIALOG-Flag festlegen.</span><span class="sxs-lookup"><span data-stu-id="f6223-183">Because copy and move operations can take time, it is wise to request the display of a progress indicator by setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="f6223-184">Sie können den Parameter _lpProgress_ auf die Implementierung von **IMAPIProgress**festlegen, sofern vorhanden, oder auf **null**.</span><span class="sxs-lookup"><span data-stu-id="f6223-184">You can set the  _lpProgress_ parameter to your implementation of **IMAPIProgress**, if you have one, or to **null**.</span></span> <span data-ttu-id="f6223-185">Wenn _lpProgress_ ist \*\*\*\*, verwendet **CopyProps** die Standard Fortschrittsanzeige von MAPI.</span><span class="sxs-lookup"><span data-stu-id="f6223-185">If  _lpProgress_ is **null**, **CopyProps** will use the default progress indicator provided by MAPI.</span></span> 
  
<span data-ttu-id="f6223-186">Sie können die Anzeige einer Statusanzeige unterdrücken, indem Sie das MAPI_DIALOG-Flag nicht festlegen.</span><span class="sxs-lookup"><span data-stu-id="f6223-186">You can suppress the display of a progress indicator by not setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="f6223-187">**CopyProps** ignoriert die Parameter _ulUIParam_ und _lpProgress_ und verhindert die Anzeige des Indikators.</span><span class="sxs-lookup"><span data-stu-id="f6223-187">**CopyProps** will ignore the  _ulUIParam_ and  _lpProgress_ parameters and avoid displaying the indicator.</span></span> 
  
 <span data-ttu-id="f6223-188">**CopyProps** kann globale und einzelne Fehler oder Fehler melden, die mit einer oder mehreren Eigenschaften auftreten.</span><span class="sxs-lookup"><span data-stu-id="f6223-188">**CopyProps** can report global and individual errors, or errors that occur with one or more of the properties.</span></span> <span data-ttu-id="f6223-189">Diese einzelnen Fehler werden in eine **SPropProblemArray** -Struktur eingefügt.</span><span class="sxs-lookup"><span data-stu-id="f6223-189">These individual errors are put in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="f6223-190">Sie können die Fehlerberichterstattung auf der Eigenschaftsebene unterdrücken, indem Sie **null**anstelle eines gültigen Zeigers für den Array Struktur Parameter der Eigenschafts Problem übergeben.</span><span class="sxs-lookup"><span data-stu-id="f6223-190">You can suppress error reporting at the property level by passing **null**, instead of a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="f6223-191">Wenn Sie Informationen zu Fehlern erhalten möchten, übergeben Sie einen gültigen **SPropProblemArray** -Struktur Zeiger im _lppProblems_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="f6223-191">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="f6223-192">Wenn **COPYPROPS** S_OK zurückgibt, überprüfen Sie auf mögliche Fehler mit einzelnen Eigenschaften in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="f6223-192">When **CopyProps** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="f6223-193">Wenn **CopyProps** einen Fehler zurückgibt, werden in der **SPropProblemArray** -Struktur keine Informationen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f6223-193">When **CopyProps** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="f6223-194">Rufen Sie stattdessen die [IMAPIProp:: getlasterroraufzurufen](imapiprop-getlasterror.md) -Methode auf, um detaillierte Fehlerinformationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f6223-194">Instead, call the [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="f6223-195">Wenn **COPYPROPS** S_OK zurückgibt, können Sie die zurückgegebene **SPropProblemArray** -Struktur freigeben, indem Sie die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f6223-195">If **CopyProps** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="f6223-196">Wenn Sie Eigenschaften kopieren, die für den Quellobjekttyp eindeutig sind, müssen Sie sicherstellen, dass das Zielobjekt denselben Typ aufweist.</span><span class="sxs-lookup"><span data-stu-id="f6223-196">If you are copying properties that are unique to the source object type, you must make sure that the destination object is of the same type.</span></span> <span data-ttu-id="f6223-197">**CopyProps** verhindert nicht, dass Sie Eigenschaften zuordnen, die normalerweise zu einem Objekttyp mit einem anderen Objekttyp gehören.</span><span class="sxs-lookup"><span data-stu-id="f6223-197">**CopyProps** does not prevent you from associating properties that typically belong to one type of object with another type of object.</span></span> <span data-ttu-id="f6223-198">Sie müssen die Eigenschaften kopieren, die für das Zielobjekt sinnvoll sind.</span><span class="sxs-lookup"><span data-stu-id="f6223-198">It is up to you to copy properties that make sense for the destination object.</span></span> <span data-ttu-id="f6223-199">Sie sollten beispielsweise keine Nachrichteneigenschaften in einen Adressbuchcontainer kopieren.</span><span class="sxs-lookup"><span data-stu-id="f6223-199">For example, you should not copy message properties to an address book container.</span></span> 
  
<span data-ttu-id="f6223-200">Um sicherzustellen, dass Sie zwischen Objekten desselben Typs kopieren, überprüfen Sie, ob das Quell-und Zielobjekt derselbe Typ ist, indem Sie entweder Objektzeiger vergleichen oder die [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f6223-200">To ensure that you are copying between objects of the same type, check that the source and destination object are the same type, either by comparing object pointers or calling the [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) method.</span></span> <span data-ttu-id="f6223-201">Legen Sie die Schnittstellenkennung, auf die von _lpInterface_ verwiesen wird, auf die Standardschnittstelle für das Source-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="f6223-201">Set the interface identifier pointed to by  _lpInterface_ to the standard interface for the source object.</span></span> <span data-ttu-id="f6223-202">Stellen Sie außerdem sicher, dass die Eigenschaft Objekttyp oder **PR_OBJECT_TYPE** ([pidtagobjecttype (](pidtagobjecttype-canonical-property.md)) für die beiden Objekte identisch ist.</span><span class="sxs-lookup"><span data-stu-id="f6223-202">Also, ensure that the object type or **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property is the same for the two objects.</span></span> <span data-ttu-id="f6223-203">Wenn Sie beispielsweise aus einer Nachricht kopieren, legen Sie _lpInterface_ auf IID_IMessage und **PR_OBJECT_TYPE** für beide Objekte auf MAPI_MESSAGE.</span><span class="sxs-lookup"><span data-stu-id="f6223-203">For example, if you are copying from a message, set  _lpInterface_ to IID_IMessage and the **PR_OBJECT_TYPE** for both objects to MAPI_MESSAGE.</span></span> 
  
<span data-ttu-id="f6223-204">Wenn ein ungültiger Zeiger im _lpDestObj_ -Parameter übergeben wird, sind die Ergebnisse unvorhersehbar.</span><span class="sxs-lookup"><span data-stu-id="f6223-204">If an invalid pointer is passed in the  _lpDestObj_ parameter, the results are unpredictable.</span></span> 
  
<span data-ttu-id="f6223-205">Um die Empfängerliste einer Nachricht zu kopieren, rufen Sie die **CopyProps** -Methode der Nachricht auf, und schließen Sie die **PR_MESSAGE_RECIPIENTS** ([pidtagmessagerecipients (](pidtagmessagerecipients-canonical-property.md))-Eigenschaft in das Tag-Array der Eigenschaft ein.</span><span class="sxs-lookup"><span data-stu-id="f6223-205">To copy a message's recipient list, call the message's **CopyProps** method and include the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property in the property tag array.</span></span> <span data-ttu-id="f6223-206">Schließen Sie die **PR_MESSAGE_ATTACHMENTS** ([pidtagmessageattachments (](pidtagmessageattachments-canonical-property.md))-Eigenschaft ein, um die Anlagen der Nachricht zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="f6223-206">To copy the message's attachments, include the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="f6223-207">Wenn Sie die Hierarchie-oder Inhaltstabelle eines Ordner-oder Adressbuch Containers kopieren möchten, schließen Sie die Eigenschaften **PR_CONTAINER_HIERARCHY** ([Pidtagcontainerhierarchy (](pidtagcontainerhierarchy-canonical-property.md)) oder **PR_CONTAINER_CONTENTS** ([pidtagcontainercontents (](pidtagcontainercontents-canonical-property.md)) in das Array für Property-Tags.</span><span class="sxs-lookup"><span data-stu-id="f6223-207">To copy a folder or address book container's hierarchy or contents table, include the **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) properties in the property tag array.</span></span> <span data-ttu-id="f6223-208">Schließen Sie die **PR_FOLDER_ASSOCIATED_CONTENTS** ([pidtagfolderassociatedcontents (](pidtagfolderassociatedcontents-canonical-property.md))-Eigenschaft in das Array ein, um die zugeordnete Inhaltstabelle eines Ordners einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="f6223-208">To include a folder's associated contents table, include the **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) property in the array.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f6223-209">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="f6223-209">MFCMAPI reference</span></span>

<span data-ttu-id="f6223-210">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="f6223-210">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f6223-211">**Datei**</span><span class="sxs-lookup"><span data-stu-id="f6223-211">**File**</span></span>|<span data-ttu-id="f6223-212">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="f6223-212">**Function**</span></span>|<span data-ttu-id="f6223-213">**Comment**</span><span class="sxs-lookup"><span data-stu-id="f6223-213">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f6223-214">MAPIFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="f6223-214">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="f6223-215">CopyNamedProps</span><span class="sxs-lookup"><span data-stu-id="f6223-215">CopyNamedProps</span></span>  <br/> |<span data-ttu-id="f6223-216">MFCMAPI verwendet die **IMAPIProp:: CopyProps** -Methode, um benannte Eigenschaften aus einer Nachricht in eine andere zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="f6223-216">MFCMAPI uses the **IMAPIProp::CopyProps** method to copy named properties from one message to another.</span></span>  <br/> |
|<span data-ttu-id="f6223-217">SingleMAPIPropListCtrl. cpp</span><span class="sxs-lookup"><span data-stu-id="f6223-217">SingleMAPIPropListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="f6223-218">CSingleMAPIPropListCtrl:: onPasteproperty</span><span class="sxs-lookup"><span data-stu-id="f6223-218">CSingleMAPIPropListCtrl::OnPasteProperty</span></span>  <br/> |<span data-ttu-id="f6223-219">MFCMAPI verwendet die **IMAPIProp:: CopyProps** -Methode, um eine Eigenschaft einzufügen, die aus einem anderen Objekt kopiert wurde.</span><span class="sxs-lookup"><span data-stu-id="f6223-219">MFCMAPI uses the **IMAPIProp::CopyProps** method to paste a property that has been copied from another object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f6223-220">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f6223-220">See also</span></span>



[<span data-ttu-id="f6223-221">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="f6223-221">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
  
[<span data-ttu-id="f6223-222">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f6223-222">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="f6223-223">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="f6223-223">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
  
[<span data-ttu-id="f6223-224">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="f6223-224">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="f6223-225">IMAPISupport::DoCopyProps</span><span class="sxs-lookup"><span data-stu-id="f6223-225">IMAPISupport::DoCopyProps</span></span>](imapisupport-docopyprops.md)
  
[<span data-ttu-id="f6223-226">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="f6223-226">IMAPISupport::DoProgressDialog</span></span>](imapisupport-doprogressdialog.md)
  
[<span data-ttu-id="f6223-227">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="f6223-227">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="f6223-228">Kanonische Pidtagcontainercontents (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f6223-228">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="f6223-229">Kanonische Pidtagcontainerhierarchy (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f6223-229">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="f6223-230">Kanonische PidTagDisplayName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f6223-230">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)
  
[<span data-ttu-id="f6223-231">Kanonische Pidtagfolderassociatedcontents (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f6223-231">PidTagFolderAssociatedContents Canonical Property</span></span>](pidtagfolderassociatedcontents-canonical-property.md)
  
[<span data-ttu-id="f6223-232">Kanonische Pidtagmessageattachments (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f6223-232">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="f6223-233">Kanonische Pidtagmessagerecipients (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f6223-233">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="f6223-234">Kanonische Pidtagobjecttype (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f6223-234">PidTagObjectType Canonical Property</span></span>](pidtagobjecttype-canonical-property.md)
  
[<span data-ttu-id="f6223-235">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="f6223-235">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="f6223-236">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="f6223-236">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="f6223-237">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f6223-237">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="f6223-238">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="f6223-238">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

