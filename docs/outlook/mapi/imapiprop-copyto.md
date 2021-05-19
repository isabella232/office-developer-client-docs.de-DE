---
title: IMAPIPropCopyTo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.CopyTo
api_type:
- COM
ms.assetid: e56042e9-5bb7-4a99-b6de-1546d4ca07f0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f76b0a5482647fe3e181a36d7dcd8cb60ffc8985
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356392"
---
# <a name="imapipropcopyto"></a><span data-ttu-id="b9714-103">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="b9714-103">IMAPIProp::CopyTo</span></span>

  
  
<span data-ttu-id="b9714-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b9714-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b9714-105">Kopiert oder verschiebt alle Eigenschaften, mit Ausnahme speziell ausgeschlossener Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b9714-105">Copies or moves all properties, except for specifically excluded properties.</span></span>
  
```cpp
HRESULT CopyTo(
 ULONG ciidExclude,
 LPCIID rgiidExclude,
 LPSPropTagArray lpExcludeProps,
 ULONG_PTR ulUIParam,
 LPMAPIPROGRESS lpProgress,
 LPCIID lpInterface,
 LPVOID lpDestObj,
 ULONG ulFlags,
 LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="b9714-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9714-106">Parameters</span></span>

 <span data-ttu-id="b9714-107">_ciidExclude_</span><span class="sxs-lookup"><span data-stu-id="b9714-107">_ciidExclude_</span></span>
  
> <span data-ttu-id="b9714-108">[in] Die Anzahl von Schnittstellen, die ausgeschlossen werden sollen, wenn Eigenschaften kopiert oder verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="b9714-108">[in] The count of interfaces to exclude when properties are copied or moved.</span></span>
    
 <span data-ttu-id="b9714-109">_rgiidExclude_</span><span class="sxs-lookup"><span data-stu-id="b9714-109">_rgiidExclude_</span></span>
  
> <span data-ttu-id="b9714-110">[in] Ein Array von Schnittstellenbezeichnern (Interface Identifiers, IIDs), die Schnittstellen angeben, die nicht verwendet werden sollten, wenn ergänzende Informationen kopiert oder in das Zielobjekt verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="b9714-110">[in] An array of interface identifiers (IIDs) that specify interfaces that should not be used when supplemental information is copied or moved to the destination object.</span></span>
    
 <span data-ttu-id="b9714-111">_lpExcludeProps_</span><span class="sxs-lookup"><span data-stu-id="b9714-111">_lpExcludeProps_</span></span>
  
> <span data-ttu-id="b9714-112">[in] Ein Zeiger auf ein Eigenschaftentagarray, das die Eigenschaftstags identifiziert, die vom Kopier- oder Verschiebevorgang ausgeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b9714-112">[in] A pointer to a property tag array that identifies the property tags that should be excluded from the copy or move operation.</span></span> <span data-ttu-id="b9714-113">Das Übergeben von **null** im  _lpExcludeProps-Parameter_ gibt an, dass alle Eigenschaften des Objekts kopiert oder verschoben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b9714-113">Passing **null** in the  _lpExcludeProps_ parameter indicates that all of the object's properties should be copied or moved.</span></span> <span data-ttu-id="b9714-114">**CopyTo** gibt MAPI_E_INVALID_PARAMETER zurück, wenn **das cValues-Element** der [SPropProblemArray-Struktur,](spropproblemarray.md) auf die  _von lpExcludeProps_ verwiesen wird, auf 0 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b9714-114">**CopyTo** returns MAPI_E_INVALID_PARAMETER when the **cValues** member of the [SPropProblemArray](spropproblemarray.md) structure pointed to by  _lpExcludeProps_ is set to 0.</span></span> 
    
 <span data-ttu-id="b9714-115">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="b9714-115">_ulUIParam_</span></span>
  
> <span data-ttu-id="b9714-116">[in] Ein Handle zum übergeordneten Fenster des Statusindikators.</span><span class="sxs-lookup"><span data-stu-id="b9714-116">[in] A handle to the parent window of the progress indicator.</span></span> 
    
 <span data-ttu-id="b9714-117">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="b9714-117">_lpProgress_</span></span>
  
> <span data-ttu-id="b9714-118">[in] Ein Zeiger auf eine Fortschrittsindikatorimplementierung.</span><span class="sxs-lookup"><span data-stu-id="b9714-118">[in] A pointer to a progress indicator implementation.</span></span> <span data-ttu-id="b9714-119">Wenn **null** im  _lpProgress-Parameter übergeben_ wird, stellt MAPI die Fortschrittsimplementierung.</span><span class="sxs-lookup"><span data-stu-id="b9714-119">If **null** is passed in the  _lpProgress_ parameter, MAPI provides the progress implementation.</span></span> <span data-ttu-id="b9714-120">Der  _lpProgress-Parameter_ wird ignoriert, es sei denn, das MAPI_DIALOG wird im  _ulFlags-Parameter_ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b9714-120">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="b9714-121">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="b9714-121">_lpInterface_</span></span>
  
> <span data-ttu-id="b9714-122">[in] Ein Zeiger auf den Schnittstellenbezeichner (Interface Identifier, IID), der die Schnittstelle darstellt, die für den Zugriff auf das Objekt verwendet werden soll, auf das der  _lpDestObj-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="b9714-122">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object pointed to by the  _lpDestObj_ parameter.</span></span> <span data-ttu-id="b9714-123">Der _lpInterface-Parameter_ darf nicht null **sein.**</span><span class="sxs-lookup"><span data-stu-id="b9714-123">The  _lpInterface_ parameter must not be **null**.</span></span>
    
 <span data-ttu-id="b9714-124">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="b9714-124">_lpDestObj_</span></span>
  
> <span data-ttu-id="b9714-125">[in] Ein Zeiger auf das Objekt, um die kopierten oder verschobenen Eigenschaften zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="b9714-125">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="b9714-126">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b9714-126">_ulFlags_</span></span>
  
> <span data-ttu-id="b9714-127">[in] Eine Bitmaske mit Flags, die den Kopier- oder Verschiebevorgang steuert.</span><span class="sxs-lookup"><span data-stu-id="b9714-127">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="b9714-128">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="b9714-128">The following flags can be set:</span></span>
    
<span data-ttu-id="b9714-129">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="b9714-129">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="b9714-130">Wenn **CopyTo** die [IMAPISupport::D oCopyTo-Methode](imapisupport-docopyto.md) aufruft, um den Kopier- oder Verschiebevorgang zu verarbeiten, sollte es stattdessen sofort mit dem Fehlerwert MAPI_E_DECLINE_COPY.</span><span class="sxs-lookup"><span data-stu-id="b9714-130">If **CopyTo** calls the [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) method to handle the copy or move operation, it should instead return immediately with the error value MAPI_E_DECLINE_COPY.</span></span> <span data-ttu-id="b9714-131">Das MAPI_DECLINE_OK wird von MAPI festgelegt, um die Rekursion zu begrenzen.</span><span class="sxs-lookup"><span data-stu-id="b9714-131">The MAPI_DECLINE_OK flag is set by MAPI to limit recursion.</span></span> <span data-ttu-id="b9714-132">Clients legen dieses Flag nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b9714-132">Clients do not set this flag.</span></span> 
    
<span data-ttu-id="b9714-133">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="b9714-133">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="b9714-134">Zeigt eine Statusanzeige an.</span><span class="sxs-lookup"><span data-stu-id="b9714-134">Displays a progress indicator.</span></span>
    
<span data-ttu-id="b9714-135">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="b9714-135">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="b9714-136">**CopyTo** sollte einen Verschiebevorgang anstelle eines Kopiervorgangs ausführen.</span><span class="sxs-lookup"><span data-stu-id="b9714-136">**CopyTo** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="b9714-137">Wenn dieses Flag nicht festgelegt ist, führt **CopyTo** einen Kopiervorgang aus.</span><span class="sxs-lookup"><span data-stu-id="b9714-137">When this flag is not set, **CopyTo** performs a copy operation.</span></span> 
    
<span data-ttu-id="b9714-138">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="b9714-138">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="b9714-139">Vorhandene Eigenschaften im Zielobjekt sollten nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="b9714-139">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="b9714-140">Wenn dieses Flag nicht festgelegt ist, überschreibt **CopyTo** vorhandene Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b9714-140">When this flag is not set, **CopyTo** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="b9714-141">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="b9714-141">_lppProblems_</span></span>
  
> <span data-ttu-id="b9714-142">[in, out] Bei der Eingabe ein Zeiger auf einen Zeiger auf eine **SPropProblemArray-Struktur;** andernfalls **null**, gibt an, dass keine Fehlerinformationen benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="b9714-142">[in, out] On input, a pointer to a pointer to an **SPropProblemArray** structure; otherwise, **null**, indicating no need for error information.</span></span> <span data-ttu-id="b9714-143">Wenn  _lppProblems_ ein gültiger Zeiger für die Eingabe ist, gibt **CopyTo** detaillierte Informationen zu Fehlern beim Kopieren einer oder mehreren Eigenschaften zurück.</span><span class="sxs-lookup"><span data-stu-id="b9714-143">If  _lppProblems_ is a valid pointer on input, **CopyTo** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b9714-144">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b9714-144">Return value</span></span>

<span data-ttu-id="b9714-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="b9714-145">S_OK</span></span> 
  
> <span data-ttu-id="b9714-146">Die Eigenschaften wurden erfolgreich kopiert oder verschoben.</span><span class="sxs-lookup"><span data-stu-id="b9714-146">The properties have been successfully copied or moved.</span></span>
    
<span data-ttu-id="b9714-147">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="b9714-147">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="b9714-148">Ein Unterobjekt kann nicht kopiert werden, da ein Unterobjekt mit demselben Anzeigenamen – angegeben durch die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft – bereits im Zielobjekt vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b9714-148">A subobject cannot be copied because a subobject with the same display name — specified by the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property — already exists in the destination object.</span></span> 
    
<span data-ttu-id="b9714-149">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="b9714-149">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="b9714-150">Der Dienstanbieter implementiert den Kopiervorgang nicht.</span><span class="sxs-lookup"><span data-stu-id="b9714-150">The service provider does not implement the copy operation.</span></span>
    
<span data-ttu-id="b9714-151">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="b9714-151">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="b9714-152">Das Quellobjekt, das den Kopier- oder Verschiebevorgang direkt oder indirekt ausführen, enthält das Zielobjekt.</span><span class="sxs-lookup"><span data-stu-id="b9714-152">The source object performing the copy or move operation directly or indirectly contains the destination object.</span></span> <span data-ttu-id="b9714-153">Bevor diese Bedingung erkannt wurde, wurden möglicherweise erhebliche Arbeiten ausgeführt, sodass die Quell- und Zielobjekte teilweise geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="b9714-153">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="b9714-154">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="b9714-154">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="b9714-155">Die vom  _lpInterface-Parameter identifizierte_ Schnittstelle wird vom Zielobjekt nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b9714-155">The interface identified by the  _lpInterface_ parameter is not supported by the destination object.</span></span> 
    
<span data-ttu-id="b9714-156">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="b9714-156">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="b9714-157">Es wurde versucht, auf ein Objekt zu zugreifen, für das der Aufrufer nicht über ausreichende Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="b9714-157">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="b9714-158">Dieser Fehler wird zurückgegeben, wenn das Zielobjekt mit dem Quellobjekt identisch ist.</span><span class="sxs-lookup"><span data-stu-id="b9714-158">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="b9714-159">Die folgenden Werte können in der **SPropProblemArray-Struktur** zurückgegeben werden, jedoch nicht als Rückgabewerte für **CopyTo**.</span><span class="sxs-lookup"><span data-stu-id="b9714-159">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **CopyTo**.</span></span> <span data-ttu-id="b9714-160">Die folgenden Fehler gelten für eine einzelne Eigenschaft:</span><span class="sxs-lookup"><span data-stu-id="b9714-160">The following errors apply to a single property:</span></span>
  
<span data-ttu-id="b9714-161">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="b9714-161">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="b9714-162">Entweder wurde MAPI_UNICODE-Flag festgelegt, **und CopyTo** unterstützt unicode nicht, oder MAPI_UNICODE nicht festgelegt, und **CopyTo** unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="b9714-162">Either the MAPI_UNICODE flag was set and **CopyTo** does not support Unicode, or MAPI_UNICODE was not set and **CopyTo** supports only Unicode.</span></span> 
    
<span data-ttu-id="b9714-163">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="b9714-163">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="b9714-164">Die Eigenschaft kann vom Aufrufer nicht geändert werden, da es sich um eine schreibgeschützte Eigenschaft handelt, die vom Besitzer des Zielobjekts berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="b9714-164">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="b9714-165">Dieser Fehler ist nicht schwerwiegender. Der Aufrufer sollte zulassen, dass der Kopiervorgang fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="b9714-165">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="b9714-166">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="b9714-166">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="b9714-167">Der Eigenschaftentyp ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="b9714-167">The property type is invalid.</span></span>
    
<span data-ttu-id="b9714-168">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="b9714-168">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="b9714-169">Der Eigenschaftstyp ist nicht der typ, der vom Aufrufer erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="b9714-169">The property type is not the type expected by the caller.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b9714-170">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b9714-170">Remarks</span></span>

<span data-ttu-id="b9714-171">Standardmäßig kopiert oder verschiebt die **IMAPIProp::CopyTo-Methode** alle Eigenschaften des aktuellen Objekts in ein Zielobjekt.</span><span class="sxs-lookup"><span data-stu-id="b9714-171">By default, the **IMAPIProp::CopyTo** method copies or moves all of the current object's properties to a destination object.</span></span> <span data-ttu-id="b9714-172">**CopyTo** wird verwendet, wenn ein Objekt genau kopiert oder verschoben werden soll, während alle oder die meisten eigenschaften intakt sind.</span><span class="sxs-lookup"><span data-stu-id="b9714-172">**CopyTo** is used when an object should be copied or moved exactly, with all or most of its properties intact.</span></span> 
  
<span data-ttu-id="b9714-173">Alle Unterobjekte im Quellobjekt werden automatisch in den Vorgang einbezogen und vollständig kopiert oder verschoben.</span><span class="sxs-lookup"><span data-stu-id="b9714-173">Any subobjects in the source object are automatically included in the operation and are copied or moved in their entirety.</span></span> <span data-ttu-id="b9714-174">Standardmäßig überschreibt **CopyTo** alle Eigenschaften im Zielobjekt, die eigenschaften des Quellobjekts entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b9714-174">By default, **CopyTo** overwrites any properties in the destination object that match properties from the source object.</span></span> <span data-ttu-id="b9714-175">Wenn eine der kopierten oder verschobenen Eigenschaften bereits im Zielobjekt vorhanden ist, werden die vorhandenen Eigenschaften von den neuen Eigenschaften überschrieben, es sei denn, das flag MAPI_NOREPLACE wird im  _ulFlags-Parameter_ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b9714-175">If any of the copied or moved properties already exist in the destination object, the existing properties are overwritten by the new properties, unless the MAPI_NOREPLACE flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="b9714-176">Vorhandene Informationen im Zielobjekt, die nicht überschrieben werden, bleiben unverändert.</span><span class="sxs-lookup"><span data-stu-id="b9714-176">Existing information in the destination object that is not overwritten is left untouched.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="b9714-177">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="b9714-177">Notes to implementers</span></span>

<span data-ttu-id="b9714-178">Sie können eine vollständige Implementierung von **CopyTo** bereitstellen oder sich auf die Implementierung verlassen, die MAPI in seinem Supportobjekt bietet.</span><span class="sxs-lookup"><span data-stu-id="b9714-178">You can provide a full implementation of **CopyTo** or rely on the implementation that MAPI provides in its support object.</span></span> <span data-ttu-id="b9714-179">Wenn Sie die MAPI-Implementierung verwenden möchten, rufen Sie **IMAPISupport::D oCopyTo auf.**</span><span class="sxs-lookup"><span data-stu-id="b9714-179">If you want to use the MAPI implementation, call **IMAPISupport::DoCopyTo**.</span></span> <span data-ttu-id="b9714-180">Wenn Sie jedoch die Verarbeitung an **DoCopyTo** delegieren und das MAPI_DECLINE_OK übergeben werden, vermeiden Sie den Supportaufruf, und geben Sie MAPI_E_DECLINE_COPY zurück.</span><span class="sxs-lookup"><span data-stu-id="b9714-180">However, if you do delegate processing to **DoCopyTo** and you are passed the MAPI_DECLINE_OK flag, avoid the support call and return MAPI_E_DECLINE_COPY instead.</span></span> <span data-ttu-id="b9714-181">MAPI wird mit diesem Flag aufrufen, um eine mögliche Rekursion zu vermeiden, die beim Kopieren von Ordnern auftreten kann.</span><span class="sxs-lookup"><span data-stu-id="b9714-181">MAPI will call with this flag to avoid the possible recursion that can happen when folders are copied.</span></span> 
  
<span data-ttu-id="b9714-182">Da der Kopiervorgang sehr lang sein kann, sollten Sie eine Statusanzeige anzeigen.</span><span class="sxs-lookup"><span data-stu-id="b9714-182">Because the copy operation can be lengthy, you should display a progress indicator.</span></span> <span data-ttu-id="b9714-183">Verwenden Sie [die IMAPIProgress-Implementierung,](imapiprogressiunknown.md) die im  _lpProgress-Parameter_ übergeben wird, falls eine dieser Implementierungen vor ist.</span><span class="sxs-lookup"><span data-stu-id="b9714-183">Use the [IMAPIProgress](imapiprogressiunknown.md) implementation passed in the  _lpProgress_ parameter, if there is one.</span></span> <span data-ttu-id="b9714-184">Wenn  _lpProgress_ **null** ist, rufen Sie die [IMAPISupport::D oProgressDialog-Methode](imapisupport-doprogressdialog.md) auf, um die MAPI-Implementierung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b9714-184">If  _lpProgress_ is **null**, call the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method to use the MAPI implementation.</span></span> 
  
<span data-ttu-id="b9714-185">Versuchen Sie nicht, bekannte schreibgeschützte Eigenschaften im Zielobjekt zu setzen. Geben Sie MAPI_E_NO_ACCESS zurück.</span><span class="sxs-lookup"><span data-stu-id="b9714-185">Do not attempt to set any known read-only properties in the destination object; return MAPI_E_NO_ACCESS instead.</span></span>
  
<span data-ttu-id="b9714-186">Die Quell- und Zielobjekte sollten die gleichen Schnittstellen verwenden.</span><span class="sxs-lookup"><span data-stu-id="b9714-186">The source and destination objects should use the same interfaces.</span></span> <span data-ttu-id="b9714-187">Geben MAPI_E_INVALID_PARAMETER zurück,  _wenn lpInterface_ nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b9714-187">Return MAPI_E_INVALID_PARAMETER if  _lpInterface_ is not set.</span></span> 
  
<span data-ttu-id="b9714-188">Geben MAPI_E_INTERFACE_NOT_SUPPORTED zurück, wenn alle bekannten Schnittstellen ausgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="b9714-188">Return MAPI_E_INTERFACE_NOT_SUPPORTED if all known interfaces are excluded.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="b9714-189">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="b9714-189">Notes to callers</span></span>

<span data-ttu-id="b9714-190">Legen Sie das #A0 MAPI_DECLINE_OK. MAPI verwendet es in den Aufrufen von **CopyTo-Implementierungen** des Nachrichtenspeicheranbieters.</span><span class="sxs-lookup"><span data-stu-id="b9714-190">Do not set the MAPI_DECLINE_OK flag; MAPI uses it in its calls to message store provider **CopyTo** implementations.</span></span> 
  
<span data-ttu-id="b9714-191">Da Kopier- und Verschiebevorgänge einige Zeit in Sich nehmen können, sollten Sie die Anzeige eines Statusindikators anfordern, indem Sie MAPI_DIALOG festlegen.</span><span class="sxs-lookup"><span data-stu-id="b9714-191">Because copy and move operations can take time, you should request the display of a progress indicator by setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="b9714-192">Sie können den  _lpProgress-Parameter_ auf Die Implementierung von **IMAPIProgress** festlegen, wenn Sie über einen verfügen, oder auf **null**.</span><span class="sxs-lookup"><span data-stu-id="b9714-192">You can set the  _lpProgress_ parameter to your implementation of **IMAPIProgress**, if you have one, or to **null**.</span></span> <span data-ttu-id="b9714-193">Wenn  _lpProgress_ **null** ist, verwendet **CopyTo** den standardmäßigen Fortschrittsindikator, den MAPI bietet.</span><span class="sxs-lookup"><span data-stu-id="b9714-193">If  _lpProgress_ is **null**, **CopyTo** will use the default progress indicator that MAPI provides.</span></span> 
  
<span data-ttu-id="b9714-194">Sie können die Anzeige eines Statusindikators unterdrücken, indem Sie das MAPI_DIALOG festlegen.</span><span class="sxs-lookup"><span data-stu-id="b9714-194">You can suppress the display of a progress indicator by not setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="b9714-195">**CopyTo** ignoriert die  _UlUIParam-_ und  _lpProgress-Parameter_ und zeigt den Indikator nicht an.</span><span class="sxs-lookup"><span data-stu-id="b9714-195">**CopyTo** will ignore the  _ulUIParam_ and  _lpProgress_ parameters and will not display the indicator.</span></span> 
  
 <span data-ttu-id="b9714-196">**CopyTo** kann globale und einzelne Fehler oder Fehler melden, die mit einer oder mehreren Eigenschaften auftreten.</span><span class="sxs-lookup"><span data-stu-id="b9714-196">**CopyTo** can report global and individual errors, or errors that occur with one or more properties.</span></span> <span data-ttu-id="b9714-197">Diese einzelnen Fehler werden in einer **SPropProblemArray-Struktur** platziert.</span><span class="sxs-lookup"><span data-stu-id="b9714-197">These individual errors are placed in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="b9714-198">Sie können die Fehlerberichterstellung auf Eigenschaftsebene unterdrücken, indem Sie **null** anstelle eines gültigen Zeigers für den Eigenschaftenproblemarraystrukturparameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="b9714-198">You can suppress error reporting at the property level by passing **null**, instead of a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="b9714-199">Wenn Sie Informationen zu Fehlern erhalten möchten, übergeben Sie einen gültigen **SPropProblemArray-Strukturzeiger** im _lppProblems-Parameter._</span><span class="sxs-lookup"><span data-stu-id="b9714-199">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="b9714-200">Wenn **CopyTo S_OK** zurückgibt, suchen Sie nach möglichen Fehlern mit einzelnen Eigenschaften in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="b9714-200">When **CopyTo** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="b9714-201">Wenn **CopyTo** einen Fehler zurückgibt, werden keine Informationen in der **SPropProblemArray-Struktur** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b9714-201">When **CopyTo** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="b9714-202">Rufen Sie stattdessen [IMAPIProp::GetLastError auf,](imapiprop-getlasterror.md) um detaillierte Fehlerinformationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b9714-202">Instead, call [IMAPIProp::GetLastError](imapiprop-getlasterror.md) to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="b9714-203">Wenn **CopyTo S_OK** zurückgibt, geben Sie die zurückgegebene **SPropProblemArray-Struktur** frei, indem Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b9714-203">If **CopyTo** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="b9714-204">Wenn Sie Eigenschaften kopieren, die für den Quellobjekttyp eindeutig sind, müssen Sie sicherstellen, dass das Zielobjekt denselben Typ hat.</span><span class="sxs-lookup"><span data-stu-id="b9714-204">If you copy properties that are unique to the source object type, you must ensure that the destination object is of the same type.</span></span> <span data-ttu-id="b9714-205">**CopyTo** verhindert nicht, dass Sie Eigenschaften, die in der Regel zu einem Objekttyp gehören, einem anderen Objekttyp zuordnen.</span><span class="sxs-lookup"><span data-stu-id="b9714-205">**CopyTo** does not prevent you from associating properties that typically belong to one type of object with another type of object.</span></span> <span data-ttu-id="b9714-206">Es liegt an Ihnen, Eigenschaften zu kopieren, die für das Zielobjekt sinnvoll sind.</span><span class="sxs-lookup"><span data-stu-id="b9714-206">It is up to you to copy properties that make sense for the destination object.</span></span> <span data-ttu-id="b9714-207">Beispielsweise sollten Sie nachrichteneigenschaften nicht in einen Adressbuchcontainer kopieren.</span><span class="sxs-lookup"><span data-stu-id="b9714-207">For example, you should not copy message properties to an address book container.</span></span> 
  
<span data-ttu-id="b9714-208">Um sicherzustellen, dass Sie zwischen Objekten desselben Typs kopieren, überprüfen Sie, ob quell- und zielobjekt derselbe Typ sind, indem Sie entweder Objektzeiger vergleichen oder [IUnknown::QueryInterface aufrufen.](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b9714-208">To ensure that you copy between objects of the same type, check that the source and destination object are the same type, either by comparing object pointers or calling [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx).</span></span> <span data-ttu-id="b9714-209">Legen Sie den Schnittstellenbezeichner, auf den  _lpInterface verweist,_ auf die Standardschnittstelle für das Quellobjekt.</span><span class="sxs-lookup"><span data-stu-id="b9714-209">Set the interface identifier pointed to by  _lpInterface_ to the standard interface for the source object.</span></span> <span data-ttu-id="b9714-210">Stellen Sie außerdem sicher, dass der Objekttyp **oder PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))-Eigenschaft für die beiden Objekte identisch ist.</span><span class="sxs-lookup"><span data-stu-id="b9714-210">Also, be sure that the object type or **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property is the same for the two objects.</span></span> <span data-ttu-id="b9714-211">Wenn Sie z. B. aus einer Nachricht kopieren, legen  Sie _lpInterface_ auf IID_IMessage und PR_OBJECT_TYPE für beide Objekte MAPI_MESSAGE.</span><span class="sxs-lookup"><span data-stu-id="b9714-211">For example, if you copy from a message, set  _lpInterface_ to IID_IMessage and the **PR_OBJECT_TYPE** for both objects to MAPI_MESSAGE.</span></span> 
  
<span data-ttu-id="b9714-212">Wenn ein ungültiger Zeiger im  _lpDestObj-Parameter_ übergeben wird, sind die Ergebnisse unvorhersehbar.</span><span class="sxs-lookup"><span data-stu-id="b9714-212">If an invalid pointer is passed in the  _lpDestObj_ parameter, the results are unpredictable.</span></span> 
  
<span data-ttu-id="b9714-213">Das Ausschließen von Eigenschaften bei **einem CopyTo-Aufruf** kann hilfreich sein.</span><span class="sxs-lookup"><span data-stu-id="b9714-213">Excluding properties on a **CopyTo** call can be useful.</span></span> <span data-ttu-id="b9714-214">Beispielsweise verfügen einige Objekte über Eigenschaften, die für eine einzelne Instanz des Objekts spezifisch sind, z. B. das Datum und die Uhrzeit der Nachrichtenzustellung.</span><span class="sxs-lookup"><span data-stu-id="b9714-214">For example, some objects have properties that are specific to a single instance of the object, such as the date and time of message delivery.</span></span> <span data-ttu-id="b9714-215">Um zu vermeiden, dass die Zustellungszeit einer Nachricht kopiert wird, wenn Sie die Nachricht in einen anderen Ordner kopieren, geben Sie **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) im #A0 aus.</span><span class="sxs-lookup"><span data-stu-id="b9714-215">To avoid copying a message's delivery time when you copy the message to a different folder, specify **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) in the property tag exclude array.</span></span> <span data-ttu-id="b9714-216">Um die Empfängerliste einer Nachricht auszuschließen, fügen Sie **die PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) -Eigenschaft zum Exclude-Array hinzu.</span><span class="sxs-lookup"><span data-stu-id="b9714-216">To exclude a message's recipient list, add the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property to the exclude array.</span></span> <span data-ttu-id="b9714-217">Zum Ausschließen der Anlagen einer Nachricht fügen Sie **die PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) -Eigenschaft zum Array hinzu.</span><span class="sxs-lookup"><span data-stu-id="b9714-217">To exclude a message's attachments, add the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property to the array.</span></span>
  
<span data-ttu-id="b9714-218">Verhindern Sie auf ähnliche Weise das Kopieren oder Verschieben der Hierarchie oder Inhaltstabelle eines Ordners oder Adressbuchcontainers, indem Sie **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) oder **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in das #A0 ausschließen.</span><span class="sxs-lookup"><span data-stu-id="b9714-218">Similarly, prevent the copying or moving of a folder or address book container's hierarchy or contents table by including **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in the property tag exclude array.</span></span>
  
<span data-ttu-id="b9714-219">Um Eigenschaften aus dem Kopier- oder Verschiebevorgang auszuschließen, schließen Sie ihre Eigenschaftstags in den  _lpExcludeProps-Parameter_ ein.</span><span class="sxs-lookup"><span data-stu-id="b9714-219">To exclude properties from the copy or move operation, include their property tags in the  _lpExcludeProps_ parameter.</span></span> <span data-ttu-id="b9714-220">Wenn Sie die Ergebnisse  des PROP_TAG übergeben, um ein Eigenschaftentag aus einem bestimmten Bezeichner im Eigenschaftentagarray zu erstellen, werden alle Eigenschaften mit diesem Bezeichner ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="b9714-220">If you pass the results of the **PROP_TAG** macro to build a property tag from a specific identifier in the property tag array, all properties with that identifier will be excluded.</span></span> <span data-ttu-id="b9714-221">Der folgende Eintrag im Eigenschaftentagarray bewirkt beispielsweise, dass alle Eigenschaften mit dem Bezeichner 0x8002 ausgeschlossen werden, unabhängig vom Typ:</span><span class="sxs-lookup"><span data-stu-id="b9714-221">For example, the following entry in the property tag array causes all properties with an identifier of 0x8002 to be excluded, regardless of type:</span></span> 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
<span data-ttu-id="b9714-222">Das **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md))-Eigenschaftstag kann nicht im  _lpExcludeProps-Array enthalten_ sein.</span><span class="sxs-lookup"><span data-stu-id="b9714-222">The **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) property tag cannot be included in the  _lpExcludeProps_ array.</span></span> 
  
<span data-ttu-id="b9714-223">Die Nützlichkeit des **CopyTo-Features** zum Ausschließen von Schnittstellen ist möglicherweise nicht so offensichtlich wie der Nutzen des Ausschließens von Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b9714-223">The usefulness of the **CopyTo** feature for excluding interfaces is perhaps not as obvious as the usefulness of excluding properties.</span></span> <span data-ttu-id="b9714-224">Sie können eine Schnittstelle ausschließen, wenn Sie in ein Objekt kopieren, das keine Kenntnis einer Gruppe von Eigenschaften hat.</span><span class="sxs-lookup"><span data-stu-id="b9714-224">You can exclude an interface when you copy to an object that has no knowledge of a group of properties.</span></span> <span data-ttu-id="b9714-225">Wenn Sie beispielsweise Eigenschaften aus einem Ordner in eine Anlage kopieren, sind die einzigen Eigenschaften, mit der die Anlage arbeiten kann, die generischen Eigenschaften, die mit jeder [IMAPIProp-Implementierung verfügbar](imapipropiunknown.md) sind.</span><span class="sxs-lookup"><span data-stu-id="b9714-225">For example, if you copy properties from a folder to an attachment, the only properties that the attachment can work with are the generic properties available with any [IMAPIProp](imapipropiunknown.md) implementation.</span></span> <span data-ttu-id="b9714-226">Durch Ausschließen [von IMAPIFolder](imapifolderimapicontainer.md) aus dem Kopiervorgang erhält die Anlage keine der spezielleren Ordnereigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b9714-226">By excluding [IMAPIFolder](imapifolderimapicontainer.md) from the copy operation, the attachment will not receive any of the more specific folder properties.</span></span> 
  
<span data-ttu-id="b9714-227">Wenn Sie den  _Parameter rgiidExclude_ verwenden, um eine Schnittstelle auszuschließen, werden auch alle von dieser Schnittstelle abgeleiteten Schnittstellen ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="b9714-227">When you use the  _rgiidExclude_ parameter to exclude an interface, it also excludes all interfaces derived from that interface.</span></span> <span data-ttu-id="b9714-228">Wenn Sie [beispielsweise IMAPIContainer](imapicontainerimapiprop.md) ausschließen, werden Ordner oder Adressbuchcontainer je nach Anbietertyp ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="b9714-228">For example, excluding [IMAPIContainer](imapicontainerimapiprop.md) causes folders or address book containers to be excluded, depending on the type of provider.</span></span> <span data-ttu-id="b9714-229">Schließen Sie **IMAPIProp** oder [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) nicht aus, da so viele Schnittstellen von ihnen stammen.</span><span class="sxs-lookup"><span data-stu-id="b9714-229">Do not exclude **IMAPIProp** or [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) because so many interfaces derive from them.</span></span> 
  
<span data-ttu-id="b9714-230">Ignorieren MAPI_E_COMPUTED Fehler, die in der **SPropProblemArray-Struktur** im  _lppProblems-Parameter zurückgegeben_ werden.</span><span class="sxs-lookup"><span data-stu-id="b9714-230">Ignore MAPI_E_COMPUTED errors returned in the **SPropProblemArray** structure in the  _lppProblems_ parameter.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b9714-231">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="b9714-231">MFCMAPI reference</span></span>

<span data-ttu-id="b9714-232">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b9714-232">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b9714-233">**Datei**</span><span class="sxs-lookup"><span data-stu-id="b9714-233">**File**</span></span>|<span data-ttu-id="b9714-234">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="b9714-234">**Function**</span></span>|<span data-ttu-id="b9714-235">**Comment**</span><span class="sxs-lookup"><span data-stu-id="b9714-235">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b9714-236">File.cpp</span><span class="sxs-lookup"><span data-stu-id="b9714-236">File.cpp</span></span>  <br/> |<span data-ttu-id="b9714-237">LoadFromMSG</span><span class="sxs-lookup"><span data-stu-id="b9714-237">LoadFromMSG</span></span>  <br/> |<span data-ttu-id="b9714-238">MFCMAPI verwendet die **IMAPIProp::CopyTo-Methode,** um Eigenschaften aus einer MSG-Datei in ein [IMAPIMessageSite-Objekt zu](imapimessagesiteiunknown.md) kopieren.</span><span class="sxs-lookup"><span data-stu-id="b9714-238">MFCMAPI uses the **IMAPIProp::CopyTo** method to copy properties from a .msg file to an [IMAPIMessageSite](imapimessagesiteiunknown.md) object.</span></span>  <br/> |
|<span data-ttu-id="b9714-239">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="b9714-239">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="b9714-240">CFolderDlg::HandlePaste</span><span class="sxs-lookup"><span data-stu-id="b9714-240">CFolderDlg::HandlePaste</span></span>  <br/> |<span data-ttu-id="b9714-241">MFCMAPI verwendet die **IMAPIProp::CopyTo-Methode,** um Eigenschaften aus einer Quellnachricht während eines Einfügevorgangs in eine Zielnachricht zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="b9714-241">MFCMAPI uses the **IMAPIProp::CopyTo** method to copy properties from a source message to a target message during a paste operation.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b9714-242">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9714-242">See also</span></span>



[<span data-ttu-id="b9714-243">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="b9714-243">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
  
[<span data-ttu-id="b9714-244">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="b9714-244">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="b9714-245">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b9714-245">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)
  
[<span data-ttu-id="b9714-246">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b9714-246">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="b9714-247">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="b9714-247">IMAPISupport::DoProgressDialog</span></span>](imapisupport-doprogressdialog.md)
  
[<span data-ttu-id="b9714-248">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="b9714-248">IMAPISupport::DoCopyTo</span></span>](imapisupport-docopyto.md)
  
[<span data-ttu-id="b9714-249">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="b9714-249">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="b9714-250">PidTagContainerContents (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b9714-250">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="b9714-251">PidTagContainerHierarchy (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b9714-251">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="b9714-252">PidTagMessageAttachments (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b9714-252">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="b9714-253">PidTagMessageDeliveryTime (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b9714-253">PidTagMessageDeliveryTime Canonical Property</span></span>](pidtagmessagedeliverytime-canonical-property.md)
  
[<span data-ttu-id="b9714-254">PidTagMessageRecipients (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b9714-254">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="b9714-255">PidTagObjectType (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b9714-255">PidTagObjectType Canonical Property</span></span>](pidtagobjecttype-canonical-property.md)
  
[<span data-ttu-id="b9714-256">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="b9714-256">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="b9714-257">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="b9714-257">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="b9714-258">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b9714-258">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="b9714-259">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="b9714-259">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

