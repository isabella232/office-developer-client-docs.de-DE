---
title: Nachrichtenempfangs Modell
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d85d269e-2251-4399-9159-a2f47a85e3d1
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 487598374f15300cc8b899a50d74b535b5a33c91
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415117"
---
# <a name="message-reception-model"></a><span data-ttu-id="501cf-103">Nachrichtenempfangs Modell</span><span class="sxs-lookup"><span data-stu-id="501cf-103">Message Reception Model</span></span>

  
  
<span data-ttu-id="501cf-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="501cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="501cf-105">Der Transportanbieter steuert, ob der MAPI-Spooler es für eingehende e-Mails Abfragen muss, oder ob er beim Eintreffen neuer e-Mails einen Rückruf an den MAPI-Spooler ausführt.</span><span class="sxs-lookup"><span data-stu-id="501cf-105">The transport provider controls whether the MAPI spooler must poll it for incoming mail or whether it performs a call back to the MAPI spooler when new mail arrives.</span></span> <span data-ttu-id="501cf-106">Der Transportanbieter legt das SP_LOGON_POLL-Flag fest, wenn es von [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md) zurückgibt, um Polling anzufordern.</span><span class="sxs-lookup"><span data-stu-id="501cf-106">The transport provider sets the SP_LOGON_POLL flag when it returns from [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) to request polling.</span></span> <span data-ttu-id="501cf-107">Andernfalls verwendet der Transportanbieter [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) , wenn eingehende e-Mail verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="501cf-107">Otherwise, the transport provider uses [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) when incoming mail is available.</span></span> <span data-ttu-id="501cf-108">Nachdem Sie erfahren haben, dass eingehende e-Mails verfügbar sind, öffnet der MAPI-Spooler eine neue Nachricht und fordert den Transportanbieter auf, die empfangenen Nachrichteneigenschaften in der Nachricht zu speichern.</span><span class="sxs-lookup"><span data-stu-id="501cf-108">After learning that incoming mail is available, the MAPI spooler opens a new message and asks the transport provider to store the received message properties into the message.</span></span> 
  
<span data-ttu-id="501cf-109">Dieser Vorgang funktioniert wie folgt:</span><span class="sxs-lookup"><span data-stu-id="501cf-109">This process works as follows:</span></span>
  
1. <span data-ttu-id="501cf-110">Verfügbare Nachrichten werden entweder vom Transportanbieter, der **IMAPISupport:: SpoolerNotify** oder vom MAPI-Warteschlangen Aufruf [IXPLogon::P oll](ixplogon-poll.md)angezeigt.</span><span class="sxs-lookup"><span data-stu-id="501cf-110">Available messages are indicated by either the transport provider calling **IMAPISupport::SpoolerNotify** or by the MAPI spooler calling [IXPLogon::Poll](ixplogon-poll.md).</span></span>
    
2. <span data-ttu-id="501cf-111">Der MAPI-Spooler ruft [IXPLogon:: StartMessage](ixplogon-startmessage.md) auf, um den Prozess zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="501cf-111">The MAPI spooler calls [IXPLogon::StartMessage](ixplogon-startmessage.md) to initiate the process.</span></span> 
    
3. <span data-ttu-id="501cf-112">Der Transportanbieter platziert einen Verweiswert an dem Speicherort, auf den in **StartMessage**verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="501cf-112">The transport provider places a reference value in the location referenced in **StartMessage**.</span></span> <span data-ttu-id="501cf-113">Anhand dieser Referenzwerte können Transportanbieter und MAPI-Spooler nachverfolgen, welche Nachricht verarbeitet wird, wenn mehrere zu übermittelnde Nachrichten vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="501cf-113">These reference values allow the transport provider and the MAPI spooler to keep track of which message is being processed when there are multiple messages to deliver.</span></span>
    
4. <span data-ttu-id="501cf-114">Der Transportanbieter speichert die Nachrichtendaten in der übergebenen [IMessage: IMAPIProp](imessageimapiprop.md) -Instanz.</span><span class="sxs-lookup"><span data-stu-id="501cf-114">The transport provider stores the message data into the passed [IMessage : IMAPIProp](imessageimapiprop.md) instance.</span></span> 
    
5. <span data-ttu-id="501cf-115">Der Transportanbieter Ruft die [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode für die **IMessage** -Instanz auf und gibt von **StartMessage**zurück.</span><span class="sxs-lookup"><span data-stu-id="501cf-115">The transport provider calls the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method on the **IMessage** instance and returns from **StartMessage**.</span></span>
    
6. <span data-ttu-id="501cf-116">Der MAPI-Warteschlangen Aufruf [IXPLogon:: TransportNotify](ixplogon-transportnotify.md) , wenn die Nachrichtenübermittlung beendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="501cf-116">The MAPI spooler calls [IXPLogon::TransportNotify](ixplogon-transportnotify.md) if it must stop message delivery.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="501cf-117">Wenn ein Transportanbieter eine hohe Anzahl von Nachrichten übermitteln muss und der Transportanbieter **IMAPISupport:: SpoolerNotify** anstelle von **IXPLogon verwendet::P oll**, sollte darauf geachtet werden, **SpoolerNotify** nicht zu häufig aufzurufen, um nicht anderen Transportanbietern die CPU-Zeit entziehen.</span><span class="sxs-lookup"><span data-stu-id="501cf-117">If a transport provider must deliver a large number of messages and the transport provider is using **IMAPISupport::SpoolerNotify** instead of **IXPLogon::Poll**, care should be taken not to call **SpoolerNotify** too frequently in order not to deprive other transport providers of CPU time.</span></span> <span data-ttu-id="501cf-118">Der MAPI-Spooler hat Logik, um dies zu verhindern, aber im Allgemeinen sollte das Intervall zwischen **SpoolerNotify** -anrufen länger sein als die Zeit, die der Transportanbieter zum Verarbeiten einer Nachricht benötigt.</span><span class="sxs-lookup"><span data-stu-id="501cf-118">The MAPI spooler does have logic to prevent this from happening, but in general the interval between **SpoolerNotify** calls should be longer than the time it takes your transport provider to process one message.</span></span> <span data-ttu-id="501cf-119">> Außerdem kann der MAPI-Spooler keine eingehenden Nachrichten sofort verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="501cf-119">> Also, the MAPI spooler may not process an incoming message immediately.</span></span> <span data-ttu-id="501cf-120">Der MAPI-Spooler kann den Transportanbieter bitten, andere Aufgaben auszuführen, bevor die eingehende Nachricht empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="501cf-120">The MAPI spooler may ask the transport provider to perform other tasks before it receives the incoming message.</span></span> 
  

