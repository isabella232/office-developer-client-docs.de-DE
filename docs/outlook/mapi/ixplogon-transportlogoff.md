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
ms.openlocfilehash: 78b4feeca263035b9c90184f10edd294e6cd7b10
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417861"
---
# <a name="ixplogontransportlogoff"></a><span data-ttu-id="25f89-103">IXPLogon::TransportLogoff</span><span class="sxs-lookup"><span data-stu-id="25f89-103">IXPLogon::TransportLogoff</span></span>

  
  
<span data-ttu-id="25f89-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="25f89-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="25f89-105">Initiiert den Abmeldevorgang.</span><span class="sxs-lookup"><span data-stu-id="25f89-105">Initiates the logoff process.</span></span> 
  
```cpp
HRESULT TransportLogoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="25f89-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="25f89-106">Parameters</span></span>

 <span data-ttu-id="25f89-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="25f89-107">_ulFlags_</span></span>
  
> <span data-ttu-id="25f89-108">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="25f89-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="25f89-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="25f89-109">Return value</span></span>

<span data-ttu-id="25f89-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="25f89-110">S_OK</span></span> 
  
> <span data-ttu-id="25f89-111">Der Aufruf war erfolgreich und hat den erwarteten Wert oder die erwarteten Werte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="25f89-111">The call succeeded and returned the expected value or values.</span></span> <span data-ttu-id="25f89-112">Wenn etwas anderes als S_OK zurückgegeben wird, wird der Anbieter abgemeldet.</span><span class="sxs-lookup"><span data-stu-id="25f89-112">If anything other than S_OK is returned, the provider is logged off.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="25f89-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="25f89-113">Remarks</span></span>

<span data-ttu-id="25f89-114">Der MAPI-Spooler ruft die **IXPLogon::TransportLogoff-Methode auf,** um eine Transportanbietersitzung für einen bestimmten Benutzer zu beenden.</span><span class="sxs-lookup"><span data-stu-id="25f89-114">The MAPI spooler calls the **IXPLogon::TransportLogoff** method to terminate a transport provider session for a particular user.</span></span> <span data-ttu-id="25f89-115">Vor dem **Aufrufen von TransportLogoff** verwirft der MAPI-Spooler alle Daten zu unterstützten Messagingadressentypen für diese Sitzung, die in der [IXPLogon::AddressTypes-Methode übergeben](ixplogon-addresstypes.md) werden.</span><span class="sxs-lookup"><span data-stu-id="25f89-115">Before calling **TransportLogoff**, the MAPI spooler discards any data about supported messaging address types for this session passed in the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="25f89-116">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="25f89-116">Notes to implementers</span></span>

<span data-ttu-id="25f89-117">Der Transportanbieter sollte jederzeit bereit sein, einen Anruf bei **TransportLogoff** zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="25f89-117">The transport provider should be prepared to accept a call to **TransportLogoff** at any time.</span></span> <span data-ttu-id="25f89-118">Wenn eine Nachricht im Prozess ist, sollte der Anbieter den Sendevorgang beenden.</span><span class="sxs-lookup"><span data-stu-id="25f89-118">If a message is in process, the provider should stop the sending process.</span></span> 
  
<span data-ttu-id="25f89-119">Der Transportanbieter sollte alle ressourcen frei geben, die für die aktuelle Sitzung zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="25f89-119">The transport provider should release all resources allocated for its current session.</span></span> <span data-ttu-id="25f89-120">Wenn der Speicher für diese Sitzung mit der [MAPIAllocateBuffer-Funktion](mapiallocatebuffer.md) zugewiesen wurde, sollte der Arbeitsspeicher mithilfe der [MAPIFreeBuffer-Funktion frei](mapifreebuffer.md) werden.</span><span class="sxs-lookup"><span data-stu-id="25f89-120">If it has allocated any memory for this session with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, it should free the memory by using the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> <span data-ttu-id="25f89-121">Der vom Transportanbieter zur Erfüllung von Aufrufen der [IXPLogon::AddressTypes-Methode](ixplogon-addresstypes.md) zugewiesene Arbeitsspeicher kann derzeit sicher freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="25f89-121">Any memory allocated by the transport provider to satisfy calls to the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method can be safely released at this time.</span></span> 
  
<span data-ttu-id="25f89-122">Normalerweise sollte ein Anbieter nach Abschluss eines **TransportLogoff-Aufrufs** zunächst sein Anmeldeobjekt ungültig machen, indem er die [IMAPISupport::MakeInvalid-Methode](imapisupport-makeinvalid.md) aufruft und dann sein Supportobjekt los gibt.</span><span class="sxs-lookup"><span data-stu-id="25f89-122">Usually, on completing a **TransportLogoff** call, a provider should first invalidate its logon object by calling the [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) method and then release its support object.</span></span> <span data-ttu-id="25f89-123">Die Implementierung von **TransportLogoff** durch den Anbieter sollte das Supportobjekt zuletzt losgelassen werden, da der MAPI-Spooler bei der Freigabe des Supportobjekts auch das Anbieterobjekt selbst losgelassen werden kann.</span><span class="sxs-lookup"><span data-stu-id="25f89-123">The provider's implementation of **TransportLogoff** should release the support object last, because when the support object is released, the MAPI spooler can also release the provider object itself.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="25f89-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25f89-124">See also</span></span>



[<span data-ttu-id="25f89-125">IMAPISupport::MakeInvalid</span><span class="sxs-lookup"><span data-stu-id="25f89-125">IMAPISupport::MakeInvalid</span></span>](imapisupport-makeinvalid.md)
  
[<span data-ttu-id="25f89-126">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="25f89-126">IMAPISupport::SpoolerYield</span></span>](imapisupport-spooleryield.md)
  
[<span data-ttu-id="25f89-127">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="25f89-127">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
  
[<span data-ttu-id="25f89-128">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="25f89-128">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="25f89-129">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="25f89-129">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="25f89-130">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="25f89-130">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

