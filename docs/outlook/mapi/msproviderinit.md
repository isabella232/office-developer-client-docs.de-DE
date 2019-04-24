---
title: MSProviderInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MSProviderInit
api_type:
- HeaderDef
ms.assetid: 230c66c4-ab04-4fa6-946f-9f4b704f2842
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9a5f8b44f9d795282ccfd61fd32a306c5478ed21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342791"
---
# <a name="msproviderinit"></a><span data-ttu-id="e6b89-103">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="e6b89-103">MSProviderInit</span></span>

  
  
<span data-ttu-id="e6b89-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e6b89-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e6b89-105">Initialisiert einen Nachrichtenspeicher Anbieter für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="e6b89-105">Initializes a message store provider for operation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e6b89-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="e6b89-106">Header file:</span></span>  <br/> |<span data-ttu-id="e6b89-107">Mapispi. h</span><span class="sxs-lookup"><span data-stu-id="e6b89-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="e6b89-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="e6b89-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e6b89-109">Nachrichtenspeicher Anbieter</span><span class="sxs-lookup"><span data-stu-id="e6b89-109">Message store providers</span></span>  <br/> |
|<span data-ttu-id="e6b89-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="e6b89-110">Called by:</span></span>  <br/> |<span data-ttu-id="e6b89-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="e6b89-111">MAPI</span></span>  <br/> |
   
```cpp
HRESULT MSProviderInit(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  ULONG ulMAPIVer,
  ULONG FAR * lpulProviderVer,
  LPMSPROVIDER FAR * lppMSProvider
);
```

## <a name="parameters"></a><span data-ttu-id="e6b89-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6b89-112">Parameters</span></span>

 <span data-ttu-id="e6b89-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="e6b89-113">_hInstance_</span></span>
  
