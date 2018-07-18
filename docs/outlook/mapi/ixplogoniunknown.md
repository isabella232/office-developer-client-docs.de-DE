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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0b16fba054533f1cb5d21f3f4b1788c073eca13b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792897"
---
# <a name="ixplogon--iunknown"></a><span data-ttu-id="d6172-103">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d6172-103">IXPLogon : IUnknown</span></span>

  
  
<span data-ttu-id="d6172-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d6172-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d6172-105">Ermöglicht den MAPI-Warteschlange Zugriff auf einem Transportdienstes.</span><span class="sxs-lookup"><span data-stu-id="d6172-105">Gives the MAPI spooler access to a transport provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d6172-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="d6172-106">Header file:</span></span>  <br/> |<span data-ttu-id="d6172-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="d6172-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="d6172-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="d6172-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="d6172-109">Transport Logon-Objekten</span><span class="sxs-lookup"><span data-stu-id="d6172-109">Transport logon objects</span></span>  <br/> |
|<span data-ttu-id="d6172-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="d6172-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="d6172-111">Transportanbieter</span><span class="sxs-lookup"><span data-stu-id="d6172-111">Transport providers</span></span>  <br/> |
|<span data-ttu-id="d6172-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="d6172-112">Called by:</span></span>  <br/> |<span data-ttu-id="d6172-113">Die MAPI-Warteschlange</span><span class="sxs-lookup"><span data-stu-id="d6172-113">The MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="d6172-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="d6172-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="d6172-115">IID_IXPLogon</span><span class="sxs-lookup"><span data-stu-id="d6172-115">IID_IXPLogon</span></span>  <br/> |
|<span data-ttu-id="d6172-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="d6172-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="d6172-117">LXPLOGON</span><span class="sxs-lookup"><span data-stu-id="d6172-117">LXPLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="d6172-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="d6172-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="d6172-119">AddressTypes</span><span class="sxs-lookup"><span data-stu-id="d6172-119">AddressTypes</span></span>](ixplogon-addresstypes.md) <br/> |<span data-ttu-id="d6172-120">Gibt die Typen von Empfängern, die der Adressbuchhierarchie behandelt.</span><span class="sxs-lookup"><span data-stu-id="d6172-120">Returns the types of recipients that the transport provider handles.</span></span>  <br/> |
|<span data-ttu-id="d6172-121">**RegisterOptions**</span><span class="sxs-lookup"><span data-stu-id="d6172-121">**RegisterOptions**</span></span> <br/> | <span data-ttu-id="d6172-122">*Nicht unterstützte oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="d6172-122">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="d6172-123">TransportNotify</span><span class="sxs-lookup"><span data-stu-id="d6172-123">TransportNotify</span></span>](ixplogon-transportnotify.md) <br/> |<span data-ttu-id="d6172-124">Signalisiert das Auftreten eines Ereignisses zu den der Transportdienst Benachrichtigung angefordert.</span><span class="sxs-lookup"><span data-stu-id="d6172-124">Signals the occurrence of an event about which the transport provider requested notification.</span></span>  <br/> |
|[<span data-ttu-id="d6172-125">Im Leerlauf</span><span class="sxs-lookup"><span data-stu-id="d6172-125">Idle</span></span>](ixplogon-idle.md) <br/> |<span data-ttu-id="d6172-126">Gibt an, dass das System im Leerlauf, der Adressbuchhierarchie niedriger Priorität Operationen aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d6172-126">Indicates that the system is idle, enabling the transport provider to perform low-priority operations.</span></span>  <br/> |
|[<span data-ttu-id="d6172-127">TransportLogoff</span><span class="sxs-lookup"><span data-stu-id="d6172-127">TransportLogoff</span></span>](ixplogon-transportlogoff.md) <br/> |<span data-ttu-id="d6172-128">Initiiert den Prozess abmelden.</span><span class="sxs-lookup"><span data-stu-id="d6172-128">Initiates the logoff process.</span></span>  <br/> |
|[<span data-ttu-id="d6172-129">SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="d6172-129">SubmitMessage</span></span>](ixplogon-submitmessage.md) <br/> |<span data-ttu-id="d6172-130">Gibt an, dass die MAPI-Warteschlange eine Nachricht an der Adressbuchhierarchie übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="d6172-130">Indicates that the MAPI spooler has a message for the transport provider to deliver.</span></span>  <br/> |
|[<span data-ttu-id="d6172-131">EndMessage</span><span class="sxs-lookup"><span data-stu-id="d6172-131">EndMessage</span></span>](ixplogon-endmessage.md) <br/> |<span data-ttu-id="d6172-132">Der Transportdienst informiert werden, dass die MAPI-Warteschlange die Verarbeitung für eine ausgehende Nachricht abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="d6172-132">Informs the transport provider that the MAPI spooler completed its processing on an outbound message.</span></span>  <br/> |
|[<span data-ttu-id="d6172-133">Umfrage</span><span class="sxs-lookup"><span data-stu-id="d6172-133">Poll</span></span>](ixplogon-poll.md) <br/> |<span data-ttu-id="d6172-134">Gibt an, ob der Adressbuchhierarchie mindestens eine eingehende Nachricht empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="d6172-134">Indicates whether the transport provider has received one or more inbound messages.</span></span>  <br/> |
|[<span data-ttu-id="d6172-135">StartMessage</span><span class="sxs-lookup"><span data-stu-id="d6172-135">StartMessage</span></span>](ixplogon-startmessage.md) <br/> |<span data-ttu-id="d6172-136">Initiiert die Übertragung von einer eingehenden Nachricht aus der Adressbuchhierarchie auf die MAPI-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="d6172-136">Initiates the transfer of an inbound message from the transport provider to the MAPI spooler.</span></span>  <br/> |
|[<span data-ttu-id="d6172-137">OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="d6172-137">OpenStatusEntry</span></span>](ixplogon-openstatusentry.md) <br/> |<span data-ttu-id="d6172-138">Öffnet die Adressbuchhierarchie Status-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d6172-138">Opens the transport provider's status object.</span></span>  <br/> |
|[<span data-ttu-id="d6172-139">ValidateState</span><span class="sxs-lookup"><span data-stu-id="d6172-139">ValidateState</span></span>](ixplogon-validatestate.md) <br/> |<span data-ttu-id="d6172-140">Externe Status der Adressbuchhierarchie überprüft.</span><span class="sxs-lookup"><span data-stu-id="d6172-140">Checks the transport provider's external status.</span></span>  <br/> |
|[<span data-ttu-id="d6172-141">FlushQueues</span><span class="sxs-lookup"><span data-stu-id="d6172-141">FlushQueues</span></span>](ixplogon-flushqueues.md) <br/> |<span data-ttu-id="d6172-142">Fordert, dass der Adressbuchhierarchie sofort alle ausstehende eingehende oder ausgehende Nachrichten übermitteln.</span><span class="sxs-lookup"><span data-stu-id="d6172-142">Requests that the transport provider immediately deliver all pending inbound or outbound messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d6172-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6172-143">See also</span></span>



[<span data-ttu-id="d6172-144">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="d6172-144">MAPI Interfaces</span></span>](mapi-interfaces.md)

