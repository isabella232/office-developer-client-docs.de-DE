---
title: Standard-Nachrichtenspeicher
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: efa178eb-feb2-443f-8f6b-2ea53a456bf2
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3f7bf720f9105f6a81b832233cc648bc1d9ac91d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576911"
---
# <a name="default-message-stores"></a><span data-ttu-id="c0d4d-103">Standard-Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="c0d4d-103">Default Message Stores</span></span>

  
  
<span data-ttu-id="c0d4d-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c0d4d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c0d4d-p101">Ein Standardnachrichtenspeicher ist eine, die Client-Anwendungen f�r allgemeine Zwecke messaging Aufgaben verwenden k�nnen. Es gibt eine Reihe von optionalen Features f�r Nachricht Speicher-Anbieter, die erforderlich werden, wenn der Anbieter die Nachricht wird als Standard-Informationsspeicher verwendet werden soll. Sie sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c0d4d-p101">A default message store is one that client applications can use for general purpose messaging tasks. There are a number of optional features for message store providers that become required if the message store provider is to be used as the default message store. They are as follows:</span></span>
  
- <span data-ttu-id="c0d4d-108">Implementieren der Spezialordner: der Ordner Posteingang und Postausgang-Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="c0d4d-108">Implementing the special folders: the Inbox, Outbox, and search-results folders.</span></span>
    
- <span data-ttu-id="c0d4d-109">Bereitstellen von Lese- und nonread Berichten.</span><span class="sxs-lookup"><span data-stu-id="c0d4d-109">Providing read and nonread reports.</span></span>
    
- <span data-ttu-id="c0d4d-110">Eingehende und ausgehende Nachrichten�bermittlungen zulassen.</span><span class="sxs-lookup"><span data-stu-id="c0d4d-110">Allowing incoming and outgoing message submissions.</span></span>
    
- <span data-ttu-id="c0d4d-111">Erm�glicht die Erstellung von Nachrichten mit beliebigen Nachrichtenklassen.</span><span class="sxs-lookup"><span data-stu-id="c0d4d-111">Allowing the creation of messages with arbitrary message classes.</span></span>
    
- <span data-ttu-id="c0d4d-112">Unterst�tzung f�r benannte und mehrwertige Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c0d4d-112">Supporting named and multiple-value properties.</span></span>
    
- <span data-ttu-id="c0d4d-113">Supporting the [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) method, even if the message store provider is tightly coupled with a transport provider.</span><span class="sxs-lookup"><span data-stu-id="c0d4d-113">Supporting the [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) method, even if the message store provider is tightly coupled with a transport provider.</span></span> 
    
- <span data-ttu-id="c0d4d-p102">Supporting associated contents tables. For more information, see [Inhalt von Tabellen](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="c0d4d-p102">Supporting associated contents tables. For more information, see [Contents Tables](contents-tables.md).</span></span>
    
- <span data-ttu-id="c0d4d-116">Benachrichtigung �ber die Warteschlange MAPI-Unterst�tzung f�r Nachrichten in der Warteschlange f�r ausgehende Nachrichten vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="c0d4d-116">Supporting notification of the MAPI spooler when there are messages in the outgoing message queue.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c0d4d-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0d4d-117">See also</span></span>



[<span data-ttu-id="c0d4d-118">Entwickeln eines Providers MAPI-Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="c0d4d-118">Developing a MAPI Message Store Provider</span></span>](developing-a-mapi-message-store-provider.md)

