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
ms.openlocfilehash: aa2869b1e3495bfb8a431e79a55d11a1ee1c5ca6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792272"
---
# <a name="imapipropcopyto"></a><span data-ttu-id="68dac-103">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="68dac-103">IMAPIProp::CopyTo</span></span>

  
  
<span data-ttu-id="68dac-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="68dac-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="68dac-105">Kopiert oder verschiebt alle Eigenschaften, mit Ausnahme von speziell Ausgeschlossene Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="68dac-105">Copies or moves all properties, except for specifically excluded properties.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="68dac-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="68dac-106">Parameters</span></span>

 <span data-ttu-id="68dac-107">_ciidExclude_</span><span class="sxs-lookup"><span data-stu-id="68dac-107">_ciidExclude_</span></span>
  
> <span data-ttu-id="68dac-108">[in] Die Anzahl der Schnittstellen zum ausschließen, wenn Eigenschaften kopiert oder verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="68dac-108">[in] The count of interfaces to exclude when properties are copied or moved.</span></span>
    
 <span data-ttu-id="68dac-109">_rgiidExclude_</span><span class="sxs-lookup"><span data-stu-id="68dac-109">_rgiidExclude_</span></span>
  
> <span data-ttu-id="68dac-110">[in] Ein Array von Schnittstellenbezeichner (IIDs), die Schnittstellen, die nicht verwendet werden soll angibt, wenn zusätzliche Informationen kopiert oder und Zielobjekt verschoben.</span><span class="sxs-lookup"><span data-stu-id="68dac-110">[in] An array of interface identifiers (IIDs) that specify interfaces that should not be used when supplemental information is copied or moved to the destination object.</span></span>
    
 <span data-ttu-id="68dac-111">_lpExcludeProps_</span><span class="sxs-lookup"><span data-stu-id="68dac-111">_lpExcludeProps_</span></span>
  
> <span data-ttu-id="68dac-112">[in] Ein Zeiger auf einen Tag Array-Eigenschaft, die die Eigenschaftentags identifiziert, die von der Kopie ausgeschlossen werden soll oder verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="68dac-112">[in] A pointer to a property tag array that identifies the property tags that should be excluded from the copy or move operation.</span></span> <span data-ttu-id="68dac-113">Übergeben von **null** in der _LpExcludeProps_ -Parameter gibt an, dass alle Eigenschaften des Objekts kopiert oder verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="68dac-113">Passing **null** in the  _lpExcludeProps_ parameter indicates that all of the object's properties should be copied or moved.</span></span> <span data-ttu-id="68dac-114">**CopyTo** gibt zurück, dass MAPI_E_INVALID_PARAMETER, wenn das **cValues** Mitglied der [SPropProblemArray](spropproblemarray.md) -Struktur mit _LpExcludeProps_ gezeigt auf 0 gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="68dac-114">**CopyTo** returns MAPI_E_INVALID_PARAMETER when the **cValues** member of the [SPropProblemArray](spropproblemarray.md) structure pointed to by  _lpExcludeProps_ is set to 0.</span></span> 
    
 <span data-ttu-id="68dac-115">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="68dac-115">_ulUIParam_</span></span>
  
> <span data-ttu-id="68dac-116">[in] Ein Handle für das übergeordnete Fenster der Statusanzeige.</span><span class="sxs-lookup"><span data-stu-id="68dac-116">[in] A handle to the parent window of the progress indicator.</span></span> 
    
 <span data-ttu-id="68dac-117">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="68dac-117">_lpProgress_</span></span>
  
> <span data-ttu-id="68dac-118">[in] Ein Zeiger auf eine Implementierung der Fortschritt-Symbol.</span><span class="sxs-lookup"><span data-stu-id="68dac-118">[in] A pointer to a progress indicator implementation.</span></span> <span data-ttu-id="68dac-119">Wenn **null** in der _LpProgress_ -Parameter übergeben wird, wird die Implementierung des Fortschritts von MAPI bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="68dac-119">If **null** is passed in the  _lpProgress_ parameter, MAPI provides the progress implementation.</span></span> <span data-ttu-id="68dac-120">Der Parameter _LpProgress_ wird ignoriert, es sei denn, das Flag MAPI_DIALOG im _UlFlags_ -Parameter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="68dac-120">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="68dac-121">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="68dac-121">_lpInterface_</span></span>
  
