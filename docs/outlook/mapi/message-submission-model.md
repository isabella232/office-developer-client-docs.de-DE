---
title: Nachrichtenübermittlungsmodell
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4bcd19f6-c225-43ac-8c27-c46388e9097a
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 653a9df6ec414aa18c44d8035a59f021d7cc19b8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793277"
---
# <a name="message-submission-model"></a><span data-ttu-id="110b7-103">Nachrichtenübermittlungsmodell</span><span class="sxs-lookup"><span data-stu-id="110b7-103">Message Submission Model</span></span>

  
  
<span data-ttu-id="110b7-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="110b7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="110b7-105">Nachrichtenübermittlung wird durch eine Reihe von Aufrufen aus die MAPI-Warteschlange der Adressbuchhierarchie erreicht.</span><span class="sxs-lookup"><span data-stu-id="110b7-105">Message submission is accomplished by a series of calls from the MAPI spooler to the transport provider.</span></span> <span data-ttu-id="110b7-106">Die Anrufe sind wie folgt berechnet:</span><span class="sxs-lookup"><span data-stu-id="110b7-106">The calls are sequenced as follows:</span></span>
  
1. <span data-ttu-id="110b7-107">Die MAPI-Warteschlange ruft [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), und übergeben eine [IMessage: IMAPIProp](imessageimapiprop.md) -Instanz, um den zu starten.</span><span class="sxs-lookup"><span data-stu-id="110b7-107">The MAPI spooler calls [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), passing in an [IMessage : IMAPIProp](imessageimapiprop.md) instance, to begin the process.</span></span> 
    
2. <span data-ttu-id="110b7-108">Der Transportdienst anschließend wird der Verweiswert – ein Transport-definierten Bezeichner verwendet in Zukunft Verweise auf diese Meldung – am Speicherort in **SubmitMessage**verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="110b7-108">The transport provider then places a reference value — a transport-defined identifier used in future references to this message — in the location referenced in **SubmitMessage**.</span></span>
    
3. <span data-ttu-id="110b7-109">Der Transportdienst greift auf die Nachrichtendaten mithilfe der übergebenen **IMessage** -Instanz.</span><span class="sxs-lookup"><span data-stu-id="110b7-109">The transport provider accesses the message data by using the passed **IMessage** instance.</span></span> <span data-ttu-id="110b7-110">Für jeden Empfänger in übergebenen **IMessage** für die Verantwortung zulässt, der Adressbuchhierarchie wird die **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))-Eigenschaft, und gibt dann zurück.</span><span class="sxs-lookup"><span data-stu-id="110b7-110">For each recipient in the passed **IMessage** for which it accepts responsibility, the transport provider sets the **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property, and then returns.</span></span>
    
4. <span data-ttu-id="110b7-111">Der Transportdienst kann die [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) -Methode verwenden, um anzugeben, ob er erkennt alle Empfänger, die nicht zugestellt werden können, oder erstellen Sie einen standard-Delivery Report.</span><span class="sxs-lookup"><span data-stu-id="110b7-111">The transport provider can use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to indicate if it recognizes any recipients that cannot be delivered to, or to create a standard delivery report.</span></span> <span data-ttu-id="110b7-112">**StatusRecips** ist eine Vereinfachung für Transportanbieter, die bestimmt haben, dass einige Empfänger an übermittelt werden kann oder, von deren zugrunde liegenden messaging-System, die die Benutzer oder eine Client-Anwendung kann die Übermittlungsinformationen empfangen hilfreich sein.</span><span class="sxs-lookup"><span data-stu-id="110b7-112">**StatusRecips** is a convenience for transport providers that have determined that some of the recipients cannot be delivered to or that have received delivery information from their underlying messaging system that the user or client application might find useful.</span></span> 
    
5. <span data-ttu-id="110b7-113">Die MAPI-Warteschlange Aufruf von [IXPLogon::EndMessage](ixplogon-endmessage.md) ist die endgültige Verantwortung Übergabe für eine Nachricht aus der Warteschlange MAPI an der Adressbuchhierarchie.</span><span class="sxs-lookup"><span data-stu-id="110b7-113">The MAPI spooler's call to [IXPLogon::EndMessage](ixplogon-endmessage.md) is the final responsibility hand-off for the message from the MAPI spooler to the transport provider.</span></span> 
    
6. <span data-ttu-id="110b7-114">Die MAPI-Warteschlange kann [IXPLogon::TransportNotify](ixplogon-transportnotify.md) verwenden, um Nachrichten, die während der **SubmitMessage** oder **EndMessage** Anrufe abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="110b7-114">The MAPI spooler can use [IXPLogon::TransportNotify](ixplogon-transportnotify.md) to cancel message processing during the **SubmitMessage** or **EndMessage** calls.</span></span> 
    

