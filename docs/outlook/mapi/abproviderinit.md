---
title: ABProviderInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ABProviderInit
api_type:
- HeaderDef
ms.assetid: c3dcd0d4-018a-47b0-b040-227034ed59d8
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: acec07df0b72685cf9ec6b21499c730b72f58c59
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328112"
---
# <a name="abproviderinit"></a><span data-ttu-id="9f411-103">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="9f411-103">ABProviderInit</span></span>
 
<span data-ttu-id="9f411-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f411-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9f411-105">Initialisiert einen Adressbuchanbieter für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="9f411-105">Initializes an address book provider for operation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9f411-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="9f411-106">Header file:</span></span>  <br/> |<span data-ttu-id="9f411-107">Mapispi. h</span><span class="sxs-lookup"><span data-stu-id="9f411-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="9f411-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="9f411-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9f411-109">Adressbuchanbieter</span><span class="sxs-lookup"><span data-stu-id="9f411-109">Address book providers</span></span>  <br/> |
|<span data-ttu-id="9f411-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="9f411-110">Called by:</span></span>  <br/> |<span data-ttu-id="9f411-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="9f411-111">MAPI</span></span>  <br/> |
   
```cpp
HRESULT ABProviderInit(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  ULONG ulMAPIVer,
  ULONG FAR * lpulProviderVer,
  LPABPROVIDER FAR * lppABProvider
);
```

## <a name="parameters"></a><span data-ttu-id="9f411-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f411-112">Parameters</span></span>

 <span data-ttu-id="9f411-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="9f411-113">_hInstance_</span></span>
  
