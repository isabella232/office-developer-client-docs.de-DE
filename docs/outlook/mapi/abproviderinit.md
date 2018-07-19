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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 03375a11be3f6f128db5f6147c5fbe901d0a0fa9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791236"
---
# <a name="abproviderinit"></a><span data-ttu-id="ceec1-103">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="ceec1-103">ABProviderInit</span></span>
 
<span data-ttu-id="ceec1-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ceec1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ceec1-105">Adressbuch-Dienstanbieter für Vorgang initialisiert.</span><span class="sxs-lookup"><span data-stu-id="ceec1-105">Initializes an address book provider for operation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ceec1-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="ceec1-106">Header file:</span></span>  <br/> |<span data-ttu-id="ceec1-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="ceec1-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="ceec1-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="ceec1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ceec1-109">Von adressbuchanbietern implementierte</span><span class="sxs-lookup"><span data-stu-id="ceec1-109">Address book providers</span></span>  <br/> |
|<span data-ttu-id="ceec1-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="ceec1-110">Called by:</span></span>  <br/> |<span data-ttu-id="ceec1-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="ceec1-111">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="ceec1-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ceec1-112">Parameters</span></span>

 <span data-ttu-id="ceec1-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="ceec1-113">_hInstance_</span></span>
  
> <span data-ttu-id="ceec1-114">[in] Die Instanz der Adressbuchanbieter Dynamic Link Library (DLL), die MAPI verwendet wird, wenn es verknüpft.</span><span class="sxs-lookup"><span data-stu-id="ceec1-114">[in] The instance of the address book provider's dynamic-link library (DLL) that MAPI used when it linked.</span></span> 
    
 <span data-ttu-id="ceec1-115">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="ceec1-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="ceec1-116">[in] Zeiger auf ein Speicherobjekt-Zuweisung die OLE **IMalloc** -Schnittstelle verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="ceec1-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="ceec1-117">Der Adressbuchanbieter müssen möglicherweise beim Arbeiten mit bestimmte Schnittstellen wie **IStream**diese Zuordnungsmethode verwenden.</span><span class="sxs-lookup"><span data-stu-id="ceec1-117">The address book provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="ceec1-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="ceec1-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="ceec1-119">[in] Zeiger auf die Funktion [MAPIAllocateBuffer](mapiallocatebuffer.md) , gegebenenfalls MAPI Speicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ceec1-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used where required by MAPI to allocate memory.</span></span> 
    
 <span data-ttu-id="ceec1-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="ceec1-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="ceec1-121">[in] Zeiger auf die Funktion [MAPIAllocateMore](mapiallocatemore.md) , gegebenenfalls MAPI verwendet werden soll, zusätzlichen Arbeitsspeicher zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="ceec1-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used where required by MAPI to allocate additional memory.</span></span> 
    
 <span data-ttu-id="ceec1-122">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="ceec1-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="ceec1-123">[in] Zeiger auf die [MAPIFreeBuffer](mapifreebuffer.md) -Funktion verwendet werden, in denen MAPI erforderlich, um Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="ceec1-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used where required by MAPI to free memory.</span></span> 
    
 <span data-ttu-id="ceec1-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ceec1-124">_ulFlags_</span></span>
  
> <span data-ttu-id="ceec1-125">[in] Bitmaske der Kennzeichen.</span><span class="sxs-lookup"><span data-stu-id="ceec1-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="ceec1-126">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="ceec1-126">The following flag can be set:</span></span>
    
<span data-ttu-id="ceec1-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="ceec1-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="ceec1-128">Der Anbieter wird im Kontext eines Windows-Diensts, eine spezielle Art von Vorgang ohne Zugriff auf eine beliebige Benutzeroberfläche geladen.</span><span class="sxs-lookup"><span data-stu-id="ceec1-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="ceec1-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="ceec1-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="ceec1-130">[in] Versionsnummer der der Dienstanbieter-Schnittstelle (SPI), MAPI. DLL-Datei verwendet.</span><span class="sxs-lookup"><span data-stu-id="ceec1-130">[in] Version number of the service provider interface (SPI) that MAPI.DLL uses.</span></span> <span data-ttu-id="ceec1-131">Die aktuelle Versionsnummer finden Sie unter der MAPISPI. H-Headerdatei.</span><span class="sxs-lookup"><span data-stu-id="ceec1-131">For the current version number, see the MAPISPI.H header file.</span></span> 
    
 <span data-ttu-id="ceec1-132">_lpulProviderVer_</span><span class="sxs-lookup"><span data-stu-id="ceec1-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="ceec1-133">[out] Zeiger auf die Versionsnummer der SPI, die diese Adressbuchanbieter verwendet.</span><span class="sxs-lookup"><span data-stu-id="ceec1-133">[out] Pointer to the version number of the SPI that this address book provider uses.</span></span> 
    
 <span data-ttu-id="ceec1-134">_lppABProvider_</span><span class="sxs-lookup"><span data-stu-id="ceec1-134">_lppABProvider_</span></span>
  
