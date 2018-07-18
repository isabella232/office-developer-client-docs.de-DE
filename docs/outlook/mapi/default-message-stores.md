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
ms.openlocfilehash: cece19329460b382be724faa9f0f522831cc197c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791494"
---
# <a name="default-message-stores"></a><span data-ttu-id="7253b-103">Standard-Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="7253b-103">Default Message Stores</span></span>

  
  
<span data-ttu-id="7253b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7253b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7253b-p101">Ein Standardnachrichtenspeicher ist eine, die Client-Anwendungen f�r allgemeine Zwecke messaging Aufgaben verwenden k�nnen. Es gibt eine Reihe von optionalen Features f�r Nachricht Speicher-Anbieter, die erforderlich werden, wenn der Anbieter die Nachricht wird als Standard-Informationsspeicher verwendet werden soll. Sie sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7253b-p101">A default message store is one that client applications can use for general purpose messaging tasks. There are a number of optional features for message store providers that become required if the message store provider is to be used as the default message store. They are as follows:</span></span>
  
- <span data-ttu-id="7253b-108">Implementieren der Spezialordner: der Ordner Posteingang und Postausgang-Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="7253b-108">Implementing the special folders: the Inbox, Outbox, and search-results folders.</span></span>
    
- <span data-ttu-id="7253b-109">Bereitstellen von Lese- und nonread Berichten.</span><span class="sxs-lookup"><span data-stu-id="7253b-109">Providing read and nonread reports.</span></span>
    
- <span data-ttu-id="7253b-110">Eingehende und ausgehende Nachrichten�bermittlungen zulassen.</span><span class="sxs-lookup"><span data-stu-id="7253b-110">Allowing incoming and outgoing message submissions.</span></span>
    
- <span data-ttu-id="7253b-111">Erm�glicht die Erstellung von Nachrichten mit beliebigen Nachrichtenklassen.</span><span class="sxs-lookup"><span data-stu-id="7253b-111">Allowing the creation of messages with arbitrary message classes.</span></span>
    
- <span data-ttu-id="7253b-112">Unterst�tzung f�r benannte und mehrwertige Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7253b-112">Supporting named and multiple-value properties.</span></span>
    
- <span data-ttu-id="7253b-113">Supporting the [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) method, even if the message store provider is tightly coupled with a transport provider.</span><span class="sxs-lookup"><span data-stu-id="7253b-113">Supporting the [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) method, even if the message store provider is tightly coupled with a transport provider.</span></span> 
    
- <span data-ttu-id="7253b-p102">Supporting associated contents tables. For more information, see [Inhalt von Tabellen](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="7253b-p102">Supporting associated contents tables. For more information, see [Contents Tables](contents-tables.md).</span></span>
    
- <span data-ttu-id="7253b-116">Benachrichtigung �ber die Warteschlange MAPI-Unterst�tzung f�r Nachrichten in der Warteschlange f�r ausgehende Nachrichten vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="7253b-116">Supporting notification of the MAPI spooler when there are messages in the outgoing message queue.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7253b-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7253b-117">See also</span></span>



[<span data-ttu-id="7253b-118">Entwickeln eines Providers MAPI-Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="7253b-118">Developing a MAPI Message Store Provider</span></span>](developing-a-mapi-message-store-provider.md)

