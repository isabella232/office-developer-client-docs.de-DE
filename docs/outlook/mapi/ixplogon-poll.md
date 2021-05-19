---
title: IXPLogonPoll
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.Poll
api_type:
- COM
ms.assetid: 1524eb06-7492-42de-b455-e0982bda7ece
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3e68c564357880b623e02081a228e881c084fa94
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425274"
---
# <a name="ixplogonpoll"></a><span data-ttu-id="c35d6-103">IXPLogon::Poll</span><span class="sxs-lookup"><span data-stu-id="c35d6-103">IXPLogon::Poll</span></span>

  
  
<span data-ttu-id="c35d6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c35d6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c35d6-105">Gibt an, ob der Transportanbieter eine oder mehrere eingehende Nachrichten empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="c35d6-105">Indicates whether the transport provider has received one or more inbound messages.</span></span>
  
```cpp
HRESULT Poll(
  ULONG FAR * lpulIncoming
);
```

## <a name="parameters"></a><span data-ttu-id="c35d6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c35d6-106">Parameters</span></span>

 <span data-ttu-id="c35d6-107">_lpulIncoming_</span><span class="sxs-lookup"><span data-stu-id="c35d6-107">_lpulIncoming_</span></span>
  
> <span data-ttu-id="c35d6-108">[out] Ein Wert, der das Vorhandensein eingehender Nachrichten angibt.</span><span class="sxs-lookup"><span data-stu-id="c35d6-108">[out] A value that indicates the existence of inbound messages.</span></span> <span data-ttu-id="c35d6-109">Ein Wert ungleich Null gibt an, dass eingehende Nachrichten vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="c35d6-109">A nonzero value indicates that there are inbound messages.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c35d6-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c35d6-110">Return value</span></span>

<span data-ttu-id="c35d6-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="c35d6-111">S_OK</span></span> 
  
> <span data-ttu-id="c35d6-112">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="c35d6-112">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c35d6-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c35d6-113">Remarks</span></span>

<span data-ttu-id="c35d6-114">Der MAPI-Spooler ruft regelmäßig die **IXPLogon::P oll-Methode** auf, wenn der Transportanbieter angibt, dass er nach neuen Nachrichten abfragen muss, was der Anbieter durch Übergeben des LOGON_SP_POLL-Flags an den Aufruf der [IXPProvider::TransportLogon-Methode](ixpprovider-transportlogon.md) am Anfang einer Sitzung tut.</span><span class="sxs-lookup"><span data-stu-id="c35d6-114">The MAPI spooler periodically calls the **IXPLogon::Poll** method if the transport provider indicates it must be polled for new messages, which the provider does by passing the LOGON_SP_POLL flag to the call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method at the beginning of a session.</span></span> <span data-ttu-id="c35d6-115">Wenn der Transportanbieter als Antwort  auf den Abrufanruf angibt, dass eine oder mehrere eingehende Nachrichten für die Behandlung verfügbar sind, ruft der MAPI-Spooler die [IXPLogon::StartMessage-Methode](ixplogon-startmessage.md) auf, damit der Anbieter die erste eingehende Nachricht verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="c35d6-115">If the transport provider indicates in response to the **Poll** call that there are one or more inbound messages available for it to process, the MAPI spooler calls the [IXPLogon::StartMessage](ixplogon-startmessage.md) method to allow the provider to process the first inbound message.</span></span> <span data-ttu-id="c35d6-116">Der Transportanbieter gibt eingehende Nachrichten an, indem der Wert im  _lpulIncoming-Parameter_ auf einen Wert ungleich Null festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="c35d6-116">The transport provider indicates inbound messages by setting the value in the  _lpulIncoming_ parameter to a nonzero value.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c35d6-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c35d6-117">See also</span></span>



[<span data-ttu-id="c35d6-118">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="c35d6-118">IXPLogon::StartMessage</span></span>](ixplogon-startmessage.md)
  
[<span data-ttu-id="c35d6-119">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="c35d6-119">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="c35d6-120">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c35d6-120">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