> <span data-ttu-id="9f411-114">in Die Instanz der Dynamic Link Library (DLL) des Adressbuch Anbieters, die MAPI bei der Verknüpfung verwendet hat.</span><span class="sxs-lookup"><span data-stu-id="9f411-114">[in] The instance of the address book provider's dynamic-link library (DLL) that MAPI used when it linked.</span></span> 
    
 <span data-ttu-id="9f411-115">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="9f411-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="9f411-116">in Zeiger auf ein Speicher Reservierungs Objekt, das die OLE **IMalloc** -Schnittstelle verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="9f411-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="9f411-117">Der Adressbuchanbieter muss diese Zuordnungsmethode möglicherweise beim Arbeiten mit bestimmten Schnittstellen wie **IStream**verwenden.</span><span class="sxs-lookup"><span data-stu-id="9f411-117">The address book provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="9f411-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="9f411-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="9f411-119">in Zeiger auf die [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion, die verwendet werden soll, wenn MAPI zum Reservieren von Arbeitsspeicher erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="9f411-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used where required by MAPI to allocate memory.</span></span> 
    
 <span data-ttu-id="9f411-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="9f411-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="9f411-121">in Zeiger auf die [MAPIAllocateMore](mapiallocatemore.md) -Funktion, die bei Bedarf von MAPI verwendet werden kann, um zusätzlichen Arbeitsspeicher zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="9f411-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used where required by MAPI to allocate additional memory.</span></span> 
    
 <span data-ttu-id="9f411-122">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="9f411-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="9f411-123">in Zeiger auf die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion, die verwendet werden soll, wenn MAPI zum Freigeben des Arbeitsspeichers erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="9f411-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used where required by MAPI to free memory.</span></span> 
    
 <span data-ttu-id="9f411-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9f411-124">_ulFlags_</span></span>
  
> <span data-ttu-id="9f411-125">in Bitmaske von Flags.</span><span class="sxs-lookup"><span data-stu-id="9f411-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="9f411-126">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="9f411-126">The following flag can be set:</span></span>
    
<span data-ttu-id="9f411-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="9f411-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="9f411-128">Der Anbieter wird im Kontext eines Windows-Diensts, einem speziellen Prozesstyp ohne Zugriff auf eine beliebige Benutzeroberfläche, geladen.</span><span class="sxs-lookup"><span data-stu-id="9f411-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="9f411-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="9f411-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="9f411-130">in Versionsnummer der Dienstanbieterschnittstelle (SPI), die MAPI. DLL verwendet.</span><span class="sxs-lookup"><span data-stu-id="9f411-130">[in] Version number of the service provider interface (SPI) that MAPI.DLL uses.</span></span> <span data-ttu-id="9f411-131">Die aktuelle Versionsnummer finden Sie unter MAPISPI. H-Headerdatei.</span><span class="sxs-lookup"><span data-stu-id="9f411-131">For the current version number, see the MAPISPI.H header file.</span></span> 
    
 <span data-ttu-id="9f411-132">_lpulProviderVer_</span><span class="sxs-lookup"><span data-stu-id="9f411-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="9f411-133">Out Zeiger auf die Versionsnummer des SPI, den dieser Adressbuchanbieter verwendet.</span><span class="sxs-lookup"><span data-stu-id="9f411-133">[out] Pointer to the version number of the SPI that this address book provider uses.</span></span> 
    
 <span data-ttu-id="9f411-134">_lppABProvider_</span><span class="sxs-lookup"><span data-stu-id="9f411-134">_lppABProvider_</span></span>
  
> <span data-ttu-id="9f411-135">Out Zeiger auf einen Zeiger auf das Objekt des initialisierten Adressbuch Anbieters.</span><span class="sxs-lookup"><span data-stu-id="9f411-135">[out] Pointer to a pointer to the initialized address book provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9f411-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9f411-136">Return value</span></span>

<span data-ttu-id="9f411-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="9f411-137">S_OK</span></span> 
  
> <span data-ttu-id="9f411-138">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="9f411-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="9f411-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="9f411-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="9f411-140">Die SPI-Version, die von MAPI verwendet wird, ist nicht mit dem SPI kompatibel, der von diesem Anbieter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9f411-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9f411-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9f411-141">Remarks</span></span>

<span data-ttu-id="9f411-142">MAPI Ruft die Einstiegspunktfunktion **ABProviderInit** auf, um einen Adressbuchanbieter nach einer Clientanmeldung zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="9f411-142">MAPI calls the entry point function **ABProviderInit** to initialize an address book provider following a client logon.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="9f411-143">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="9f411-143">Notes to implementers</span></span>

<span data-ttu-id="9f411-144">Ein Adressbuchanbieter muss **ABProviderInit** als Einstiegspunktfunktion in der DLL des Anbieters implementieren.</span><span class="sxs-lookup"><span data-stu-id="9f411-144">An address book provider must implement **ABProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="9f411-145">Die Implementierung muss auf dem Prototyp der **ABPROVIDERINIT** -Funktion basieren, der auch in MAPISPI angegeben ist. H.</span><span class="sxs-lookup"><span data-stu-id="9f411-145">The implementation must be based on the **ABPROVIDERINIT** function prototype, also specified in MAPISPI.H.</span></span> <span data-ttu-id="9f411-146">MAPI definiert **ABPROVIDERINIT** für die Verwendung des standardMÄßIGen MAPI-Initialisierungsaufruf Typs STDMAPIINITCALLTYPE, wodurch **ABPROVIDERINIT** der Cdecl-Aufrufkonvention folgt.</span><span class="sxs-lookup"><span data-stu-id="9f411-146">MAPI defines **ABPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **ABProviderInit** to follow the CDECL calling convention.</span></span> 
  
<span data-ttu-id="9f411-147">Ein Anbieter kann mehrmals initialisiert werden, wenn er in mehreren Profilen gleichzeitig verwendet wird oder mehr als einmal im gleichen Profil angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9f411-147">A provider can be initialized multiple times, as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="9f411-148">Da das Provider-Objekt den Kontext enthält, muss **ABProviderInit** für jede Initialisierung ein anderes Anbieterobjekt in _lppABProvider_ zurückgeben, auch für mehrere Initialisierungen im selben Prozess.</span><span class="sxs-lookup"><span data-stu-id="9f411-148">Because the provider object contains context, **ABProviderInit** must return a different provider object in  _lppABProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="9f411-149">Der Adressbuchanbieter sollte die Funktionen, auf die von _lpAllocateBuffer_, _lpAllocateMore_und _lpFreeBuffer_ verwiesen wird, für die meisten Speicherzuweisungen und-Zuordnungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="9f411-149">The address book provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="9f411-150">Insbesondere muss der Anbieter diese Funktionen verwenden, um Arbeitsspeicher für die Verwendung durch Clientanwendungen zu reservieren, wenn Objektschnittstellen wie [IMAPIProp::](imapiprop-getprops.md) GetProps und [IMAPITable:: QueryRows](imapitable-queryrows.md)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="9f411-150">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="9f411-151">Wenn der Anbieter auch die Verwendung der OLE-Speicherzuweisung erwartet, sollte er die **IUnknown:: AddRef** -Methode des Zuweisungs Objekts aufrufen, auf die durch den _lpMalloc_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="9f411-151">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="9f411-152">Weitere Informationen zum Schreiben von **ABProviderInit**finden Sie unter [Implementieren der Einstiegspunktfunktion eines Adressbuch Anbieters](implementing-an-address-book-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="9f411-152">For more information on writing **ABProviderInit**, see [Implementing an Address Book Provider Entry Point Function](implementing-an-address-book-provider-entry-point-function.md).</span></span> <span data-ttu-id="9f411-153">Weitere Informationen zu Einstiegspunktfunktionen finden Sie unter [Implementieren einer Dienstanbieter-Einstiegspunktfunktion](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="9f411-153">For more information on entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9f411-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f411-154">See also</span></span>

- [<span data-ttu-id="9f411-155">IABProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9f411-155">IABProvider : IUnknown</span></span>](iabprovideriunknown.md) 
- [<span data-ttu-id="9f411-156">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="9f411-156">MSProviderInit</span></span>](msproviderinit.md)
- [<span data-ttu-id="9f411-157">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="9f411-157">XPProviderInit</span></span>](xpproviderinit.md)

