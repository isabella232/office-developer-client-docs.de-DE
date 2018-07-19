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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: cf1febe89c49b29cdfaf8d27760c4fb27b4c4990
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793278"
---
# <a name="msproviderinit"></a><span data-ttu-id="77329-103">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="77329-103">MSProviderInit</span></span>

  
  
<span data-ttu-id="77329-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="77329-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="77329-105">Initialisiert eine Nachricht Speicheranbieter Vorgang.</span><span class="sxs-lookup"><span data-stu-id="77329-105">Initializes a message store provider for operation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="77329-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="77329-106">Header file:</span></span>  <br/> |<span data-ttu-id="77329-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="77329-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="77329-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="77329-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="77329-109">Nachricht-Anbieter</span><span class="sxs-lookup"><span data-stu-id="77329-109">Message store providers</span></span>  <br/> |
|<span data-ttu-id="77329-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="77329-110">Called by:</span></span>  <br/> |<span data-ttu-id="77329-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="77329-111">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="77329-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="77329-112">Parameters</span></span>

 <span data-ttu-id="77329-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="77329-113">_hInstance_</span></span>
  
> <span data-ttu-id="77329-114">[in] Die Instanz der Nachricht Speichern des Anbieters Dynamic Link Library (DLL), die MAPI verwendet wird, wenn es verknüpft.</span><span class="sxs-lookup"><span data-stu-id="77329-114">[in] The instance of the message store provider's dynamic-link library (DLL) that MAPI used when it linked.</span></span> 
    
 <span data-ttu-id="77329-115">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="77329-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="77329-116">[in] Zeiger auf ein Speicherobjekt-Zuweisung die OLE **IMalloc** -Schnittstelle verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="77329-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="77329-117">Der Nachricht Speicheranbieter müssen möglicherweise beim Arbeiten mit bestimmte Schnittstellen wie **IStream**diese Zuordnungsmethode verwenden.</span><span class="sxs-lookup"><span data-stu-id="77329-117">The message store provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="77329-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="77329-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="77329-119">[in] Zeiger auf die Funktion [MAPIAllocateBuffer](mapiallocatebuffer.md) , Speicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="77329-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="77329-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="77329-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="77329-121">[in] Zeiger auf die [MAPIAllocateMore](mapiallocatemore.md) -Funktion, mit der zusätzlichen Arbeitsspeicher zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="77329-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="77329-122">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="77329-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="77329-123">[in] Zeiger auf die [MAPIFreeBuffer](mapifreebuffer.md) -Funktion verwendet werden, um Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="77329-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="77329-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="77329-124">_ulFlags_</span></span>
  
> <span data-ttu-id="77329-125">[in] Bitmaske der Kennzeichen.</span><span class="sxs-lookup"><span data-stu-id="77329-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="77329-126">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="77329-126">The following flag can be set:</span></span>
    
<span data-ttu-id="77329-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="77329-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="77329-128">Der Anbieter wird im Kontext eines Windows-Diensts, eine spezielle Art von Vorgang ohne Zugriff auf eine beliebige Benutzeroberfläche geladen.</span><span class="sxs-lookup"><span data-stu-id="77329-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="77329-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="77329-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="77329-130">[in] Versionsnummer der der Dienstanbieter-Schnittstelle (SPI), die MAPI verwendet.</span><span class="sxs-lookup"><span data-stu-id="77329-130">[in] Version number of the service provider interface (SPI) that MAPI uses.</span></span> <span data-ttu-id="77329-131">Die aktuelle Versionsnummer finden Sie unter der Headerdatei Mapispi.h.</span><span class="sxs-lookup"><span data-stu-id="77329-131">For the current version number, see the Mapispi.h header file.</span></span> 
    
 <span data-ttu-id="77329-132">_lpulProviderVer_</span><span class="sxs-lookup"><span data-stu-id="77329-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="77329-133">[out] Zeiger auf die Versionsnummer der SPI, die diese Nachricht Speicher-Anbieter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="77329-133">[out] Pointer to the version number of the SPI that this message store provider uses.</span></span> 
    
 <span data-ttu-id="77329-134">_lppMSProvider_</span><span class="sxs-lookup"><span data-stu-id="77329-134">_lppMSProvider_</span></span>
  
> <span data-ttu-id="77329-135">[out] Zeiger auf einen Zeiger auf den initialisierten Message Store Provider-Objekt.</span><span class="sxs-lookup"><span data-stu-id="77329-135">[out] Pointer to a pointer to the initialized message store provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="77329-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="77329-136">Return value</span></span>

<span data-ttu-id="77329-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="77329-137">S_OK</span></span> 
  
