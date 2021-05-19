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
ms.openlocfilehash: 090a765fd6c758e5f146caa0e7f36276b052f69e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421123"
---
# <a name="message-submission-model"></a><span data-ttu-id="e1b54-103">Nachrichtenübermittlungsmodell</span><span class="sxs-lookup"><span data-stu-id="e1b54-103">Message Submission Model</span></span>

  
  
<span data-ttu-id="e1b54-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1b54-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1b54-105">Die Nachrichtenübermittlung erfolgt durch eine Reihe von Anrufen vom MAPI-Spooler an den Transportanbieter.</span><span class="sxs-lookup"><span data-stu-id="e1b54-105">Message submission is accomplished by a series of calls from the MAPI spooler to the transport provider.</span></span> <span data-ttu-id="e1b54-106">Die Aufrufe werden wie folgt sequenziert:</span><span class="sxs-lookup"><span data-stu-id="e1b54-106">The calls are sequenced as follows:</span></span>
  
1. <span data-ttu-id="e1b54-107">Der MAPI-Spooler ruft [IXPLogon::SubmitMessage](ixplogon-submitmessage.md)auf und übertrumpft eine [IMessage : IMAPIProp-Instanz,](imessageimapiprop.md) um den Prozess zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="e1b54-107">The MAPI spooler calls [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), passing in an [IMessage : IMAPIProp](imessageimapiprop.md) instance, to begin the process.</span></span> 
    
2. <span data-ttu-id="e1b54-108">Der Transportanbieter platziert dann einen Referenzwert – einen transportdefinierten Bezeichner, der in zukünftigen Verweisen auf diese Nachricht verwendet wird – an dem Speicherort, auf den in **SubmitMessage verwiesen wird.**</span><span class="sxs-lookup"><span data-stu-id="e1b54-108">The transport provider then places a reference value — a transport-defined identifier used in future references to this message — in the location referenced in **SubmitMessage**.</span></span>
    
3. <span data-ttu-id="e1b54-109">Der Transportanbieter zugrifft mithilfe der übergebenen **IMessage-Instanz** auf die Nachrichtendaten.</span><span class="sxs-lookup"><span data-stu-id="e1b54-109">The transport provider accesses the message data by using the passed **IMessage** instance.</span></span> <span data-ttu-id="e1b54-110">Für jeden Empfänger in der übergebenen **IMessage,** für die er die Verantwortung übernimmt, legt der Transportanbieter die **eigenschaft PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) fest und gibt dann zurück.</span><span class="sxs-lookup"><span data-stu-id="e1b54-110">For each recipient in the passed **IMessage** for which it accepts responsibility, the transport provider sets the **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property, and then returns.</span></span>
    
4. <span data-ttu-id="e1b54-111">Der Transportanbieter kann die [IMAPISupport::StatusRecips-Methode](imapisupport-statusrecips.md) verwenden, um anzugeben, ob Empfänger erkannt werden, die nicht zugestellt werden können, oder um einen Standardzustellungsbericht zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e1b54-111">The transport provider can use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to indicate if it recognizes any recipients that cannot be delivered to, or to create a standard delivery report.</span></span> <span data-ttu-id="e1b54-112">**StatusRecips** ist ein Komfort für Transportanbieter, die festgestellt haben, dass einige empfänger nicht zugestellt werden können oder Übermittlungsinformationen von ihrem zugrunde liegenden Messagingsystem erhalten haben, die der Benutzer oder die Clientanwendung möglicherweise nützlich finden.</span><span class="sxs-lookup"><span data-stu-id="e1b54-112">**StatusRecips** is a convenience for transport providers that have determined that some of the recipients cannot be delivered to or that have received delivery information from their underlying messaging system that the user or client application might find useful.</span></span> 
    
5. <span data-ttu-id="e1b54-113">Der Aufruf des MAPI-Spoolers bei [IXPLogon::EndMessage](ixplogon-endmessage.md) ist die endgültige Übergabe der Verantwortung für die Nachricht vom MAPI-Spooler an den Transportanbieter.</span><span class="sxs-lookup"><span data-stu-id="e1b54-113">The MAPI spooler's call to [IXPLogon::EndMessage](ixplogon-endmessage.md) is the final responsibility hand-off for the message from the MAPI spooler to the transport provider.</span></span> 
    
6. <span data-ttu-id="e1b54-114">Der MAPI-Spooler kann [IXPLogon::TransportNotify](ixplogon-transportnotify.md) verwenden, um die Nachrichtenverarbeitung während der **SubmitMessage-** oder **EndMessage-Aufrufe abbricht.**</span><span class="sxs-lookup"><span data-stu-id="e1b54-114">The MAPI spooler can use [IXPLogon::TransportNotify](ixplogon-transportnotify.md) to cancel message processing during the **SubmitMessage** or **EndMessage** calls.</span></span> 
    