> <span data-ttu-id="68dac-122">[in] Ein Zeiger auf die Schnittstellenbezeichner (IID), der die Schnittstelle für verwendet werden, um Zugriff auf das Objekt, durch den Parameter _LpDestObj_ auf darstellt.</span><span class="sxs-lookup"><span data-stu-id="68dac-122">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object pointed to by the  _lpDestObj_ parameter.</span></span> <span data-ttu-id="68dac-123">Der Parameter _LpInterface_ darf nicht **null**sein.</span><span class="sxs-lookup"><span data-stu-id="68dac-123">The  _lpInterface_ parameter must not be **null**.</span></span>
    
 <span data-ttu-id="68dac-124">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="68dac-124">_lpDestObj_</span></span>
  
> <span data-ttu-id="68dac-125">[in] Ein Zeiger auf das Objekt, das die Eigenschaften kopierten oder verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="68dac-125">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="68dac-126">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="68dac-126">_ulFlags_</span></span>
  
> <span data-ttu-id="68dac-127">[in] Eine Bitmaske aus Flags, die den Vorgang kopieren oder verschieben steuert.</span><span class="sxs-lookup"><span data-stu-id="68dac-127">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="68dac-128">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="68dac-128">The following flags can be set:</span></span>
    
<span data-ttu-id="68dac-129">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="68dac-129">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="68dac-130">Wenn **CopyTo** die [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) -Methode aufgerufen, um die Kopie zu behandeln oder verschoben wird, muss er stattdessen direkt mit den Fehlerwert MAPI_E_DECLINE_COPY zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="68dac-130">If **CopyTo** calls the [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) method to handle the copy or move operation, it should instead return immediately with the error value MAPI_E_DECLINE_COPY.</span></span> <span data-ttu-id="68dac-131">Das Flag MAPI_DECLINE_OK wird von MAPI festgelegt, um Rekursion zu begrenzen.</span><span class="sxs-lookup"><span data-stu-id="68dac-131">The MAPI_DECLINE_OK flag is set by MAPI to limit recursion.</span></span> <span data-ttu-id="68dac-132">Clients stellen Sie dieses Flag keine.</span><span class="sxs-lookup"><span data-stu-id="68dac-132">Clients do not set this flag.</span></span> 
    
<span data-ttu-id="68dac-133">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="68dac-133">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="68dac-134">Eine Statusanzeige angezeigt.</span><span class="sxs-lookup"><span data-stu-id="68dac-134">Displays a progress indicator.</span></span>
    
<span data-ttu-id="68dac-135">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="68dac-135">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="68dac-136">**CopyTo** sollte einen Verschiebevorgang anstatt einen Kopiervorgang ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="68dac-136">**CopyTo** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="68dac-137">Wenn dieses Flag nicht festgelegt ist, führt **CopyTo** durch einen Kopiervorgang.</span><span class="sxs-lookup"><span data-stu-id="68dac-137">When this flag is not set, **CopyTo** performs a copy operation.</span></span> 
    
<span data-ttu-id="68dac-138">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="68dac-138">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="68dac-139">Vorhandene Eigenschaften im Zielobjekt sollte nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="68dac-139">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="68dac-140">Wenn dieses Flag nicht festgelegt ist, wird die **CopyTo** vorhandene Eigenschaften überschrieben.</span><span class="sxs-lookup"><span data-stu-id="68dac-140">When this flag is not set, **CopyTo** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="68dac-141">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="68dac-141">_lppProblems_</span></span>
  
> <span data-ttu-id="68dac-142">[in, out] Bei Eingabe einen Zeiger auf einen Zeiger auf eine **SPropProblemArray** -Struktur. andernfalls **null**, gibt an, keine Notwendigkeit zur Fehlerinformationen.</span><span class="sxs-lookup"><span data-stu-id="68dac-142">[in, out] On input, a pointer to a pointer to an **SPropProblemArray** structure; otherwise, **null**, indicating no need for error information.</span></span> <span data-ttu-id="68dac-143">Wenn _LppProblems_ einen gültigen Zeiger für die Eingabe ist, gibt **CopyTo** detaillierte Informationen zu Fehlern in eine oder mehrere Eigenschaften kopieren.</span><span class="sxs-lookup"><span data-stu-id="68dac-143">If  _lppProblems_ is a valid pointer on input, **CopyTo** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="68dac-144">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="68dac-144">Return value</span></span>

<span data-ttu-id="68dac-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="68dac-145">S_OK</span></span> 
  
> <span data-ttu-id="68dac-146">Die Eigenschaften haben erfolgreich kopiert oder verschoben.</span><span class="sxs-lookup"><span data-stu-id="68dac-146">The properties have been successfully copied or moved.</span></span>
    
