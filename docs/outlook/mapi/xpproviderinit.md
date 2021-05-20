---
title: XPProviderInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.XPProviderInit
api_type:
- COM
ms.assetid: df6eacf4-1cf9-4c25-806f-f87c38dad597
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ee0ff8d32436f71020be2cdc91d6677bd4ec8e43
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428536"
---
# <a name="xpproviderinit"></a><span data-ttu-id="47111-103">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="47111-103">XPProviderInit</span></span>

  
  
<span data-ttu-id="47111-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47111-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47111-105">Initialisiert einen Transportanbieter für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="47111-105">Initializes a transport provider for operation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="47111-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="47111-106">Header file:</span></span>  <br/> |<span data-ttu-id="47111-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="47111-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="47111-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="47111-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="47111-109">Transportanbieter</span><span class="sxs-lookup"><span data-stu-id="47111-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="47111-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="47111-110">Called by:</span></span>  <br/> |<span data-ttu-id="47111-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="47111-111">MAPI</span></span>  <br/> |
   
```cpp
HRESULT XPProviderInit(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  ULONG ulMAPIVer,
  ULONG FAR * lpulProviderVer,
  LPXPPROVIDER FAR * lppXPProvider
);
```

## <a name="parameters"></a><span data-ttu-id="47111-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="47111-112">Parameters</span></span>

 <span data-ttu-id="47111-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="47111-113">_hInstance_</span></span>
  
> <span data-ttu-id="47111-114">[in] Die Instanz der Dll (Dynamic Link Library) des Transportanbieters, die MAPI beim Laden der DLL verwendet hat.</span><span class="sxs-lookup"><span data-stu-id="47111-114">[in] The instance of the transport provider's dynamic-link library (DLL) that MAPI used when it loaded the DLL.</span></span>
    
 <span data-ttu-id="47111-115">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="47111-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="47111-116">[in] Zeiger auf ein Speicherzuweisungsobjekt, das die OLE **IMalloc-Schnittstelle verfügbar** machen soll.</span><span class="sxs-lookup"><span data-stu-id="47111-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="47111-117">Der Transportanbieter muss diese Zuweisungsmethode möglicherweise verwenden, wenn er mit bestimmten Schnittstellen wie **IStream arbeitet.**</span><span class="sxs-lookup"><span data-stu-id="47111-117">The transport provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="47111-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="47111-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="47111-119">[in] Zeiger auf die [MAPIAllocateBuffer-Funktion,](mapiallocatebuffer.md) die zum Zuordnen von Arbeitsspeicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="47111-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="47111-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="47111-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="47111-121">[in] Zeiger auf die [MAPIAllocateMore-Funktion,](mapiallocatemore.md) die zum Zuordnen von zusätzlichem Arbeitsspeicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="47111-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="47111-122">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="47111-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="47111-123">[in] Zeiger auf die [MAPIFreeBuffer-Funktion,](mapifreebuffer.md) die zum Freispeichern verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="47111-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="47111-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="47111-124">_ulFlags_</span></span>
  
> <span data-ttu-id="47111-125">[in] Bitmaske von Flags.</span><span class="sxs-lookup"><span data-stu-id="47111-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="47111-126">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="47111-126">The following flag can be set:</span></span>
    
<span data-ttu-id="47111-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="47111-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="47111-128">Der Anbieter wird im Kontext eines Windows geladen, einem speziellen Prozesstyp ohne Zugriff auf eine Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="47111-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="47111-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="47111-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="47111-130">[in] Versionsnummer der Dienstanbieterschnittstelle (SPI), die Mapi.dll wird.</span><span class="sxs-lookup"><span data-stu-id="47111-130">[in] Version number of the service provider interface (SPI) that Mapi.dll uses.</span></span> <span data-ttu-id="47111-131">Die aktuelle Versionsnummer finden Sie in der Mapispi.h-Headerdatei.</span><span class="sxs-lookup"><span data-stu-id="47111-131">For the current version number, see the Mapispi.h header file.</span></span> 
    
 <span data-ttu-id="47111-132">_lpulProviderVer_</span><span class="sxs-lookup"><span data-stu-id="47111-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="47111-133">[out] Zeiger auf die Versionsnummer des SPI, den dieser Transportanbieter verwendet.</span><span class="sxs-lookup"><span data-stu-id="47111-133">[out] Pointer to the version number of the SPI that this transport provider uses.</span></span> 
    
 <span data-ttu-id="47111-134">_lppXPProvider_</span><span class="sxs-lookup"><span data-stu-id="47111-134">_lppXPProvider_</span></span>
  
> <span data-ttu-id="47111-135">[out] Zeiger auf einen Zeiger auf das initialisierte Transportanbieterobjekt.</span><span class="sxs-lookup"><span data-stu-id="47111-135">[out] Pointer to a pointer to the initialized transport provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="47111-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="47111-136">Return value</span></span>

<span data-ttu-id="47111-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="47111-137">S_OK</span></span> 
  
