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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ee0ff8d32436f71020be2cdc91d6677bd4ec8e43
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325655"
---
# <a name="xpproviderinit"></a><span data-ttu-id="fc465-103">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="fc465-103">XPProviderInit</span></span>

  
  
<span data-ttu-id="fc465-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc465-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc465-105">Initialisiert einen Transportanbieter für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="fc465-105">Initializes a transport provider for operation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fc465-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="fc465-106">Header file:</span></span>  <br/> |<span data-ttu-id="fc465-107">Mapispi. h</span><span class="sxs-lookup"><span data-stu-id="fc465-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="fc465-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="fc465-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="fc465-109">Transport Anbieter</span><span class="sxs-lookup"><span data-stu-id="fc465-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="fc465-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="fc465-110">Called by:</span></span>  <br/> |<span data-ttu-id="fc465-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="fc465-111">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="fc465-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="fc465-112">Parameters</span></span>

 <span data-ttu-id="fc465-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="fc465-113">_hInstance_</span></span>
  
> <span data-ttu-id="fc465-114">in Die Instanz der Dynamic Link Library (DLL) des Transportanbieters, die MAPI beim Laden der DLL verwendet hat.</span><span class="sxs-lookup"><span data-stu-id="fc465-114">[in] The instance of the transport provider's dynamic-link library (DLL) that MAPI used when it loaded the DLL.</span></span>
    
 <span data-ttu-id="fc465-115">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="fc465-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="fc465-116">in Zeiger auf ein Speicher Reservierungs Objekt, das die OLE **IMalloc** -Schnittstelle verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="fc465-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="fc465-117">Der Transportanbieter muss diese Zuordnungsmethode möglicherweise beim Arbeiten mit bestimmten Schnittstellen wie **IStream**verwenden.</span><span class="sxs-lookup"><span data-stu-id="fc465-117">The transport provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="fc465-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="fc465-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="fc465-119">in Zeiger auf die [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion, die zum Reservieren von Arbeitsspeicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fc465-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="fc465-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="fc465-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="fc465-121">in Zeiger auf die [MAPIAllocateMore](mapiallocatemore.md) -Funktion, die zum Zuweisen von zusätzlichem Arbeitsspeicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fc465-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="fc465-122">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="fc465-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="fc465-123">in Zeiger auf die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion, die verwendet werden, um Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="fc465-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="fc465-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fc465-124">_ulFlags_</span></span>
  
> <span data-ttu-id="fc465-125">in Bitmaske von Flags.</span><span class="sxs-lookup"><span data-stu-id="fc465-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="fc465-126">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="fc465-126">The following flag can be set:</span></span>
    
<span data-ttu-id="fc465-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="fc465-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="fc465-128">Der Anbieter wird im Kontext eines Windows-Diensts, einem speziellen Prozesstyp ohne Zugriff auf eine beliebige Benutzeroberfläche, geladen.</span><span class="sxs-lookup"><span data-stu-id="fc465-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="fc465-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="fc465-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="fc465-130">in Versionsnummer der Dienstanbieterschnittstelle (SPI), die von MAPI. dll verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fc465-130">[in] Version number of the service provider interface (SPI) that Mapi.dll uses.</span></span> <span data-ttu-id="fc465-131">Die aktuelle Versionsnummer finden Sie in der Headerdatei Mapispi. h.</span><span class="sxs-lookup"><span data-stu-id="fc465-131">For the current version number, see the Mapispi.h header file.</span></span> 
    
 <span data-ttu-id="fc465-132">_lpulProviderVer_</span><span class="sxs-lookup"><span data-stu-id="fc465-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="fc465-133">Out Zeiger auf die Versionsnummer des SPI, die dieser Transportanbieter verwendet.</span><span class="sxs-lookup"><span data-stu-id="fc465-133">[out] Pointer to the version number of the SPI that this transport provider uses.</span></span> 
    
 <span data-ttu-id="fc465-134">_lppXPProvider_</span><span class="sxs-lookup"><span data-stu-id="fc465-134">_lppXPProvider_</span></span>
  
> <span data-ttu-id="fc465-135">Out Zeiger auf einen Zeiger auf das initialisierte Transportanbieter Objekt.</span><span class="sxs-lookup"><span data-stu-id="fc465-135">[out] Pointer to a pointer to the initialized transport provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fc465-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fc465-136">Return value</span></span>

<span data-ttu-id="fc465-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="fc465-137">S_OK</span></span> 
  
> <span data-ttu-id="fc465-138">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="fc465-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="fc465-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="fc465-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="fc465-140">Die SPI-Version, die von MAPI verwendet wird, ist nicht mit dem SPI kompatibel, der von diesem Anbieter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fc465-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fc465-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fc465-141">Remarks</span></span>

<span data-ttu-id="fc465-142">MAPI Ruft die Einstiegspunktfunktion **XPProviderInit** auf, um einen Transportanbieter nach einer Clientanmeldung zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="fc465-142">MAPI calls the entry point function **XPProviderInit** to initialize a transport provider following a client logon.</span></span> <span data-ttu-id="fc465-143">**XPProviderInit** wird einmal für jeden Transportanbieter aufgerufen, der im Profil des Clients angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="fc465-143">**XPProviderInit** is called once for each transport provider specified in the client's profile.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="fc465-144">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="fc465-144">Notes to implementers</span></span>

<span data-ttu-id="fc465-145">Ein Transportanbieter muss **XPProviderInit** als Einstiegspunktfunktion in der DLL des Anbieters implementieren.</span><span class="sxs-lookup"><span data-stu-id="fc465-145">A transport provider must implement **XPProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="fc465-146">Die Implementierung muss auf dem **XPPROVIDERINIT** -Funktionsprototyp basieren, der auch in Mapispi. h angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="fc465-146">The implementation must be based on the **XPPROVIDERINIT** function prototype, also specified in Mapispi.h.</span></span> <span data-ttu-id="fc465-147">MAPI definiert **XPPROVIDERINIT** für die Verwendung des standardMÄßIGen MAPI-Initialisierungsaufruf Typs STDMAPIINITCALLTYPE, wodurch **XPPROVIDERINIT** der Cdecl-Aufrufkonvention folgt.</span><span class="sxs-lookup"><span data-stu-id="fc465-147">MAPI defines **XPPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **XPProviderInit** to follow the CDECL calling convention.</span></span> <span data-ttu-id="fc465-148">Ein Vorteil von CDECL besteht darin, dass Aufrufe auch dann versucht werden können, wenn die Anzahl der Anruf Parameter nicht mit der Anzahl der definierten Parameter übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="fc465-148">An advantage of CDECL is that calls can be attempted even if the number of calling parameters does not match the number of defined parameters.</span></span> 
  
<span data-ttu-id="fc465-149">Ein Anbieter kann mehrmals initialisiert werden, wenn er in mehreren Profilen gleichzeitig verwendet wird oder mehr als einmal im gleichen Profil angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="fc465-149">A provider can be initialized multiple times as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="fc465-150">Da das Provider-Objekt den Kontext enthält, muss **XPProviderInit** für jede Initialisierung ein anderes Anbieterobjekt in _lppXPProvider_ zurückgeben, auch für mehrere Initialisierungen im selben Prozess.</span><span class="sxs-lookup"><span data-stu-id="fc465-150">Because the provider object contains context, **XPProviderInit** must return a different provider object in  _lppXPProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="fc465-151">Der Transportanbieter sollte die Funktionen, auf die von _lpAllocateBuffer_, _lpAllocateMore_und _lpFreeBuffer_ verwiesen wird, für die meisten Speicherzuweisungen und-Aufhebungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="fc465-151">The transport provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="fc465-152">Insbesondere muss der Anbieter diese Funktionen verwenden, um Arbeitsspeicher für die Verwendung durch Clientanwendungen zu reservieren, wenn Objektschnittstellen wie [IMAPIProp::](imapiprop-getprops.md) GetProps und [IMAPITable:: QueryRows](imapitable-queryrows.md)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="fc465-152">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="fc465-153">Wenn der Anbieter auch die Verwendung der OLE-Speicherzuweisung erwartet, sollte er die **IUnknown:: AddRef** -Methode des Zuweisungs Objekts aufrufen, auf die durch den _lpMalloc_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="fc465-153">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="fc465-154">Weitere Informationen zum Schreiben von **XPProviderInit**finden Sie unter [Initialisieren des Transport Anbieters](initializing-the-transport-provider.md).</span><span class="sxs-lookup"><span data-stu-id="fc465-154">For more information about writing **XPProviderInit**, see [Initializing the Transport Provider](initializing-the-transport-provider.md).</span></span> <span data-ttu-id="fc465-155">Weitere Informationen zu Einstiegspunktfunktionen finden Sie unter [Implementieren einer Dienstanbieter-Einstiegspunktfunktion](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="fc465-155">For more information about entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fc465-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fc465-156">See also</span></span>



[<span data-ttu-id="fc465-157">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="fc465-157">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="fc465-158">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fc465-158">IXPProvider : IUnknown</span></span>](ixpprovideriunknown.md)
  
[<span data-ttu-id="fc465-159">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="fc465-159">MSProviderInit</span></span>](msproviderinit.md)