<span data-ttu-id="68dac-147">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="68dac-147">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="68dac-148">Ein Unterobjekt kann nicht kopiert werden, da ein Unterobjekt mit dem gleichen Namen anzeigen – von der **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft angegebenen – im Zielobjekt bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="68dac-148">A subobject cannot be copied because a subobject with the same display name — specified by the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property — already exists in the destination object.</span></span> 
    
<span data-ttu-id="68dac-149">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="68dac-149">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="68dac-150">Der Dienstanbieter implementiert den Kopiervorgang nicht.</span><span class="sxs-lookup"><span data-stu-id="68dac-150">The service provider does not implement the copy operation.</span></span>
    
<span data-ttu-id="68dac-151">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="68dac-151">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="68dac-152">Ausführen des Vorgangs kopieren oder verschieben direkt oder indirekt Quellobjekt enthält Zielobjekt.</span><span class="sxs-lookup"><span data-stu-id="68dac-152">The source object performing the copy or move operation directly or indirectly contains the destination object.</span></span> <span data-ttu-id="68dac-153">Erhebliche Arbeit möglicherweise durchgeführt wurden, bevor diese Bedingung ermittelt wurde, damit die Quell- und Ziel-Objekte teilweise geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="68dac-153">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="68dac-154">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="68dac-154">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="68dac-155">Die Schnittstelle, die vom _LpInterface_ -Parameter wird durch das Zielobjekt nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="68dac-155">The interface identified by the  _lpInterface_ parameter is not supported by the destination object.</span></span> 
    
<span data-ttu-id="68dac-156">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="68dac-156">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="68dac-157">Es wurde versucht, auf ein Objekt zuzugreifen, für den der Anrufer nicht über ausreichende Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="68dac-157">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="68dac-158">Dieser Fehler wird zurückgegeben, wenn Zielobjekt Quellobjekt identisch ist.</span><span class="sxs-lookup"><span data-stu-id="68dac-158">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="68dac-159">Die folgenden Werte können in der Struktur **SPropProblemArray** , aber nicht als Rückgabewerte für **CopyTo**zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="68dac-159">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **CopyTo**.</span></span> <span data-ttu-id="68dac-160">Die folgenden Fehler gelten für eine einzelne Eigenschaft:</span><span class="sxs-lookup"><span data-stu-id="68dac-160">The following errors apply to a single property:</span></span>
  
<span data-ttu-id="68dac-161">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="68dac-161">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="68dac-162">Entweder die Option MAPI_UNICODE festgelegt wurde und **CopyTo** unterstützt keine Unicode oder Parameter MAPI_UNICODE wurde nicht festgelegt und **CopyTo** nur Unicode unterstützt.</span><span class="sxs-lookup"><span data-stu-id="68dac-162">Either the MAPI_UNICODE flag was set and **CopyTo** does not support Unicode, or MAPI_UNICODE was not set and **CopyTo** supports only Unicode.</span></span> 
    
<span data-ttu-id="68dac-163">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="68dac-163">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="68dac-164">Die Eigenschaft kann nicht vom Anrufer geändert werden, da es eine schreibgeschützte Eigenschaft, mit der Besitzer des Zielobjekts berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="68dac-164">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="68dac-165">Dieser Fehler ist nicht schwerwiegend. der Aufrufer sollte den Kopiervorgang fortgesetzt zulassen.</span><span class="sxs-lookup"><span data-stu-id="68dac-165">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="68dac-166">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="68dac-166">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="68dac-167">Der Eigenschaftstyp ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="68dac-167">The property type is invalid.</span></span>
    
<span data-ttu-id="68dac-168">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="68dac-168">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="68dac-169">Der Eigenschaftentyp ist nicht vom Anrufer erwartet.</span><span class="sxs-lookup"><span data-stu-id="68dac-169">The property type is not the type expected by the caller.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="68dac-170">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="68dac-170">Remarks</span></span>

<span data-ttu-id="68dac-171">Standardmäßig wird die **IMAPIProp::CopyTo** -Methode kopiert oder verschiebt alle Eigenschaften des aktuellen Objekts ein Zielobjekt.</span><span class="sxs-lookup"><span data-stu-id="68dac-171">By default, the **IMAPIProp::CopyTo** method copies or moves all of the current object's properties to a destination object.</span></span> <span data-ttu-id="68dac-172">**CopyTo** wird verwendet, wenn ein Objekt kopiert oder genau mit der gesamten oder die meisten ihrer Eigenschaften intakt verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="68dac-172">**CopyTo** is used when an object should be copied or moved exactly, with all or most of its properties intact.</span></span> 
  