> <span data-ttu-id="47111-138">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="47111-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="47111-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="47111-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="47111-140">Die von MAPI verwendete SPI-Version ist nicht mit dem von diesem Anbieter verwendeten SPI kompatibel.</span><span class="sxs-lookup"><span data-stu-id="47111-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="47111-141">Hinweise</span><span class="sxs-lookup"><span data-stu-id="47111-141">Remarks</span></span>

<span data-ttu-id="47111-142">MAPI ruft die Einstiegspunktfunktion **XPProviderInit** auf, um einen Transportanbieter nach einer Clientanmeldung zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="47111-142">MAPI calls the entry point function **XPProviderInit** to initialize a transport provider following a client logon.</span></span> <span data-ttu-id="47111-143">**XPProviderInit** wird einmal für jeden Transportanbieter aufgerufen, der im Clientprofil angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="47111-143">**XPProviderInit** is called once for each transport provider specified in the client's profile.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="47111-144">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="47111-144">Notes to implementers</span></span>

<span data-ttu-id="47111-145">Ein Transportanbieter muss **XPProviderInit** als Einstiegspunktfunktion in der DLL des Anbieters implementieren.</span><span class="sxs-lookup"><span data-stu-id="47111-145">A transport provider must implement **XPProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="47111-146">Die Implementierung muss auf dem **XPPROVIDERINIT-Funktionsprototyp** basieren, der auch in Mapispi.h angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="47111-146">The implementation must be based on the **XPPROVIDERINIT** function prototype, also specified in Mapispi.h.</span></span> <span data-ttu-id="47111-147">MAPI definiert **XPPROVIDERINIT** für die Verwendung des standardmäßigen MAPI-Initialisierungsaufruftyps STDMAPIINITCALLTYPE, wodurch **XPProviderInit** der CDECL-Aufrufkonvention folgt.</span><span class="sxs-lookup"><span data-stu-id="47111-147">MAPI defines **XPPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **XPProviderInit** to follow the CDECL calling convention.</span></span> <span data-ttu-id="47111-148">Ein Vorteil von CDECL ist, dass Aufrufe auch dann versucht werden können, wenn die Anzahl der aufrufenden Parameter nicht mit der Anzahl der definierten Parameter übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="47111-148">An advantage of CDECL is that calls can be attempted even if the number of calling parameters does not match the number of defined parameters.</span></span> 
  
<span data-ttu-id="47111-149">Ein Anbieter kann mehrmals initialisiert werden, da er in mehreren Profilen gleichzeitig angezeigt wird oder mehr als einmal im gleichen Profil angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="47111-149">A provider can be initialized multiple times as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="47111-150">Da das provider-Objekt Kontext enthält, muss **XPProviderInit** ein anderes Anbieterobjekt in  _lppXPProvider_ für jede Initialisierung zurückgeben, auch für mehrere Initialisierungen im gleichen Prozess.</span><span class="sxs-lookup"><span data-stu-id="47111-150">Because the provider object contains context, **XPProviderInit** must return a different provider object in  _lppXPProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="47111-151">Der Transportanbieter sollte die Funktionen verwenden, auf die  _lpAllocateBuffer_,  _lpAllocateMore_ und  _lpFreeBuffer_ für die meisten Speicherzuweisungen und Deallocation verwiesen.</span><span class="sxs-lookup"><span data-stu-id="47111-151">The transport provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="47111-152">Insbesondere muss der Anbieter diese Funktionen verwenden, um Speicher für die Verwendung durch Clientanwendungen beim Aufrufen von Objektschnittstellen wie [IMAPIProp::GetProps](imapiprop-getprops.md) und [IMAPITable::QueryRows zu reservieren.](imapitable-queryrows.md)</span><span class="sxs-lookup"><span data-stu-id="47111-152">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="47111-153">Wenn der Anbieter auch die Verwendung der OLE-Speicherzuweisung erwartet, sollte er die **IUnknown::AddRef-Methode** des Zuweisungsobjekts aufrufen, auf das der  _lpMalloc-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="47111-153">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="47111-154">Weitere Informationen zum Schreiben von **XPProviderInit** finden Sie unter [Initializing the Transport Provider](initializing-the-transport-provider.md).</span><span class="sxs-lookup"><span data-stu-id="47111-154">For more information about writing **XPProviderInit**, see [Initializing the Transport Provider](initializing-the-transport-provider.md).</span></span> <span data-ttu-id="47111-155">Weitere Informationen zu Einstiegspunktfunktionen finden Sie unter [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="47111-155">For more information about entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="47111-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="47111-156">See also</span></span>



[<span data-ttu-id="47111-157">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="47111-157">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="47111-158">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="47111-158">IXPProvider : IUnknown</span></span>](ixpprovideriunknown.md)
  
[<span data-ttu-id="47111-159">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="47111-159">MSProviderInit</span></span>](msproviderinit.md)

