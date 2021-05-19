---
title: Nachrichtenempfangsmodell
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
# <a name="message-reception-model"></a><span data-ttu-id="d2b77-103">Nachrichtenempfangsmodell</span><span class="sxs-lookup"><span data-stu-id="d2b77-103">Message Reception Model</span></span>

  
  
<span data-ttu-id="d2b77-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d2b77-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d2b77-105">Der Transportanbieter steuert, ob der MAPI-Spooler eingehende E-Mails abruft oder ob ein Rückruf an den MAPI-Spooler beim Eintreffen neuer E-Mails durchführt wird.</span><span class="sxs-lookup"><span data-stu-id="d2b77-105">The transport provider controls whether the MAPI spooler must poll it for incoming mail or whether it performs a call back to the MAPI spooler when new mail arrives.</span></span> <span data-ttu-id="d2b77-106">Der Transportanbieter legt das SP_LOGON_POLL fest, wenn er von [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) zum Anfordern der Abfrage zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="d2b77-106">The transport provider sets the SP_LOGON_POLL flag when it returns from [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) to request polling.</span></span> <span data-ttu-id="d2b77-107">Andernfalls verwendet der Transportanbieter [IMAPISupport::SpoolerNotify,](imapisupport-spoolernotify.md) wenn eingehende E-Mails verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="d2b77-107">Otherwise, the transport provider uses [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) when incoming mail is available.</span></span> <span data-ttu-id="d2b77-108">Nachdem sie gelernt haben, dass eingehende E-Mails verfügbar sind, öffnet der MAPI-Spooler eine neue Nachricht und fordert den Transportanbieter auf, die empfangenen Nachrichteneigenschaften in der Nachricht zu speichern.</span><span class="sxs-lookup"><span data-stu-id="d2b77-108">After learning that incoming mail is available, the MAPI spooler opens a new message and asks the transport provider to store the received message properties into the message.</span></span> 
  
<span data-ttu-id="d2b77-109">Dieser Vorgang funktioniert wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d2b77-109">This process works as follows:</span></span>
  
1. <span data-ttu-id="d2b77-110">Verfügbare Nachrichten werden entweder vom Transportanbieter angegeben, der **IMAPISupport::SpoolerNotify** aufruft, oder durch den MAPI-Spooler, der [IXPLogon::P oll aufruft.](ixplogon-poll.md)</span><span class="sxs-lookup"><span data-stu-id="d2b77-110">Available messages are indicated by either the transport provider calling **IMAPISupport::SpoolerNotify** or by the MAPI spooler calling [IXPLogon::Poll](ixplogon-poll.md).</span></span>
    
2. <span data-ttu-id="d2b77-111">Der MAPI-Spooler ruft [IXPLogon::StartMessage auf,](ixplogon-startmessage.md) um den Prozess zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="d2b77-111">The MAPI spooler calls [IXPLogon::StartMessage](ixplogon-startmessage.md) to initiate the process.</span></span> 
    
3. <span data-ttu-id="d2b77-112">Der Transportanbieter platziert einen Referenzwert an dem Speicherort, auf den in **StartMessage verwiesen wird.**</span><span class="sxs-lookup"><span data-stu-id="d2b77-112">The transport provider places a reference value in the location referenced in **StartMessage**.</span></span> <span data-ttu-id="d2b77-113">Mit diesen Referenzwerten können der Transportanbieter und der MAPI-Spooler nachverfolgen, welche Nachricht verarbeitet wird, wenn mehrere Nachrichten zu liefern sind.</span><span class="sxs-lookup"><span data-stu-id="d2b77-113">These reference values allow the transport provider and the MAPI spooler to keep track of which message is being processed when there are multiple messages to deliver.</span></span>
    
4. <span data-ttu-id="d2b77-114">Der Transportanbieter speichert die Nachrichtendaten in der übergebenen [IMessage : IMAPIProp-Instanz.](imessageimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="d2b77-114">The transport provider stores the message data into the passed [IMessage : IMAPIProp](imessageimapiprop.md) instance.</span></span> 
    
5. <span data-ttu-id="d2b77-115">Der Transportanbieter ruft die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) für die **IMessage-Instanz** auf und gibt von **StartMessage zurück.**</span><span class="sxs-lookup"><span data-stu-id="d2b77-115">The transport provider calls the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method on the **IMessage** instance and returns from **StartMessage**.</span></span>
    
6. <span data-ttu-id="d2b77-116">Der MAPI-Spooler ruft [IXPLogon::TransportNotify](ixplogon-transportnotify.md) auf, wenn die Nachrichtenzustellung beendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="d2b77-116">The MAPI spooler calls [IXPLogon::TransportNotify](ixplogon-transportnotify.md) if it must stop message delivery.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="d2b77-117">Wenn ein Transportanbieter eine große Anzahl von Nachrichten bereitstellen muss und der Transportanbieter **IMAPISupport::SpoolerNotify** anstelle von **IXPLogon::P oll** verwendet, sollte darauf achten, **dass SpoolerNotify** nicht zu häufig anruft, um anderen Transportanbietern keine CPU-Zeit zu entziehen.</span><span class="sxs-lookup"><span data-stu-id="d2b77-117">If a transport provider must deliver a large number of messages and the transport provider is using **IMAPISupport::SpoolerNotify** instead of **IXPLogon::Poll**, care should be taken not to call **SpoolerNotify** too frequently in order not to deprive other transport providers of CPU time.</span></span> <span data-ttu-id="d2b77-118">Der MAPI-Spooler verfügt über eine Logik, um dies zu verhindern, aber im Allgemeinen sollte das Intervall zwischen **SpoolerNotify-Aufrufen** länger sein als die Zeit, die ihr Transportanbieter benötigt, um eine Nachricht zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="d2b77-118">The MAPI spooler does have logic to prevent this from happening, but in general the interval between **SpoolerNotify** calls should be longer than the time it takes your transport provider to process one message.</span></span> <span data-ttu-id="d2b77-119">> Wird eine eingehende Nachricht möglicherweise nicht sofort vom MAPI-Spooler verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="d2b77-119">> Also, the MAPI spooler may not process an incoming message immediately.</span></span> <span data-ttu-id="d2b77-120">Der MAPI-Spooler kann den Transportanbieter bitten, andere Aufgaben auszuführen, bevor die eingehende Nachricht empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="d2b77-120">The MAPI spooler may ask the transport provider to perform other tasks before it receives the incoming message.</span></span> 
  