<span data-ttu-id="68dac-173">Alle Unterobjekte im Quellobjekt werden automatisch in den Vorgang einbezogen und kopiert oder vollständig verschoben.</span><span class="sxs-lookup"><span data-stu-id="68dac-173">Any subobjects in the source object are automatically included in the operation and are copied or moved in their entirety.</span></span> <span data-ttu-id="68dac-174">Standardmäßig wird die **CopyTo** Eigenschaften im Zielobjekt, die Eigenschaften aus dem Quellobjekt entsprechen überschrieben.</span><span class="sxs-lookup"><span data-stu-id="68dac-174">By default, **CopyTo** overwrites any properties in the destination object that match properties from the source object.</span></span> <span data-ttu-id="68dac-175">Wenn die kopierte oder verschobenen Eigenschaften bereits im Zielobjekt vorhanden sind, werden die vorhandenen Eigenschaften von den Eigenschaften der neuen überschrieben, wenn das Flag MAPI_NOREPLACE im _UlFlags_ -Parameter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="68dac-175">If any of the copied or moved properties already exist in the destination object, the existing properties are overwritten by the new properties, unless the MAPI_NOREPLACE flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="68dac-176">Vorhandene Informationen im Zielobjekt, das nicht überschrieben wird, bleibt unverändert.</span><span class="sxs-lookup"><span data-stu-id="68dac-176">Existing information in the destination object that is not overwritten is left untouched.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="68dac-177">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="68dac-177">Notes to implementers</span></span>

<span data-ttu-id="68dac-178">Sie können bieten eine vollständige Implementierung der **CopyTo** oder verlassen sich auf die Implementierung, die MAPI in dessen Support-Objekt bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="68dac-178">You can provide a full implementation of **CopyTo** or rely on the implementation that MAPI provides in its support object.</span></span> <span data-ttu-id="68dac-179">Wenn Sie die MAPI-Implementierung verwenden möchten, rufen Sie **IMAPISupport::DoCopyTo**.</span><span class="sxs-lookup"><span data-stu-id="68dac-179">If you want to use the MAPI implementation, call **IMAPISupport::DoCopyTo**.</span></span> <span data-ttu-id="68dac-180">Wenn Sie führen Sie die Verarbeitung für **DoCopyTo** delegieren, und Sie das Flag MAPI_DECLINE_OK übergeben werden, vermeiden Sie den Anruf an den Support und zurückzugeben Sie MAPI_E_DECLINE_COPY stattdessen.</span><span class="sxs-lookup"><span data-stu-id="68dac-180">However, if you do delegate processing to **DoCopyTo** and you are passed the MAPI_DECLINE_OK flag, avoid the support call and return MAPI_E_DECLINE_COPY instead.</span></span> <span data-ttu-id="68dac-181">MAPI wird Aufrufen dieses Flag die mögliche Rekursion zu vermeiden, die auftreten können, wenn Ordner kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="68dac-181">MAPI will call with this flag to avoid the possible recursion that can happen when folders are copied.</span></span> 
  
<span data-ttu-id="68dac-182">Da der Kopiervorgang langen sein kann, sollte eine Statusanzeige angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="68dac-182">Because the copy operation can be lengthy, you should display a progress indicator.</span></span> <span data-ttu-id="68dac-183">Verwenden Sie die [IMAPIProgress](imapiprogressiunknown.md) -Implementierung, die in den _LpProgress_ -Parameter übergeben, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="68dac-183">Use the [IMAPIProgress](imapiprogressiunknown.md) implementation passed in the  _lpProgress_ parameter, if there is one.</span></span> <span data-ttu-id="68dac-184">Wenn _LpProgress_ **null**ist, rufen Sie die [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) -Methode, um die MAPI-Implementierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="68dac-184">If  _lpProgress_ is **null**, call the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method to use the MAPI implementation.</span></span> 
  
<span data-ttu-id="68dac-185">Versuchen Sie keine bekannten Eigenschaften Read-only im Zielobjekt festgelegt; Geben Sie stattdessen MAPI_E_NO_ACCESS zurück.</span><span class="sxs-lookup"><span data-stu-id="68dac-185">Do not attempt to set any known read-only properties in the destination object; return MAPI_E_NO_ACCESS instead.</span></span>
  
<span data-ttu-id="68dac-186">Die Quell- und Ziel-Objekte sollten die gleichen Schnittstellen verwenden.</span><span class="sxs-lookup"><span data-stu-id="68dac-186">The source and destination objects should use the same interfaces.</span></span> <span data-ttu-id="68dac-187">MAPI_E_INVALID_PARAMETER zurück, wenn _LpInterface_ nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="68dac-187">Return MAPI_E_INVALID_PARAMETER if  _lpInterface_ is not set.</span></span> 
  
