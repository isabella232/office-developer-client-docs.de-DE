---
title: IXPLogon IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon
api_type:
- COM
ms.assetid: 4d24ecaf-11d0-4362-8207-be3407736d7b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 46f4e3fc8f554f332ab9b1d8a6cb33e9e21dd9a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432534"
---
# <a name="ixplogon--iunknown"></a><span data-ttu-id="585ac-103">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="585ac-103">IXPLogon : IUnknown</span></span>

  
  
<span data-ttu-id="585ac-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="585ac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="585ac-105">Gewährt dem MAPI-Spooler Zugriff auf einen Transportanbieter.</span><span class="sxs-lookup"><span data-stu-id="585ac-105">Gives the MAPI spooler access to a transport provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="585ac-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="585ac-106">Header file:</span></span>  <br/> |<span data-ttu-id="585ac-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="585ac-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="585ac-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="585ac-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="585ac-109">Transportanmeldeobjekte</span><span class="sxs-lookup"><span data-stu-id="585ac-109">Transport logon objects</span></span>  <br/> |
|<span data-ttu-id="585ac-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="585ac-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="585ac-111">Transportanbieter</span><span class="sxs-lookup"><span data-stu-id="585ac-111">Transport providers</span></span>  <br/> |
|<span data-ttu-id="585ac-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="585ac-112">Called by:</span></span>  <br/> |<span data-ttu-id="585ac-113">Der MAPI-Spooler</span><span class="sxs-lookup"><span data-stu-id="585ac-113">The MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="585ac-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="585ac-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="585ac-115">IID_IXPLogon</span><span class="sxs-lookup"><span data-stu-id="585ac-115">IID_IXPLogon</span></span>  <br/> |
|<span data-ttu-id="585ac-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="585ac-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="585ac-117">LXPLOGON</span><span class="sxs-lookup"><span data-stu-id="585ac-117">LXPLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="585ac-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="585ac-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="585ac-119">AddressTypes</span><span class="sxs-lookup"><span data-stu-id="585ac-119">AddressTypes</span></span>](ixplogon-addresstypes.md) <br/> |<span data-ttu-id="585ac-120">Gibt die Empfängertypen zurück, die vom Transportanbieter verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="585ac-120">Returns the types of recipients that the transport provider handles.</span></span>  <br/> |
|<span data-ttu-id="585ac-121">**RegisterOptions**</span><span class="sxs-lookup"><span data-stu-id="585ac-121">**RegisterOptions**</span></span> <br/> | <span data-ttu-id="585ac-122">*Nicht unterstützt oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="585ac-122">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="585ac-123">TransportNotify</span><span class="sxs-lookup"><span data-stu-id="585ac-123">TransportNotify</span></span>](ixplogon-transportnotify.md) <br/> |<span data-ttu-id="585ac-124">Signalisiert das Auftreten eines Ereignisses, über das der Transportanbieter eine Benachrichtigung angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="585ac-124">Signals the occurrence of an event about which the transport provider requested notification.</span></span>  <br/> |
|[<span data-ttu-id="585ac-125">Leerlauf</span><span class="sxs-lookup"><span data-stu-id="585ac-125">Idle</span></span>](ixplogon-idle.md) <br/> |<span data-ttu-id="585ac-126">Gibt an, dass sich das System im Leerlauf befindet, sodass der Transportanbieter Vorgänge mit niedriger Priorität ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="585ac-126">Indicates that the system is idle, enabling the transport provider to perform low-priority operations.</span></span>  <br/> |
|[<span data-ttu-id="585ac-127">TransportLogoff</span><span class="sxs-lookup"><span data-stu-id="585ac-127">TransportLogoff</span></span>](ixplogon-transportlogoff.md) <br/> |<span data-ttu-id="585ac-128">Initiiert den Abmeldevorgang.</span><span class="sxs-lookup"><span data-stu-id="585ac-128">Initiates the logoff process.</span></span>  <br/> |
|[<span data-ttu-id="585ac-129">SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="585ac-129">SubmitMessage</span></span>](ixplogon-submitmessage.md) <br/> |<span data-ttu-id="585ac-130">Gibt an, dass der MAPI-Spooler über eine Nachricht verfügt, die der Transportanbieter zu liefern hat.</span><span class="sxs-lookup"><span data-stu-id="585ac-130">Indicates that the MAPI spooler has a message for the transport provider to deliver.</span></span>  <br/> |
|[<span data-ttu-id="585ac-131">EndMessage</span><span class="sxs-lookup"><span data-stu-id="585ac-131">EndMessage</span></span>](ixplogon-endmessage.md) <br/> |<span data-ttu-id="585ac-132">Informiert den Transportanbieter, dass der MAPI-Spooler seine Verarbeitung für eine ausgehende Nachricht abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="585ac-132">Informs the transport provider that the MAPI spooler completed its processing on an outbound message.</span></span>  <br/> |
|[<span data-ttu-id="585ac-133">Umfrage</span><span class="sxs-lookup"><span data-stu-id="585ac-133">Poll</span></span>](ixplogon-poll.md) <br/> |<span data-ttu-id="585ac-134">Gibt an, ob der Transportanbieter eine oder mehrere eingehende Nachrichten empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="585ac-134">Indicates whether the transport provider has received one or more inbound messages.</span></span>  <br/> |
|[<span data-ttu-id="585ac-135">StartMessage</span><span class="sxs-lookup"><span data-stu-id="585ac-135">StartMessage</span></span>](ixplogon-startmessage.md) <br/> |<span data-ttu-id="585ac-136">Initiiert die Übertragung einer eingehenden Nachricht vom Transportanbieter an den MAPI-Spooler.</span><span class="sxs-lookup"><span data-stu-id="585ac-136">Initiates the transfer of an inbound message from the transport provider to the MAPI spooler.</span></span>  <br/> |
|[<span data-ttu-id="585ac-137">OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="585ac-137">OpenStatusEntry</span></span>](ixplogon-openstatusentry.md) <br/> |<span data-ttu-id="585ac-138">Öffnet das Statusobjekt des Transportanbieters.</span><span class="sxs-lookup"><span data-stu-id="585ac-138">Opens the transport provider's status object.</span></span>  <br/> |
|[<span data-ttu-id="585ac-139">ValidateState</span><span class="sxs-lookup"><span data-stu-id="585ac-139">ValidateState</span></span>](ixplogon-validatestate.md) <br/> |<span data-ttu-id="585ac-140">Überprüft den externen Status des Transportanbieters.</span><span class="sxs-lookup"><span data-stu-id="585ac-140">Checks the transport provider's external status.</span></span>  <br/> |
|[<span data-ttu-id="585ac-141">FlushQueues</span><span class="sxs-lookup"><span data-stu-id="585ac-141">FlushQueues</span></span>](ixplogon-flushqueues.md) <br/> |<span data-ttu-id="585ac-142">Fordert an, dass der Transportanbieter sofort alle ausstehenden eingehenden oder ausgehenden Nachrichten zuliefert.</span><span class="sxs-lookup"><span data-stu-id="585ac-142">Requests that the transport provider immediately deliver all pending inbound or outbound messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="585ac-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="585ac-143">See also</span></span>



[<span data-ttu-id="585ac-144">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="585ac-144">MAPI Interfaces</span></span>](mapi-interfaces.md)