> <span data-ttu-id="77329-138">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="77329-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="77329-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="77329-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="77329-140">Die SPI-Version von MAPI verwendet wird, ist nicht kompatibel mit der SPI, die von diesem Anbieter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="77329-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="77329-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="77329-141">Remarks</span></span>

<span data-ttu-id="77329-142">MAPI-aufrufen, die Eintrags-Funktion **MSProviderInit** einen Anbieter für anmelden nach einer Clientanmeldung nicht initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="77329-142">MAPI calls the entry point function **MSProviderInit** to initialize a message store provider following a client logon.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="77329-143">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="77329-143">Notes to implementers</span></span>

<span data-ttu-id="77329-144">Eine Nachricht Speicheranbieter muss als Funktion Entry Point in die DLL des Anbieters **MSProviderInit** implementieren.</span><span class="sxs-lookup"><span data-stu-id="77329-144">A message store provider must implement **MSProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="77329-145">Die Implementierung der **MSPROVIDERINIT** Funktionsprototyp auch im angegebenen MAPISPI basieren. H.</span><span class="sxs-lookup"><span data-stu-id="77329-145">The implementation must be based on the **MSPROVIDERINIT** function prototype, also specified in MAPISPI.H.</span></span> <span data-ttu-id="77329-146">MAPI definiert **MSPROVIDERINIT** Verwendung standard MAPI Initialisierung Aufruftyps, STDMAPIINITCALLTYPE, wodurch **MSProviderInit** CDECL-Aufrufkonvention folgen.</span><span class="sxs-lookup"><span data-stu-id="77329-146">MAPI defines **MSPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **MSProviderInit** to follow the CDECL calling convention.</span></span> <span data-ttu-id="77329-147">Ein Vorteil CDECL ist, dass Anrufe versucht werden können, selbst wenn die Anzahl der aufrufenden Parameter nicht die Anzahl der definierten Parameter übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="77329-147">An advantage of CDECL is that calls can be attempted even if the number of calling parameters does not match the number of defined parameters.</span></span> 
  
<span data-ttu-id="77329-148">Ein Anbieter kann mehrere Male, als Ergebnis in mehrere Profile angezeigt wird, in der gleichzeitigen Verwendung oder nur einmal in das gleiche Profil angezeigt werden initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="77329-148">A provider can be initialized multiple times, as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="77329-149">Da das Anbieterobjekt Kontext enthält, muss **MSProviderInit** in _LppMSProvider_ für jede Initialisierung, auch für mehrere wie in demselben Prozess einer anderen Anbieter-Objekt zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="77329-149">Because the provider object contains context, **MSProviderInit** must return a different provider object in  _lppMSProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="77329-150">Der Provider-DLL sollte nicht mit Mapix.dll verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="77329-150">The provider DLL should not be linked with Mapix.dll.</span></span> <span data-ttu-id="77329-151">In diesem Fall sollte diese Zeiger für oder Aufheben der arbeitsspeicherreservierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="77329-151">Instead, it should use these pointers for memory allocation or deallocation.</span></span> 
  
<span data-ttu-id="77329-152">Der Nachricht Speicheranbieter sollten die Funktionen, die auf den _LpAllocateBuffer_, _LpAllocateMore_und _LpFreeBuffer_ für die meisten arbeitsspeicherreservierung und Freigabe verwenden.</span><span class="sxs-lookup"><span data-stu-id="77329-152">The message store provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="77329-153">Insbesondere muss den Anbieter diese Funktionen für die Verwendung von Clientanwendungen Speicher beim Aufruf von wie [IMAPIProp::GetProps](imapiprop-getprops.md) und [IMAPITable::QueryRows](imapitable-queryrows.md)-Schnittstellen verwenden.</span><span class="sxs-lookup"><span data-stu-id="77329-153">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="77329-154">Wenn der Anbieter auch erwartet, verwenden Sie die Zuweisung der OLE-Speicher, sollten sie die **IUnknown:: AddRef** -Methode, der das Zuordnungsobjekt auf das durch den Parameter _LpMalloc_ aufrufen.</span><span class="sxs-lookup"><span data-stu-id="77329-154">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="77329-155">Weitere Informationen über das Schreiben von **MSProviderInit**finden Sie unter [Message-Anbieter laden](loading-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="77329-155">For more information about writing **MSProviderInit**, see [Loading Message Store Providers](loading-message-store-providers.md).</span></span> <span data-ttu-id="77329-156">Weitere Informationen zu Entry Point-Funktionen finden Sie unter [Implementieren einer Service Provider Eintrag zeigen-Funktion](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="77329-156">For more information about entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="77329-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="77329-157">See also</span></span>



[<span data-ttu-id="77329-158">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="77329-158">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="77329-159">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="77329-159">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)
  
[<span data-ttu-id="77329-160">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="77329-160">XPProviderInit</span></span>](xpproviderinit.md)

