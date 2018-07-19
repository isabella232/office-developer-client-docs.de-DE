---
title: IXPLogonTransportLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.TransportLogoff
api_type:
- COM
ms.assetid: b2b368ce-4486-4f90-985f-59e50ca95229
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 195f2d718428eb8bb618fc982488c276d8a536da
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792891"
---
# <a name="ixplogontransportlogoff"></a><span data-ttu-id="523ae-103">IXPLogon::TransportLogoff</span><span class="sxs-lookup"><span data-stu-id="523ae-103">IXPLogon::TransportLogoff</span></span>

  
  
<span data-ttu-id="523ae-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="523ae-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="523ae-105">Initiiert den Prozess abmelden.</span><span class="sxs-lookup"><span data-stu-id="523ae-105">Initiates the logoff process.</span></span> 
  
```cpp
HRESULT TransportLogoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="523ae-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="523ae-106">Parameters</span></span>

 <span data-ttu-id="523ae-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="523ae-107">_ulFlags_</span></span>
  
> <span data-ttu-id="523ae-108">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="523ae-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="523ae-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="523ae-109">Return value</span></span>

<span data-ttu-id="523ae-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="523ae-110">S_OK</span></span> 
  
> <span data-ttu-id="523ae-111">Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="523ae-111">The call succeeded and returned the expected value or values.</span></span> <span data-ttu-id="523ae-112">Wenn alles andere als S_OK zurückgegeben wird, wird der Anbieter abgemeldet.</span><span class="sxs-lookup"><span data-stu-id="523ae-112">If anything other than S_OK is returned, the provider is logged off.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="523ae-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="523ae-113">Remarks</span></span>

<span data-ttu-id="523ae-114">Die MAPI-Warteschlange die **IXPLogon::TransportLogoff** -Methode aufgerufen, um eine Sitzung Transport Anbieter für einen bestimmten Benutzer zu beenden.</span><span class="sxs-lookup"><span data-stu-id="523ae-114">The MAPI spooler calls the **IXPLogon::TransportLogoff** method to terminate a transport provider session for a particular user.</span></span> <span data-ttu-id="523ae-115">Vor dem Aufruf von **TransportLogoff**, verwirft die MAPI-Warteschlange von Daten zu unterstützten messaging-Adresstypen für diese Sitzung in der [IXPLogon::AddressTypes](ixplogon-addresstypes.md) -Methode übergeben.</span><span class="sxs-lookup"><span data-stu-id="523ae-115">Before calling **TransportLogoff**, the MAPI spooler discards any data about supported messaging address types for this session passed in the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="523ae-116">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="523ae-116">Notes to implementers</span></span>

<span data-ttu-id="523ae-117">Der Adressbuchhierarchie sollte vorbereitet werden, können Sie jederzeit einen Anruf an **TransportLogoff** akzeptieren kann.</span><span class="sxs-lookup"><span data-stu-id="523ae-117">The transport provider should be prepared to accept a call to **TransportLogoff** at any time.</span></span> <span data-ttu-id="523ae-118">Wenn eine Nachricht verarbeitet wird, sollte der Anbieter die sendende Abbrechen.</span><span class="sxs-lookup"><span data-stu-id="523ae-118">If a message is in process, the provider should stop the sending process.</span></span> 
  
<span data-ttu-id="523ae-119">Der Transportdienst sollte alle Ressourcen für die aktuelle Sitzung freigeben.</span><span class="sxs-lookup"><span data-stu-id="523ae-119">The transport provider should release all resources allocated for its current session.</span></span> <span data-ttu-id="523ae-120">Wenn es für diese Sitzung mit der Funktion [MAPIAllocateBuffer](mapiallocatebuffer.md) Speicher zugewiesen hat, sollten sie den Arbeitsspeicher freizugeben, mithilfe der [MAPIFreeBuffer](mapifreebuffer.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="523ae-120">If it has allocated any memory for this session with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, it should free the memory by using the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> <span data-ttu-id="523ae-121">Von Speicher vom Transportanbieter zum Aufrufen der Methode [IXPLogon::AddressTypes](ixplogon-addresstypes.md) erfüllen kann zu diesem Zeitpunkt sicher freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="523ae-121">Any memory allocated by the transport provider to satisfy calls to the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method can be safely released at this time.</span></span> 
  
<span data-ttu-id="523ae-122">In der Regel für das Gespräch **TransportLogoff** durchführen, sollte ein Anbieter zunächst dessen Anmeldung-Objekt durch Aufrufen der Methode [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) ungültig und anschließend wieder seines Support-Objekts.</span><span class="sxs-lookup"><span data-stu-id="523ae-122">Usually, on completing a **TransportLogoff** call, a provider should first invalidate its logon object by calling the [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) method and then release its support object.</span></span> <span data-ttu-id="523ae-123">Implementierung der **TransportLogoff** der Anbieter sollte Support-Objekt letzten, freigeben, da beim Support-Objekt veröffentlicht hat, die MAPI-Warteschlange auch das Provider-Objekt selbst freigeben kann.</span><span class="sxs-lookup"><span data-stu-id="523ae-123">The provider's implementation of **TransportLogoff** should release the support object last, because when the support object is released, the MAPI spooler can also release the provider object itself.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="523ae-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="523ae-124">See also</span></span>



[<span data-ttu-id="523ae-125">IMAPISupport::MakeInvalid</span><span class="sxs-lookup"><span data-stu-id="523ae-125">IMAPISupport::MakeInvalid</span></span>](imapisupport-makeinvalid.md)
  
[<span data-ttu-id="523ae-126">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="523ae-126">IMAPISupport::SpoolerYield</span></span>](imapisupport-spooleryield.md)
  
[<span data-ttu-id="523ae-127">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="523ae-127">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
  
[<span data-ttu-id="523ae-128">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="523ae-128">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="523ae-129">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="523ae-129">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="523ae-130">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="523ae-130">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

