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
ms.openlocfilehash: 0415e782a98102314ce732f744c0d29590f646c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795868"
---
# <a name="xpproviderinit"></a><span data-ttu-id="d54c9-103">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="d54c9-103">XPProviderInit</span></span>

  
  
<span data-ttu-id="d54c9-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d54c9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d54c9-105">Initialisiert eine Adressbuchhierarchie für Vorgang.</span><span class="sxs-lookup"><span data-stu-id="d54c9-105">Initializes a transport provider for operation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d54c9-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="d54c9-106">Header file:</span></span>  <br/> |<span data-ttu-id="d54c9-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="d54c9-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="d54c9-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="d54c9-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d54c9-109">Transportanbieter</span><span class="sxs-lookup"><span data-stu-id="d54c9-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="d54c9-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="d54c9-110">Called by:</span></span>  <br/> |<span data-ttu-id="d54c9-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="d54c9-111">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="d54c9-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d54c9-112">Parameters</span></span>

 <span data-ttu-id="d54c9-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="d54c9-113">_hInstance_</span></span>
  
> <span data-ttu-id="d54c9-114">[in] Die Instanz der Adressbuchhierarchie Dynamic Link Library (DLL), MAPI verwendet, wenn sie die DLL-Datei geladen.</span><span class="sxs-lookup"><span data-stu-id="d54c9-114">[in] The instance of the transport provider's dynamic-link library (DLL) that MAPI used when it loaded the DLL.</span></span>
    
 <span data-ttu-id="d54c9-115">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="d54c9-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="d54c9-116">[in] Zeiger auf ein Speicherobjekt-Zuweisung die OLE **IMalloc** -Schnittstelle verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="d54c9-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="d54c9-117">Der Transportdienst müssen möglicherweise beim Arbeiten mit bestimmte Schnittstellen wie **IStream**diese Zuordnungsmethode verwenden.</span><span class="sxs-lookup"><span data-stu-id="d54c9-117">The transport provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="d54c9-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="d54c9-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="d54c9-119">[in] Zeiger auf die Funktion [MAPIAllocateBuffer](mapiallocatebuffer.md) , Speicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d54c9-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="d54c9-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="d54c9-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="d54c9-121">[in] Zeiger auf die [MAPIAllocateMore](mapiallocatemore.md) -Funktion, mit der zusätzlichen Arbeitsspeicher zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="d54c9-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="d54c9-122">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="d54c9-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="d54c9-123">[in] Zeiger auf die [MAPIFreeBuffer](mapifreebuffer.md) -Funktion verwendet werden, um Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="d54c9-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="d54c9-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d54c9-124">_ulFlags_</span></span>
  
> <span data-ttu-id="d54c9-125">[in] Bitmaske der Kennzeichen.</span><span class="sxs-lookup"><span data-stu-id="d54c9-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="d54c9-126">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="d54c9-126">The following flag can be set:</span></span>
    
<span data-ttu-id="d54c9-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="d54c9-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="d54c9-128">Der Anbieter wird im Kontext eines Windows-Diensts, eine spezielle Art von Vorgang ohne Zugriff auf eine beliebige Benutzeroberfläche geladen.</span><span class="sxs-lookup"><span data-stu-id="d54c9-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="d54c9-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="d54c9-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="d54c9-130">[in] Versionsnummer der der Dienstanbieter-Schnittstelle (SPI), die die Datei MAPI verwendet.</span><span class="sxs-lookup"><span data-stu-id="d54c9-130">[in] Version number of the service provider interface (SPI) that Mapi.dll uses.</span></span> <span data-ttu-id="d54c9-131">Die aktuelle Versionsnummer finden Sie unter der Headerdatei Mapispi.h.</span><span class="sxs-lookup"><span data-stu-id="d54c9-131">For the current version number, see the Mapispi.h header file.</span></span> 
    
 <span data-ttu-id="d54c9-132">_lpulProviderVer_</span><span class="sxs-lookup"><span data-stu-id="d54c9-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="d54c9-133">[out] Zeiger auf die Versionsnummer der SPI, die dieser Transportdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="d54c9-133">[out] Pointer to the version number of the SPI that this transport provider uses.</span></span> 
    
 <span data-ttu-id="d54c9-134">_lppXPProvider_</span><span class="sxs-lookup"><span data-stu-id="d54c9-134">_lppXPProvider_</span></span>
  
> <span data-ttu-id="d54c9-135">[out] Zeiger auf einen Zeiger auf den initialisierten Transportobjekt Anbieter.</span><span class="sxs-lookup"><span data-stu-id="d54c9-135">[out] Pointer to a pointer to the initialized transport provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d54c9-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d54c9-136">Return value</span></span>

<span data-ttu-id="d54c9-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="d54c9-137">S_OK</span></span> 
  