> <span data-ttu-id="e6b89-114">in Die Instanz der Dynamic Link Library (DLL) des Nachrichtenspeicher Anbieters, die MAPI bei der Verknüpfung verwendet hat.</span><span class="sxs-lookup"><span data-stu-id="e6b89-114">[in] The instance of the message store provider's dynamic-link library (DLL) that MAPI used when it linked.</span></span> 
    
 <span data-ttu-id="e6b89-115">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="e6b89-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="e6b89-116">in Zeiger auf ein Speicher Reservierungs Objekt, das die OLE **IMalloc** -Schnittstelle verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="e6b89-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="e6b89-117">Der Nachrichtenspeicher Anbieter muss diese Zuordnungsmethode möglicherweise beim Arbeiten mit bestimmten Schnittstellen wie **IStream**verwenden.</span><span class="sxs-lookup"><span data-stu-id="e6b89-117">The message store provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="e6b89-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="e6b89-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="e6b89-119">in Zeiger auf die [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion, die zum Reservieren von Arbeitsspeicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e6b89-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="e6b89-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="e6b89-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="e6b89-121">in Zeiger auf die [MAPIAllocateMore](mapiallocatemore.md) -Funktion, die zum Zuweisen von zusätzlichem Arbeitsspeicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e6b89-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="e6b89-122">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="e6b89-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="e6b89-123">in Zeiger auf die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion, die verwendet werden, um Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="e6b89-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="e6b89-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e6b89-124">_ulFlags_</span></span>
  
> <span data-ttu-id="e6b89-125">in Bitmaske von Flags.</span><span class="sxs-lookup"><span data-stu-id="e6b89-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="e6b89-126">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="e6b89-126">The following flag can be set:</span></span>
    
<span data-ttu-id="e6b89-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="e6b89-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="e6b89-128">Der Anbieter wird im Kontext eines Windows-Diensts, einem speziellen Prozesstyp ohne Zugriff auf eine beliebige Benutzeroberfläche, geladen.</span><span class="sxs-lookup"><span data-stu-id="e6b89-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="e6b89-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="e6b89-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="e6b89-130">in Die Versionsnummer der Dienstanbieterschnittstelle, die von MAPI verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e6b89-130">[in] Version number of the service provider interface (SPI) that MAPI uses.</span></span> <span data-ttu-id="e6b89-131">Die aktuelle Versionsnummer finden Sie in der Headerdatei Mapispi. h.</span><span class="sxs-lookup"><span data-stu-id="e6b89-131">For the current version number, see the Mapispi.h header file.</span></span> 
    
 <span data-ttu-id="e6b89-132">_lpulProviderVer_</span><span class="sxs-lookup"><span data-stu-id="e6b89-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="e6b89-133">Out Zeiger auf die Versionsnummer des SPI, den dieser Nachrichtenspeicher Anbieter verwendet.</span><span class="sxs-lookup"><span data-stu-id="e6b89-133">[out] Pointer to the version number of the SPI that this message store provider uses.</span></span> 
    
 <span data-ttu-id="e6b89-134">_lppMSProvider_</span><span class="sxs-lookup"><span data-stu-id="e6b89-134">_lppMSProvider_</span></span>
  
> <span data-ttu-id="e6b89-135">Out Zeiger auf einen Zeiger auf das initialisierte Nachrichtenspeicher-Anbieterobjekt.</span><span class="sxs-lookup"><span data-stu-id="e6b89-135">[out] Pointer to a pointer to the initialized message store provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e6b89-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e6b89-136">Return value</span></span>

<span data-ttu-id="e6b89-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="e6b89-137">S_OK</span></span> 
  
> <span data-ttu-id="e6b89-138">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="e6b89-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="e6b89-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="e6b89-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="e6b89-140">Die SPI-Version, die von MAPI verwendet wird, ist nicht mit dem SPI kompatibel, der von diesem Anbieter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e6b89-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e6b89-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e6b89-141">Remarks</span></span>

<span data-ttu-id="e6b89-142">MAPI Ruft die Einstiegspunktfunktion **MSProviderInit** auf, um einen Nachrichtenspeicher Anbieter nach einer Clientanmeldung zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="e6b89-142">MAPI calls the entry point function **MSProviderInit** to initialize a message store provider following a client logon.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="e6b89-143">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="e6b89-143">Notes to implementers</span></span>

<span data-ttu-id="e6b89-144">Ein Nachrichtenspeicher Anbieter muss **MSProviderInit** als Einstiegspunktfunktion in der DLL des Anbieters implementieren.</span><span class="sxs-lookup"><span data-stu-id="e6b89-144">A message store provider must implement **MSProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="e6b89-145">Die Implementierung muss auf dem Prototyp der **MSPROVIDERINIT** -Funktion basieren, der auch in MAPISPI angegeben ist. H.</span><span class="sxs-lookup"><span data-stu-id="e6b89-145">The implementation must be based on the **MSPROVIDERINIT** function prototype, also specified in MAPISPI.H.</span></span> <span data-ttu-id="e6b89-146">MAPI definiert **MSPROVIDERINIT** für die Verwendung des standardMÄßIGen MAPI-Initialisierungsaufruf Typs STDMAPIINITCALLTYPE, wodurch **MSPROVIDERINIT** der Cdecl-Aufrufkonvention folgt.</span><span class="sxs-lookup"><span data-stu-id="e6b89-146">MAPI defines **MSPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **MSProviderInit** to follow the CDECL calling convention.</span></span> <span data-ttu-id="e6b89-147">Ein Vorteil von CDECL besteht darin, dass Aufrufe auch dann versucht werden können, wenn die Anzahl der Anruf Parameter nicht mit der Anzahl der definierten Parameter übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="e6b89-147">An advantage of CDECL is that calls can be attempted even if the number of calling parameters does not match the number of defined parameters.</span></span> 
  
<span data-ttu-id="e6b89-148">Ein Anbieter kann mehrmals initialisiert werden, wenn er in mehreren Profilen gleichzeitig verwendet wird oder mehr als einmal im gleichen Profil angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e6b89-148">A provider can be initialized multiple times, as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="e6b89-149">Da das Provider-Objekt den Kontext enthält, muss **MSProviderInit** für jede Initialisierung ein anderes Anbieterobjekt in _lppMSProvider_ zurückgeben, auch für mehrere Initialisierungen im selben Prozess.</span><span class="sxs-lookup"><span data-stu-id="e6b89-149">Because the provider object contains context, **MSProviderInit** must return a different provider object in  _lppMSProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="e6b89-150">Die Anbieter-DLL sollte nicht mit mapix. dll verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="e6b89-150">The provider DLL should not be linked with Mapix.dll.</span></span> <span data-ttu-id="e6b89-151">Stattdessen sollten Sie diese Zeiger für die Speicherbelegung oder-dereservierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="e6b89-151">Instead, it should use these pointers for memory allocation or deallocation.</span></span> 
  
<span data-ttu-id="e6b89-152">Der Nachrichtenspeicher Anbieter sollte die Funktionen, auf die von _lpAllocateBuffer_, _lpAllocateMore_und _lpFreeBuffer_ verwiesen wird, für die meisten Speicherzuweisungen und-Aufhebungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="e6b89-152">The message store provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="e6b89-153">Insbesondere muss der Anbieter diese Funktionen verwenden, um Arbeitsspeicher für die Verwendung durch Clientanwendungen zu reservieren, wenn Objektschnittstellen wie [IMAPIProp::](imapiprop-getprops.md) GetProps und [IMAPITable:: QueryRows](imapitable-queryrows.md)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e6b89-153">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="e6b89-154">Wenn der Anbieter auch die Verwendung der OLE-Speicherzuweisung erwartet, sollte er die **IUnknown:: AddRef** -Methode des Zuweisungs Objekts aufrufen, auf die durch den _lpMalloc_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="e6b89-154">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="e6b89-155">Weitere Informationen zum Schreiben von **MSProviderInit**finden Sie unter [Loading Message Store Providers](loading-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="e6b89-155">For more information about writing **MSProviderInit**, see [Loading Message Store Providers](loading-message-store-providers.md).</span></span> <span data-ttu-id="e6b89-156">Weitere Informationen zu Einstiegspunktfunktionen finden Sie unter [Implementieren einer Dienstanbieter-Einstiegspunktfunktion](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="e6b89-156">For more information about entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e6b89-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6b89-157">See also</span></span>



[<span data-ttu-id="e6b89-158">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="e6b89-158">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="e6b89-159">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e6b89-159">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)
  
[<span data-ttu-id="e6b89-160">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="e6b89-160">XPProviderInit</span></span>](xpproviderinit.md)

