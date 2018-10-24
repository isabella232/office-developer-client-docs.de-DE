---
title: Standardnachrichtentspeicher
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: efa178eb-feb2-443f-8f6b-2ea53a456bf2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3f7bf720f9105f6a81b832233cc648bc1d9ac91d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576911"
---
# <a name="default-message-stores"></a><span data-ttu-id="a003a-103">Standardnachrichtentspeicher</span><span class="sxs-lookup"><span data-stu-id="a003a-103">Default Message Stores</span></span>

  
  
<span data-ttu-id="a003a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a003a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a003a-p101">Eine Standardnachrichtentspeicher ist ein Speicher, den Clientanwendungen für allgemeine Aufgaben im Zusammenhang mit Nachrichten verwenden können. Es gibt eine Reihe optionaler Features für Nachrichtenspeicheranbieter, die erforderlich werden, wenn der Nachrichtenspeichernanbieter als Standardnachrichtentspeicher verwendet werden soll. Dies sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a003a-p101">A default message store is one that client applications can use for general purpose messaging tasks. There are a number of optional features for message store providers that become required if the message store provider is to be used as the default message store. They are as follows:</span></span>
  
- <span data-ttu-id="a003a-108">Implementieren der Spezialordner: der Ordner Posteingang und Postausgang-Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="a003a-108">Implementing the special folders: the Inbox, Outbox, and search-results folders.</span></span>
    
- <span data-ttu-id="a003a-109">Bereitstellen von Lese- und nonread Berichten.</span><span class="sxs-lookup"><span data-stu-id="a003a-109">Providing read and nonread reports.</span></span>
    
- <span data-ttu-id="a003a-110">Zulassen der Übermittlung von eingehenden und ausgehenden Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="a003a-110">Allowing incoming and outgoing message submissions.</span></span>
    
- <span data-ttu-id="a003a-111">Zulassen der Erstellung von Nachrichten mit beliebigen Nachrichtenklassen.</span><span class="sxs-lookup"><span data-stu-id="a003a-111">Allowing the creation of messages with arbitrary message classes.</span></span>
    
- <span data-ttu-id="a003a-112">Unterstützung benannter und mehrwertige Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a003a-112">Supporting named and multiple-value properties.</span></span>
    
- <span data-ttu-id="a003a-113">Unterstützung der [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)-Methode, auch dann, wenn der Nachrichtenspeicheranbieter eng mit einem Transportanbieter verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="a003a-113">Supporting the [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) method, even if the message store provider is tightly coupled with a transport provider.</span></span> 
    
- <span data-ttu-id="a003a-p102">Unterstützung zugehöriger Inhaltstabellen. Weitere Informationen finden Sie unter [Inhaltstabellen](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="a003a-p102">Supporting associated contents tables. For more information, see [Contents Tables](contents-tables.md).</span></span>
    
- <span data-ttu-id="a003a-116">Unterstützung der Benachrichtigung des MAPI-Spoolers, wenn sich Nachrichten in der Warteschlange für ausgehende Nachrichten befinden.</span><span class="sxs-lookup"><span data-stu-id="a003a-116">Supporting notification of the MAPI spooler when there are messages in the outgoing message queue.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a003a-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a003a-117">See also</span></span>



[<span data-ttu-id="a003a-118">Entwickeln eines MAPI-Nachrichtenspeicheranbieters</span><span class="sxs-lookup"><span data-stu-id="a003a-118">Developing a MAPI Message Store Provider</span></span>](developing-a-mapi-message-store-provider.md)