<span data-ttu-id="68dac-188">MAPI_E_INTERFACE_NOT_SUPPORTED zurück, wenn alle bekannte Schnittstellen ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="68dac-188">Return MAPI_E_INTERFACE_NOT_SUPPORTED if all known interfaces are excluded.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="68dac-189">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="68dac-189">Notes to callers</span></span>

<span data-ttu-id="68dac-190">Legen Sie die Kennzeichen MAPI_DECLINE_OK nicht; MAPI setzt es seine Anrufe auf Speicher-Anbieter **CopyTo** Implementierungen message.</span><span class="sxs-lookup"><span data-stu-id="68dac-190">Do not set the MAPI_DECLINE_OK flag; MAPI uses it in its calls to message store provider **CopyTo** implementations.</span></span> 
  
<span data-ttu-id="68dac-191">Da verschieben und kopieren können Zeit in Anspruch nehmen, sollten Sie die Anzeige einer Statusanzeige durch Festlegen des MAPI_DIALOG-Flags anfordern.</span><span class="sxs-lookup"><span data-stu-id="68dac-191">Because copy and move operations can take time, you should request the display of a progress indicator by setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="68dac-192">Sie können den Parameter _LpProgress_ festlegen, die Implementierung von **IMAPIProgress**, falls vorhanden, oder **null**.</span><span class="sxs-lookup"><span data-stu-id="68dac-192">You can set the  _lpProgress_ parameter to your implementation of **IMAPIProgress**, if you have one, or to **null**.</span></span> <span data-ttu-id="68dac-193">Wenn _LpProgress_ **null**ist, verwendet **CopyTo** die Standard-Statusanzeige MAPI bietet.</span><span class="sxs-lookup"><span data-stu-id="68dac-193">If  _lpProgress_ is **null**, **CopyTo** will use the default progress indicator that MAPI provides.</span></span> 
  
