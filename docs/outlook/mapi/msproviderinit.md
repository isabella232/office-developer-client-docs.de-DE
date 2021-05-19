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
ms.openlocfilehash: 9a5f8b44f9d795282ccfd61fd32a306c5478ed21
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416237"
---
# <a name="msproviderinit"></a><span data-ttu-id="7efef-103">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="7efef-103">MSProviderInit</span></span>

  
  
<span data-ttu-id="7efef-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7efef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7efef-105">Initialisiert einen Nachrichtenspeicheranbieter für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="7efef-105">Initializes a message store provider for operation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7efef-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="7efef-106">Header file:</span></span>  <br/> |<span data-ttu-id="7efef-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="7efef-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="7efef-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="7efef-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7efef-109">Anbieter von Nachrichtenspeichern</span><span class="sxs-lookup"><span data-stu-id="7efef-109">Message store providers</span></span>  <br/> |
|<span data-ttu-id="7efef-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="7efef-110">Called by:</span></span>  <br/> |<span data-ttu-id="7efef-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="7efef-111">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="7efef-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7efef-112">Parameters</span></span>

 <span data-ttu-id="7efef-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="7efef-113">_hInstance_</span></span>
  
> <span data-ttu-id="7efef-114">[in] Die Instanz der DYNAMIC-Link Library (DLL) des Nachrichtenspeicheranbieters, die MAPI beim Verknüpfen verwendet hat.</span><span class="sxs-lookup"><span data-stu-id="7efef-114">[in] The instance of the message store provider's dynamic-link library (DLL) that MAPI used when it linked.</span></span> 
    
 <span data-ttu-id="7efef-115">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="7efef-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="7efef-116">[in] Zeiger auf ein Speicherzuweisungsobjekt, das die OLE **IMalloc-Schnittstelle verfügbar** machen soll.</span><span class="sxs-lookup"><span data-stu-id="7efef-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="7efef-117">Der Nachrichtenspeicheranbieter muss diese Zuordnungsmethode möglicherweise verwenden, wenn er mit bestimmten Schnittstellen wie **IStream arbeitet.**</span><span class="sxs-lookup"><span data-stu-id="7efef-117">The message store provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="7efef-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="7efef-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="7efef-119">[in] Zeiger auf die [MAPIAllocateBuffer-Funktion,](mapiallocatebuffer.md) die zum Zuordnen von Arbeitsspeicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7efef-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="7efef-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="7efef-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="7efef-121">[in] Zeiger auf die [MAPIAllocateMore-Funktion,](mapiallocatemore.md) die zum Zuordnen von zusätzlichem Arbeitsspeicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7efef-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="7efef-122">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="7efef-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="7efef-123">[in] Zeiger auf die [MAPIFreeBuffer-Funktion,](mapifreebuffer.md) die zum Freispeichern verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7efef-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="7efef-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7efef-124">_ulFlags_</span></span>
  
> <span data-ttu-id="7efef-125">[in] Bitmaske von Flags.</span><span class="sxs-lookup"><span data-stu-id="7efef-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="7efef-126">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="7efef-126">The following flag can be set:</span></span>
    
<span data-ttu-id="7efef-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="7efef-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="7efef-128">Der Anbieter wird im Kontext eines Windows geladen, einem speziellen Prozesstyp ohne Zugriff auf eine Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="7efef-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="7efef-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="7efef-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="7efef-130">[in] Versionsnummer der von MAPI verwendeten Dienstanbieterschnittstelle (Service Provider Interface, SPI).</span><span class="sxs-lookup"><span data-stu-id="7efef-130">[in] Version number of the service provider interface (SPI) that MAPI uses.</span></span> <span data-ttu-id="7efef-131">Die aktuelle Versionsnummer finden Sie in der Mapispi.h-Headerdatei.</span><span class="sxs-lookup"><span data-stu-id="7efef-131">For the current version number, see the Mapispi.h header file.</span></span> 
    
 <span data-ttu-id="7efef-132">_lpulProviderVer_</span><span class="sxs-lookup"><span data-stu-id="7efef-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="7efef-133">[out] Zeiger auf die Versionsnummer des SPI, den dieser Nachrichtenspeicheranbieter verwendet.</span><span class="sxs-lookup"><span data-stu-id="7efef-133">[out] Pointer to the version number of the SPI that this message store provider uses.</span></span> 
    
 <span data-ttu-id="7efef-134">_lppMSProvider_</span><span class="sxs-lookup"><span data-stu-id="7efef-134">_lppMSProvider_</span></span>
  
> <span data-ttu-id="7efef-135">[out] Zeiger auf einen Zeiger auf das initialisierte Objekt des Nachrichtenspeicheranbieters.</span><span class="sxs-lookup"><span data-stu-id="7efef-135">[out] Pointer to a pointer to the initialized message store provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7efef-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7efef-136">Return value</span></span>

<span data-ttu-id="7efef-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="7efef-137">S_OK</span></span> 
  
