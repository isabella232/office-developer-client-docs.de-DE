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
ms.openlocfilehash: 17470f9ff552eaa4908973c4f033db2b4e754d7c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792878"
---
# <a name="ixplogonpoll"></a><span data-ttu-id="72d0a-103">IXPLogon::Poll</span><span class="sxs-lookup"><span data-stu-id="72d0a-103">IXPLogon::Poll</span></span>

  
  
<span data-ttu-id="72d0a-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="72d0a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="72d0a-105">Gibt an, ob der Adressbuchhierarchie mindestens eine eingehende Nachricht empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="72d0a-105">Indicates whether the transport provider has received one or more inbound messages.</span></span>
  
```cpp
HRESULT Poll(
  ULONG FAR * lpulIncoming
);
```

## <a name="parameters"></a><span data-ttu-id="72d0a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="72d0a-106">Parameters</span></span>

 <span data-ttu-id="72d0a-107">_lpulIncoming_</span><span class="sxs-lookup"><span data-stu-id="72d0a-107">_lpulIncoming_</span></span>
  
> <span data-ttu-id="72d0a-108">[out] Ein Wert, der angibt, das Vorhandensein von eingehenden Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="72d0a-108">[out] A value that indicates the existence of inbound messages.</span></span> <span data-ttu-id="72d0a-109">Ein Wert ungleich Null gibt an, dass eingehende Nachrichten vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="72d0a-109">A nonzero value indicates that there are inbound messages.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="72d0a-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="72d0a-110">Return value</span></span>

<span data-ttu-id="72d0a-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="72d0a-111">S_OK</span></span> 
  
> <span data-ttu-id="72d0a-112">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="72d0a-112">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="72d0a-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="72d0a-113">Remarks</span></span>

<span data-ttu-id="72d0a-114">Die MAPI-Warteschlange in regelmäßigen Abständen um die **IXPLogon::Poll** -Methode aufgerufen, wenn der Adressbuchhierarchie gibt an, dass es für neue Nachrichten abgefragt werden muss, dem der Anbieter, indem Sie die LOGON_SP_POLL übergeben zu den Anruf an die [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) -flag Methode am Anfang einer Sitzung.</span><span class="sxs-lookup"><span data-stu-id="72d0a-114">The MAPI spooler periodically calls the **IXPLogon::Poll** method if the transport provider indicates it must be polled for new messages, which the provider does by passing the LOGON_SP_POLL flag to the call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method at the beginning of a session.</span></span> <span data-ttu-id="72d0a-115">Wenn der Adressbuchhierarchie gibt als Antwort auf die **Umfrage** Anruf, die eine vorhanden sind oder mehr eingehende Nachrichten an den Prozess, die MAPI-Warteschlange für sie verfügbar Ruft die [IXPLogon::StartMessage](ixplogon-startmessage.md) -Methode, um den Anbieter an den Prozess der ersten ermöglichen, eingehend Nachricht.</span><span class="sxs-lookup"><span data-stu-id="72d0a-115">If the transport provider indicates in response to the **Poll** call that there are one or more inbound messages available for it to process, the MAPI spooler calls the [IXPLogon::StartMessage](ixplogon-startmessage.md) method to allow the provider to process the first inbound message.</span></span> <span data-ttu-id="72d0a-116">Der Transportdienst gibt eingehende Nachrichten durch Festlegen des Werts in der _LpulIncoming_ -Parameter auf einen anderen Wert an.</span><span class="sxs-lookup"><span data-stu-id="72d0a-116">The transport provider indicates inbound messages by setting the value in the  _lpulIncoming_ parameter to a nonzero value.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="72d0a-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="72d0a-117">See also</span></span>



[<span data-ttu-id="72d0a-118">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="72d0a-118">IXPLogon::StartMessage</span></span>](ixplogon-startmessage.md)
  
[<span data-ttu-id="72d0a-119">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="72d0a-119">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="72d0a-120">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="72d0a-120">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