<span data-ttu-id="68dac-194">Sie können die Anzeige einer Statusanzeige installieren, indem Sie das Flag MAPI_DIALOG nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="68dac-194">You can suppress the display of a progress indicator by not setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="68dac-195">**CopyTo** die Parameter _UlUIParam_ und _LpProgress_ ignoriert und das Symbol wird nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="68dac-195">**CopyTo** will ignore the  _ulUIParam_ and  _lpProgress_ parameters and will not display the indicator.</span></span> 
  
 <span data-ttu-id="68dac-196">**CopyTo** können melden, globale und einzelne Fehler oder Fehler, die mit einer oder mehrerer Eigenschaften auftreten.</span><span class="sxs-lookup"><span data-stu-id="68dac-196">**CopyTo** can report global and individual errors, or errors that occur with one or more properties.</span></span> <span data-ttu-id="68dac-197">Diese einzelnen Fehler befinden sich in einer **SPropProblemArray** Struktur.</span><span class="sxs-lookup"><span data-stu-id="68dac-197">These individual errors are placed in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="68dac-198">Sie können die Fehlerberichterstattung Ebene der Eigenschaft, indem Sie **null**, anstatt einen gültigen Zeiger, für den Parameter Property Problem Array Struktur übergeben unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="68dac-198">You can suppress error reporting at the property level by passing **null**, instead of a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="68dac-199">Wenn Sie Informationen zu Fehlern erhalten möchten, übergeben Sie einen gültigen **SPropProblemArray** Struktur Zeiger des _LppProblems_ -Parameters.</span><span class="sxs-lookup"><span data-stu-id="68dac-199">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="68dac-200">Wenn **CopyTo** S_OK zurückgegeben wird, überprüfen Sie auf mögliche Fehler mit einzelnen Eigenschaften in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="68dac-200">When **CopyTo** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="68dac-201">Wenn **CopyTo** einen Fehler zurückgibt, wird keine Informationen in der Struktur **SPropProblemArray** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="68dac-201">When **CopyTo** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="68dac-202">Rufen Sie stattdessen [IMAPIProp::GetLastError](imapiprop-getlasterror.md) , um ausführliche Fehlerinformationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="68dac-202">Instead, call [IMAPIProp::GetLastError](imapiprop-getlasterror.md) to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="68dac-203">Wenn **CopyTo** S_OK zurückgibt, frei die zurückgegebene Struktur **SPropProblemArray** durch Aufrufen der [MAPIFreeBuffer](mapifreebuffer.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="68dac-203">If **CopyTo** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="68dac-204">Wenn Sie Eigenschaften, die für den Objekttyp Quelle eindeutig sind kopieren, müssen Sie sicherstellen, dass Zielobjekt des gleichen Typs ist.</span><span class="sxs-lookup"><span data-stu-id="68dac-204">If you copy properties that are unique to the source object type, you must ensure that the destination object is of the same type.</span></span> <span data-ttu-id="68dac-205">**CopyTo** verhindert nicht, dass Sie Eigenschaften, die um einen Objekttyp mit einem anderen Typ des Objekts in der Regel gehören, zuordnen.</span><span class="sxs-lookup"><span data-stu-id="68dac-205">**CopyTo** does not prevent you from associating properties that typically belong to one type of object with another type of object.</span></span> <span data-ttu-id="68dac-206">Zum Schluss kommen zum Kopieren von Eigenschaften, die für Zielobjekt sinnvoll ist.</span><span class="sxs-lookup"><span data-stu-id="68dac-206">It is up to you to copy properties that make sense for the destination object.</span></span> <span data-ttu-id="68dac-207">Beispielsweise sollten Sie eine Adressbuchcontainer nicht Nachrichteneigenschaften kopieren.</span><span class="sxs-lookup"><span data-stu-id="68dac-207">For example, you should not copy message properties to an address book container.</span></span> 
  
<span data-ttu-id="68dac-208">Um sicherzustellen, dass Sie zwischen Objekten des gleichen Typs kopieren, prüfen Sie, ob das Quell- und Ziel-Objekt den gleichen Typ, entweder durch Vergleichen Objektzeigern oder den Aufruf von [QueryInterface](http://msdn.microsoft.com/de-de/library/ms682521%28v=VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="68dac-208">To ensure that you copy between objects of the same type, check that the source and destination object are the same type, either by comparing object pointers or calling [IUnknown::QueryInterface](http://msdn.microsoft.com/de-de/library/ms682521%28v=VS.85%29.aspx).</span></span> <span data-ttu-id="68dac-209">Legen Sie die Schnittstelle-ID auf den _LpInterface_ der standard-Benutzeroberfläche für das Quellobjekt.</span><span class="sxs-lookup"><span data-stu-id="68dac-209">Set the interface identifier pointed to by  _lpInterface_ to the standard interface for the source object.</span></span> <span data-ttu-id="68dac-210">Darüber hinaus werden Sie sicher, dass der Objekttyp oder **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))-Eigenschaft für die beiden Objekte identisch ist.</span><span class="sxs-lookup"><span data-stu-id="68dac-210">Also, be sure that the object type or **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property is the same for the two objects.</span></span> <span data-ttu-id="68dac-211">Wenn Sie aus einer Nachricht kopieren, legen Sie _LpInterface_ IID_IMessage und die **PR_OBJECT_TYPE** für beide Objekte MAPI_MESSAGE fest.</span><span class="sxs-lookup"><span data-stu-id="68dac-211">For example, if you copy from a message, set  _lpInterface_ to IID_IMessage and the **PR_OBJECT_TYPE** for both objects to MAPI_MESSAGE.</span></span> 
  
<span data-ttu-id="68dac-212">Wenn ein ungültiger Zeiger im _LpDestObj_ -Parameter übergeben wird, sind die Ergebnisse unvorhersehbar.</span><span class="sxs-lookup"><span data-stu-id="68dac-212">If an invalid pointer is passed in the  _lpDestObj_ parameter, the results are unpredictable.</span></span> 
  
<span data-ttu-id="68dac-213">Ausschließen von Eigenschaften für einen Anruf **CopyTo** kann hilfreich sein.</span><span class="sxs-lookup"><span data-stu-id="68dac-213">Excluding properties on a **CopyTo** call can be useful.</span></span> <span data-ttu-id="68dac-214">Beispielsweise haben einige Objekte, Eigenschaften, die für eine einzelne Instanz des Objekts, wie etwa das Datum und die Uhrzeit der Nachrichtenübermittlung spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="68dac-214">For example, some objects have properties that are specific to a single instance of the object, such as the date and time of message delivery.</span></span> <span data-ttu-id="68dac-215">Geben Sie zum Vermeiden von Zeitaufwands für die Bereitstellung einer Nachricht, wenn Sie die Nachricht auf einen anderen Ordner kopieren, kopieren **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) die Array-Eigenschaft Tag ausschließen.</span><span class="sxs-lookup"><span data-stu-id="68dac-215">To avoid copying a message's delivery time when you copy the message to a different folder, specify **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) in the property tag exclude array.</span></span> <span data-ttu-id="68dac-216">Um eine Nachricht Empfängerliste auszuschließen, fügen Sie die **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))-Eigenschaft dem Exclude-Array.</span><span class="sxs-lookup"><span data-stu-id="68dac-216">To exclude a message's recipient list, add the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property to the exclude array.</span></span> <span data-ttu-id="68dac-217">Um eine e-Mail-Anlagen auszuschließen, fügen Sie die **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))-Eigenschaft dem Array hinzu.</span><span class="sxs-lookup"><span data-stu-id="68dac-217">To exclude a message's attachments, add the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property to the array.</span></span>
  