> <span data-ttu-id="d54c9-138">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="d54c9-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="d54c9-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="d54c9-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="d54c9-140">Die SPI-Version von MAPI verwendet wird, ist nicht kompatibel mit der SPI, die von diesem Anbieter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d54c9-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d54c9-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d54c9-141">Remarks</span></span>

<span data-ttu-id="d54c9-142">MAPI-aufrufen, die Eintrags-Funktion **XPProviderInit** ein Transportdienstes nach einer Clientanmeldung nicht initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="d54c9-142">MAPI calls the entry point function **XPProviderInit** to initialize a transport provider following a client logon.</span></span> <span data-ttu-id="d54c9-143">**XPProviderInit** wird einmal für jede Adressbuchhierarchie im Profil des Clients angegebene aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="d54c9-143">**XPProviderInit** is called once for each transport provider specified in the client's profile.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d54c9-144">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="d54c9-144">Notes to implementers</span></span>

<span data-ttu-id="d54c9-145">Ein Transportdienstes muss als Funktion Entry Point in die DLL des Anbieters **XPProviderInit** implementieren.</span><span class="sxs-lookup"><span data-stu-id="d54c9-145">A transport provider must implement **XPProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="d54c9-146">Die Implementierung der **XPPROVIDERINIT** Funktionsprototyp auch im angegebenen Mapispi.h basieren.</span><span class="sxs-lookup"><span data-stu-id="d54c9-146">The implementation must be based on the **XPPROVIDERINIT** function prototype, also specified in Mapispi.h.</span></span> <span data-ttu-id="d54c9-147">MAPI definiert **XPPROVIDERINIT** Verwendung standard MAPI Initialisierung Aufruftyps, STDMAPIINITCALLTYPE, wodurch **XPProviderInit** CDECL-Aufrufkonvention folgen.</span><span class="sxs-lookup"><span data-stu-id="d54c9-147">MAPI defines **XPPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **XPProviderInit** to follow the CDECL calling convention.</span></span> <span data-ttu-id="d54c9-148">Ein Vorteil CDECL ist, dass Anrufe versucht werden können, selbst wenn die Anzahl der aufrufenden Parameter nicht die Anzahl der definierten Parameter übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="d54c9-148">An advantage of CDECL is that calls can be attempted even if the number of calling parameters does not match the number of defined parameters.</span></span> 
  
<span data-ttu-id="d54c9-149">Ein Anbieter kann mehrmals initialisiert werden, als Ergebnis in mehrere Profile angezeigt wird, in der gleichzeitigen Verwendung oder nur einmal in das gleiche Profil angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d54c9-149">A provider can be initialized multiple times as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="d54c9-150">Da das Anbieterobjekt Kontext enthält, muss **XPProviderInit** in _LppXPProvider_ für jede Initialisierung, auch für mehrere wie in demselben Prozess einer anderen Anbieter-Objekt zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="d54c9-150">Because the provider object contains context, **XPProviderInit** must return a different provider object in  _lppXPProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="d54c9-151">Der Transportdienst sollten die Funktionen, die auf den _LpAllocateBuffer_, _LpAllocateMore_und _LpFreeBuffer_ für die meisten arbeitsspeicherreservierung und Freigabe verwenden.</span><span class="sxs-lookup"><span data-stu-id="d54c9-151">The transport provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="d54c9-152">Insbesondere muss den Anbieter diese Funktionen für die Verwendung von Clientanwendungen Speicher beim Aufruf von wie [IMAPIProp::GetProps](imapiprop-getprops.md) und [IMAPITable::QueryRows](imapitable-queryrows.md)-Schnittstellen verwenden.</span><span class="sxs-lookup"><span data-stu-id="d54c9-152">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="d54c9-153">Wenn der Anbieter auch erwartet, verwenden Sie die Zuweisung der OLE-Speicher, sollten sie die **IUnknown:: AddRef** -Methode, der das Zuordnungsobjekt auf das durch den Parameter _LpMalloc_ aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d54c9-153">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="d54c9-154">Weitere Informationen über das Schreiben von **XPProviderInit**finden Sie unter [der Adressbuchhierarchie initialisieren](initializing-the-transport-provider.md).</span><span class="sxs-lookup"><span data-stu-id="d54c9-154">For more information about writing **XPProviderInit**, see [Initializing the Transport Provider](initializing-the-transport-provider.md).</span></span> <span data-ttu-id="d54c9-155">Weitere Informationen zu Entry Point-Funktionen finden Sie unter [Implementieren einer Service Provider Eintrag zeigen-Funktion](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="d54c9-155">For more information about entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d54c9-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d54c9-156">See also</span></span>



[<span data-ttu-id="d54c9-157">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="d54c9-157">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="d54c9-158">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d54c9-158">IXPProvider : IUnknown</span></span>](ixpprovideriunknown.md)
  
[<span data-ttu-id="d54c9-159">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="d54c9-159">MSProviderInit</span></span>](msproviderinit.md)

