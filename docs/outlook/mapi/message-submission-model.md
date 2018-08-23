---
title: Nachrichtenübermittlungsmodell
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4bcd19f6-c225-43ac-8c27-c46388e9097a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8cb34360f5a0a3e67aca1ac53fe639724135f594
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584541"
---
# <a name="message-submission-model"></a><span data-ttu-id="c1ca5-103">Nachrichtenübermittlungsmodell</span><span class="sxs-lookup"><span data-stu-id="c1ca5-103">Message Submission Model</span></span>

  
  
<span data-ttu-id="c1ca5-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1ca5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1ca5-105">Nachrichtenübermittlung wird durch eine Reihe von Aufrufen aus die MAPI-Warteschlange der Adressbuchhierarchie erreicht.</span><span class="sxs-lookup"><span data-stu-id="c1ca5-105">Message submission is accomplished by a series of calls from the MAPI spooler to the transport provider.</span></span> <span data-ttu-id="c1ca5-106">Die Anrufe sind wie folgt berechnet:</span><span class="sxs-lookup"><span data-stu-id="c1ca5-106">The calls are sequenced as follows:</span></span>
  
1. <span data-ttu-id="c1ca5-107">Die MAPI-Warteschlange ruft [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), und übergeben eine [IMessage: IMAPIProp](imessageimapiprop.md) -Instanz, um den zu starten.</span><span class="sxs-lookup"><span data-stu-id="c1ca5-107">The MAPI spooler calls [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), passing in an [IMessage : IMAPIProp](imessageimapiprop.md) instance, to begin the process.</span></span> 
    
2. <span data-ttu-id="c1ca5-108">Der Transportdienst anschließend wird der Verweiswert – ein Transport-definierten Bezeichner verwendet in Zukunft Verweise auf diese Meldung – am Speicherort in **SubmitMessage**verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="c1ca5-108">The transport provider then places a reference value — a transport-defined identifier used in future references to this message — in the location referenced in **SubmitMessage**.</span></span>
    
3. <span data-ttu-id="c1ca5-109">Der Transportdienst greift auf die Nachrichtendaten mithilfe der übergebenen **IMessage** -Instanz.</span><span class="sxs-lookup"><span data-stu-id="c1ca5-109">The transport provider accesses the message data by using the passed **IMessage** instance.</span></span> <span data-ttu-id="c1ca5-110">Für jeden Empfänger in übergebenen **IMessage** für die Verantwortung zulässt, der Adressbuchhierarchie wird die **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))-Eigenschaft, und gibt dann zurück.</span><span class="sxs-lookup"><span data-stu-id="c1ca5-110">For each recipient in the passed **IMessage** for which it accepts responsibility, the transport provider sets the **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property, and then returns.</span></span>
    
4. <span data-ttu-id="c1ca5-111">Der Transportdienst kann die [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) -Methode verwenden, um anzugeben, ob er erkennt alle Empfänger, die nicht zugestellt werden können, oder erstellen Sie einen standard-Delivery Report.</span><span class="sxs-lookup"><span data-stu-id="c1ca5-111">The transport provider can use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to indicate if it recognizes any recipients that cannot be delivered to, or to create a standard delivery report.</span></span> <span data-ttu-id="c1ca5-112">**StatusRecips** ist eine Vereinfachung für Transportanbieter, die bestimmt haben, dass einige Empfänger an übermittelt werden kann oder, von deren zugrunde liegenden messaging-System, die die Benutzer oder eine Client-Anwendung kann die Übermittlungsinformationen empfangen hilfreich sein.</span><span class="sxs-lookup"><span data-stu-id="c1ca5-112">**StatusRecips** is a convenience for transport providers that have determined that some of the recipients cannot be delivered to or that have received delivery information from their underlying messaging system that the user or client application might find useful.</span></span> 
    
5. <span data-ttu-id="c1ca5-113">Die MAPI-Warteschlange Aufruf von [IXPLogon::EndMessage](ixplogon-endmessage.md) ist die endgültige Verantwortung Übergabe für eine Nachricht aus der Warteschlange MAPI an der Adressbuchhierarchie.</span><span class="sxs-lookup"><span data-stu-id="c1ca5-113">The MAPI spooler's call to [IXPLogon::EndMessage](ixplogon-endmessage.md) is the final responsibility hand-off for the message from the MAPI spooler to the transport provider.</span></span> 
    
6. <span data-ttu-id="c1ca5-114">Die MAPI-Warteschlange kann [IXPLogon::TransportNotify](ixplogon-transportnotify.md) verwenden, um Nachrichten, die während der **SubmitMessage** oder **EndMessage** Anrufe abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="c1ca5-114">The MAPI spooler can use [IXPLogon::TransportNotify](ixplogon-transportnotify.md) to cancel message processing during the **SubmitMessage** or **EndMessage** calls.</span></span> 
    