<span data-ttu-id="68dac-218">In ähnlicher Weise zu verhindern, dass das Kopieren oder Verschieben eines Ordners oder Adressbuchcontainer des Hierarchie oder Inhalt Tabelle, einschließlich **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) oder **PR_CONTAINER_CONTENTS** ([ PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in der Eigenschaft Tag Array ausschließen.</span><span class="sxs-lookup"><span data-stu-id="68dac-218">Similarly, prevent the copying or moving of a folder or address book container's hierarchy or contents table by including **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in the property tag exclude array.</span></span>
  
<span data-ttu-id="68dac-219">Ausschließen von Eigenschaften aus der Kopie oder Verschiebevorgang, deren Eigenschaftentags im _LpExcludeProps_ -Parameter enthalten.</span><span class="sxs-lookup"><span data-stu-id="68dac-219">To exclude properties from the copy or move operation, include their property tags in the  _lpExcludeProps_ parameter.</span></span> <span data-ttu-id="68dac-220">Wenn Sie die Ergebnisse des Makros **PROP_TAG** zum Erstellen einer Eigenschaftentag aus einem bestimmten Kennzeichen im Array Tag-Eigenschaft übergeben wird, werden alle Eigenschaften mit diesem Bezeichner ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="68dac-220">If you pass the results of the **PROP_TAG** macro to build a property tag from a specific identifier in the property tag array, all properties with that identifier will be excluded.</span></span> <span data-ttu-id="68dac-221">Der folgende Eintrag im Array Tag-Eigenschaft bewirkt beispielsweise alle Eigenschaften mit der ID 0x8002, ausgeschlossen werden sollen, unabhängig vom Typ:</span><span class="sxs-lookup"><span data-stu-id="68dac-221">For example, the following entry in the property tag array causes all properties with an identifier of 0x8002 to be excluded, regardless of type:</span></span> 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
<span data-ttu-id="68dac-222">Das **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md))-Tag-Eigenschaft kann nicht im Array _LpExcludeProps_ enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="68dac-222">The **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) property tag cannot be included in the  _lpExcludeProps_ array.</span></span> 
  
<span data-ttu-id="68dac-223">Die Nützlichkeit des **CopyTo** Features zum Ausschließen von Schnittstellen ist möglicherweise nicht offensichtlich die Nützlichkeit von Eigenschaften ausschließen.</span><span class="sxs-lookup"><span data-stu-id="68dac-223">The usefulness of the **CopyTo** feature for excluding interfaces is perhaps not as obvious as the usefulness of excluding properties.</span></span> <span data-ttu-id="68dac-224">Wenn Sie auf ein Objekt kopieren, die keiner Gruppe von Eigenschaften vorhanden sind, können Sie eine Schnittstelle ausschließen.</span><span class="sxs-lookup"><span data-stu-id="68dac-224">You can exclude an interface when you copy to an object that has no knowledge of a group of properties.</span></span> <span data-ttu-id="68dac-225">Wenn Sie Eigenschaften aus einem Ordner in einer Anlage kopieren, sind die einzigen Eigenschaften, mit denen die Anlage zusammenarbeiten kann beispielsweise die generischen Eigenschaften [IMAPIProp](imapipropiunknown.md) Implementierung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="68dac-225">For example, if you copy properties from a folder to an attachment, the only properties that the attachment can work with are the generic properties available with any [IMAPIProp](imapipropiunknown.md) implementation.</span></span> <span data-ttu-id="68dac-226">Der Kopiervorgang [IMAPIFolder](imapifolderimapicontainer.md) ausgeschlossen, erhalten die Anlage nicht bestimmte Ordner Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="68dac-226">By excluding [IMAPIFolder](imapifolderimapicontainer.md) from the copy operation, the attachment will not receive any of the more specific folder properties.</span></span> 
  