> <span data-ttu-id="7efef-138">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="7efef-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="7efef-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="7efef-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="7efef-140">Die von MAPI verwendete SPI-Version ist nicht mit dem von diesem Anbieter verwendeten SPI kompatibel.</span><span class="sxs-lookup"><span data-stu-id="7efef-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7efef-141">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7efef-141">Remarks</span></span>

<span data-ttu-id="7efef-142">MAPI ruft die Einstiegspunktfunktion **MSProviderInit** auf, um einen Nachrichtenspeicheranbieter nach einer Clientanmeldung zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="7efef-142">MAPI calls the entry point function **MSProviderInit** to initialize a message store provider following a client logon.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7efef-143">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="7efef-143">Notes to implementers</span></span>

<span data-ttu-id="7efef-144">Ein Nachrichtenspeicheranbieter muss **MSProviderInit** als Einstiegspunktfunktion in der DLL des Anbieters implementieren.</span><span class="sxs-lookup"><span data-stu-id="7efef-144">A message store provider must implement **MSProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="7efef-145">Die Implementierung muss auf dem **MSPROVIDERINIT-Funktionsprototyp** basieren, der auch in MAPISPI.H angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="7efef-145">The implementation must be based on the **MSPROVIDERINIT** function prototype, also specified in MAPISPI.H.</span></span> <span data-ttu-id="7efef-146">MAPI definiert **MSPROVIDERINIT** für die Verwendung des standardmäßigen MAPI-Initialisierungsaufruftyps STDMAPIINITCALLTYPE, wodurch **MSProviderInit** der CDECL-Aufrufkonvention folgt.</span><span class="sxs-lookup"><span data-stu-id="7efef-146">MAPI defines **MSPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **MSProviderInit** to follow the CDECL calling convention.</span></span> <span data-ttu-id="7efef-147">Ein Vorteil von CDECL ist, dass Aufrufe auch dann versucht werden können, wenn die Anzahl der aufrufenden Parameter nicht mit der Anzahl der definierten Parameter übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7efef-147">An advantage of CDECL is that calls can be attempted even if the number of calling parameters does not match the number of defined parameters.</span></span> 
  
<span data-ttu-id="7efef-148">Ein Anbieter kann mehrmals initialisiert werden, da er in mehreren Profilen gleichzeitig angezeigt wird oder mehr als einmal im gleichen Profil angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="7efef-148">A provider can be initialized multiple times, as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="7efef-149">Da das provider-Objekt Kontext enthält, muss **MSProviderInit** ein anderes Anbieterobjekt in  _lppMSProvider_ für jede Initialisierung zurückgeben, auch für mehrere Initialisierungen im gleichen Prozess.</span><span class="sxs-lookup"><span data-stu-id="7efef-149">Because the provider object contains context, **MSProviderInit** must return a different provider object in  _lppMSProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="7efef-150">Die Anbieter-DLL sollte nicht mit dem Mapix.dll.</span><span class="sxs-lookup"><span data-stu-id="7efef-150">The provider DLL should not be linked with Mapix.dll.</span></span> <span data-ttu-id="7efef-151">Stattdessen sollten diese Zeiger für die Speicherzuweisung oder -verteilung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7efef-151">Instead, it should use these pointers for memory allocation or deallocation.</span></span> 
  
<span data-ttu-id="7efef-152">Der Nachrichtenspeicheranbieter sollte die Funktionen verwenden, auf die  _von lpAllocateBuffer,_  _lpAllocateMore_ und  _lpFreeBuffer_ für die meisten Speicherzuweisungen und Deallocation verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="7efef-152">The message store provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="7efef-153">Insbesondere muss der Anbieter diese Funktionen verwenden, um Speicher für die Verwendung durch Clientanwendungen beim Aufrufen von Objektschnittstellen wie [IMAPIProp::GetProps](imapiprop-getprops.md) und [IMAPITable::QueryRows zu reservieren.](imapitable-queryrows.md)</span><span class="sxs-lookup"><span data-stu-id="7efef-153">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="7efef-154">Wenn der Anbieter auch die Verwendung der OLE-Speicherzuweisung erwartet, sollte er die **IUnknown::AddRef-Methode** des Zuweisungsobjekts aufrufen, auf das der  _lpMalloc-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="7efef-154">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="7efef-155">Weitere Informationen zum Schreiben von **MSProviderInit** finden Sie unter [Loading Message Store Providers](loading-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="7efef-155">For more information about writing **MSProviderInit**, see [Loading Message Store Providers](loading-message-store-providers.md).</span></span> <span data-ttu-id="7efef-156">Weitere Informationen zu Einstiegspunktfunktionen finden Sie unter [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="7efef-156">For more information about entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7efef-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7efef-157">See also</span></span>



[<span data-ttu-id="7efef-158">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="7efef-158">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="7efef-159">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7efef-159">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)
  
[<span data-ttu-id="7efef-160">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="7efef-160">XPProviderInit</span></span>](xpproviderinit.md)