> <span data-ttu-id="ceec1-135">[out] Zeiger auf einen Zeiger auf das initialisierten Address Book Anbieter-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ceec1-135">[out] Pointer to a pointer to the initialized address book provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ceec1-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ceec1-136">Return value</span></span>

<span data-ttu-id="ceec1-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="ceec1-137">S_OK</span></span> 
  
> <span data-ttu-id="ceec1-138">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="ceec1-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="ceec1-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="ceec1-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="ceec1-140">Die SPI-Version von MAPI verwendet wird, ist nicht kompatibel mit der SPI, die von diesem Anbieter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ceec1-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ceec1-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ceec1-141">Remarks</span></span>

<span data-ttu-id="ceec1-142">MAPI-aufrufen, die Eintrags-Funktion **ABProviderInit** nach einer Clientanmeldung Adressbuch-Dienstanbieter nicht initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="ceec1-142">MAPI calls the entry point function **ABProviderInit** to initialize an address book provider following a client logon.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ceec1-143">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="ceec1-143">Notes to implementers</span></span>

<span data-ttu-id="ceec1-144">Adressbuch-Dienstanbieter muss als Funktion Entry Point in die DLL des Anbieters **ABProviderInit** implementieren.</span><span class="sxs-lookup"><span data-stu-id="ceec1-144">An address book provider must implement **ABProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="ceec1-145">Die Implementierung der **ABPROVIDERINIT** Funktionsprototyp auch im angegebenen MAPISPI basieren. H.</span><span class="sxs-lookup"><span data-stu-id="ceec1-145">The implementation must be based on the **ABPROVIDERINIT** function prototype, also specified in MAPISPI.H.</span></span> <span data-ttu-id="ceec1-146">MAPI definiert **ABPROVIDERINIT** Verwendung standard MAPI Initialisierung Aufruftyps, STDMAPIINITCALLTYPE, wodurch **ABProviderInit** CDECL-Aufrufkonvention folgen.</span><span class="sxs-lookup"><span data-stu-id="ceec1-146">MAPI defines **ABPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **ABProviderInit** to follow the CDECL calling convention.</span></span> 
  
<span data-ttu-id="ceec1-147">Ein Anbieter kann mehrere Male, als Ergebnis in mehrere Profile angezeigt wird, in der gleichzeitigen Verwendung oder nur einmal in das gleiche Profil angezeigt werden initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="ceec1-147">A provider can be initialized multiple times, as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="ceec1-148">Da das Anbieterobjekt Kontext enthält, muss **ABProviderInit** in _LppABProvider_ für jede Initialisierung, auch für mehrere wie in demselben Prozess einer anderen Anbieter-Objekt zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="ceec1-148">Because the provider object contains context, **ABProviderInit** must return a different provider object in  _lppABProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="ceec1-149">Der Adressbuchanbieter sollten die Funktionen, die auf den _LpAllocateBuffer_, _LpAllocateMore_und _LpFreeBuffer_ für die meisten arbeitsspeicherreservierung und Freigabe verwenden.</span><span class="sxs-lookup"><span data-stu-id="ceec1-149">The address book provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="ceec1-150">Insbesondere muss den Anbieter diese Funktionen für die Verwendung von Clientanwendungen Speicher beim Aufruf von wie [IMAPIProp::GetProps](imapiprop-getprops.md) und [IMAPITable::QueryRows](imapitable-queryrows.md)-Schnittstellen verwenden.</span><span class="sxs-lookup"><span data-stu-id="ceec1-150">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="ceec1-151">Wenn der Anbieter auch erwartet, verwenden Sie die Zuweisung der OLE-Speicher, sollten sie die **IUnknown:: AddRef** -Methode, der das Zuordnungsobjekt auf das durch den Parameter _LpMalloc_ aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ceec1-151">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="ceec1-152">Weitere Informationen zum Schreiben von **ABProviderInit**finden Sie unter [Implementieren einer Adresse Adressbuch Anbieter Eintrag Point-Funktion](implementing-an-address-book-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="ceec1-152">For more information on writing **ABProviderInit**, see [Implementing an Address Book Provider Entry Point Function](implementing-an-address-book-provider-entry-point-function.md).</span></span> <span data-ttu-id="ceec1-153">Weitere Informationen zu Entry Point-Funktionen finden Sie unter [Implementieren einer Service Provider Eintrag zeigen-Funktion](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="ceec1-153">For more information on entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ceec1-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ceec1-154">See also</span></span>

- [<span data-ttu-id="ceec1-155">IABProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ceec1-155">IABProvider : IUnknown</span></span>](iabprovideriunknown.md) 
- [<span data-ttu-id="ceec1-156">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="ceec1-156">MSProviderInit</span></span>](msproviderinit.md)
- [<span data-ttu-id="ceec1-157">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="ceec1-157">XPProviderInit</span></span>](xpproviderinit.md)