<span data-ttu-id="68dac-227">Wenn Sie den Parameter _RgiidExclude_ verwenden, um eine Schnittstelle auszuschließen, werden auch alle Schnittstellen, die von dieser Schnittstelle abgeleitet ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="68dac-227">When you use the  _rgiidExclude_ parameter to exclude an interface, it also excludes all interfaces derived from that interface.</span></span> <span data-ttu-id="68dac-228">Ausschließen von [IMAPIContainer](imapicontainerimapiprop.md) bewirkt beispielsweise, dass Ordner oder Adresse Adressbuch-Container, je nach den Typ des Anbieters ausgeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="68dac-228">For example, excluding [IMAPIContainer](imapicontainerimapiprop.md) causes folders or address book containers to be excluded, depending on the type of provider.</span></span> <span data-ttu-id="68dac-229">Schließen Sie keine **IMAPIProp** oder [IUnknown](http://msdn.microsoft.com/de-de/library/ms680509%28v=VS.85%29.aspx) , da so viele Schnittstellen, die von ihnen abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="68dac-229">Do not exclude **IMAPIProp** or [IUnknown](http://msdn.microsoft.com/de-de/library/ms680509%28v=VS.85%29.aspx) because so many interfaces derive from them.</span></span> 
  
<span data-ttu-id="68dac-230">Ignorieren Sie MAPI_E_COMPUTED Fehler in der Struktur **SPropProblemArray** im _LppProblems_ -Parameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="68dac-230">Ignore MAPI_E_COMPUTED errors returned in the **SPropProblemArray** structure in the  _lppProblems_ parameter.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="68dac-231">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="68dac-231">MFCMAPI reference</span></span>

<span data-ttu-id="68dac-232">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="68dac-232">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="68dac-233">**Datei**</span><span class="sxs-lookup"><span data-stu-id="68dac-233">**File**</span></span>|<span data-ttu-id="68dac-234">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="68dac-234">**Function**</span></span>|<span data-ttu-id="68dac-235">**Comment**</span><span class="sxs-lookup"><span data-stu-id="68dac-235">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="68dac-236">File.cpp</span><span class="sxs-lookup"><span data-stu-id="68dac-236">File.cpp</span></span>  <br/> |<span data-ttu-id="68dac-237">LoadFromMSG</span><span class="sxs-lookup"><span data-stu-id="68dac-237">LoadFromMSG</span></span>  <br/> |<span data-ttu-id="68dac-238">MFCMAPI (engl.) verwendet die **IMAPIProp::CopyTo** -Methode, um Eigenschaften aus einer MSG-Datei in ein [IMAPIMessageSite](imapimessagesiteiunknown.md) -Objekt zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="68dac-238">MFCMAPI uses the **IMAPIProp::CopyTo** method to copy properties from a .msg file to an [IMAPIMessageSite](imapimessagesiteiunknown.md) object.</span></span>  <br/> |
|<span data-ttu-id="68dac-239">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="68dac-239">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="68dac-240">CFolderDlg::HandlePaste</span><span class="sxs-lookup"><span data-stu-id="68dac-240">CFolderDlg::HandlePaste</span></span>  <br/> |<span data-ttu-id="68dac-241">MFCMAPI (engl.) verwendet die **IMAPIProp::CopyTo** -Methode, um Eigenschaften aus einer Datenquelle Nachricht in einer Zielnachricht während eines Einfügevorgangs zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="68dac-241">MFCMAPI uses the **IMAPIProp::CopyTo** method to copy properties from a source message to a target message during a paste operation.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="68dac-242">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68dac-242">See also</span></span>



[<span data-ttu-id="68dac-243">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="68dac-243">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
  
[<span data-ttu-id="68dac-244">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="68dac-244">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="68dac-245">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="68dac-245">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)
  
[<span data-ttu-id="68dac-246">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="68dac-246">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="68dac-247">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="68dac-247">IMAPISupport::DoProgressDialog</span></span>](imapisupport-doprogressdialog.md)
  
[<span data-ttu-id="68dac-248">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="68dac-248">IMAPISupport::DoCopyTo</span></span>](imapisupport-docopyto.md)
  
[<span data-ttu-id="68dac-249">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="68dac-249">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="68dac-250">PidTagContainerContents (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="68dac-250">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="68dac-251">PidTagContainerHierarchy (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="68dac-251">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="68dac-252">PidTagMessageAttachments (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="68dac-252">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="68dac-253">PidTagMessageDeliveryTime (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="68dac-253">PidTagMessageDeliveryTime Canonical Property</span></span>](pidtagmessagedeliverytime-canonical-property.md)
  
[<span data-ttu-id="68dac-254">PidTagMessageRecipients (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="68dac-254">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="68dac-255">PidTagObjectType (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="68dac-255">PidTagObjectType Canonical Property</span></span>](pidtagobjecttype-canonical-property.md)
  
[<span data-ttu-id="68dac-256">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="68dac-256">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="68dac-257">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="68dac-257">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="68dac-258">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="68dac-258">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="68dac-259">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="68dac-259">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

